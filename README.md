## Çiçek Türü Sınıflandırma Projem

## 1.Projenin Amacı
Bu proje, Convolutional Neural Network (CNN) kullanarak çiçek türlerini sınıflandırmayı amaçlıyor. Görüntü verilerinden otomatik olarak özellik çıkarımı yaparak doğru sınıflandırma gerçekleştirmek hedeflenmiştir. Bu alandaki ilk projem olduğu için başlangıç düzeyinde bir proje oluştumak istedim.

## 2.Veri Seti
Kullanılan veri seti: TensorFlow Datasets içerisindeki tf_flowers veri seti
Veri boyutu: Görseller 224x224 RGB formatına dönüştürülmüş.
Sınıf sayısı: 5 farklı çiçek türü (ör. papatya, gül vb.)
Bölünme oranı: %80 eğitim %20 doğrulama/test
Ayrıca veri çeşitliliğini artırmak için data augmentation (çevirme, döndürme, ölçekleme) ve normalizasyon (0-1 aralığına çekme) uygulanmıştır.

## 3.Kullanılan Yöntemler
CNN Modeli (Sequential API):
Conv2D (özellik çıkarımı için)
MaxPooling2D (boyut küçültme)
Flatten (tam bağlı katmana geçiş)
Dense katmanlar (sınıflandırma için)
Dropout (overfitting’i önlemek için)
Optimizasyon: Adam optimizer
Callback’ler:
EarlyStopping (erken durdurma)
ReduceLROnPlateau (öğrenme oranını azaltma)
ModelCheckpoint (en iyi modeli kaydetme)
Eğitim süresi: 10 epoch 

## 4.Elde Edilen Sonuçlar
Model, eğitim sonrası eğitim ve doğrulama doğruluk değerlerini göstermiştir.
Doğruluk grafikleri (accuracy & loss) çizilmiştir.
Test doğruluğu (test_acc) ≈ %85 civarındadır.
Sınıflandırma raporu (precision, recall, f1-score) ve karışıklık matrisi verilmiş. Bu sayede hangi çiçek türlerinin daha iyi veya zor sınıflandırıldığı görselleştirilmiştir.

## 5.Gelecek Çalışmalar
 Daha derin CNN mimarileri veya transfer öğrenme yöntemleri kullanılarak doğruluk oranı artırılabilir. Kullanıcı dostu bir web veya mobil uygulama arayüzü eklenerek model, kullanıcıların yüklediği görselleri gerçek zamanlı olarak sınıflandırabilecek hale getirilebilir. Veri seti, internetten veya kullanıcıların yüklediği görsellerden sürekli güncellenerek modelin farklı türleri kapsaması sağlanabilir.
 Uzun vadede, bilgisayarla görme ve derin öğrenme tekniklerini yalnızca görüntü sınıflandırmada değil, aynı zamanda kendi alanımla birleştirip nöropsikoloji alanında da kullanmayı hedefliyorum. Özellikle beyin görüntüleme verilerinin analizi, bilişsel işlevlerle ilişkili görsel desenlerin sınıflandırılması ve klinik değerlendirmelerde karar destek sistemlerinin geliştirilmesi gibi alanlarda bu yöntemlerin önemli katkılar sağlayabileceğini düşünüyorum.

## Linkler 
https://www.kaggle.com/code/rozelinsungur/cnn-le-ek-t-r-siniflandirma-rozelin-sungur
