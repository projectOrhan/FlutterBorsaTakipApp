# FlutterBorsaTakipApp
Flutter'da Finnhub.io API kullanarak borsa takibi yapan bir uygulama.
<br>
Burada Finnhub.io'yu deneyebilmek için ücretsiz API anahtarı sağlaması tercih sebebi oldu. Siz dilerseniz başka benzer API'leri kullanabilirsiniz.
<br>
It's an app in Flutter that uses Finnhub API to track stock data.
Here I chose Finnhub.io because it provides a free API key to try it out. You can use other similar APIs if you wish.

<br>

## Örnek Kurulum
başlangıçta main.dart içerisindeki bu tanımlamaya Finnhub.io dan edindiğiniz API key'i girmeniz yeterlidir. 
<br>
At startup, simply enter the API key you obtained from Finnhub.io in this definition in main.dart. 
<br><br>
final String apiKey = 'your-api-key'; // Finnhub API key
<br>

Ardından, uygulamayı flutter run ile çalıştırdıktan sonra uygulamaya verilerin aktığını ve güncellendiğini göreceksiniz.
<br>
Then, after running the app with flutter run, you will see data flowing into the app and updating.
<br>

### Notlar
Kod her 10 saniyede 1 güncelleme isteğinde bulunur. Örneğin, 5 saniyede bir veri çekmek istendiğinde 429 kodlu hata çok sık alınabiliyor. Bu da çok fazla istekte bulunduğumuz anlamına geliyor. Bu yüzden 10 saniyede bir yeni verileri çekmek üzere ayarlanmıştır. Kullandığınız API'ye göre bunu arttırıp azaltabilirsiniz.
<br>
The code requests an update every 10 seconds. For example, if you want to pull data every 5 seconds, error 429 can be received very often. This means that we are making too many requests. So it is set to pull new data every 10 seconds. You can increase or decrease this depending on the API you are using.
<br>
Timer.periodic(const Duration(seconds: 10), (Timer t) => checkForUpdates()); // 10 saniyede 1 güncelleme kontrolü yapar.
<br>
Bu kısımdan bu ayarı yapabilirsiniz.



    
