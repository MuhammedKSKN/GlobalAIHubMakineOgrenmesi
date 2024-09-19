# GlobalAIHubMakineOgrenmesi

## Kaggle Notebook Link : 
https://www.kaggle.com/code/hayali26/drinking-predict-model

# Alkol Tüketimi Tahmin Modeli

Bu proje, Kore'deki bir hastaneden toplanan sağlık ve yaşam tarzı verilerini kullanarak alkol tüketimini tahmin eden bir makine öğrenmesi modeli geliştirmeyi amaçlamaktadır. Model, çeşitli sağlık göstergeleri ve yaşam tarzı verilerini kullanarak bireylerin alkol tüketim durumunu tahmin eder.

## Veri Seti

Veri seti, 12.000 kayıt ve 16 değişken içermektedir. Değişkenler şunlardır:

- **Sex**: Cinsiyet (male, female)
- **Age**: Yaş (5 yıl aralıklarla yuvarlanmış)
- **Height**: Boy (5 cm aralıklarla yuvarlanmış)
- **Weight**: Kilo (kg)
- **Waistline**: Bel çevresi
- **Sight_left**: Sol göz görme yeteneği (mükemmel görüş = 1.0)
- **Sight_right**: Sağ göz görme yeteneği (mükemmel görüş = 1.0)
- **Hear_left**: Sol kulak işitme durumu (1: normal, 2: anormal)
- **Hear_right**: Sağ kulak işitme durumu (1: normal, 2: anormal)
- **SBP**: Sistolik kan basıncı (mmHg)
- **DBP**: Diyastolik kan basıncı (mmHg)
- **BLDS**: Açlık kan şekeri (mg/dL)
- **Tot_chole**: Total kolesterol (mg/dL)
- **HDL_chole**: HDL kolesterol (mg/dL)
- **LDL_chole**: LDL kolesterol (mg/dL)
- **Triglyceride**: Trigliserit (mg/dL)
- **Hemoglobin**: Hemoglobin (g/dL)
- **Urine_protein**: İdrar proteini (1: -, 2: +/-, 3: +1, 4: +2, 5: +3, 6: +4)
- **Serum_creatinine**: Serum kreatinin (mg/dL)
- **SGOT_AST**: SGOT (Glutamat-oksaloasetat transaminaz) / AST (Aspartat transaminaz) (IU/L)
- **SGOT_ALT**: ALT (Alanin transaminaz) (IU/L)
- **Gamma_GTP**: Gamma-glutamil transpeptidaz (IU/L)
- **SMK_stat_type_cd**: Sigara içme durumu (1: hiç içmemiş, 2: bırakmış, 3: hâlâ içiyor)
- **DRK_YN**: Alkol tüketimi (1: içiyor, 0: içmiyor)

## Kurulum

1. Gerekli kütüphaneleri yükleyin:


## Kullanılan Algoritmaların Amacı:
CatBoost (Gözetimli Öğrenme): Bu algoritma, etiketli verilerle (girişler ve doğru sonuçlar) eğitilir ve sınıflandırma ya da regresyon problemlerini çözmek için kullanılır. Yani, hangi girişin hangi sonuca karşılık geldiğini bilir ve buna göre bir model oluşturur. Bu yüzden, girdi ile çıktılar arasında doğrudan bir ilişki kurarak tahminler yapar. Sonuç olarak, etiketlenmiş veri setlerinde yüksek doğruluk oranlarına ulaşması beklenir.

K-Means (Gözetimsiz Öğrenme): K-Means algoritması, etiketsiz verilerle çalışır ve verileri sadece özellikleri arasındaki benzerliklere dayanarak kümeler (gruplar) oluşturur. Yani, algoritmanın elinde sınıflandırma yapmak için bir "doğru cevap" yoktur. K-Means'ın çıktıları, sınıf etiketleriyle değil, veri noktalarının kümelere atanmasıyla ilgilidir. Bu algoritma, etiketli bir veri seti üzerinde doğruluk hesaplandığında yanlış bir değerlendirme yöntemi olabilir çünkü K-Means, sınıflandırma yapmak yerine kümeler oluşturur. Sonuç olarak, doğruluk oranının düşük çıkması normaldir.
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
