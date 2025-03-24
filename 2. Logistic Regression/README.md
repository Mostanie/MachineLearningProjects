Projenin Amacı: Bu projede makine öğrenmesinin classification dalında en temel algoritması olan logistic regression ile bir kağıt paranın sahte mi gerçek mi olduğunu kağıdın boyutunu kullanarak bulmaya çalıştık. Bu ana amacın yanındaki amacımız ise bu modeli önce hazır kütüphanelerle eğitip daha sonra da kütüphane kullanmadan yazılan kodla performans ve doğruluk açısından karşılaştırmaktır.

Performans Metrikleri: Bu iki modeli performans ve doğruluk açısından karşılaştırmadan önce performans metriklerini anlamakta fayda vardır.

Negatif Sınıf: 0 ya da False yani para sahte. Pozitif Sınıf: 1 ya da True yani para gerçek.

True Positive (TP): Modelin doğru bir şekilde pozitif sınıfı tahmin ettiği örneklerdir. Yani, model gerçekten pozitif olan bir örneği doğru şekilde pozitif olarak sınıflandırmışsa, bu True Positive olarak kabul edilir.

True Negative (TN): Modelin doğru bir şekilde negatif sınıfı tahmin ettiği örneklerdir. Yani, model gerçekten negatif olan bir örneği doğru şekilde negatif olarak sınıflandırmışsa, bu True Negative olarak kabul edilir.

False Positive (FP): Modelin yanlış bir şekilde negatif sınıfı pozitif olarak tahmin ettiği örneklerdir. Yani, aslında negatif olan bir örneği model pozitif olarak sınıflandırmışsa, bu False Positive olarak kabul edilir. Bu, modelin "yanlış alarm" verdiği durumu ifade eder.

False Negative (FN): Modelin yanlış bir şekilde pozitif sınıfı negatif olarak tahmin ettiği örneklerdir. Yani, aslında pozitif olan bir örneği model negatif olarak sınıflandırmışsa, bu False Negative olarak kabul edilir. Bu, modelin bazı önemli pozitif örnekleri "kaçırdığı" durumu ifade eder.

Accuracy (Doğruluk): Accuracy, modelin yaptığı tüm tahminler arasında doğru tahminlerin oranını gösterir. Yani, modelin hem doğru pozitif hem de doğru negatif tahminlerinin toplamının, tüm tahminlerin toplamına bölünmesidir. Yüksek bir accuracy değeri, modelin genel olarak doğru tahminler yaptığını gösterir.

Precision (Kesinlik): Precision, modelin pozitif olarak tahmin ettiği örneklerin ne kadarının gerçekten pozitif olduğunu gösterir. Yani, modelin pozitif sınıf tahminlerinin ne kadarının doğru olduğunu ölçer. Eğer modelin kesinliği yüksekse, yanlış pozitif tahminler (negatif örneklerin pozitif olarak sınıflandırılması) az olur.

Recall (Hatırlama): Recall, gerçek pozitif örneklerin ne kadarını doğru şekilde tahmin edebildiğimizi gösterir. Yani, modelin aslında pozitif olan örnekleri ne kadar iyi tespit edebildiğini ölçer. Yüksek bir recall değeri, modelin pozitif örnekleri "kaçırmadığını" ve doğru şekilde sınıflandırdığını belirtir.

F1-Score: F1-Score, precision ve recall arasında bir denge sağlar. Eğer modelin precision'ı yüksekse ancak recall'ı düşükse veya tam tersi bir durum varsa, F1-Score bu iki metriğin dengelenmesine yardımcı olur. F1-Score, özellikle sınıflar arasındaki dağılımın dengesiz olduğu durumlarda önemli olur, çünkü sadece bir metrikle değil, her iki metriği de göz önünde bulundurur.

Şimdi tüm bilgileri edindiğimize göre karşılaştırma işlemine başlayabiliriz:

Öncelikle kütüphane kullanılmadan eğitilen sınıfın bilgilerini vereceğim daha sonra kütüphane kullanılarak eğitilen bilgilere geçeceğiz:

![Ekran görüntüsü 2025-03-24 135839](https://github.com/user-attachments/assets/e52acb06-34f0-414e-8873-51df3af851ba) ![Ekran görüntüsü 2025-03-24 140323](https://github.com/user-attachments/assets/1d607e3a-5f52-4f78-abf8-3d9c24cf519c)


![Ekran görüntüsü 2025-03-24 135920](https://github.com/user-attachments/assets/9a55d6ac-468b-47f4-94b3-59fa63398b81)


![Ekran görüntüsü 2025-03-24 140048](https://github.com/user-attachments/assets/812ec3e9-8aec-46a7-ad02-131f5c725f28)


![Ekran görüntüsü 2025-03-24 140116](https://github.com/user-attachments/assets/8e42027e-8030-47be-9452-6e16746eb98d)

Şimdi kütüphane ile yazılan kodun çıktılarına bakalım:

![Ekran görüntüsü 2025-03-24 140323](https://github.com/user-attachments/assets/1d607e3a-5f52-4f78-abf8-3d9c24cf519c)


![Ekran görüntüsü 2025-03-24 140338](https://github.com/user-attachments/assets/b44bf295-9104-4021-a82e-07ad7dd49a65)


![Ekran görüntüsü 2025-03-24 140353](https://github.com/user-attachments/assets/b4c5401b-897e-4576-b071-88a40e85ea7d)

![Ekran görüntüsü 2025-03-24 140401](https://github.com/user-attachments/assets/5dab0ba5-c38c-4d37-90bc-da17c7a473fe)






