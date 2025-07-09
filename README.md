# 🛒 Tüketici Davranışı ve E-Ticaret: Satın Alma Kararını Hangi Faktörler Etkiliyor?

---

## ⚠️ Uyarı

Bu proje yalnızca **eğitim ve analiz amacıyla** hazırlanmıştır.  
Ticari bir amaç güdülmemektedir ve herhangi bir şirket ile doğrudan ilişkili değildir.

---

Bu projede, bir e-ticaret web sitesine ait kullanıcı oturum verileri analiz edilerek, kullanıcıların satın alma davranışlarını etkileyen faktörler incelenmiştir. Amaç, ziyaretçilerin hangi davranışsal ve teknik özelliklere sahip olduğunda alışveriş yapma olasılıklarının arttığını anlamaktır.

---

## 📁 Veri Kümesi

- **Kaynak:** [UCI Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset)
- **Toplam Satır (Oturum):** 12,330
- **Değişken Sayısı:** 18
- **Hedef Değişken:** `Revenue` (Satın alma gerçekleşti mi?)

---

## 📊 Kullanılan Değişkenler (Örnekler)

| Değişken               | Açıklama |
|------------------------|----------|
| `PageValues`           | Sayfanın parasal katkı değeri |
| `BounceRates`          | Kullanıcının siteyi hemen terk etme oranı |
| `ProductRelated_Duration` | Ürün sayfalarında geçirilen toplam süre |
| `VisitorType`          | Yeni veya geri dönen kullanıcı |
| `Month`                | Ziyaretin gerçekleştiği ay |
| `Weekend`              | Ziyaret hafta sonu mu? |

---

## 🔍 Analiz Adımları

1. **Veri Ön İşleme ve Keşifsel Analiz (EDA):**
   - Satın alma yapan/yapmayan kullanıcı profilleri
   - Sayfa değeri, çıkış oranı, ürün ilgisi gibi değişkenlerin etkisi
2. **Korelasyon Analizi:**
   - `PageValues`, `ProductRelated_Duration` gibi değişkenler `Revenue` ile yüksek korelasyona sahip
   - Çoklu bağlantı (multicollinearity) tespit edilip sadeleştirme yapıldı
3. **Modelleme (Lojistik Regresyon):**
   - İlk model yüksek doğruluk fakat düşük `recall` verdi (%35)
   - `class_weight='balanced'` ile yeniden eğitim → `Recall = %75`, `Accuracy = %86.2`
4. **Model Değerlendirme:**
   - F1-score, karışıklık matrisi, precision-recall analizi yapıldı
   - Satın alma davranışı daha başarılı şekilde tahmin edildi

---


## 🛠️ Kullanılan Araçlar

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## 👤 Hazırlayan

**Deniz Atabey**  

---

## 📌 Lisans

[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)

---
