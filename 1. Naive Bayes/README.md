# Naive Bayes Algoritmasının Futbol Verisi Üzerinde Kullanımı

Projenin Amacı: Bu projede güçlü bir makine öğrenmesi algoritması olan Naive Bayes algoritmasının gücünü bir oyuncunun en az bir gol atıp atmadığını ayıran bir model oluşturmak için kullandık. Bu ana amacın yanındaki amacımız ise bu modeli önce hazır kütüphanelerle eğitip daha sonra da kütüphane kullanmadan yazılan kodla performans ve doğruluk açısından karşılaştırmaktır.

Performans Metrikleri: Bu iki modeli performans ve doğruluk açısından karşılaştırmadan önce performans metriklerini anlamakta fayda vardır. 

Negatif Sınıf: 0 yani futbolcu hiç gol atamamış.
Pozitif Sınıf: 1 yani futbolcu en az 1 gol atmış.


True Positive (TP): Modelin doğru bir şekilde pozitif sınıfı tahmin ettiği örneklerdir. Yani, model gerçekten pozitif olan bir örneği doğru şekilde pozitif olarak sınıflandırmışsa, bu True Positive olarak kabul edilir.

True Negative (TN): Modelin doğru bir şekilde negatif sınıfı tahmin ettiği örneklerdir. Yani, model gerçekten negatif olan bir örneği doğru şekilde negatif olarak sınıflandırmışsa, bu True Negative olarak kabul edilir.

False Positive (FP): Modelin yanlış bir şekilde negatif sınıfı pozitif olarak tahmin ettiği örneklerdir. Yani, aslında negatif olan bir örneği model pozitif olarak sınıflandırmışsa, bu False Positive olarak kabul edilir. Bu, modelin "yanlış alarm" verdiği durumu ifade eder.

False Negative (FN): Modelin yanlış bir şekilde pozitif sınıfı negatif olarak tahmin ettiği örneklerdir. Yani, aslında pozitif olan bir örneği model negatif olarak sınıflandırmışsa, bu False Negative olarak kabul edilir. Bu, modelin bazı önemli pozitif örnekleri "kaçırdığı" durumu ifade eder.

Accuracy (Doğruluk): Accuracy, modelin yaptığı tüm tahminler arasında doğru tahminlerin oranını gösterir. Yani, modelin hem doğru pozitif hem de doğru negatif tahminlerinin toplamının, tüm tahminlerin toplamına bölünmesidir. Yüksek bir accuracy değeri, modelin genel olarak doğru tahminler yaptığını gösterir.

Precision (Kesinlik): Precision, modelin pozitif olarak tahmin ettiği örneklerin ne kadarının gerçekten pozitif olduğunu gösterir. Yani, modelin pozitif sınıf tahminlerinin ne kadarının doğru olduğunu ölçer. Eğer modelin kesinliği yüksekse, yanlış pozitif tahminler (negatif örneklerin pozitif olarak sınıflandırılması) az olur.

Recall (Hatırlama): Recall, gerçek pozitif örneklerin ne kadarını doğru şekilde tahmin edebildiğimizi gösterir. Yani, modelin aslında pozitif olan örnekleri ne kadar iyi tespit edebildiğini ölçer. Yüksek bir recall değeri, modelin pozitif örnekleri "kaçırmadığını" ve doğru şekilde sınıflandırdığını belirtir.

F1-Score: F1-Score, precision ve recall arasında bir denge sağlar. Eğer modelin precision'ı yüksekse ancak recall'ı düşükse veya tam tersi bir durum varsa, F1-Score bu iki metriğin dengelenmesine yardımcı olur. F1-Score, özellikle sınıflar arasındaki dağılımın dengesiz olduğu durumlarda önemli olur, çünkü sadece bir metrikle değil, her iki metriği de göz önünde bulundurur.

Şimdi tüm bilgileri edindiğimize göre karşılaştırma işlemine başlayabiliriz:

Öncelikle confusion matrix ile başlayabiliriz:

![image](https://github.com/user-attachments/assets/e371a9c8-db48-4c6b-801f-316036dfcab6)


İki kodumuzda da değerler aynı olduğu için iki görsel ekleme ihtiyacı duymadım. Hem accuracy hem de confusion matrixdeki değerler konum bazlı da eşleşiyor.

![image](https://github.com/user-attachments/assets/de399131-9725-4e93-b655-d07dfc272079)

Yine performans metrik değerlerinde de tamamen örtüşme olmuştur.


Doğruluk açısından kodlarımız arasında bu örnek için bir farklılık olmadığını gördük peki hız konusunda hangi kod daha iyi?


with scikit-learn

![image](https://github.com/user-attachments/assets/3742900f-7d16-4e21-9fb9-8bca1617b046)

![image](https://github.com/user-attachments/assets/b8272688-ac94-4f54-88b6-7128e4cdcd0b)


without scikit-learn

![image](https://github.com/user-attachments/assets/6a231494-4c9b-4d0b-8b21-bb63cddbed45)

![image](https://github.com/user-attachments/assets/864b42ba-583a-44c5-9440-1363d847607e)








