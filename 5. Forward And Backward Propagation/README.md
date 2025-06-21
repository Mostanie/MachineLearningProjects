Kütüphaneleri ve Veri Setini Yükleme:
  NumPy, Pandas, Matplotlib, Seaborn ve scikit-learn’den veri yükleme araçları içe aktarılır. \n
  Iris veri seti yüklenir (4 özellik, 3 sınıf: Setosa, Versicolor, Virginica). \n
  Veriler Pandas DataFrame’e çevrilir, train/test olarak %80/%20 oranında bölünür. \n
  Özellikler standartlaştırılır (ortalama=0, varyans=1) ve hedef değişken one-hot encoding ile dönüştürülür.

Sinir Ağı Sınıfı (NeuralNetwork):
  __init__: Katman boyutlarını (ör. [4, 10, 3]) alır ve ağırlık/bias’ları rastgele başlatır.
  initialize_parameters: Ağırlıklar küçük rastgele değerlerle, bias’lar sıfırla başlatılır.
  sigmoid ve sigmoid_derivative: Gizli katmanlar için sigmoid aktivasyon fonksiyonu ve türevi.
  softmax: Çıkış katmanı için olasılık dağılımı üretir.
  forward: İleri yayılım; girişten çıkışa kadar katmanları hesaplar, aktivasyonları ve z değerlerini saklar.
  compute_loss: Cross-entropy kaybını hesaplar (sınıflandırma için).
  backward: Geri yayılım; gradyanları hesaplayarak ağırlık ve bias’ları günceller.
  train: Modeli belirtilen epoch sayısı kadar eğitir, her epoch’ta ileri/geri yayılım yapar ve kaybı kaydeder.

Modeli Eğitme:
  Sinir ağı [4, 10, 3] yapısıyla oluşturulur (4 giriş, 10 gizli nöron, 3 çıkış).
  1000 epoch boyunca 0.1 öğrenme oranıyla eğitilir.
  Kayıp değerleri her epoch’ta kaydedilir ve konsola 100 epoch’ta bir yazdırılır.
  Kayıp eğrisi Matplotlib ile çizilir (kayıp-epoch grafiği).

Modeli Değerlendirme:
  Test verisiyle tahmin yapılır, tahmin edilen sınıflar çıkarılır.
  Doğruluk (accuracy) hesaplanır: Tahminlerin gerçek sınıflarla eşleşme oranı.
  Karmaşıklık matrisi (confusion matrix) Seaborn ile görselleştirilir, hangi sınıfların doğru/yanlış tahmin edildiğini gösterir.


![resim](https://github.com/user-attachments/assets/b67d0d1b-fb83-483d-9bde-82f73ba5a781)

Epocha göre loss değerleri takip edilir.

![resim](https://github.com/user-attachments/assets/3fe73b10-72c2-4cad-a200-e45a3fa3c89b)

Tahminler değerlendirilir.


![resim](https://github.com/user-attachments/assets/63a5750c-39ff-4797-9e20-7586c7dd7b3d)

İris veri setinin görselleştirilmiş halidir.



