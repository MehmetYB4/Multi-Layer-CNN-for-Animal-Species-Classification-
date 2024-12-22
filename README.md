# Çok Katmanlı CNN ile Hayvan Türü Sınıflandırması 🐾💻

Bu proje, 10 farklı hayvan türünün görüntülerini sınıflandırmak için bir Çok Katmanlı Evrişimli Sinir Ağı (CNN) modeli eğitir ve değerlendirir. Proje, modelin performansını farklı senaryolar altında (orijinal, manipüle edilmiş ve renk sabitliği uygulanmış görüntüler) inceleyerek, gerçek dünya koşullarındaki performansını analiz etmeyi amaçlar.

## İçindekiler

* [Proje Hakkında](#proje-hakkında)
* [Veri Seti](#veri-seti)
* [Model Mimarisi](#model-mimarisi)
* [Model Eğitimi](#model-eğitimi)
* [Değerlendirme](#değerlendirme)
* [Sonuçlar](#sonuçlar)
* [Kullanım](#kullanım)
* [Gereksinimler](#gereksinimler)
* [Lisans](#lisans)
* [İletişim](#iletişim)

## Proje Hakkında

Bu proje, hayvan türlerini tanımak için derin öğrenme tekniklerini kullanır. Bir CNN modeli, çeşitli hayvan türlerinin görüntülerini içeren bir veri seti üzerinde eğitilir. Modelin performansı, farklı ışıklandırma koşullarında çekilmiş veya manipüle edilmiş görüntüler üzerinde de test edilir. Renk sabitliği algoritmalarının modelin robustluğuna etkisi incelenir.

## Veri Seti

Projede kullanılan veri seti, 10 farklı hayvan türünün 6500 görüntüsünden oluşur. Her sınıf için 650 görüntü bulunmaktadır. Sınıflar şunlardır:

* collie
* dolphin
* elephant
* fox
* moose
* rabbit
* sheep
* squirrel
* giant panda
* polar bear

Veri seti, eğitim ve test kümelerine ayrılmıştır.

## Model Mimarisi

Model, aşağıdaki katmanlardan oluşan bir Çok Katmanlı CNN mimarisine sahiptir:

* **Evrişim Katmanları (Conv2D):** Farklı filtre boyutları ve aktivasyon fonksiyonları ile birden fazla evrişim katmanı kullanılır.
* **Batch Normalizasyonu (BatchNormalization):** Eğitim sürecini hızlandırmak ve modelin genelleme yeteneğini artırmak için kullanılır.
* **Max Pooling Katmanları (MaxPooling2D):** Özellik haritalarının boyutunu küçültür ve hesaplama maliyetini azaltır.
* **Dropout Katmanları (Dropout):** Aşırı öğrenmeyi önlemek için kullanılır.
* **Yoğun Katmanlar (Dense):** Sınıflandırma için kullanılır. Son katman, softmax aktivasyon fonksiyonu kullanır.

## Model Eğitimi

Model, Adam optimizer'ı ve sparse_categorical_crossentropy kayıp fonksiyonu kullanılarak eğitilir. Eğitim sırasında accuracy metriği izlenir.

## Değerlendirme

Modelin performansı, orijinal test verileri, manipüle edilmiş görüntüler ve renk sabitliği uygulanmış görüntüler üzerinde değerlendirilir. Başarı oranı, her senaryo için ayrı ayrı hesaplanır.

## Sonuçlar

| Senaryo                             | Başarı Oranı |
|-------------------------------------|--------------|
| Orijinal Test Verileri             | %83.38       |
| Manipüle Edilmiş Görüntüler       | %21.16       |
| Renk Sabitliği Uygulanmış         | %79.38       |

## Kullanım

1. Projeyi klonlayın.
2. Gerekli kütüphaneleri yükleyin.
3. Veri setini indirin ve hazırlayın.
4. Modeli eğitin.
5. Modeli test edin ve sonuçları değerlendirin.

## Gereksinimler

* Python 3.x
* TensorFlow
* Keras
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn

## Lisans

MIT Lisansı

## İletişim

Mehmet Yusuf Bircan - mehmetyusuf.software@gmail.com

Kaggle 🔗 https://www.kaggle.com/code/mehmetyusuf/multi-layer-cnn-for-animal-species-classification
