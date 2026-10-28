# PSD Ekosistemi Belgeleri

Bu depo, PSD Ekosistemi ile ilgili proje, yazılım, altyapı ve lisans
belgelerini bir araya getirir. İçerik ağırlıklı olarak PDF yayınlarından,
bunun yanında düzenlenebilir ODT belgelerinden ve düz metin bir öneriden
oluşur. [ABD İngilizcesi README](<README.md>) dosyası da mevcuttur.

## Belge Kütüphanesi

### PSD Ekosistemi ve GNU/Linux

- [PSD Ekosistemi, 1. belge](<ecosystem/PSD_Ecosystem.pdf>)
- [PSD Ekosistemi, 2. belge](<ecosystem/PSD_Ecosystem2.pdf>)
- [PSD Ekosistemi, 3. belge](<ecosystem/PSD_Ecosystem3.pdf>)
- [PSD nedir?](<ecosystem/psdnedir.pdf>)
- [Sivil PSD GNU/Linux Copyleft](<ecosystem/psdgnulinux_sivil_copyleft.pdf>)

### Kullanıcı Arayüzleri ve Geliştirme

- [PSD TUI](<interfaces/psdtui.pdf>) ve [PSD TUI, 2. belge](<interfaces/psdtui2.pdf>)
- [C++ Çekirdeği](<kernel/cppkernel.pdf>)
- [Çekirdek Programlama 101](<kernel/kernel_programming_101.pdf>)
- [Çerçeve tabanlı yapay zeka ile işletim sistemine entegre yapay zeka](<kernel/work.pdf>)
- [Linux ve GNU geliştiricileri: Linux çekirdeğini çatallama ve lisanslama](<kernel/linuxgnudevelopers.pdf>)
- [Hurd için C++ ile kullanıcı alanı sürücüsü yazabilir miyim?](<kernel/C++ Can I write userspace drivers with C++ for hurd.pdf>)
- [Hurd](<kernel/hurd.pdf>)
- [Linux ve C++](<kernel/linuxcpp.pdf>)
- [C++ ile bellek yönetimi](<kernel/memcpp.pdf>)
- [Linux için ağ alt sistemi](<networking/network subsystem for linux.pdf>)
- [Unix geliştirme](<unix/unixdev.pdf>) ([düzenlenebilir ODT](<unix/unixdev.odt>))

### Lisp ve Kabuk Dilleri

- [QShell deposunu inceleme rehberi](<lısp/bu depoda dikkat etmem gereken yerler nelerdir qsh.pdf>) ([Markdown](<lısp/bu depoda dikkat etmem gereken yerler nelerdir qsh.md>)): Guile tabanlı mimariyi, incelenmesi gereken temel dizinleri ve sistem betiklerinde QShell kullanımını ele alan Türkçe bir rehber.

### Dağıtım Planlaması

- [PSD deposu değerlendirmesi ve mimari görünümü](<distro/bu depoda dikkat etmem gereken yerler nelerdir qsh 1.pdf>) ([Markdown](<distro/bu depoda dikkat etmem gereken yerler nelerdir qsh 1.md>)): Depoyu tasarım belgeleri olarak değerlendiren, öngörülen Çekirdek, UMFS, Guile ve QShell katmanlarını ve önerilen öncelikleri ele alan Türkçe belge.

### MassForge

- [Git ve CI/CD platformu mimari tasarımı](<massforge/git_platform_mimari_tasarimi.pdf>) ([Markdown](<massforge/git_platform_mimari_tasarimi.md>)): C/C++ ve GNU Assembler odaklı, yüksek performanslı bir Git ve CI/CD platformunun çekirdek, depolama, CI/CD motoru, web teknolojileri ve ölçekleme başlıklarını kapsayan mimari yol haritası.

### Topluluklar, Kuruluşlar ve Hizmetler

- [KamuNet](<networking/kamunet.pdf>)
- [DAO](<organizations/dao.pdf>) ([düzenlenebilir ODT](<organizations/dao.odt>))
- [QB Networks girişim önerisi](<organizations/qbnetworks_startup.pdf>) ([düzenlenebilir ODT](<organizations/qbnetworks_startup.odt>); [düz metin](<organizations/qbnetworks_startup.txt>))
- [Serebral](<organizations/serebral.pdf>)
- [MassCollabs hizmetleri](<organizations/mass.tr.pdf>)

### Lisanslama

