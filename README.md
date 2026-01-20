# ML-FINAL

Bu projede bir evin bir ayda tükettiği enerji miktarlarını görüyoruz.
Bu enerji değeri gün içerisindeki saate, hangi gün olduğuna (haftaiçi, haftasonu gibi) değerlere bağlıdır. Elimizde tek bir aya ait veri olduğu için aylara göre karşılaştırma yapamıyoruz.

## Dataset Okuma İşlemi
<img width="1187" height="404" alt="image" src="https://github.com/user-attachments/assets/760f85bd-1d50-46e7-aae6-0c89c7b8bfa9" />

## Verinin Temizlenmesi

Ben bu aşamada ilk olarak nan değeri olan satırlara baktım ve sadece tek bir satırda NaN verisi olduğu için ve o veri bizim verimizin yanında yüzdelik olarak çok düşük 
olduğu için o satırı temizleme işlemi yaptım.

Sonrasında işlem yapabilmek adına (ortalama değer bulmak gibi) dataların hangi tipte olduğuna baktım ve int/float harici object veri tipi gördüm.
Bunlara uygun dönüştürmeyi yaptım ve time sütunu için bize verilen unix değeri tarih formatına çevirdim. 
<img width="890" height="344" alt="image" src="https://github.com/user-attachments/assets/afd3dabe-d37e-43b8-9157-e75fc9cf1764" />
Dönüştürme işleminin ardından time sütunu
<img width="898" height="247" alt="image" src="https://github.com/user-attachments/assets/09a2367e-cef4-4ecf-8957-d343d9b700d1" />

## Pivot Tablolar 
Bu datasetine göre günlere ayırma işlemi yaptığımızda elimizde 7 adet sınıf olur ve bu günlerin hepsi için ayrı ayrı saat değerlerine bakabiliriz.
Pazartesi günü saat 7'de ortalama enerji tüketimi kaçtır?
Çarşamba günü gece saatleri enerji tüketimi ortalaması nasıldır?
Hafta sonları mı yoksa hafta içleri mi enerji harcanır?
gibi sorulara cevap bulmamızı sağlar. 

## Model Eğitini Örnek Görsel
<img width="892" height="148" alt="image" src="https://github.com/user-attachments/assets/be816622-7b53-47e7-a6ab-6f59b68a046e" />
<img width="813" height="475" alt="image" src="https://github.com/user-attachments/assets/5f4bbe3e-f225-448c-b8e3-7bad20611e96" />

Bildiğim kadarıyla bu kadarını yapabildim. Saatlik gecikme(lag) eklemeye çalıştım fakat o değeri nasıl kullanacağımı bilemedim bu yüzden bu aşamada bıraktım.

Kod içeriğimde çok fazla deneme var grafik görme açısından, veriyi analiz etme/yorumlama açısından biraz karışık bir kod düzeni. Yaptığım şeyleri (modele verimli olan işlemleri (veri temizleme, eğitme gibi)) hepsini açıklamaya çalıştım. Son haftalarda derslerde katılım sağlayamadığım için (alttan dersimle çakışıyordu) daha çok veri temizleme kısmını yapabildim aynı zamanda pivot tablonun pratiğini değil ama mantığını oturttum. 

