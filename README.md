# CNN ile Hayvan Türlerini Sınıflandırma Projesi
Bu proje, derin öğrenme yöntemlerini kullanarak hayvan türlerini sınıflandırmak için bir Convolutional Neural Network (CNN) modelinin tasarlanması ve test edilmesi üzerine odaklanmaktadır.

## Projenin Amacı
Projede, temel CNN mimarisini kullanarak 10 farklı hayvan türü arasında sınıflandırma yapmak hedeflenmiştir. Model performansı farklı test koşulları altında değerlendirilecek ve çeşitli manipülasyonlar sonucunda elde edilen verilerle sonuçlar karşılaştırılacaktır.

## Kullanılan Veri Seti
Veri seti, Kaggle'daki Animals with Attributes 2 (https://www.kaggle.com/datasets/rrebirrth/animals-with-attributes-2) veri setidir.

Veri seti özellikleri:

JPEGImages klasöründe 50 farklı hayvan sınıfı bulunmaktadır.
Proje kapsamında yalnızca aşağıdaki 10 sınıf kullanılmıştır:
Collie
Dolphin
Elephant
Fox
Moose
Rabbit
Sheep
Squirrel
Giant Panda
Polar Bear
Her sınıftan yalnızca ilk 650 resim alınarak dengeli bir veri kümesi oluşturulmuştur. Görseller, modele uygun olacak şekilde boyutlandırılmış ve normalize edilmiştir.

## Proje Adımları
### 1. Veri Setinin Hazırlanması
Veri Kaggle'dan indirildi ve belirli sınıflar ayrıldı.
Görseller, belirlenen boyutlarda normalize edildi ve eğitim/test seti olarak rastgele %70/%30 oranında ayrıldı.
Eğitim setine veri artırma (augmentation) uygulandı.

### 2. CNN Modelinin Tasarlanması
Model, aşağıdaki katmanları içerecek şekilde oluşturulmuştur:
Convolutional Layer
Pooling Layer
Fully Connected Layer
Dropout
Kaybı minimize etmek için categorical_crossentropy kayıp fonksiyonu ve adam optimizasyon algoritması kullanılmıştır.

### 3. Modelin Eğitimi
Model, eğitim seti üzerinde eğitilmiştir. Eğitim sürecinde doğruluk (accuracy) ve kayıp değerleri değerlendirilmiştir.
Overfitting'i önlemek için dropout gibi teknikler uygulanmıştır.

### 4. Modelin Test Edilmesi
Model, test seti üzerinde değerlendirilmiş ve doğruluk oranı kaydedilmiştir.

### 5. Görüntü Manipülasyonu
Test setindeki görüntüler, farklı ışıklandırma koşulları ile manipüle edilmiştir.

### 6. Manipüle Edilmiş Görüntülerle Test
Model, manipüle edilmiş görüntüler üzerinde test edilmiş ve doğruluk oranı kaydedilmiştir.

### 7. Sonuçların Karşılaştırılması ve Raporlama
Orijinal, manipüle edilmiş ve renk sabitliği uygulanmış test setlerinin sonuçları karşılaştırılmıştır.