- [Lisanslama 101](<licensing/lisanslama-101.pdf>) ve [Lisanslama 101, 2. belge](<licensing/lisanslama-101-2.pdf>)
- [BSD 3-Clause ve BNGPL karşılaştırması](<licensing/bsd3clause_vs_bngpl.pdf>)
- [BNGPL 1.0 veya sonrası kapsamında çerçeve](<licensing/framework_bngpl.pdf>)
- [Askerî BNGPL lisanslaması](<licensing/askerilisans.pdf>)
- [BNGPL 1.0](<licensing/bngpl-1.0.md>), [BNGPL 2.0](<licensing/bngpl-2.0.md>) ve [BNGPL 3.0](<licensing/bngpl-3.0.md>)
- [GNU Affero Genel Kamu Lisansı 3.0](<licensing/agpl-3.0.md>)
- [Lisans istisnası](<licensing/exception.md>): sivil PSD GNU/Linux copyleft belgesinin AGPLv3-or-later kapsamında olduğu belirtilmiştir.

### Dosya Sistemleri

- [Dosya sistemi ve Linux üzerinde dosya sistemi geliştirme rehberi](<fs/dosya_sistemi_rehberi.pdf>) ([Markdown](<fs/dosya_sistemi_rehberi.md>))
- [Debian PSD UMFS rehberi](<fs/debianpsdumfs.pdf>) ([Markdown](<fs/debianpsdumfs.md>))
- [UMFS teorisi](<fs/umfs/umfs_theory.pdf>) ([Markdown](<fs/umfs/umfs_theory.md>))
- [UMFS bindings](<fs/umfs/bu yapida bindings ne anlama gelir.pdf>) ([Markdown](<fs/umfs/bu yapida bindings ne anlama gelir.md>))
- [UMFS bindings, bölüm 1: Guile](<fs/umfs/bu yapida bindings ne anlama gelir 1.pdf>) ([Markdown](<fs/umfs/bu yapida bindings ne anlama gelir 1.md>))
- [UMFS bindings, bölüm 2: lisanslama](<fs/umfs/bu yapida bindings ne anlama gelir 2.pdf>) ([Markdown](<fs/umfs/bu yapida bindings ne anlama gelir 2.md>))
- [ext2/ext3 kod analizi](<fs/ext2-3/ext2fs_kod_analizi.pdf>) ([Markdown](<fs/ext2-3/ext2fs_kod_analizi.md>))
- [Hurd dosya sistemi kılavuzu](<fs/hurd/hurd_filesystem_guide.pdf>) ([Markdown](<fs/hurd/hurd_filesystem_guide.md>))
- [PSD dosya sistemi kılavuzu](<fs/psdfs/psd_dosya_sistemi_kilavuzu.pdf>) ([Markdown](<fs/psdfs/psd_dosya_sistemi_kilavuzu.md>))
- [ReFS ve Windows dosya sistemleri raporu](<fs/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.pdf>) ([Markdown](<fs/windowsfs/refs_ve_windows_dosya_sistemleri_raporu.md>))

### Toplum ve Lisans Analizi

- [AGPL ve BNGPL lisanslarının Marksist açıdan karşılaştırılması](<society/lisans_society.pdf>) ([Markdown](<society/lisans_society.md>))
- [AGPL ve BNGPL lisanslarının Marksist karşılaştırması](<society/lisanslarin_marksist_karsilastirmasi.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi.md>))
- [AGPL ve BNGPL lisanslarının genişletilmiş Marksist karşılaştırması, 2. sürüm](<society/lisanslarin_marksist_karsilastirmasi_v2.pdf>) ([Markdown](<society/lisanslarin_marksist_karsilastirmasi_v2.md>))

### Bellek

- [Bellek genel bakışı](<bellek/bellek.pdf>)
- [Bellek ayırma, 1. belge](<bellek/malloc_1.pdf>)
- [Bellek ayırma, 2. belge](<bellek/malloc_2.pdf>)

## Proje Geçmişi

Depoda ilk commit'ten son proje commit'ine kadar yapılan değişikliklerin
özeti:

- **7 Ekim 2026:** Üç PSD Ekosistemi yayınıyla koleksiyon başlatıldı ve iki
  PSD TUI yayını eklendi.
- **8 Ekim 2026:** C++ çekirdekleri, Hurd, C++ kullanıcı alanı sürücüleri,
  Linux, bellek yönetimi, Linux ağ iletişimi ve KamuNet hakkında belgeler
  eklendi.
- **9 Ekim 2026:** Lisanslama kılavuzları, DAO yayınları, PSD'ye giriş ve QB
  Networks girişim önerisi eklendi. `.gitignore`, `README.md` ve başlangıçta
  MIT lisanslı `LICENSE` ile depo temelleri oluşturuldu.
- **10 Ekim 2026:** Unix geliştirme belgeleri eklendi; BNGPL 1.0 yayımlandı
  ve kök `LICENSE` ile README bu lisansa göre güncellendi.
- **11 Ekim 2026:** BSD 3-Clause ile BNGPL'yi karşılaştıran, BNGPL kapsamında
  bir çerçeveyi tanıtan, Serebral için LibreOffice desteğini belgeleyen ve
  MassCollabs hizmetlerini açıklayan yayınlar eklendi.
