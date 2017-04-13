# turkish-image-captioning

Bu alan Görüntü Altyazılama  için Otomatik Tercümeyle Eğitim Kümesi Oluşturulabilir mi? (Could We Create A Training Set For Image Captioning Using Automatic Translation? ) başlıklı makaleye ait kodları ve kullanılan Türkçe altyazıları içermektedir (içerecektir). 


[Flickr30k](Flickr30k/train): Flickr30k veri setine ait Turkce altyazilar. 
NOT: Burada model egitilirken TasvirEt altyazilarina ait imgeler ve altyazilari kullanilmamalidir. Cunku Flickr30k veri seti, Flickr8k veri setindeki imgeleri ve altyazilari icermektedir. Bu duruma dikkat edilmelidir.  


[MSCOCO](MSCOCO): MSCOCO veri setine ait Turkce altyazilar. [Egitme](MSCOCO/train): MSCOCO veri setinin egitme kumesinin Turkce altyazilari. [Dogrulama](MSCOCO/val): MSCOCO veri setini dogrulamak icin MSCOCO Validasyon setindeki 500 imge 2 kisi tarafindan el ile altyazilanmistir. [Kullanilan Imgeler](MSCOCO/val/val_file_names.txt) sunlardir. Her imgeye ait 2 farkli kisi tarafindan uretilen dogrulama altyazilari 1 ve 2 uzantilari ile verilmistir. .json uzantili dosyalar metrik hesaplanirken kullanilan sisteme uygun haldedir. Ayni zamanda zemberekten gecirilmis halleri de mevcuttur.


Burada sonuc metriklerini hesaplamak icin [Microsoft COCO Caption Evaluation code](https://github.com/tylin/coco-caption) kullanilmistir.


Modeli egitirken [NeuralTalk2](https://github.com/karpathy/neuraltalk2) kodu kullanildi. Test adiminda -dump_path secenegi aktif edilmelidir. Bu sayede dosya isimleri 1.jpg, 2.jpg gibi degil, orijinal isimleri ile kullanilabilecektir. Metrikler hesaplanirken imge dosyalarinin tam isimleri gerekmektedir.
