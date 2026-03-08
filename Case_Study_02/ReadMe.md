# Case_Study_02_ACV

## İleri Veri Analitiği | Elektrik Tüketim Analizi


## Proje Özeti

Bu çalışma, elektrik tüketim verileri üzerinden **keşifsel veri analizi (EDA)**, **veri görselleştirme** ve **veri hikayesi oluşturmayı** amaçlamaktadır.

Projenin temel amacı, ham veriden anlamlı içgörüler üretmek ve bu içgörüleri **analitik ve görsel bir çerçevede** sunmaktır.


## Problem Tanımı

Bu projede aşağıdaki sorulara yanıt aranmıştır:

* İlçelere göre elektrik tüketimi nasıl değişmektedir?
* Mevsimsel olarak tüketim trendleri nasıldır?
* Tüketimde belirgin artış veya azalış dönemleri var mı?
* Karar vericiler için hangi içgörüler üretilebilir?


## Veri Seti Bilgisi

**Dosya:**

```
data/elektrik_veri.xlsx
```

Excel dosyası **5 farklı sayfadan** oluşmaktadır.

### 1️⃣ Tahsilat

* **636,993 ödeme kaydı**
* Ödeme kanalları:

  * Banka
  * Nakit
  * Mahsup
* Her satır **bir ödeme işlemini** temsil eder.

### 2️⃣ Tahsilat 1

* **917,632 fatura kaydı**
* Faturaların **zamanında veya geç ödenme bilgisi**
* Yaklaşık **%86 zamanında ödeme oranı**

### 3️⃣ Tahakkuk (3 ayrı ilçe sayfası)

Toplam **1.18 milyon tüketim kaydı** içerir.

Her kayıt şu bilgileri içerir:

* Elektrik tüketimi (**kWh**)
* Fatura tarihi
* Hesap sınıfı (Mesken, Ticari, Tarımsal vb.)
* Vade tarihi

Veri seti toplamda yaklaşık:

* **2.74 milyon kayıt**
* **28,299 müşteri**

içermektedir.


## 🔎 Analiz Süreci

Çalışma **3 ana aşamada** gerçekleştirilmiştir.

### Veri Keşfi

* Eksik veri analizi
* Aykırı değer kontrolü
* Temel istatistiksel özetler
* Veri temizleme işlemleri


### Veri Görselleştirme

* İlçe bazlı tüketim karşılaştırmaları
* Mevsimsel tüketim grafikleri
* Trend analizleri

Oluşturulan grafikler:

```
outputs/figures/
```

klasöründe bulunmaktadır.


### Veri Hikayesi

Bu aşamada:

* Analiz bulguları yorumlanmıştır
* Stratejik çıkarımlar yapılmıştır
* Karar vericiler için öneriler geliştirilmiştir


## Temel Bulgular

Analiz sonucu oluşturulan grafikler ve görseller:

```
outputs/figures/
```

klasöründe yer almaktadır.


## Kullanılan Teknolojiler

Projede aşağıdaki araç ve kütüphaneler kullanılmıştır:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook


## Çalıştırma Talimatı

Projeyi çalıştırmak için aşağıdaki adımları izleyebilirsiniz:

```bash
git clone <repo_link>
cd case_study_02
pip install -r requirements.txt
jupyter notebook
```
## Veriseti Linki:

https://drive.google.com/file/d/11-ACN608r8xHKxaH_4if6AR31XD9Cief/view?usp=sharing

Notebook dosyalarının **sırasıyla çalıştırılması önerilir**.

1. `notebook_01_veri_kesfi.ipynb`
2. `notebook_02_gorsellestirme.ipynb`
3. `notebook_03_veri_hikayesi.ipynb`
