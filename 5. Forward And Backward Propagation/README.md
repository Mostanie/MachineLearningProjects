Kütüphaneleri ve Veri Setini Yükleme: <br>
  &nbsp;&nbsp;&nbsp;NumPy, Pandas, Matplotlib, Seaborn ve scikit-learn’den veri yükleme araçları içe aktarılır. <br>
  &nbsp;&nbsp;&nbsp;Iris veri seti yüklenir (4 özellik, 3 sınıf: Setosa, Versicolor, Virginica). <br>
  &nbsp;&nbsp;&nbsp;Veriler Pandas DataFrame’e çevrilir, train/test olarak %80/%20 oranında bölünür. <br>
  &nbsp;&nbsp;&nbsp;Özellikler standartlaştırılır (ortalama=0, varyans=1) ve hedef değişken one-hot encoding ile dönüştürülür.

Sinir Ağı Sınıfı (NeuralNetwork): <br>
  &nbsp;&nbsp;&nbsp;__init__: Katman boyutlarını (ör. [4, 10, 3]) alır ve ağırlık/bias’ları rastgele başlatır. <br>
  &nbsp;&nbsp;&nbsp;initialize_parameters: Ağırlıklar küçük rastgele değerlerle, bias’lar sıfırla başlatılır. <br>
  &nbsp;&nbsp;&nbsp;sigmoid ve sigmoid_derivative: Gizli katmanlar için sigmoid aktivasyon fonksiyonu ve türevi. <br>
  &nbsp;&nbsp;&nbsp;softmax: Çıkış katmanı için olasılık dağılımı üretir. <br>
  &nbsp;&nbsp;&nbsp;forward: İleri yayılım; girişten çıkışa kadar katmanları hesaplar, aktivasyonları ve z değerlerini saklar. <br>
  &nbsp;&nbsp;&nbsp;compute_loss: Cross-entropy kaybını hesaplar (sınıflandırma için). <br> 
  &nbsp;&nbsp;&nbsp;backward: Geri yayılım; gradyanları hesaplayarak ağırlık ve bias’ları günceller. <br>
  &nbsp;&nbsp;&nbsp;train: Modeli belirtilen epoch sayısı kadar eğitir, her epoch’ta ileri/geri yayılım yapar ve kaybı kaydeder. <br>

Modeli Eğitme: <br>
  &nbsp;&nbsp;&nbsp;Sinir ağı [4, 10, 3] yapısıyla oluşturulur (4 giriş, 10 gizli nöron, 3 çıkış). <br>
  &nbsp;&nbsp;&nbsp;1000 epoch boyunca 0.1 öğrenme oranıyla eğitilir. <br>
  &nbsp;&nbsp;&nbsp;Kayıp değerleri her epoch’ta kaydedilir ve konsola 100 epoch’ta bir yazdırılır. <br>
  &nbsp;&nbsp;&nbsp;Kayıp eğrisi Matplotlib ile çizilir (kayıp-epoch grafiği). <br>

Modeli Değerlendirme: <br>
  &nbsp;&nbsp;&nbsp;Test verisiyle tahmin yapılır, tahmin edilen sınıflar çıkarılır. <br>
  &nbsp;&nbsp;&nbsp;Doğruluk (accuracy) hesaplanır: Tahminlerin gerçek sınıflarla eşleşme oranı. <br>
  &nbsp;&nbsp;&nbsp;Karmaşıklık matrisi (confusion matrix) Seaborn ile görselleştirilir, hangi sınıfların doğru/yanlış tahmin edildiğini gösterir. <br>


![resim](https://github.com/user-attachments/assets/b67d0d1b-fb83-483d-9bde-82f73ba5a781)

Epocha göre loss değerleri takip edilir.

![resim](https://github.com/user-attachments/assets/3fe73b10-72c2-4cad-a200-e45a3fa3c89b)

Tahminler değerlendirilir.


![resim](https://github.com/user-attachments/assets/63a5750c-39ff-4797-9e20-7586c7dd7b3d)

İris veri setinin görselleştirilmiş halidir.



