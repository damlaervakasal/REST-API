# REST-API
API (Application Programming Interface) Nedir?
API bir yazılım parçasının başka bir yazılım parçası ile konuşabilmesidir. Bir yazılımın gerçekleştirebildiği işlemlere belirli koşullar dahilinde dışarıdan erişilip bu işlemlerin kullanılmasını sağlayan arayüzdür.

bir uzaktaki sunucuya request de bulunuyoruz. Uzaktaki sunucudan response yani cevap dönüyor.
Özetle, bir uygulamada gerçekleştirmek istediğimiz ek bir işlemi, o işlemi sağlayan başka bir uygulamadan API kullanarak gerçekleştirebiliriz.

HTTP protokolü

iki kod parçasının iletişime geçmesi belirli kural ve prosedürlere uymalı. Buna protokol denir.

sunucu ile istemci yani web server ile client arasındaki veri iletişimin kurallarını belirleyen protokoldür.

** Postman: API testlerinde sıklıkla kullanılan HTTP client(istemci)dır. **

REST API Nedir?
REpresentational State Transfer, Temsili durum transferi Yani ilgili isteğe karşılık gelen verinin JSON/ XML formatlarında gönderilmesi

JSON Placeholder nedir?
ücretsiz kullanıcağımız rest api sunuyor.

REST mimarisinin prensiplerini taşıyan API'lardır. Tüm prensiplerin karşılanması durumunda RESTfull API olarak da adlandırılır.

REST API Prensipleri
- Client-Server(istemci-sunucu)
- Uniform Interface(Teki Tip Arayüz)
- Statelessness(Durumsuzluk)
- Cacheable(Önbelleklenebilir)
- Layered System(Katmanlı Sistem)
- Code on demand - Optional (İsteğe bağlı kod)




Client-Server(istemci-sunucu)


Client(istemci) requesti(isteği) gönderen konumdadır. Server(sunucu) da bu request e karşılık çoğunlukla JSON formatında bir  presentation (sunum) gönderiyor.



Uniform Interface(Teki Tip Arayüz)


- aynı kaynağa gelen istekler hep aynı şekilde cevaplanmalıdır.
- istemci tarafında kaynağın değiştirebilmesi
- istemci ve sunucu birbirinin ihtiyaç duyduğu bilgilerin tamamını göndermelidir.
parse etme: ayrıştırma
- Sunucu(server) istemci tarafına göndereceği sunumun dosya tipini belirtmeli.(Bu ne işe yarar JSON ya da XML türünde dosya gönderdiğinde client(istemci) bu dosyanın içerisindeki verileri nasıl parse edeceğini bu verilere göre yapar.) İstemci(client) aynı URI a istek yolladığında GET ya da POST olması durumunda farklı metodlar kullandığımızdan dolayı sonuçlar değişir. 



Statelessness(Durumsuzluk)

state: o anda ki durum 

stateful ve stateless
Stateful' u bir örnekle açıklamak gerekirse süreki gittiğimiz kahve dükkanına artık kahveyi yapan kişiye ne içmek istediğimiz söylemeden, daha önce defalarca söyledğimiz şekilde içeçeğimizi yapıyorsa bu olaya stateful (durum bilgisi olan). Her kahve dükkanına gittiğimizde ne içtiğimiz anlatmak durumunda kalıyorsak buna stateless denir.

REST mimarisinde de yapılan her istek birbirinden bağımsızdır. Biz rest api  yaptığtığımız her requestte  o request e karşılık gelen tüm detayları belirtmemiz gerekir. 



Cacheable(Önbelleklenebilir)

örnek vermek gerekirse lise de hazırladığımız formül kağıdı cache işlemi görür. Yani ihtiyacımız olan şeyleri daha yakınımıza almak diye düşünebiliriz.
Client (sunucu) gelen isteklere verilen cevapların önbelleklenebilir olup olmadığını belirtmelidir. Örneğin “Cache-Control”, “Expires” gibi HTTP başlıkları önbellek ile ilgili bilgiler taşır.



Layered System(Katmanlı Sistem)

istemcinin direkt sunucu olarak iletişime geçtiğini düşünüyoruz. Ancak burada ara katmanlar kullanabilir. Bu ara katmanalar gönderilen requestten ve alınan response (cevap) herhangi bir değşik yapmamalıdır. Aradaki katmanlar bağlantılı olduğu katmanlarla ilgilenirler. Bağlantısı olmayan katmanlarla ilgili herhangi bir bilgi taşımazlar. Örnek vermek gerekirse yük dengeleyici


Code on demand - Optional (İsteğe bağlı kod)

Sunucu, istemci tarafına istemcinin işlevini genişletecek ek kodlar gönderebilir. Bu özellik istemci tarafında yapılması gereken işlemleri hafifletir.
Örneğin sunucu, istemci tarafına döneceği HTML dökümanın içerisine JavaScript kodları ekleyebilir.


