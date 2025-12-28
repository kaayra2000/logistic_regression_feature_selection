# Feature Selection Analiz Raporu

**Yöntem:** Sarmalayıcı Yöntem - RFE + Lojistik Regresyon
**Veri Kümesi:** processed_dataset.csv
**Boyut:** (39644, 59)
**Kaynak:** UCI Online News Popularity
**Tarih:** 2025-12-28 14:56:48

---

## 📊 Genel Değerlendirme


Sarmalayıcı yöntem olarak **Recursive Feature Elimination (RFE)** kullanılmıştır. 
Bu yöntem, **Lojistik Regresyon** algoritması ile birlikte uygulanmıştır.

### Yöntem Detayları:
- RFE, başlangıçta tüm özelliklerle başlar
- Her iterasyonda model eğitilir ve en az önemli özellik(ler) elenir
- Bu işlem istenilen özellik sayısına ulaşılana kadar devam eder
- Lojistik Regresyon katsayıları özellik önemini belirler

### Model Parametreleri:
- **Estimator:** LogisticRegression
- **Solver:** lbfgs
- **Max Iterations:** 1000
- **Step:** 1 (her adımda 1 özellik ele)

### Avantajları:
- Model performansını doğrudan optimize eder
- Özellikler arası etkileşimleri dikkate alır
- Sıralı özellik seçimi sağlar

### Dezavantajları:
- Hesaplama maliyeti yüksek olabilir
- Seçilen modele bağımlı


**Seçilen Özellik Sayısı:** 15

---

## Özellik Sıralaması

| Sıra | Özellik | Normalize Skor | Yorum |
|------|---------|----------------|-------|
| 1 | n_non_stop_words | 1.0000 | 🥇 En önemli özelliklerden |
| 2 | n_unique_tokens | 1.0000 | 🥇 En önemli özelliklerden |
| 3 | n_non_stop_unique_tokens | 1.0000 | 🥇 En önemli özelliklerden |
| 4 | data_channel_is_socmed | 1.0000 | 🥈 Çok yüksek önem |
| 5 | data_channel_is_tech | 1.0000 | 🥈 Çok yüksek önem |
| 6 | kw_avg_min | 1.0000 | 🥉 Yüksek önem |
| 7 | kw_max_min | 1.0000 | 🥉 Yüksek önem |
| 8 | kw_min_min | 1.0000 | 🥉 Yüksek önem |
| 9 | kw_max_avg | 1.0000 | 🥉 Yüksek önem |
| 10 | kw_avg_avg | 1.0000 | 🥉 Yüksek önem |
| 11 | self_reference_avg_sharess | 1.0000 | Orta-yüksek önem |
| 12 | kw_avg_max | 1.0000 | Orta-yüksek önem |
| 13 | kw_min_avg | 1.0000 | Orta-yüksek önem |
| 14 | LDA_00 | 1.0000 | Orta-yüksek önem |
| 15 | is_weekend | 1.0000 | Orta-yüksek önem |

---

## 📋 Seçilen Özellikler Listesi

Seçilen en iyi 15 özellik:

1. `n_non_stop_words`
2. `n_unique_tokens`
3. `n_non_stop_unique_tokens`
4. `data_channel_is_socmed`
5. `data_channel_is_tech`
6. `kw_avg_min`
7. `kw_max_min`
8. `kw_min_min`
9. `kw_max_avg`
10. `kw_avg_avg`
11. `self_reference_avg_sharess`
12. `kw_avg_max`
13. `kw_min_avg`
14. `LDA_00`
15. `is_weekend`

---

## 📝 Ek Notlar


RFE yöntemi, Lojistik Regresyon modelinin katsayılarını kullanarak özellik önemini belirler.
Bu nedenle, seçilen özellikler Lojistik Regresyon için en ayırt edici olanlardır.

**Not:** Veriler StandardScaler ile ölçeklendirilmiştir, bu Lojistik Regresyon için önemlidir.


---

## 📈 Skor İstatistikleri

| Metrik | Değer |
|--------|-------|
| Maksimum Normalize Skor | 1.0000 |
| Minimum Normalize Skor (Top 15) | 1.0000 |
| Ortalama Normalize Skor (Top 15) | 1.0000 |
