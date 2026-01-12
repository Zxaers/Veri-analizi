# Veri-analizi
# 🎮 Video Game Sales Prediction (Oyun Satış Tahmin Projesi)

Bu proje, video oyunlarının türü, platformu, yayımcısı ve inceleme puanları gibi özelliklerini kullanarak **ticari başarısını (Hit olup olmayacağını)** tahmin eden bir Makine Öğrenmesi (Machine Learning) modelidir.

## 📌 Proje Hakkında
Video oyun sektörü milyar dolarlık bir endüstridir. Bu projede, oyunların teknik ve demografik özelliklerine bakarak **"Global_Sales" (Küresel Satış)** verisi üzerinden bir başarı sınıflandırması yapılmıştır.

Proje süresince iki farklı yaklaşım denenmiştir:
1. **Regresyon:** Kesin satış rakamını tahmin etme (Düşük başarı nedeniyle sınıflandırmaya geçildi).
2. **Sınıflandırma (Classification):** Oyunun belirli bir satış barajını (örn. 500k) geçip geçmeyeceğini tahmin etme (**Seçilen Yöntem**).

## 📂 Veri Seti
Kullanılan veri seti: `Video_Games_Sales_as_at_22_Dec_2016.csv`
* **Kaynak:** Kaggle / Web Scraping
* **Veri Boyutu:** ~16.700 Satır
* **Özellikler:** Platform, Year, Genre, Publisher, NA_Sales, EU_Sales, Critic_Score, User_Score, Rating.

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler
Proje **Python** dili ile geliştirilmiştir.
* **Veri Analizi:** Pandas, NumPy
* **Makine Öğrenmesi:** Scikit-learn (Random Forest, Linear Regression)
* **Görselleştirme:** Matplotlib, Seaborn

## ⚙️ Uygulanan Adımlar (Methodology)
1. **Veri Temizliği (Data Cleaning):**
   - `Critic_Score` ve `User_Score` gibi sütunlardaki eksik veriler, veri kaybını önlemek için **medyan (median)** ile dolduruldu.
   - Gereksiz ve çok fazla boşluk içeren sütunlar çıkarıldı.

2. **Özellik Mühendisliği (Feature Engineering):**
   - Kategorik veriler (`Platform`, `Genre`) **One-Hot Encoding** yöntemiyle sayısal verilere çevrildi.
   - `Publisher` (Yayımcı) sütunu optimize edildi: En çok oyun yayınlayan ilk 20 firma tutuldu, geri kalanlar "Other" olarak gruplandı.
   - **Hedef Değişken:** Satış rakamları 0.5 Milyon (500k) barajına göre `1 (Başarılı)` ve `0 (Normal)` olarak sınıflandırıldı.

3. **Modelleme (Modeling):**
   - Algoritma: **Random Forest Classifier**
   - Veri Seti Bölümü: %80 Eğitim (Train), %20 Test.

## 📊 Sonuçlar
Modelin test verisi üzerindeki performansı:

| Metrik | Değer |
|Str|Str|
| **Doğruluk (Accuracy)** | **%40** |
| **Model** | Random Forest Classifier |
## 🚀 Kurulum ve Çalıştırma

![Yazar](https://img.shields.io/badge/Yazar-Acar%20Efe%20Yaman-blue?style=for-the-badge&logo=github)

Projeyi kendi bilgisayarınızda çalıştırmak için:

1. Repoyu klonlayın:
 ```bash
pip install pandas numpy scikit-learn matplotlib seaborn
   git clone 
   [(https://github.com/Zxaers/Veri-analizi)]


