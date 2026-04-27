Kalp Yetmezliği Tahmini - Kolektif Öğrenme (Ensemble Learning)

Bu proje, makine öğrenmesi yöntemlerini kullanarak kalp yetmezliği riskini tahmin etmeyi amaçlayan bir sınıflandırma çalışmasıdır. Proje kapsamında Kolektif Öğrenme (Ensemble Learning) algoritmaları kullanılmış ve performansları karşılaştırılmıştır.

📊 Proje Özeti

Veri Seti: kalp_yetmezliği.csv (Kalp hastalığına dair klinik özellikler)

Problem Türü: İkili Sınıflandırma (Binary Classification)

Hedef Değişken: HeartDisease (0: Sağlıklı, 1: Hasta)

🛠️ Kullanılan Teknolojiler ve Modeller

Projede üç temel kolektif öğrenme algoritması kullanılmıştır:
Random Forest (Bagging)
XGBoost (Boosting)
AdaBoost (Boosting)

Uygulanan Teknikler:
Encoding: Kategorik veriler pd.get_dummies ile sayısal formata çevrildi.
Cross-Validation: Modellerin başarısı 10-Katlı Çapraz Doğrulama (Stratified 10-Fold CV) ile test edildi.
Hiperparametre Optimizasyonu: RandomizedSearchCV kullanılarak modellerin en iyi parametreleri bulundu.
Model Açıklanabilirliği: SHAP analizi yapılarak hangi özelliğin (feature) tahmine ne kadar etki ettiği görselleştirildi.
Özellik Seçimi: RFECV (Recursive Feature Elimination) ile en optimum özellik sayısı belirlendi.

📈 Bulgular ve Sonuçlar
Proje sonucunda elde edilen 10-Fold CV sonuçları:
Model	        Accuracy	  F1-Score	  ROC-AUC
Random Forest	 0.8671      0.8830    0.9286
XGBoost	       0.8660      0.8812    0.9304
AdaBoost	     0.8649      0.8817    0.9228
Öne Çıkan Özellikler (SHAP Analizi)
Yapılan SHAP analizine göre modelin karar vermesinde en etkili olan özellikler şunlardır:
[ST Slope]
[Exercise Angina]
🚀 Nasıl Çalıştırılır?
Depoyu klonlayın: git clone https://github.com/kullaniciadi/repo-adi.git
Kütüphaneleri yükleyin: pip install -r requirements.txt
Ana kodu çalıştırın: python src/main.py
