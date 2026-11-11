# Dosya Sistemi ve Linux Üzerinde Dosya Sistemi Geliştirme Rehberi

**Dosya sistemi (File System)**, verilerin depolama aygıtlarında (hard disk, SSD, USB bellek vb.) nasıl saklanacağını, organize edileceğini, isimlendirileceğini ve bunlara nasıl erişileceğini belirleyen **yapısal kurallar ve veri modelleri bütünüdür**. Dosya sistemi olmasaydı, depolama aygıtınız sadece devasa bir sıfırlar ve birler yığını olurdu; hangi verinin nerede başlayıp nerede bittiğini bilemezdiniz.

Linux üzerinde kendi dosya sisteminizi yazmak, işletim sistemi çekirdeği (kernel) seviyesinde veya kullanıcı alanı (user-space) seviyesinde derin bir yolculuktur. Bu yolculuğa başlamak için izlemeniz gereken harita ve incelemeniz gereken ilk örnekler aşağıdadır.

---

### 🚀 Nereden ve Nasıl Başlamalısınız?

Bir dosya sistemi yazmak için önünüzde iki temel yol vardır: Çekirdek Alanı (Kernel Space) ve Kullanıcı Alanı (User Space). **Kesinlikle Kullanıcı Alanı (FUSE) ile başlamalısınız.**

#### 1. FUSE (Filesystem in Userspace) ile Başlayın
Çekirdek kodu yazmak zordur; en ufak bir hatada işletim sisteminiz çöker (Kernel Panic). FUSE, Linux çekirdeğine dokunmadan, sıradan bir C/C++ veya Python programı yazar gibi dosya sistemi geliştirmenizi sağlar.
* **Avantajı:** Çökme durumunda sadece yazdığınız program kapanır, sistem zarar görmez. Hata ayıklama (debugging) çok kolaydır.
* **Nasıl Çalışır:** FUSE size `open()`, `read()`, `write()`, `readdir()` gibi standart sistem çağrılarını fonksiyon olarak sunar. Siz bu fonksiyonların içini doldurursunuz.

#### 2. Yol Haritası
* **C Dilini ve Pointer Yapılarını Güçlendirin:** Dosya sistemleri doğrudan hafıza ve disk blokları yönetimiyle ilgilidir.
* **İşletim Sistemleri Teorisi Öğrenin:** *Superblock*, *Inode*, *Directory Entry (dentry)* ve *Data Blocks* kavramlarını mutlaka su gibi bilmelisiniz.
* **Küçük Bir RAM Disk Yapın:** Verileri diske yazmak yerine, bilgisayarın RAM'inde tutan geçici bir FUSE dosya sistemi yazarak ilk pratiğinizi yapın.

---

### 🔍 İlk Hangi Dosya Sistemini İncelemelisiniz?

Karmaşık modern dosya sistemleri (EXT4, Btrfs, XFS) içinde kaybolmamak için kesinlikle en basit ve minimalist yapılardan başlamalısınız.

#### 1. ext2 (Second Extended Filesystem)
Linux'un atası sayılan, modern EXT4'ün temelini oluşturan yapıdır. 
* **Neden incelenmeli:** Günümüz dosya sistemlerinin karmaşık optimizasyonlarına (journaling, extents vb.) sahip değildir. Temel Linux VFS (Virtual File System) mimarisini anlamak için **en temiz kaynaktır**. Linux çekirdek kaynak kodlarında `fs/ext2/` dizinini inceleyebilirsiniz.

#### 2. SimpleFS / RamFS
Eğitim amacıyla yazılmış, açık kaynaklı minimalist dosya sistemleridir.
* **Neden incelenmeli:** Github üzerinde "SimpleFS" veya "Writing a file system in Linux" aramaları yaptığınızda karşınıza çıkacak 500-1000 satırlık kodlar, devasa çekirdek kodlarından çok daha öğreticidir.

#### 3. FAT16 / FAT32
Linux'a özgü olmasa da yapısı inanılmaz derecede basittir.
* **Neden incelenmeli:** Dosyaların bir "zincir" (Linked List) mantığıyla nasıl bağlanacağını anlamak için harika bir matematiksel model sunar. FUSE ile bir FAT okuyucu yazmak harika bir başlangıç projesidir.

---

### 🛠️ Geliştirici Araçları ve Kaynak Önerileri

* **Libfuse:** FUSE geliştirme kütüphanesinin resmi deposundaki Örnek Kodları inceleyin.
* **Kitap:** *Robert Love - Linux Kernel Development* (Linux çekirdeğinin dosya sistemlerine bakışını anlamak için).
* **Kitap:** *Operating Systems: Three Easy Pieces (OSTEP)* (Dosya sistemleri teorik kısmı için ücretsiz ve harika bir kitaptır).
