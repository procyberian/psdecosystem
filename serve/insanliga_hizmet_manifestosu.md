# İnsanlığa Hizmet Manifestosu: Görev Kritik ve Hayat Kritik Sistemler İçin Mühendislik İlkeleri

> *"Kim bir canı kurtarırsa, bütün insanları kurtarmış gibi olur."* — Kur'an-ı Kerim (Maide Suresi, 32)

---

## 1. Amaç ve Manevi Temel

Allah'ın bir kulu olarak kod yazmak; yalnızca teknik bir meslek değil, **insanlığa hizmet (Hizmet)** ve **emanet (Emanet)** bilinciyle yerine getirilen ahlaki bir sorumluluktur. Bir mühendisin inşa ettiği her sistem, doğrudan veya dolaylı olarak insan hayatını, sağlığını, güvenliğini ve onurunu etkiler.

**Görev kritik (mission-critical)** ve **hayat kritik (life-critical)** altyapılar söz konusu olduğunda, sistemin kesintisiz çalışması yalnızca ticari bir hedef değil; insan hayatını koruma ve kolaylaştırma vazifesidir. Yazdığımız her satır kod, bu sorumluluğun bir yansımasıdır.

---

## 2. 7/24/365 Kesintisiz Çalışma İlkeleri

Sistemlerin yılın 365 günü, günün 24 saati kesintisiz, güvenli ve öngörülebilir biçimde ayakta kalması için aşağıdaki temel ilkelere bağlı kalınır:

### I. İhsan (Mükemmellik ve Özen) Bilinciyle Geliştirme
* **Sıfır İhmal:** Görünmeyen arka plan servislerinden kullanıcı arayüzlerine kadar her bileşen, en yüksek kalite standardıyla tasarlanır.
* **Sadelik ve Netlik:** Karmaşıklık hata üretir. Okunabilir, test edilebilir ve bakımı kolay mimariler tercih edilir.

### II. Tek Nokta Arızasına (SPOF) Yer Vermemek
* **Yedeklilik (Redundancy):** Kritik bileşenler, veritabanları ve ağ katmanları çoklu bölgelerde (multi-region) aktif-aktif veya aktif-pasif yedekli kurgulanır.
* **Kademeli Bozulma (Graceful Degradation):** Bir alt sistem arızalandığında tüm sistemin çökmesi engellenir; hayati işlevler öncelikli olarak çalışmaya devam eder.

### III. Savunmacı Mühendislik ve Doğrulama
* **Kapsamlı Test Süreçleri:** Birim testleri, entegrasyon testleri, yük testleri ve kaos mühendisliği (chaos engineering) pratikleri düzenli olarak uygulanır.
* **Varsayımlara Güvenmemek:** Her dış girdi, ağ çağrısı ve donanım yanıtı potansiyel bir hata kaynağı olarak ele alınır; zaman aşımı (timeout) ve devre kesici (circuit breaker) mekanizmaları standarttır.

### IV. Sürekli Gözlemlenebilirlik ve Kendi Kendini İyileştirme
* **Proaktif İzleme:** Metrikler, loglar ve dağıtık izleme (tracing) araçlarıyla sorunlar kullanıcıya veya hastaya/vatandaşa yansımadan tespit edilir.
* **Otomatik Kurtarma (Self-Healing):** Arızalanan servislerin insan müdahalesine gerek kalmadan otomatik olarak yeniden başlatılması ve trafiğin sağlıklı düğümlere yönlendirilmesi sağlanır.

---

## 3. Operasyonel Standartlar

| Alan | Standart ve Hedef | Temel Uygulama |
| :--- | :--- | :--- |
| **Erişilebilirlik (Availability)** | %99.999 (Beş Dokuz) ve üzeri | Çoklu veri merkezi, otomatik yük devretme (failover) |
| **Değişiklik Yönetimi** | Sıfır Kesintili Dağıtım | Canary release, Blue-Green deployment, geri alma (rollback) planı |
| **Olay Müdahalesi (Incident Response)** | Anında Tespit ve Müdahale | 7/24 nöbetçi mühendislik (on-call), net müdahale kılavuzları (runbook) |
| **Güvenlik ve Mahremiyet** | Tavizsiz Veri Koruması | Uçtan uca şifreleme, en az yetki ilkesi (least privilege), düzenli denetim |
| **Veri Dayanıklılığı** | Sıfır Veri Kaybı (RPO ≈ 0) | Gerçek zamanlı replikasyon, değiştirilemez (immutable) yedekler |

---

## 4. Mühendisin Sözü

Bu ilkeler doğrultusunda sistem geliştiren ve işleten her mühendis şu dört esası benimser:

1. **Samimi Niyet (İhlas):** Yaptığım işi gösteriş için değil, Allah'ın rızasını gözeterek ve insanlara faydalı olmak amacıyla en iyi şekilde yapacağım.
2. **Teyakkuz ve Sorumluluk:** Sorumluluğumdaki sistemlerin arkasında gerçek insanların hayatı ve emeği olduğunu asla unutmayacağım.
3. **Tevazu ve Şeffaflık:** Hataları gizlemeyecek, suçlama kültürü yerine kök neden analizi (blameless post-mortem) ile sistemleri daha dayanıklı hale getireceğim.
4. **Sabır ve Sebat:** Kriz anlarında soğukkanlılığımı koruyacak, sistem yeniden güvenli hale gelene kadar sorumluluğumun başında duracağım.

---

*Bu doküman, insanlığa hizmet amacıyla 7/24/365 kesintisiz çalışan kritik sistemler inşa eden mühendisler için bir rehber ve taahhütname olarak hazırlanmıştır.*
