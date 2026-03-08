# Case_Study_03_ACV
İleri Veri Analitiği - Case Studies

# Enerji Tüketim Verilerinde Anomali Analizi

## Proje Hakkında

Bu projede akıllı sayaçlardan elde edilen elektrik ölçüm verileri kullanılarak **normal dışı enerji tüketim davranışlarının tespit edilmesi** amaçlanmıştır.

Akım, gerilim ve enerji tüketimi gibi elektriksel parametreler analiz edilerek aşağıdaki durumlar belirlenmeye çalışılmıştır:

* Olası kaçak elektrik kullanımı
* Sayaç arızaları
* Faz dengesizlikleri
* Şebeke kaynaklı anormal durumlar

Projenin amacı, ham ölçüm verilerini analiz ederek **operasyonel karar destek sağlayabilecek içgörüler üretmektir.**


# Veri Seti

Veri seti akıllı sayaçlardan **15 dakikalık periyotlarla kaydedilen elektrik ölçüm verilerini** içermektedir.

**Veri seti özellikleri**

* Toplam kayıt sayısı: **353.949**
* Toplam değişken sayısı: **18**

Önemli değişkenler:

| Değişken          | Açıklama                 |
| ----------------- | ------------------------ |
| tesisat_no_id     | Abone kimliği            |
| il / ilce         | Abonenin bulunduğu konum |
| l1, l2, l3        | Faz akım değerleri       |
| v1, v2, v3        | Faz gerilim değerleri    |
| t0                | Toplam enerji tüketimi   |
| ri / rc           | Reaktif enerji değerleri |
| load_profile_date | Ölçüm zamanı             |

Gerilim değişkenlerinde yaklaşık **%21 eksik veri** bulunmaktadır.


# Proje Aşamaları

## 1- Veri Ön İşleme

* Veri setinin yüklenmesi
* Tarih değişkeninin zaman serisi formatına çevrilmesi
* Eksik gerilim değerlerinin doldurulması
* Veri sıralama ve kontrol işlemleri


## 2- Feature Engineering

Elektriksel davranışı daha iyi analiz edebilmek için yeni değişkenler oluşturulmuştur.

* Ortalama akım
* Ortalama gerilim
* Faz dengesizliği
* Tüketim farkı (zaman bazlı)


## 3- Kural Tabanlı Anomali Tespiti

Elektrik dağıtım sistemlerinde görülebilecek bazı anormal durumlar kurallar ile tespit edilmiştir.

Örnek durumlar:

* **Akım var fakat tüketim yok**
* **Tüketim var fakat akım çok düşük**
* **Faz dengesizliği yüksek**

Bu kurallar kullanılarak her kayıt için bir **anomali skoru** oluşturulmuştur.


## 4- Makine Öğrenmesi ile Anomali Tespiti

Kural tabanlı yönteme ek olarak **Isolation Forest algoritması** kullanılarak makine öğrenmesi tabanlı anomali tespiti gerçekleştirilmiştir.

Model aşağıdaki değişkenleri kullanarak anormal gözlemleri belirlemektedir:

* Akım değerleri
* Gerilim değerleri
* Reaktif enerji
* Ortalama akım
* Ortalama gerilim
* Faz dengesizliği


# Analiz Çıktıları

Proje kapsamında aşağıdaki analizler gerçekleştirilmiştir:

* İl bazında anomali dağılımı
* Günlük anomali trend analizi
* En yüksek riskli abonelerin belirlenmesi

Bu analizler elektrik dağıtım şirketlerinin **saha operasyonlarını planlamasına yardımcı olabilir.**


# Kullanılan Teknolojiler

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook


# Sonuç

Bu proje akıllı sayaç verilerinin analiz edilerek **anomali tespiti yapılabileceğini** göstermektedir.

Veri ön işleme, feature engineering ve makine öğrenmesi yöntemleri kullanılarak enerji tüketim verilerinden anlamlı içgörüler elde edilmiştir.

