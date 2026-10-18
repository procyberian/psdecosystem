# PSD Ekosistemi Belgeleri

Bu depo, PSD Ekosistemi ile ilgili proje, yazılım, altyapı ve lisans
belgelerini bir araya getirir. İçerik ağırlıklı olarak PDF yayınlarından,
bunun yanında düzenlenebilir ODT belgelerinden ve düz metin bir öneriden
oluşur. [ABD İngilizcesi README](<README.md>) dosyası da mevcuttur.

## Belge Kütüphanesi

### PSD Ekosistemi ve GNU/Linux

- [PSD Ekosistemi, 1. belge](<PSD_Ecosystem.pdf>)
- [PSD Ekosistemi, 2. belge](<PSD_Ecosystem2.pdf>)
- [PSD Ekosistemi, 3. belge](<PSD_Ecosystem3.pdf>)
- [PSD nedir?](<psdnedir.pdf>)
- [Sivil PSD GNU/Linux Copyleft](<psdgnulinux_sivil_copyleft.pdf>)

### Kullanıcı Arayüzleri ve Geliştirme

- [PSD TUI](<psdtui.pdf>) ve [PSD TUI, 2. belge](<psdtui2.pdf>)
- [C++ Çekirdeği](<cppkernel.pdf>)
- [Çekirdek Programlama 101](<kernel_programming_101.pdf>)
- [Hurd için C++ ile kullanıcı alanı sürücüsü yazabilir miyim?](<C++ Can I write userspace drivers with C++ for hurd.pdf>)
- [Hurd](<hurd.pdf>)
- [Linux ve C++](<linuxcpp.pdf>)
- [C++ ile bellek yönetimi](<memcpp.pdf>)
- [Linux için ağ alt sistemi](<network subsystem for linux.pdf>)
- [Unix geliştirme](<unixdev.pdf>) ([düzenlenebilir ODT](<unixdev.odt>))

### Topluluklar, Kuruluşlar ve Hizmetler

- [KamuNet](<kamunet.pdf>)
- [DAO](<dao.pdf>) ([düzenlenebilir ODT](<dao.odt>))
- [QB Networks girişim önerisi](<qbnetworks_startup.pdf>) ([düzenlenebilir ODT](<qbnetworks_startup.odt>); [düz metin](<qbnetworks_startup.txt>))
- [Serebral](<serebral.pdf>)
- [MassCollabs hizmetleri](<mass.tr.pdf>)

### Lisanslama

- [Lisanslama 101](<lisanslama-101.pdf>) ve [Lisanslama 101, 2. belge](<lisanslama-101-2.pdf>)
- [BSD 3-Clause ve BNGPL karşılaştırması](<bsd3clause_vs_bngpl.pdf>)
- [BNGPL 1.0 veya sonrası kapsamında çerçeve](<framework_bngpl.pdf>)
- [Askerî BNGPL lisanslaması](<askerilisans.pdf>)
- [BNGPL 1.0](<bngpl-1.0.md>), [BNGPL 2.0](<bngpl-2.0.md>) ve [BNGPL 3.0](<bngpl-3.0.md>)
- [GNU Affero Genel Kamu Lisansı 3.0](<agpl-3.0.md>)
- [Lisans istisnası](<exception.md>): sivil PSD GNU/Linux copyleft belgesinin AGPLv3-or-later kapsamında olduğu belirtilmiştir.

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

[ChangeLog](<ChangeLog>), ilk commit'ten son proje commit'ine kadar olan
değişiklikleri tarih sırasıyla ve eklenen belgelerin adlarıyla kaydeder.

## Lisans

Telif hakkı (c) 2026-2027 PSD Yazarları.

Belgeye özgü bir istisna bulunmadıkça bu depo, Proje Sahibi tarafından resmen
yayımlanan ve bu yükseltme yoluna izin veren sonraki bir sürüm veya Broad
Netwide General Public License (BNGPL), Sürüm 3.0 kapsamında lisanslanır.
Koşullar için [LICENSE](<LICENSE>) dosyasına ve [BNGPL 3.0 metnine](<bngpl-3.0.md>)
bakın. [psdgnulinux_sivil_copyleft.pdf](<psdgnulinux_sivil_copyleft.pdf>)
belgesi için geçerli istisna [exception.md](<exception.md>) dosyasında
kaydedilmiştir.

Bu materyal herhangi bir garanti verilmeksizin, “olduğu gibi” sunulur.
İkili biçimde dağıtılması veya bir bulut ya da SaaS arayüzü üzerinden
sunulması durumunda, ilgili BNGPL koşulları uyarınca telif ve lisans
bildirimlerine lisansın belirttiği şekilde erişim sağlanmalıdır.
