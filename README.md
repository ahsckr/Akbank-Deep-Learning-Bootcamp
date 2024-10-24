# Fish_Classification: Görüntü Tabanlı Balık Sınıflandırma Projesi

## Proje Özeti
Bu proje, derin öğrenme tekniklerini kullanarak farklı balık türlerini sınıflandırmayı amaçlamaktadır. Özellikle konvolüsyonel sinir ağları (CNN) kullanılarak, veri setindeki balık görüntüleri üzerinden türlerin doğru bir şekilde tanımlanması hedeflenmektedir. Proje, TensorFlow ve Keras kütüphaneleri ile geliştirilmiş olup, ön işleme için MobileNetV2 mimarisinden faydalanılmıştır.

## Kaggle Notebook Link
https://www.kaggle.com/code/ahsencakir/fish-classification

https://www.kaggle.com/code/beyzakaraoban/fish-classification

## Veri Seti
Projede kullanılan veri seti, [Kaggle Fish Dataset](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset/data) adlı veri setinden alınmıştır. Bu veri seti, çeşitli balık türlerini temsil eden binlerce görüntüden oluşmaktadır. Veri seti, modelin genelleme performansını artırmak için eğitim, doğrulama ve test setlerine bölünmüştür.

## Temel Özellikler
- **Model Mimarisi**: Balık türlerini sınıflandırmak için özel bir Konvolüsyonel Sinir Ağı (CNN) modeli oluşturulmuştur. Model, birden fazla konvolüsyon ve max pooling katmanı ile tam bağlantılı (fully connected) katmanlardan oluşmaktadır.
- **Ön İşleme**: Görüntüler, MobileNetV2'nin önceden eğitilmiş ağırlıklarına uygun olarak ölçeklendirilmiş ve işlenmiştir.
- **Eğitim**: Model, aşırı öğrenmeyi önlemek için erken durdurma (early stopping) kullanılarak eğitilmiştir. Optimizasyon için Adam algoritması, kayıp fonksiyonu olarak ise kategorik çapraz entropi kullanılmıştır.
- **Değerlendirme**: Modelin doğruluğu ve kayıp değerleri test seti üzerinde ölçülmüştür. Detaylı analiz için karışıklık matrisi (confusion matrix) ve sınıflandırma raporu da oluşturulmuştur.

## Model Performansı
Model, test seti üzerinde yüksek bir doğruluk oranı elde etmiştir. Aşağıda eğitim ve değerlendirme sürecinde elde edilen performans metrikleri yer almaktadır:
- **Eğitim Doğruluğu**: ~98.37%
- **Doğrulama Doğruluğu**: ~99.22%
- **Test Doğruluğu**: ~97.17%

## Sonuçların Görselleştirilmesi
Eğitim süreci boyunca modelin doğruluk ve kayıp değerleri grafikler ile görselleştirilmiştir. Ayrıca, sınıfların karışıklık matrisleri ve pasta grafikleri ile modelin sınıflandırma başarısı detaylandırılmıştır.
