# Veri-Bilimi

 Aşağıdaki bölümlerde bir veri setinin Train, Test ve Validation (validasyon) olarak neye göre ayrıldığı ve ne işe yaradığı anlatılmaktadır.

## Train Veri Seti
Train veri seti üzerinde temel modelleme denemeleri yapılarak en doğru makine öğrenmesi algoritması seçilmeye çalışılır. Gözlem/veri sayısına bağlı olarak en az %60 en fazla %90 olarak şekilde datadan train için bölüm ayrılabilir.
## Validation Veri Seti
Validation bölümü train veri seti içinden seçilir. Train veri seti üzerinde doğru model seçimi yapılarak algoritma belirlenir. Validation bölümünde ise uygulanan model iyileştirilmeye çalışılır. Bunun için hiper parametrik (hyperparameter tuning) uygulamalar denenerek en optimum katsayılar/ağırlıklar bulunmaya çalışılır. Özellikle çok büyük veri setleri üzerinde sürekli Train datası üzerinden çalışılamayacağı için küçük bir bölüm alınarak validation olarak tanımlanır.
## Test Veri Seti
İçinde Validation datasının yer aldığı Train veri setinden kalan bölüme Test veri seti diyebiliriz. Bu bölümde tahminler ile gerçek veriler karşılaştırılır. Test bölümü için ayrılmış data üzerinde daha önce train veri seti üzerinden öğrenilmiş makine öğrenmesi modeli uygulanır. Uygulama esnasında test veri setindeki Target  değişkeni kaldırılır. Ardından kurulan modele test verisindeki değişkenler eklenerek modelden Target değişken tahmin edilmesi beklenir. Ardından tahmin edilen değişkenler ile daha önce veri setinden çıkarılan Target değişken karşılaştırılıp model performansı ölçülür.
