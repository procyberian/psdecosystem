# Windows Kurumsal Dosya Sistemleri ve ReFS Kapasite Raporu

Bu rapor, Windows kurumsal dosya sistemleri (NTFS ve ReFS) ile ReFS'in veri merkezlerindeki ölçeklenebilirlik, kapasite sınırları ve kullanım senaryoları üzerine yapılan görüşmelerin tüm çıktılarını içermektedir.

---

## 1. Windows Kurumsal Dosya Sistemlerine Genel Bakış

Windows kurumsal ortamlarında temel olarak iki ana dosya sistemi kullanılır:

*   **NTFS (New Technology File System):** İşletim sistemi birimleri ve genel amaçlı sunucular için standart varsayılan dosya sistemidir. Modern sürümlerde 8 PB'a kadar birim boyutlarını destekler. Erişim Denetim Listeleri (ACL), şifreleme (EFS), disk kotaları ve BitLocker entegrasyonu gibi gelişmiş kurumsal özelliklere sahiptir.
*   **ReFS (Resilient File System):** Büyük ölçekli veri bütünlüğü, yüksek kullanılabilirlik ve yüksek performanslı sunucu/sanallaştırma iş yükleri (Hyper-V, Storage Spaces Direct vb.) için özel olarak tasarlanmıştır. *Not: ReFS, Windows için önyükleme (boot) birimi olarak kullanılamaz.*

---

## 2. ReFS Kapasite Sınırları ve Depolama Limitleri

ReFS, tek bir işletim sistemi havuzunda (volume) hem maksimum disk boyutu hem de tek bir dosya boyutu için **35 Petabayt (PB)** depolama kapasitesi sunar.

### Detaylı Limit Tablosu
| Özellik | ReFS Sınırı |
| :--- | :--- |
| **Maksimum Hacim (Disk) Boyutu** | 35 PB (35.000 Terabayt) |
| **Maksimum Dosya Boyutu** | 35 PB |
| **Maksimum Karakter Uzunluğu** | Dosya yolu başına 32.767 karakter |
| **Maksimum Dosya/Klasör Sayısı** | Tek bir dizinde $2^{64}$ adet (~18 kentilyon) |

---

## 3. Veri Merkezi Ölçeklerine Göre ReFS Değerlendirmesi

**35 PB sınırı, ReFS dosya sisteminde oluşturulabilecek "tek bir mantıksal havuzun (volume)" sınırıdır.** Bir veri merkezinde bu havuzlardan yüzlerce veya binlerce oluşturulabileceği için veri merkezinin toplam kapasitesi Exabayt (EB) seviyelerine çıksa bile ReFS bu ölçeklenebilirliği yönetebilir.

### Ölçek Analizi

1.  **Küçük ve Orta Ölçekli Veri Merkezleri (Colocation / Yerel Veri Merkezleri)**
    *   **Durum:** Fazlasıyla Yeterli.
    *   **Açıklama:** Genellikle 50-200 kabin barındıran bu tesislerin toplam aktif depolama ihtiyacı 5-20 PB arasındadır. ReFS tek başına tüm altyapıyı tek bir mimari altında toplamaya yeterlidir.
2.  **Büyük Ölçekli Kurumsal (Enterprise) Veri Merkezleri**
    *   **Durum:** Uygundur ve Tam Hedef Kitlesidir.
    *   **Açıklama:** Bankalar, telekom operatörleri ve hastane zincirlerinde veri miktarı 50-150 PB civarına ulaşabilir. ReFS'in 35 PB'lık tekil havuz limiti, verilerin mantıksal iş yüklerine göre (Hyper-V sanal makineleri, büyük veri analitiği, Veeam yedekleme havuzları vb.) bölünerek yönetilmesi için idealdir.
3.  **Devasa Ölçekli (Hyperscale) Veri Merkezleri**
    *   **Durum:** Yetersizdir (Yalnızca lokal/uç iş yükleri için tercih edilir).
    *   **Açıklama:** AWS, Google, Azure ve Meta gibi Exabayt seviyesinde veri işleyen devler, bu limitler çok küçük kalacağı için Windows tabanlı ReFS yerine kendi geliştirdikleri özel dağıtık dosya sistemlerini (Ceph, GFS vb.) kullanırlar.

---

## 4. ReFS'in Kurumsal Avantajları

*   **Blok Klonlama (Block Cloning):** Sanal disklerin (VHDX) kopyalanması veya checkpoint işlemlerinin metadata yönlendirmesi sayesinde saniyeler içinde tamamlanmasını sağlar.
*   **Veri Dayanıklılığı ve Onarım:** Bütünlük akışları (integrity streams) ile arka planda verileri sürekli tarayarak "bit rot" (veri bozulması) durumlarını otomatik tespit eder ve Storage Spaces aynalaması üzerinden kendiliğinden onarır.