- **12 Ekim 2026:** BNGPL 2.0 ve 3.0 yayımlandı; kök lisans ve README
  güncellendi. Askerî BNGPL belgeleri eklendi ve sivil PSD GNU/Linux
  copyleft yayını için AGPLv3-or-later istisnası kaydedildi.
- **18 Ekim 2026:** `bellek/` altına üç bellek yayını eklendi.
- **18 Ekim 2026:** AGPL 3.0 lisans metni eklendi; proje geçmişi ve lisans
  koşulları belgelerde açıklandı.
- **18 Ekim 2026:** *Çekirdek Programlama 101* yayını eklendi.
- **18 Ekim 2026:** Çerçeve tabanlı ile işletim sistemine entegre yapay zekayı
  anlatan `work.pdf` ve Linux çekirdeğini çatallamayı, GPLv2, GPLv3 ve AGPLv3
  lisanslama sonuçlarıyla birlikte ele alan `linuxgnudevelopers.pdf` eklendi.
- **24 Ekim 2026:** `fs/` altına ext2/ext3, Hurd, PSD ve ReFS/Windows dosya
  sistemlerini kapsayan, her biri Markdown ve PDF biçiminde dosya sistemi
  belgeleri eklendi.
- **25 Ekim 2026:** `society/` altına AGPL ve BNGPL lisanslarını Marksist
  açıdan karşılaştıran, Markdown ve PDF biçiminde Türkçe belge eklendi.
- **25 Ekim 2026:** `society/` altına AGPL ve BNGPL lisanslarının Marksist
  açıdan iki ek Türkçe karşılaştırması, genişletilmiş ikinci sürümü de dahil
  olmak üzere, Markdown ve PDF biçiminde eklendi.
- **26 Ekim 2026:** Yayınlar konu klasörlerinde düzenlendi; dosya sistemi ve
  toplum belgeleri mevcut konu klasörlerinde bırakıldı.
- **26 Ekim 2026:** `fs/umfs/umfs_theory` eklendi; UMFS (Universal Massive
  File System) tasarımını, çekirdek ve sistem betik katmanlarını ve yapay zeka
  değerlendirmelerini ele alan Türkçe belge, Markdown ve PDF biçiminde sunuldu.
- **26 Ekim 2026:** `fs/umfs/` altına dil bağlayıcılarını (bindings), Guile'ın
  gömülü Lisp motoru olarak kullanımını ve GNU AGPL v3 veya üzeri lisanslamayı
  ele alan üç Türkçe UMFS notu, Markdown ve PDF biçiminde eklendi.
- **26 Ekim 2026:** Guile tabanlı mimariyi, incelenmesi gereken temel
  dizinleri ve sistem betiklerinde QShell kullanımını ele alan Türkçe QShell
  depo rehberi Markdown ve PDF biçimlerinde eklendi.
- **26 Ekim 2026:** `distro/` altına depoyu ve öngörülen Çekirdek, UMFS, Guile
  ve QShell mimarisini değerlendiren Türkçe belge, Markdown ve PDF biçiminde
  eklendi.
- **28 Ekim 2026:** `massforge/` altına C/C++ ve GNU Assembler odaklı,
  yüksek performanslı bir Git ve CI/CD platformunun mimari tasarımını anlatan
  Türkçe belge, Markdown ve PDF biçiminde eklendi.

[ChangeLog](<ChangeLog>), ilk commit'ten son proje commit'ine kadar olan
değişiklikleri tarih sırasıyla ve eklenen belgelerin adlarıyla kaydeder.

## Lisans

Telif hakkı (c) 2026-2027 PSD Yazarları.

Belgeye özgü bir istisna bulunmadıkça bu depo, Proje Sahibi tarafından resmen
yayımlanan ve bu yükseltme yoluna izin veren sonraki bir sürüm veya Broad
Netwide General Public License (BNGPL), Sürüm 3.0 kapsamında lisanslanır.
koşullar için [LICENSE](<LICENSE>) dosyasına ve [BNGPL 3.0 metnine](<licensing/bngpl-3.0.md>)
bakın. [psdgnulinux_sivil_copyleft.pdf](<ecosystem/psdgnulinux_sivil_copyleft.pdf>)
belgesi için geçerli istisna [exception.md](<licensing/exception.md>) dosyasında
kaydedilmiştir.

Bu materyal herhangi bir garanti verilmeksizin, “olduğu gibi” sunulur.
İkili biçimde dağıtılması veya bir bulut ya da SaaS arayüzü üzerinden
sunulması durumunda, ilgili BNGPL koşulları uyarınca telif ve lisans
bildirimlerine lisansın belirttiği şekilde erişim sağlanmalıdır.
