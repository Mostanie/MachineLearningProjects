Model kullanılmadan yazılan kodun sonuçları:

![image](https://github.com/user-attachments/assets/d773aef7-650f-47ab-ac5d-346560cd2d78)
![image](https://github.com/user-attachments/assets/8adf6905-8e8a-4e9f-83c1-94a46c0cac98)

Model kullanılarak yazılan kodun sonuçları:

![image](https://github.com/user-attachments/assets/4b509936-150b-473e-a962-46a06aa15b90)

![image](https://github.com/user-attachments/assets/dfd06240-8cad-4de6-9163-a948a4723ec7)



Eğittiğimiz iki regresyon modelinin performansını karşılaştırmak için MSE, RMSE ve R² skorlarını kullandık. İlk model en küçük kareler (Least Squares Estimation - LSE) yöntemiyle,
ikinci model ise Scikit-learn kütüphanesi kullanılarak eğitilmiştir.

Her iki modelin de R² skoru yaklaşık 0.935 olup, bu değer modellerin bağımlı değişkenin varyansının yaklaşık %93.5'ini açıkladığını göstermektedir. MSE ve RMSE değerleri de iki model
için neredeyse aynıdır.

Bu durum, veri setinin basit ve doğrusal ilişkilere uygun olduğunu, kullanılan farklı yaklaşımların benzer sonuçlar ürettiğini göstermektedir. Modelin tahmin performansı açısından iki
yöntem arasında anlamlı bir fark bulunmamaktadır. Ancak pratikte, Scikit-learn gibi kütüphanelerin kullanım kolaylığı, model doğrulama araçları ve geniş yelpazede algoritma desteği
sebebiyle tercih edilebilirliği daha yüksektir.

Sonuç olarak, her iki model de doğrusal regresyon problemi için oldukça iyi bir performans sergilemiş ve maliyet açısından neredeyse eşit sonuçlar vermiştir. Ayrıca model kullanılmadan yazılan kodumuz parametreleri daha hızlı öğrenmiştir.
