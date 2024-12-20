# T-display-S3-ve-Si4732-ile-DSP-Radyo-
Lilygo'nun ürettiği T-display S3 ve Skyworks Si4732 ile AM/FM radyo alıcısı
PU2CLR çağrı işaretli [Ricardo Lima Caratti'nin harikulade kütüphâneleri](https://github.com/pu2clr/SI4735/) ile [ESP32 için hazırlamış olduğu uygulama](https://github.com/pu2clr/SI4735/tree/master/examples/SI47XX_06_ESP32/OLED_ALL_IN_ONE) esas alınarak [Ralph Xavier'in T-display S3'e uyarladığı yazılımda](https://github.com/ralphxavier/SI4735/tree/master/Lilygo_T-Display_S3/ALL_IN_ONE_T-Display_S3#start-of-content) bâzı değişiklikler yapılmıştır.
Bu değişiklikler şunlardır:
 1) Kısa dalga yayın bandlarının sınırları olması gereken sınırlara çekildi.
 2) VHF'de (FM) alt band sınırı 64 MHZ'den 87.5 MHz'e getirildi.
 3) Siyah ekranda beyaz yazılar çok gözalıcı göründüğünden, camgöbeği (cyan) renkle değiştirildi. RDS yazıları gri yapıldı. 
     Ana frekans gösterge rengi VFD gibiymişçesine açık yeşil renge ayarlandı.
  4) Pil seviye göstergesinde kırmızıdan bir önceki seviye sarıdan turuncuya değiştirildi.
  5) VHF'de (FM) 1 MHZ'lik adım ilâve edildi.
  6) Menü ögeleri mümkün olduğunca Türkçeleştirildi.
  7) Baskı devre dizaynında    encoder bağlantıları  değişikliğinden  dolayı  öncelikle  encoder'a
     ait bağlantı bacakları değiştirildi. Daha sonra da bu değişiklikten dolayı  menülerde gezinti
     yönü düzenlendi.
  8) T-display S3'ün LCD  arkaışığı 38. GPIO tarafından kontrol ediliyor. Bu giriş 0 seviyesindeyken
     arkaışık yanıyor. Ancak, arkaışık  oldukça fazla  akım çektiği  gibi,  sürekli  aynı  istasyonu
     dinlerken veya Li-Ion pil doldurulurken gereksizdir. Bu yüzden, 2. menüye ISIK ögesi eklendi. Bu 
     öge seçildiğinde radyo çalışmaya  devam etmekle birlikte arkaışık söner. Encoder'a basılmasıyla 
     birlikte arkaışık yeniden yanmaya başlar. 
Yazılımı Arduino IDE'de derlemek için gerekli ayarlar **T-display-s3 alıcı ayarlar.png** dosyasında gösterilmiştir.
