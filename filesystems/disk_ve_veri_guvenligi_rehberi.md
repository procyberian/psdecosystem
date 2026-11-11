# Disk Güvenliği, Dosya Sistemleri (ZFS & Ceph Odaklı) ve Adli Bilişim Rehberi

Bu döküman; veri merkezimizden yedekleme hizmeti alacak **müşteriler**, altyapıyı inşa eden ve yöneten **sistem yöneticileri/programcılar** ve sistemlerin dayanıklılığını test eden **bilgi güvenliği (Red Team/Pentest) ekipleri** için ortak bir teknik temel oluşturmak amacıyla hazırlanmıştır.

---

## 1. Veri Güvenliği ve Disk Geometrisi

Verinin kalıcı depolama birimlerinde (HDD/SSD) nasıl tutulduğunu bilmek, hem veri kurtarma algoritmaları yazmak hem de güvenli veri imha yöntemleri (data wiping) geliştirmek için şarttır.

### Donanım Seviyesinde Veri Yapısı
*   **HDD (Hard Disk Drive):** Veriler manyetik plakalar (platters) üzerindeki sektörlerde (sectors - geleneksel olarak 512 bayt, modern disklerde Advanced Format ile 4KB) saklanır. Adli bilişimde disk kafasının hizalama hataları veya manyetik kalıntılar (remanence) üzerinden veri analizi yapılabilir.
*   **SSD (Solid State Drive):** Veriler NAND flaş bellek hücrelerinde saklanır. SSD'lerin mekanik disklerden en büyük farkı **Wear Leveling (Aşınma Dengeleme)** ve **TRIM** mekanizmalarıdır. 
    *   *Güvenlik ve Kurtarma Etkisi:* TRIM komutu çalıştığında, işletim sistemi silinen blokları denetleyiciye (controller) bildirir ve arka planda veri tamamen temizlenir (Garbage Collection). Bu durum, SSD'lerde geleneksel yöntemlerle veri kurtarmayı neredeyse imkansız hale getirir.

### Veri Güvenliği Katsayıları ve Katmanları
1.  **Durağan Veri Şifreleme (Encryption at Rest):** Verinin fiziksel olarak çalınmasına karşı tam disk şifreleme (FDE) mekanizmaları kullanılmalıdır.
2.  **Yedekleme Stratejisi (3-2-1 Kuralı):** En az 3 kopya veri, 2 farklı medya türünde, en az 1 kopyası coğrafi olarak farklı bir veri merkezinde (remote data center) tutulmalıdır.
3.  **Bütünlük Doğrulaması (Data Integrity):** Verinin bozulup bozulmadığını (bit rot) tespit etmek için her blok veya dosya seviyesinde kriptografik bütünlük doğrulamaları (Checksum/Merkle Tree) kullanılmalıdır.

---

## 2. Dosya Sistemleri ve İşletim Sistemi İlişkileri

Dosya sistemleri, ham blok cihazlarını (raw block devices) anlamlı hiyerarşik yapılara dönüştüren yazılım katmanlarıdır. Her işletim sisteminin çekirdek (kernel) seviyesinde desteklediği yerel, harici ve dağıtık dosya sistemleri farklılık gösterir.

### Dosya Sistemlerinin Karşılaştırma Matrisi

