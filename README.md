# Dogal-dil-isleme-yontemleri-ile-urun-yorumlarindan-duygu-analizi
e-ticaret sitesinden cekilen urunlerın yorumlarını bir veri setine kaydedip uzerinde duzeltmeler ve ceviri yaparak duygu analizi yapmak 


# Urun Yorumlarini ve Puanlarini Siteden Cekmek

- Oncelikle e-ticaret sitesindeki cep telefonlarinin yorumlarini ve verilen puani cekmek icin web scraping kullanildi.
- Kullanicin verdigi puan 1-2 ise negatif, 3 ise notr, 4-5 ise pozitif olarak degerlendirildi.
- Bunlar bir veri setine kayit edildi.

# Yorumlari Duzeltme Islemi

- Kayit edilen veri setinden cekilen yorumlara duzeltme islemi uygulandı.
- Bu sayede yazim yanlislari ve anlam kayiplari gibi problemler giderildi.
- Duzeltilen yorumlar ayri bir veri setine kayit edildi.

# Yorumlari Cevirmek

- Yorumlar duzeltildikten sonra ingilizce diline cevrildi.
- Cevrilen yorumlar yeni veri setine kayit edildi.

# Textblob Duygu Analizi

- Cevrilen yorumlarin oldugu veri seti kullanilarak duygu analizi yapildi ve sonuclar tabloya kayit edildi.
- Eger analiz sonucu cikan skor 0'dan kucuk ise negatif, 0'dan buyuk ise pozitif, diger durumlarda ise notr olarak kayit edildi.

# Vader Duygu Analizi 

- Cevrilen yorumlarin oldugu veri seti kullanilarak duygu analizi yapildi ve sonuclar tabloya kayit edildi.
- Eger analiz sonucu cikan skor 0.05'den buyuk ise pozitif, -0.05'den kucuk ise negatif, -0.05'den buyuk veya esit ise ve 0.05'den kucuk ise notr olarak kayit edildi.

# Basari Oranı

- Kullanicinin verdigi puan ile yaptiği yorumun duygu analizi skorlarinin benzerligi her iki duygu analizi kutuphanesi icin test edildi.
- Son olarak iki duygu analizi skorlarinin arasindaki benzerlik basari puani elde edildi.


# Sorunlar 

1. Secilen sayfa araligi kadar sayfayi gezmiyor ve bir yerde tikanip hata veriyor.
   - Bunu manuel olarak asmak icin her hata verdiginde sayfa sayisini bir artirarak daha fazla yorum elde edilebilir.
  
2. Tarama sonucu elde edilen yorum sayisi ve puan sayisi esit olmuyor.
   - Bunu cozmek için ise fazla olandan pop() fonksiyonu ile fazlaliktan kurtulmak.

3. Tabloya yeni bir sutun eklemek istendiginde "Unnamed :0, Unnamed :0.1" gibi yeni sutunlar ekleniyor.
   - Bunun cozumu için drop() fonksiyonu kullaniliyor.
