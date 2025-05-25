# Medical Image Segmentation with U-Net (PolypHemuSBench)

## 📂 Project Contents

- `DeepLearning2.ipynb`: Project source code in Jupyter Notebook
- `Deep Learning 2 Raporu.pdf`: Project report (in Turkish)
- Model training and testing
- Sample visual outputs
- Metric analysis
- Evaluation and suggestions

## 🧠 Methods and Architecture

- **Model**: U-Net (Encoder–Decoder based CNN for segmentation)
- **Dataset**: [PolypHemuSBench](https://polyphemus.grand-challenge.org/)
- **Input Size**: 256x256
- **Epochs**: 150
- **Optimizer**: Adam (lr=0.001)
- **Loss Function**: Dice Loss
- **Learning Rate Scheduler**: StepLR (step_size=30, gamma=0.1)

### 🎨 Data Augmentation
To improve generalization and reduce overfitting:

- `RandomHorizontalFlip`
- `RandomVerticalFlip`
- `RandomRotation(30)`
- `RandomAffine`
- `ColorJitter`

## 📊 Performance Metrics

| Metric     | Test Result |
|------------|-------------|
| F1 Score   | 0.2811      |
| IoU        | 0.1850      |
| Accuracy   | 0.0499      |
| Precision  | 0.0142      |
| Recall     | 0.0377      |

## 🖼️ Visual Output
Model predictions and ground truth masks are visually compared. Example images are available in the report.

## 🔍 Evaluation
While the model showed promising F1 and IoU scores on the validation set, it struggled on the test set—particularly with a low precision score, indicating many false positives. This suggests overfitting and class imbalance issues.

## 💡 Suggestions for Improvement

- Combine BCE + Dice loss for better class balance and learning
- Try advanced architectures like Attention U-Net
- Expand data augmentation strategies
- Use class-weighted or focal loss to handle class imbalance
- Tune prediction threshold to optimize precision-recall trade-off


---


# U-Net ile Medikal Görüntü Segmentasyonu (PolypHemuSBench)


## 📂 Proje İçeriği

- `DeepLearning2.ipynb`: Projenin Python kodları (Jupyter Notebook)
- `Deep Learning 2 Raporu.pdf`: Proje raporu (Türkçe)
- Eğitim ve test süreci
- Görsel çıktı örnekleri
- Metrik analizleri
- Sonuç ve öneriler

## 🧠 Kullanılan Yöntemler ve Mimari

- **Model**: U-Net (Encoder-Decoder yapılı CNN mimarisi)
- **Veri Seti**: [PolypHemuSBench](https://polyphemus.grand-challenge.org/)
- **Giriş Boyutu**: 256x256
- **Epoch**: 150
- **Optimizer**: Adam (lr=0.001)
- **Kayıp Fonksiyonu**: Dice Loss
- **Öğrenme Oranı Güncelleyici**: StepLR (step_size=30, gamma=0.1)

### 🎨 Veri Artırma (Augmentation)
- `RandomHorizontalFlip`
- `RandomVerticalFlip`
- `RandomRotation(30)`
- `RandomAffine`
- `ColorJitter`

## 📊 Performans Metrikleri

| Metrik     | Test Sonucu |
|------------|-------------|
| F1 Score   | 0.2811      |
| IoU        | 0.1850      |
| Accuracy   | 0.0499      |
| Precision  | 0.0142      |
| Recall     | 0.0377      |

## 🖼️ Model Çıktısı
Modelin tahmin ettiği maskeler ve gerçek maskeler görsel olarak karşılaştırılmıştır. Örnek görseller raporda bulunmaktadır.

## 🔍 Değerlendirme
Model doğrulama verisinde yüksek F1 ve IoU skorlarına ulaşmasına rağmen, test setinde düşük precision değeri nedeniyle fazla sayıda yanlış pozitif tahmin üretmiştir. Bu durum overfitting ve sınıf dengesizliğinden kaynaklanıyor olabilir.

## 💡 Geleceğe Yönelik Öneriler

- BCE + Dice kombinasyonu ile daha dengeli kayıp fonksiyonu kullanımı
- Attention U-Net gibi gelişmiş mimarilerin test edilmesi
- Daha fazla augmentasyon tekniği
- Class-weighted veya focal loss kullanımı
- Tahmin eşik değerinin ayarlanması


---