| Dosya Sistemi | Geliştirici / OS Çıkış Noktası | Maksimum Dosya Boyutu | Temel Özellikleri | Veri Merkezi ve Güvenlik Odaklı Analizi |
| :--- | :--- | :--- | :--- | :--- |
| **ZFS (OpenZFS)** | Sun Microsystems / OpenZFS (BSD/Linux) | 16 EB | Copy-on-Write (CoW), Entegre Hacim Yönetimi (SPA/ZVOL), Yerleşik Şifreleme, Sıkıştırma. | Veri merkezleri için en güvenli dosya sistemlerinden biridir. Donanımsal RAID denetleyicilerine ihtiyaç duymaz (ZRAID). Merkle Tree tabanlı checksum yapısı sayesinde "sessiz veri bozulmalarını" (bit rot) otomatik tespit eder ve onarır (scrubbing). |
| **Ceph (CephFS / RADOS)** | Inktank / Red Hat / Açık Kaynak | Sınırsız (Dağıtık/Ölçeklenebilir) | Dağıtık Nesne, Blok ve Dosya Depolama, CRUSH Algoritması, Replikasyon/Erasure Coding. | Tek bir sunucu yerine binlerce sunucudan oluşan cluster mimarilerinde kullanılır. Donanım bağımsızdır; disk veya düğüm (node) arızalarında veriyi otomatik olarak yeniden dengeler (self-healing). Adli bilişimde ağ trafiği ve cluster loglarının analizi kritik önem taşır. |
| **EXT4** | Linux (Canonical/RedHat vb.) | 16 TB | Günlüklü (Journaling), Kararlı, Yaygın. | Linux sunucuların varsayılanıdır. Performansı yüksektir ancak yerleşik şifreleme ve anlık görüntü (snapshot) özellikleri ZFS kadar gelişmiş değildir. |
| **XFS** | SGI / Linux (Red Hat) | 8 EB | Yüksek ölçeklenebilirlik, paralel I/O. | Büyük depolama alanları ve yüksek veri işleme hızı gerektiren veri tabanı sunucuları için idealdir. |
| **BTRFS** | Oracle / Linux Open Source | 16 EB | Copy-on-Write (CoW), Snapshot, Built-in RAID. | Hızlı imaj alma ve yedekleme için uygundur. Veri bütünlüğünü sağlamak için arka planda sürekli doğrulama yapar. |
| **NTFS** | Microsoft Windows | 16 TB (Teorik 8 PB) | MFT (Master File Table), ACL (İzinler), Journaling. | Windows ekosisteminin standardıdır. Linux sistemlerde `ntfs-3g` sürücüleri veya modern `ntfs3` kernel modülü ile okunabilir/yazılabilir. |
| **APFS** | Apple (macOS / iOS) | 8 EB | CoW, Güçlü Şifreleme, Space Sharing. | Flash/SSD optimizasyonu mükemmeldir. Sadece Apple ekosisteminde tam performansla çalışır; Linux/Windows'ta üçüncü parti adli araçlar gerektirir. |
| **UFS** | BSD Ekosistemi | 8 ZB | Kararlı, güvenli, Unix standardı. | BSD tabanlı depolama ve ağ cihazlarında (FreeBSD, pfSense, opnsense vb.) kritik sistem bileşenlerini tutmak için tercih edilir. |

### İşletim Sistemi ve Sürüm İlişkileri (Uyumluluk Sınırları)
*   **Linux Çekirdeği ve ZFS:** ZFS lisans yapısı (CDDL) ile Linux çekirdeğinin lisansı (GPL) uyuşmadığı için ZFS yerel olarak Linux kernel ağacına dahil edilemez; DKMS (Dynamic Kernel Module Support) veya Ubuntu Pro gibi dağıtımların yerleşik kullanıcı alanı modülleri üzerinden yönetilir.
*   **Ceph Cluster Optimizasyonu:** Ceph istemcileri (CephFS/RBD) modern Linux çekirdeklerinde (Kernel v5.x/v6.x) en yüksek performansını gösterir. Özellikle son dönem güncellemelerinde alt hacim karantina (subvolume quarantine) ve ACL önbellekleme mekanizmaları ile güvenlik sıkılaştırılmıştır.
*   **Windows Server ve ReFS:** ReFS (Resilient File System), Microsoft'un büyük veri havuzları için geliştirdiği şifreleme ve bütünlük sistemidir. Dosya sistemi metadata sürümleri işletim sistemi versiyonuna (Server 2016 vs Server 2022) sıkı sıkıya bağlı olduğundan geriye dönük uyumluluk sorunları yaratabilir.

---

## 3. Platform Bağımsız Adli Bilişim ve Veri Kurtarma Araçları

Adli bilişim (Digital Forensics) ve veri analizi süreçlerinde ham disk imajları (E01, RAW/DD, AFF) üzerinde çalışılır.

### Disk İmajı ve Dosya Sistemi Analizi
*   **The Sleuth Kit (TSK) & Autopsy:** TSK komut satırı araçları (`fls`, `icat`, `ils`), Autopsy ise bunun grafik arayüzüdür (GUI). Standart dosya sistemlerinin yanı sıra havuz tabanlı veya dağıtık sistemlerde doğrudan ham block imajları üzerinden metadata analizi yapabilir. Silinen dosyaları, inode yapılarını ve dosya sistemi zaman damgalarını (MACB) listeler.
*   **FTK Imager (CLI/GUI):** Delil bütünlüğünü bozmadan (Write-Blocker kullanarak veya mantıksal olarak) diskin bit-bit (`raw/dd`) veya sıkıştırılmış adli imajını (`E01`) alır. MD5 ve SHA-1 hash değerlerini otomatik hesaplayarak bütünlüğü doğrular.

