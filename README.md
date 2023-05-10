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

![png1](https://github.com/damlaervakasal/REST-API/blob/main/png/1.png)

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



## HTTP Nedir
Hyper  Text Transfer Protocol
- client ile server arasındaki veri akışının kurallarını belirleyen protokoldür.
- istek-cevap (request, response) modeline göre çalışır

istek ve cevabın oluşturulacağı yapıtı HTTP belirler.

REST belirli prensipleri belirli kısıtlamaları olan bir mimari yapı, HTTP ise o mimari yapının kullanıldığı veri akışının kurallarını belirleyen protokol. 

REST Mimarisinde HTTP'nin Rolü

REST mimarisinin prensiplerinden ilki istemci - sunucu çalışma modelidir. Biz bir istekte bulunuruz ve sunucu isteğimize karşılık olan durumu (state) bize bir sunum (presentation) olarak gönderir. HTTP protokolü burada bu sunum transferi için kurulan iletişimin kurallarını belirler. REST mimarisine uygun API'ların neredeyse tamamında HTTP protokolü kullanılır.

HTTP Request

![png2](https://github.com/damlaervakasal/REST-API/blob/main/png/2.png)
1- request line: 
burada kullanılacak olan HTTP metodu/ gidilicek olan PAD (dosya yolu)    ve  HTTP versiyon belirtilir.
2- request headers 
burada HTTP isteğine ait header vardır. İstek başlıkları yapılan isteğin özelliklerini isim ve değer halinde belirtir.
3- a blank line separates header & body
header ile mesaj bodysini birbirinden ayırmayı sağlar.
4- request massage body
yukarıdaki 
id... olan yazarı da o olan kitaba ait verileri istiyor

HTTP Response 

![png3](https://github.com/damlaervakasal/REST-API/blob/main/png/3.png)
1- Status Line
Burada verilen protokol versiyonu ve HTTP status kod döner. Yani başarılı olup olmadığına dair bir bilgi döner.
2- Response Headers
cevaba ait özelliklerin isim ve değer halinde belirtir.
3- a blank line separates header & body
header ile mesaj bodysini birbirinden ayırmayı sağlar.
4- response massage body
rest deki presentation(sunum) gelecek

Status code

Informational responses (bildirimsel cevaplar) ----> 100-199
Succesful responses (başarılı cevaplar) ----> 200-299
redirections (yönlendirme cevapları) -----> 300-399
Client errors(İstemci hataları) -----> 400-499
Server errors(Sunucu hataları) -----> 500-599 


HTTP Methods

GET
- Verileri almak - listelemek için kullanılan istek metodudur.
- http://api.example.com/users
- http://api.example.com/users/1

POST
- Belirli bir kaynağa veri göndermek için kullanılır.
- http://api.example.com/users
PUT
- Belirli bir kaynaktaki verinin tamamının değiştirilmesi için kullanılan metodtur.
- http://api.example.com/users/1
- { “name": "Gurcan", "age": 40}
PATCH
- Belirli bir kaynaktaki verilerin bir kısmının değiştirilmesi için kullanılan metodtur.
- http://api.example.com/users/1
- { "name": "Gurcan"}
DELETE
- Belirli bir kaynaktaki verilerin silinmesi için kullanılan metodtur.
- http://api.example.com/users/1
CONNECT - TRACE - OPTIONS - HEAD

SAFE Metotlar

GET – HEAD – OPTIONS : Sunucu “state” tarafında değişiklik oluşturmazlar. “Read-only” yapısındadırlar.

IDEMPOTENT Metotlar

GET – HEAD - OPTIONS – DELETE – PUT – TRACE : Tekrar durumunda sunucu state yapısında herhangi bir yan etki bırakmazlar. Safe metodlar, idempotent'tır.


Endpoint (Sorgu Adresi)

REST API kullanımında gönderilen istek ile verilen cevap için belirlenen buluşma noktasıdır.
Root(Base) /Path yapısından oluşur, isimler kullanılır, fiil ilgili HTTP metodu ile belirtilir. Dökümantasyon tarafından belirtilir.
- https://jsonplaceholder.typicode.com /posts
Değişen değer için genelde (:) kullanılır.
- https://jsonplaceholder.typicode.com/posts/1 => /posts/:id veya /posts/{{id}}
- https://jsonplaceholder.typicode.com/posts/1/comments
Sorgu parametreleri için (?) kullanılır.
- Aslında sorgu parametreleri REST yapısının bir parçası değildir ancak sorgu adreslerinde sıkça rastlarız.
- http://example.com/articles?sort=author&date=published



JSON(JavaScript Object Notation)

JSON veri depolamak veri iletmek için kullaılan metin tabanlı bir söz dizimi yapısıdır.
JSON dan önce en çok veri depolamak veri iletmek için XML kullanılıyordu.
XML içi içe geçmiş hiyerarşik etiketlerrden oluşur. Ağaç yapısı olarak kullanılır.

Neden JSON kullanıyoruz XML kullanmıyoruz ?  
farklı programlama dillerine göre daha kolay işlenebilmesi, daha olay okunabilmesi gibi avantajları olduğundan dolayı.

POSTMAN

Postman nedir?
Postman bir API platformudur. API geliştirmek , test etmek ve/veya hazır bir API kullanımı için gerekli isteklerde bulunabileceğimiz bir uygulamadır.



Postman Kullanım Senaryoları:

- Bir uygulama geliştirmek istiyoruz ve geliştirmeye başlamada kullanmak istediğimiz ücretli veya ücretsiz bir REST API tarafına ilgili istekleri göndererek gelen sunumları inceleyebiliriz.
- Kendimizin bir REST API oluşturduğu bir senaryoyu düşünelim. Geliştirme aşamasında Postman yardımıyla gelen isteklere karşı uygulamamızın vereceği cevapları test edebiliriz.

Star Wars API(SWAPI)
SWAPI, Star Wars ekosistemine ait olan filmlerin, kahramanların, gezegenlerin vb bilgilerin sunulduğu ücretsiz bir API ortamıdır.

TMDB
TMDB API, IMDB benzeri bir film ve TV programları portalidir.
- API key
- Query parametresi, Path değişkenleri, Session, Token
- POST, DELETE HTTP metotları



Fake API Kullanımı (JSON-SERVER)

Bu pratiğimizde bir Fake (göstermelik) REST API oluşturacağız. Fake REST API oluşturmanın avantajları:
- Frontend (Ön yüz) tarafı hazır olan bir uygulamayı test etmek isteyebiliriz.
- Yapmayı düşündüğümüz bir Backend (Arka yüz) çalışması için bir prototip oluşturmak isteyebiliriz.
- Postman gibi bir API platformunda farklı HTTP metotlarına ait istekler gerçekleştirmek isteyebiliriz.
FAKE REST API oluşturmak için json-server npm paketinden faydalanacağız, bunun için bilgisayarımızda JavaScript çalışma Node.js ( https://nodejs.org/en/) uygulamasının yüklü olması gerekmektedir. Başlangıç olarak
```
npm init
```
komutu ile package.json dosyası oluşturacağız.
```
npm i json-server
```
komutu ile json-server paketini indiriyoruz.
API için kullanacağımız örnek employees.json dosyası : https://github.com/Kodluyoruz/taskforce/blob/main/rest/FakeAPI/files/employees.json . Bu dosyayı oluşturacağımız api klasörünün içerisinde yerleştiriyoruz.
Projemizde bulunan package.json dosyası içerisindeki script bölümünü aşağıdaki şekilde güncelliyoruz.
```
  "scripts": {     "start:server": "json-server --watch api/employees.json"   },
```
Bu sayede aşağıdaki komut ile FAKE API çalışmaya başlayacak.
```
npm run start:server
```

Örnek İstekler

```
GET ALL EMPLOYEES - GET : http://localhost:3000/employees GET AN EMPLOYEE DETAILS - GET : http://localhost:3000/employees/:employee_id EMPLOYEES - ROLES RELATION - GET : http://localhost:3000/employees?_expand=role ADD AN EMPLOYEE - POST : http://localhost:3000/employees UPDATE AN EMPLOYEE - PATCH(PUT) : http://localhost:3000/employees/:employee_id DELETE AN EMPLOYEE - DELETE : http://localhost:3000/employees/:employee_id
```



cURL
URL üzerinden veri transferi yapmamızı sağlayan bir komut satırı aracıdır. REST API çerçeverinde sorgu adreslerine yapılan isteklerde sıklıkla kullanılır. HTTP, HTTPS, FTP, FTPS, GOPHER, GOPHERS, IMAP, IMAPS vs.. bir çok protokolü desteklemektedir.


cURL komut sseçenekleri

- -i (--include): Çıktı içerisinde HTTP başlıklarını da gösterir.
- -I (--head): Yalnızca HTTP başlıklarını görmek için kullanılır.
- -o (--output) <file> : Çıktıyı bir dosyaya yazdırmak için kullanılır.
- -v (--verbose): Daha fazla detay.


Çalışmada bulunan cURL komutları

```
GET A FILM DTEAIL (SWAPI) curl https://swapi.dev/api/films/1/ GET POPULAR MOVIES (TMDBAPI) curl https://api.themoviedb.org/3/movie/popular?api_key=your_api_key GET POPULAR MOVIES (TMDBAPI) -d seçeneği ile curl -X GET -G -d api_key=your_api_key https://api.themoviedb.org/3/movie/popular GET A MOVIE DETAIL (TMDBAPI) -d seçeneği ile curl -X GET -G -d api_key=your_api_key https://api.themoviedb.org/3/movie/:movie_id GET ALL EMPLOYEES (Fake API) curl http://localhost:3000/employees GET AN EMPLOYEE DETAIL (Fake API) curl http://localhost:3000/employees/:employee_id POST AN EMPLOYEE (Fake API) curl -X POST -H "Content-Type: application/json" -d '{ "first_name": "Ricardo", "last_name": "Quaresma", "email": "ricardo@test.tr", "gender": "Male", "roleId": 3 }' http://localhost:3000/employees DELETE AN EMPLOYEE (Fake API) curl -X DELETE http://localhost:3000/employees/:employee_id UPDATE AN EMPLOYEE (Fake API) - PATCH curl -X PATCH -H "Content-Type: application/json" -d '{ "first_name": "Ricardo", "last_name": "Quaresma"}' http://localhost:3000/employees/:employee_id UPDATE AN EMPLOYEE (Fake API) - PUT curl -X PUT -H "Content-Type: application/json" -d '{ "first_name": "Ricardo", "last_name": "Quaresma"}' http://localhost:3000/employees/:employee_id
```
