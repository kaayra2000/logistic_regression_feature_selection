# 📊 Lojistik Regresyon Performans Değerlendirme Raporu

**Tarih:** 2025-12-28 15:28:47
**Yöntem:** Lojistik Regresyon + K-Fold Cross Validation (K=5)
**Test Oranı:** %20

---

## 📈 Sonuç Tablosu

| Yöntem | Özellik Sayısı | Doğruluk (Accuracy) | F1-Skoru | Eğitim Süresi (s) |
|--------|----------------|---------------------|----------|-------------------|
| Tüm Özellikler ⭐ | 58 | 0.6552 | 0.6544 | 0.1823 |
| Filtreleme (Pearson) | 15 | 0.6431 | 0.6413 | 0.0168 |
| Sarmalayıcı (RFE) | 15 | 0.6510 | 0.6502 | 0.0347 |
| Gömülü (Random Forest) | 15 | 0.6278 | 0.6253 | 0.0221 |

> [!NOTE]
> En başarılı yöntem: **Tüm Özellikler** (Accuracy: 0.6552, F1: 0.6544)

---

## 🎯 En Başarılı Yöntem Detayları

**Yöntem:** Tüm Özellikler
**Özellik Sayısı:** 58
**Doğruluk:** 0.6552 (65.52%)
**F1-Skoru:** 0.6544

---

## ⚠️ Aşırı Öğrenme Analizi

- **Tüm Özellikler:** ✅ Tespit Edilmedi (Fark: 0.0023)
- **Filtreleme (Pearson):** ✅ Tespit Edilmedi (Fark: -0.0000)
- **Sarmalayıcı (RFE):** ✅ Tespit Edilmedi (Fark: 0.0006)
- **Gömülü (Random Forest):** ✅ Tespit Edilmedi (Fark: 0.0014)

---

## 📋 Karışıklık Matrisi (Tüm Özellikler)

|  | Tahmin: 0 | Tahmin: 1 |
|--|-----------|-----------|
| **Gerçek: 0** | 2236 (TN) | 1462 (FP) |
| **Gerçek: 1** | 1272 (FN) | 2959 (TP) |

**Açıklama:**
- TN (True Negative): Doğru tahmin edilen negatif örnekler
- FP (False Positive): Yanlış pozitif tahminler
- FN (False Negative): Yanlış negatif tahminler
- TP (True Positive): Doğru tahmin edilen pozitif örnekler