### Dosya Kurtarma ve Dosya Kazıma (File Carving)
*   **TestDisk:** Dosya sistemi tabloları bozulmuş, partition haritası silinmiş diskleri onarmak için mükemmel bir araçtır. Silinen partition'ları tarayıp geri getirir ve boot sektörlerini tamir eder.
*   **PhotoRec:** Dosya sisteminden bağımsız olarak çalışır (File Carving). Disk üzerindeki verileri ham blok seviyesinde okur ve bilinen dosya başlıklarını (Magic Numbers/Signatures - örn: PDF için `%PDF-`, JPEG için `FF D8 FF`) arayarak verileri kurtarır. **ZFS veya Ceph disklerinde veri parçalandığı (fragmentation) veya şeritlendiği (striping) durumlarda ham kazıma işlemleri karmaşık matematiksel birleşmeler gerektirir.**
*   **Foremost & Scalpel:** Konfigürasyon dosyalarına (`foremost.conf`) göre belirli dosya türlerini ham imaj içerisinden "kazıyarak" çıkaran yüksek performanslı adli araçlardır.

### Gelişmiş Veri ve Bellek (RAM) Analizi
*   **Volatility Framework:** Canlı sistemden alınan RAM imajlarının analizi için kullanılır. Dosya şifreleme anahtarları (ZFS yerel şifreleme keyleri, BitLocker, LUKS anahtarları), açık ağ bağlantıları ve memory'de çalışan zararlı kodlar bu araçla tespit edilir.

---

## 4. Paydaşlar İçin Eylem Planı (Roadmap)

### Müşteriler İçin: Güvenli Yedekleme Yol Haritası
1.  **Envanter Çıkarma:** Yedeklenecek verinin hangi dosya sisteminde tutulduğunu belirleyin. Dağıtık mimariler için uygun replikasyon stratejisini seçin.
2.  **İstemci Tarafı Şifreleme (Zero-Knowledge):** Verilerinizi veri merkezine göndermeden önce kendi belirlediğiniz kriptografik anahtarlarla (AES-256) şifreleyin.
3.  **Bütünlük Takibi:** Veri merkezine aktarılan her yedek dosyasının aktarım öncesi ve sonrası SHA-256 hash değerlerini karşılaştırarak "sessiz veri bozulmalarına" karşı önlem alın.

### Sistem Yöneticileri ve Programcılar İçin: Tasarım ve Kodlama Rehberi
*   **Düşük Seviyeli I/O İşlemleri (C/C++):** Ham blok cihazları üzerinde çalışırken işletim sisteminin buffer mekanizmalarını (`O_DIRECT` veya `O_SYNC` bayrakları ile) bypass ederek verinin diske fiziksel olarak yazıldığından emin olun.
*   **Havuz Kontrolü ve API Entegrasyonu:** ZFS/Ceph gibi gelişmiş altyapılarda depolama durumunu izlemek ve otomatik havuz (pool) genişletmek için libzfs veya librados kütüphanelerini entegre ederek C/C++/Go tabanlı otomasyon araçları kodlayın.
*   **Güvenli Silme Algoritmaları (Data Wiping):** ZFS ve Ceph gibi Copy-on-Write (CoW) tabanlı sistemlerde eski verinin üzerine yazma (in-place overwrite) mantığı çalışmaz. Bu nedenle güvenli silme için snapshot'ların tamamen temizlenmesi, havuzun scrub edilmesi veya block-level şifreleme anahtarının yok edilmesi (crypto-shredding) yöntemini kodlayın.

### Bilgi Güvenliği ve Red Team (Pentest) Ekipleri İçin: Test Metodolojisi
*   **Adli Bilişim Direnç Testi (Anti-Forensics Assessment):** Sistemlerde iz bırakmadan operasyon yapma veya geride kalan verinin kurtarılıp kurtarılamayacağını test edin. CoW sistemlerin geçmiş bloklarda bıraktığı verileri (slack space) inceleyin.
*   **Yetki Yükseltme ve Dosya İzinleri Analizi:** SUID/SGID bitleri ayarlanmış tehlikeli binary'leri, zayıf ACL yapılandırmalarını ve Ceph auth/ZFS yetkilendirme (allow) protokollerini denetleyin.
*   **Şifreleme Analizi:** `Volatility` kullanarak, şifreli disklerin anahtarlarının ham RAM imajlarından elde edilip edilemediğini simüle edin. Donanımsal write-blocker'lar ve adli imaj alma süreçlerinin standartlara (ISO/IEC 27037) uygunluğunu doğrulayın.
