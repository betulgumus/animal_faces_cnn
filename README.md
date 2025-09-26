Proje Amacı

Bu proje, Convolutional Neural Network (CNN) kullanarak hayvan resimlerini sınıflandırmayı amaçlamaktadır.
Model, kedi, köpek ve vahşi hayvan resimlerini %89.6 doğrulukla ayırt edebilmektedir.

Veri Seti Hakkında Bilgi

Veri Seti: Animal Faces HQ (AFHQ)
Sınıflar: 3 sınıf (Cat, Dog, Wild)
Toplam Resim: ~4000 resim
Resim Boyutu: 512x512 → 128x128 (eğitim için)
Veri Kaynağı: Kaggle - Animal Faces

Sınıf Dağılımı:

Cat (Kedi): 1,313 resim
Dog (Köpek): 1,313 resim
Wild (Vahşi): 1,313 resim

Veri Önişleme

Resim boyutu normalizasyonu (128x128)
Pixel değerleri 0-1 arası normalizasyon
Train-Validation split (%80-%20)

Data Augmentation

Rotation (±20 derece)
Width/Height shift (%20)
Horizontal flip
Zoom range (%20)

CNN Model Mimaris
Sequential Model:
Conv2D(32, 3x3) + ReLU + MaxPool(2x2)
 Conv2D(64, 3x3) + ReLU + MaxPool(2x2)  
 Conv2D(128, 3x3) + ReLU + MaxPool(2x2)
 Flatten
 Dropout(0.5)
 Dense(512) + ReLU
 Dropout(0.3)
 Dense(3) + Softmax

 Hiperparametreler

Optimizer: Adam
Loss Function: Categorical Crossentropy
Batch Size: 32
Epochs: 8 (Early Stopping ile)
Learning Rate: 0.001

Elde Edilen Sonuçlar
Model Performansı

Eğitim Doğruluğu: %90.4
Validation Doğruluğu: %89.6
Test Doğruluğu: %89.6

 Model Değerlendirmesi
Güçlü Yanları:

Yüksek doğruluk oranı (%89.6)
Overfitting problemi yok
Dengeli sınıf performansı

İyileştirme Alanları:

Transfer Learning kullanılabilir
Daha fazla epoch ile eğitim
Hiperparametre optimizasyonu

Sonuç ve Değerlendirme
Bu proje, CNN mimarisinin görüntü sınıflandırma problemlerindeki başarısını göstermektedir. %89.6 doğruluk oranı ile model, pratik uygulamalarda kullanılabilir seviyededir.
Gelecek Çalışmalar:

Transfer Learning (ResNet, VGG) implementasyonu
Grad-CAM görselleştirmesi
Model ensemble teknikleri
Mobil uygulama geliştirme

Geliştirici:

İsim: Betül Gümüş
Tarih: 26 Eylül 2025
Proje: Akbank Derin Öğrenme Bootcamp

Link:
https://www.kaggle.com/code/betulgumus/notebook0f32096ea7
