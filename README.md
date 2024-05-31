# FlutterBorsaTakipApp
Flutter'da Finnhub.io API kullanarak borsa takibi yapan bir uygulama.
It's an app in Flutter that uses Finnhub API to track stock data.


## Örnek Kurulum
başlangıçta main.dart içerisindeki bu tanımlamaya Finnhub.io dan edindiğiniz API key'i girmeniz yeterlidir. 
<br>
final String apiKey = 'your-api-key'; // Finnhub API key
<br>

Ardından, uygulamayı flutter run ile çalıştırdıktan sonra uygulamaya verilerin aktığını ve güncellendiğini göreceksiniz.
<br>

### Notlar
Kod her 10 saniyede 1 güncelleme isteğinde bulunur. Örneğin 5 saniyede bir veri çekmek istendiğinde 429 kodlu hata çok sık alınabiliyor. Bu da çok fazla istekte bulunduğumuz anlamına geliyor. Bu yüzden 10 saniyede bir yeni verileri çekmek üzere ayarlanmıştır. Kullandığınız API'ye göre bunu arttırıp azaltabilirsiniz.
<br>
Timer.periodic(const Duration(seconds: 10), (Timer t) => checkForUpdates()); // 10 saniyede 1 güncelleme kontrolü yapar.
<br>
Bu kısımdan bu ayarı yapabilirsiniz.



    
