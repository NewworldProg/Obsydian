---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/portal/index.php?c=main&pk=ebdd8fd28e415a15a48173a8b560d682_ita_23#?pk=ebdd8fd28e415a15a48173a8b560d682_ita_23&IDJedinica=1434715&c=jedinice"
author:
published:
created: 2025-06-10
description:
tags:
  - "clippings"
---
Koren obrazovanja je gorak, ali je plod sladak. **Aristotel**

---

---

+ Rezime

### Uvod u web programiranje

00:19:24

Jedinica: 4 od 17

U ovom kursu bavimo se razvojem web aplikacija pomoću različitih Java tehologija i Java jezika. S obzirom na to da ovakve aplikacije funkcionišu preko mreže, ==neophodno je poznavanje načina funkcionisanja prevashodno svetske globalne mreže, interneta.==

Osnovni ==internet protokoli predstavljaju temelj funkcionisanja interneta==. Zbog toga, poznavanje ovih protokola predstavlja osnovu za razumevanje funkcionisanja web aplikacija i za njihovu uspešnu izgradnju.

==Internet predstavlja kolosalnu mrežu svih mreža==. Generalno, ==sve mašine== na internetu mogu biti klasifikovane na ==dva tipa==: ==servere i klijente==. ==Klijenti== su mašine koje ==zahtevaju određene informacije==, a ==server== je taj koji te informacije ==stavlja na raspolaganje== klijentima. Informacije putuju od provajdera informacija (što je, naravno, server) do primaoca informacija (klijenta), pri čemu je ta ==komunikacija uslovljena određenim skupom pravila==. Ova pravila se ==nazivaju *protokol*.== Protokol na kome počiva kompletan ==internet je TCP/IP protokol== i o njemu ćemo detaljno govoriti u nastavku lekcije.

==WWW== – World Wide Web – predstavlja samo ==jedan od servisa dostupnih na internetu==. ==Osnovni elementi== World Wide Weba ==su web pregledač (browser)==, ==web server== i ==web aplikacija==, koji ==za== međusobnu ==komunikaciju koriste **HyperText Transfer Protocol (HTTP)**==. ==Klijenti šalju HTTP **zahtev** (request)== upućen web serveru, a ==server uzvraća podatke u formi HTTP **odgovora** (response)==. Praktično, klijenti i serveri su osnovni gradivni blokovi World Wide Weba, dok je HTTP jezik kojim oni „govore”.  
  

### ==TCP/IP==

U uvodnom delu ove lekcije pomenuli smo ==HTTP protokol kao osnovni protokol World Wide== ==Weba.== S obzirom na to da je WWW samo jedan od servisa koji su dostupni na internetu, te da je njegovo postojanje direktno uslovljeno postojanjem interneta, jasno je da ovaj protokol mora biti ==podskup nekog mnogo šireg protokola==. Naravno, reč je ==TCP/IP protokolu, na kome počiva praktično celokupna razmena podataka preko globalne mreže==, interneta. ==Ovaj protokol se može podeliti na nekoliko slojeva,== i to u zavisnosti od faza kroz koje podaci prolaze prilikom putovanja kroz mrežu.

Prilikom kreiranja web aplikacija, programer nije u obavezi da poznaje arhitekturu na kojoj počiva njegov sistem. Međutim, samo dobro poznavanje kompletne arhitekture sistema omogućava pravilno rukovanje njime.

==Da bi jedna web strana bila transportovana od tačke A (server) do tačke B (klijent), mora biti ispunjeno mnoštvo uslova== i u tom procesu učestvuje mnoštvo aktera. Taj proces je ilustrovan na slici 4.1; on podrazumeva četiri različita nivoa odigravanja.  
  
![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_04_01.jpg)

*Slika 4.1. Razmena podataka između dva hosta preko interneta  
  
*

- Prvi, najniži nivo je ==**Network Access Layer**==. Na ovom nivou ==obezbeđuju se validnost== ==komunikacije== između uređaja, ==ispravnost dostave sirovih podataka== i slično. Ovo je sloj koji ==najčešće nije dostupan (niti potreban) programeru web aplikacije==.
- ==**Internet Layer**== je sloj na kome se ==razmenjuju paketi između računara==. Ovaj sloj je velika saobraćajnica IP (Internet Protocol) paketa, na kojoj se ==nalazi mnoštvo „stanica” identifikovanih IP adresama==. Svaki ==IP paket u sebi nosi podatak i IP adresu,== na osnovu koje sistem zna gde taj podatak treba dostaviti.
- ==Kroz== ==**Transport Layer**== se razmenjuju podaci na osnovu jednog od dva sistema (protokola):  
	- Jedan sistem je ==**TCP (Transport Control Protocol)**==. On funkcioniše tako što ==dva računara uspostavljaju uzajamnu komunikaciju, a zatim, sinhronizovano, razmenjuju informacije== jedan sa drugim, da bi, n==akon što je razmena informacija završena, raskinuli uzajamnu vezu i oslobodili resurse za sledeću komunikaciju==. Ovaj protokol se smatra ==veoma sigurnim== jer ==garantuje dostavu podataka,== pa se zato na njemu zasniva većina sistema na internetu (npr. WWW, FTP, SSH, email).
	- Drugi protokol transportnog nivoa je ==**UDP (User Datagram Protocol)**.== Ovaj protokol nije tako siguran kao TCP, jer ==ne garantuje da će paket koji je poslat stići do cilja.== Ovaj protokol ==šalje podatke na adresu ne zahtevajući eksplicitnu potvrdu o uspostavljenoj komunikaciji i dostavi== tih podataka. Zbog toga su najčešće sfera korišćenja UDP protokola sistemi koji ne zahtevaju sigurnu dostavu podataka, već se ide na što bržu dostavu, po cenu da poneki podatak bude i izgubljen (npr.live video streaming, online gaming). Ovo je nivo u kome se web programer može naći ponekad, u slučaju da aplikacija ima neke specifične zahteve.
- ==**Application Layer**== je ==sloj kroz koji putuju podaci u raznim preformatiranim oblicima.== „Formati” podataka koji se koriste prilikom ovih putovanja ==zapravo su protokoli aplikacionog sloja ([FTP](https://www.link-elearning.com/linkdl/opisPojma.php?id=161747 "FTP"), HTTP, [SMTP](https://www.link-elearning.com/linkdl/opisPojma.php?id=161748 "SMTP")...).== Ti protokoli su veoma bitni za web programiranje, a svakako ==najbitniji među njima je **HTTP (HyperText Transport Protocol)**==. Tako opet dolazimo do pojma koji smo definisali na početku lekcije – HTTP.

### ==Osnove HTTP-a==

HTTP je request–response protokol, što znači da njegov način funkcionisanja počiva na međusobnom smenjivanju zahteva i odgovora između klijenta i servera. ==Kada klijent zatraži neki resurs==, taj zahtev obično ==sadrži identifikaciju zahtevanog resursa==, i to u formi ==[Uniform Resource Locator a](https://www.link-elearning.com/linkdl/opisPojma.php?id=161746 "<u>Uniform Resource Locator</u>a") (URL)==. URL je hijerarhijska sekvenca komponenata, strukturirana kao na slici 4.2.  
  
![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_04_02.jpg)

*Slika 4.2. Različiti segmenti URL-a*

  
U ovom primeru, [www.yourbookstore.com](http://www.yourbookstore.com/) predstavlja host name. Odmah nakon hosta, odvojen dvotačkom, naveden je broj porta. Host name i port zajedno se drugačije nazivaju ***authority***.

bookstore u ovom primeru predstavlja putanju – ili, da pojednostavimo, folder u kome se nalazi traženi resurs. Na kraju dolazimo i do resursa, i to je u ovom primeru bookServlet. To je zapravo dokument koji je tražen. Nakon navedenog resursa, ovaj URL sadrži i query string.

Neki delovi prikazanog URL-a su opcioni, uključujući broj porta i query string. Kada je naveden, query string predstavlja seriju parova ključeva i vrednosti kojima prethodi znak pitanja i gde su parovi razdvojeni karakterom ampersand (&).

Query string se koristi za prosleđivanje parametara; u primeru na slici je definisan parametar sa nazivom action i vrednošću bookDetails.

Query string se može pojaviti samo u okviru GET metode. Pored GET metode, HTTP protokol poznaje i druge metode: POST, DELETE i PUT. Ali, šta su zapravo ove metode?

Da biste ovo razumeli, pogledajte kako bi izgledalo jedno slanje zahteva klijenta serveru. Inače, klijent se u ovom procesu drugačije naziva **user agent**, dok se server naziva **origin server**.

HTTP komunikacija između servera i klijenta započinje **HTTP zahtevom** klijenta.

Prilikom slanja zahteva, user agent ili klijent prosleđuje serveru informacije o tome koje [MIME](https://www.link-elearning.com/linkdl/opisPojma.php?id=161749 "MIME") tipove (Multimedia Internet Mail Extensions – ovo su razni oblici dokumenata: HTML, slike, arhive...) može da prihvati, koju verziju HTTP protokola zahteva, o kojoj verziji user agenta je reč, koji je kodni raspored zahteva, referer (stranu sa koje je došao zahtev, ukoliko je došao sa neke strane), podatke o kolačićima, koji je status keša user agenta (da li je strana keširana na klijentu) i tako dalje.

Zahtev sadrži u sebi i HTTP metod, odnosno obrazac koji web server treba da ispoštuje prilikom obrade zahteva i rukovanja resursima. Metod bi najbolje mogao da se okarakteriše kao najobičnija naredba. Ako u pregledaču otkucamo npr.:

```java
www.mysite.com/index.html
```

zahtev se upućuje na tu adresu, i mogli bismo biti sigurni da će negde u klijentskom zahtevu koji se upućuje serveru postojati linija:

```java
GET /index.html HTTP/1.1
```

kao i linija:

```java
host: www.mysite.com
```

gde je:

- GET naziv metoda;
- /index.html adresa koja se zahteva;
- HTTP/1.1 verzija protokola i
- host: www.mysite.com naziv top domena za taj sajt.

  
Na osnovu ovih informacija, web server formira **HTTP odgovor** i prosleđuje ga klijentu.

Na zahtev formatiran na pomenuti način, server formira odgovor i prosleđuje ga nazad pošiljaocu (a server u svakom trenutku zna [IP adresu](https://www.link-elearning.com/linkdl/opisPojma.php?id=161750 "IP adresu") i port gde se od njega očekuje da prosledi odgovor).

Odgovor servera sadrži status: **200** ako je sve u redu, ili neki od mnogih brojeva koji označavaju greške ukoliko nešto nije kako treba. Brojevi koji se najčešće pojavljuju su **404** (tražena strana ne postoji) i **500** (greška u web aplikaciji). Zapravo, statusi se po brojevima dele na određene grupacije:

- 1xx za informacije;
- 2xx sve vrste uspešnih apstrakcija;
- 3xx redirekcije;
- 4xx klijentske greške;
- 5xx serverske greške.

  
Pored statusa, u odgovoru se obično nalazi i zaglavlje (header), kao i sam sadržaj dokumenta.

Ceo **HTTP request–response** proces izgleda ovako:

Klijent unosi adresu:

```java
http:
```

User agent otvara socket preko porta 80 i šalje zahtev preko njega:

```java
GET /index.html HTTP/1.0
host: www.mysite.com
```

Server, nakon što prihvati zahtev, na isti port, preko istog socketa, šalje odgovor, koji bi mogao da izgleda ovako:

```java
HTTP/1.0200OK
Content-Type: text/html
Content-Length: 500
 
<html>
      <body>
            ... some server response ...
      </body>
</html>
```

  
Nakon toga, potpuno je nebitno šta će user agent učiniti sa dobijenim odgovorom. U slučaju web pregledača, ovaj odgovor će biti parsiran, preveden i emitovan korisniku, ali aplikacija se može baviti i raznim drugim stvarima.

Na osnovu ovih informacija, vidi se da stvari putem HTTP-a funkcionišu dosta jednostavno.  
  

### Rukovanje stanjima

Videli smo kako se tokom request–response procesa prosleđuju podaci. Klijent traži od servera podatke i server mu šalje te podatke u odgovoru. Ali, problem je u tome što server nije u stanju da prepozna ko mu je šta tražio. On, jednostavno, na osnovu IP adrese i porta, prosleđuje odgovor nazad, i to je sve. To znači da nije u stanju da vidi da li je, na primer, korisnik još uvek na web strani koju je emitovao. Zatp se kaže da je HTTP protokol *stateless*.

Ovakav način funkcionisanja je logičan, s obzirom na to da se dva različita posla obavljaju na dve različite lokacije (klijentu i serveru) nevezani jedan za drugi, ali nosi i svoje probleme, jer je, da bi se podaci o stanju prosleđivali tokom response–request procesa, potrebno upotrebiti posebne metode.

Postoje tri različita načina da se rukuje stanjem u Java web aplikaciji. U ovoj lekciji objasnićemo načine njihovog funkcionisanja, a u narednim i kako se praktično upotrebljavaju.

Prvi način je upotreba HTTP metoda **GET** i **POST**.  
  

### GET/POST (HTTP metode)

Ove dva metode pomenute su u kontekstu HTTP zahteva (requesta).  
  
**GET**

GET, kao osnovni i najčešći metod za dobijanje serverskog odgovora, prilaže adresu na kojoj se nalazi željeni odgovor. Ali, pored tražene adrese, zahtev može sadržati i određene parametre koje je server u stanju da razlikuje, pa tako i programer može da ih upotrebi u serverskom kodu.

Parametri poslati kroz GET metod nisu nimalo bezbedni; štaviše, veoma su nebezbedni, jer se emituju u query stringu (string koji predstavlja kompletnu adresu strane). Ovo ne znači da query string za prenos informacija treba izbegavati kada je reč o informacijama koje nemaju bezbednosni kontekst. Zato se GET parametri često kriptuju.

Na primer:

```java
www.mysite.com/index.jsp?id=098f6bcd4621d373cade4e832627b4f6
```

Na ovakav način ne prenose se nikakve bezbednosno vitalne informacije, već ovakav kod obično prezentuje kodiranu reprezentaciju nekog dela izvora podataka gde se određene informacije nalaze. Tek odatle, mogu se izvršiti određene ozbiljnije provere (npr. provera korisnika). Ali, čak i ako je izveden na taj način, prenos bitnih podataka putem query stringa je nebezbedan i nepreporučljiv. Pored toga, tako nije moguće preneti veliku količinu informacija.

Dakle, query string ne treba u potpunosti izbegavati, ali je preporučljivo da se on koristi samo sa informacijama koje nemaju bezbednosni kontekst.

Na primer:

```java
www.mysite.com/index.jsp?product=15
```

Ovde je pristup slanja podataka kroz query string dobar, jer maliciozni korisnik ne može da uradi ništa aplikaciji ukucavanjem pogrešnog broja proizvoda (osim da dođe do nekog drugog proizvoda), a link je čitak i funkcionalan. Naravno, obavezno je da sva odstupanja od željenog scenarija budu obrađena u serverskom kodu.

Jedan od oblika manipulacije query stringom je i prepisivanje URL-a.

Prepisivanje URL-a funkcioniše tako što na samom web serveru odredimo određene konvencije, koje će web server poštovati i na osnovu njih praviti odgovore. Te konvencije su međusloj između stvarne hijerarhije fajlova na web serveru i onoga što korisnik zahteva u upitu.

Malopređašnji primer:

```java
www.mysite.com/index.jsp?product=15
```

mogli bismo prevesti u:

```java
www.mysite.com/product/15
```

ukoliko kažemo serveru da deo adrese *product* tretira kao:

```java
index.jsp?product=
```

a deo sa brojem (u ovom slučaju 15) kao drugi deo adrese.

Na ovaj način moguće su moćne manipulacije nazivima adresa (URI-ima). Na primer, bez problema je moguće sve.jsp ekstenzije na serveru prikazati kao.aspx ili bilo koje druge ekstenzije, a da se pri tome na serveru i dalje izvršavaju Java aplikacije.

Prepisivanje URL-a, kao modul, treba zasebno startovati u okviru Apache servera i često je isključeno ili zabranjeno, ukoliko ne koristite sopstveni server za host.

Razlog je to što ovaj modul može dovesti do problema prilikom nepažljivog rukovanja. Na primer, može se lako desiti da zaključate folder u kome radite i da posle toga ne možete više da mu pristupite, što može biti veliki problem ako koristite udaljeni, automatski hosting sistem.  
  
**POST**

POST metod funkcioniše nešto drugačije od GET metoda i bezbednosno je na samo malo višem nivou. Naime, prilikom slanja zahteva serveru, ukoliko zahtev poziva ovaj metod, u telu zahteva se očekuje i set serijalizovanih podataka koje server, odnosno aplikacija na serveru može uzeti za obradu. Informacije prenesene ovim putem ne mogu se videti „golim okom”, ali već pregledom izvornog HTML koda strane, lako je doći do svih transportovanih podataka.

Ovakav način prosleđivanja podataka koristi se obično za aplikacije na kojima se obrađuju kontrole (forme) i nije naročito dobar za promociju određene web strane, zato što nije moguće samo proslediti adresu strane, jer ona neće dati rezultate bez podataka koje zahteva. A da bismo te podatke prosledili, potrebna nam je forma koja će ih serijalizovati i poslati.

Drugi način za rukovanje stanjem jesu kolačići – cookies.  
  

### Cookies (kolačići)

Dva do sada pomenuta načina, iako to nije neizvodljivo, nisu baš uzori za bezbedno čuvanje stanja u request–response procesu. Informacije putuju pred očima korisnika u često nekriptovanoj formi i čine ove metode nebezbednim za bilo koju informaciju koja treba da bude sigurna i skrivena.

Cookie je nešto bolji način da se očuva sigurnosni integritet informacije kroz proces. Zapravo, on i ne učestvuje aktivno u procesu, već čuva podatak na klijentskom računaru (ne učestvuje u procesu u smislu toga da se neće videti, ali jednom aktiviran, cookie jeste deo svih zahteva tom serveru do isteka važnosti). Ovakav pristup omogućava da podaci budu čuvani vremenski neograničeno i da se manipulacija njima vrši samo onda kada je to potrebno i da se time smanji opterećenje protoka.

Kolačići se nalaze na klijentskom računaru, pa postoji šansa da budu obrisani ili ukradeni, ali su odličan način da server prilikom svakog zahteva, ukoliko to želi, precizno zna sa kojim klijentom komunicira.

Treba naglasiti da kolačići (kao ni sessioni, o kojima će biti reči u sledećem segmentu) nisu preporučljivi za skladištenje velike količine podataka. Ovo su mali blokovi podataka (ne veći od 4k po sajtu) koji služe za to da se u njih smeste samo najosnovniji podaci koji povezuju klijenta i server. Na primer, ID korisnika čije će sve ostale informacije pod tim brojem biti izvučene iz nekog izvora podataka na samom serveru.  
  

### Sessions (sesije)

Konačno, poslednji i najpopularniji način za čuvanje stanja na web serveru je sesija. Generalno, sesija funkcioniše slično kolačićima, ali podrazumeva da ćete podatke o klijentu uskladištiti na samom serveru.

Ovo funkcioniše tako što se, kada klijent prvi put zatraži otvaranje sesije, na web serveru generiše jedinstveni broj (JSESSIONID) koji će ubuduće predstavljati tog klijenta u listi sesija. Ovaj ID se zapamti u fajlu na serveru (Session Store File) i biva prosleđen klijentu. Klijentska aplikacija, zatim, formira kolačić u kome se nalazi ovaj broj i uz svaki zahtev ga prosleđuje serveru kako bi server identifikovao sesiju i iz nje prosledio tražene podatke.

Iako je predviđeno da sesije funkcionišu pomoću kolačića, nije obavezno imati kolačiće da bi se rukovalo sesijama. Moguće je do sesije doći i ručno, tako što se u query stringu serveru prosleđuje i ID sesije:

```java
http:
```

  
Što se informacija tiče, za sesije, kao i za ostale opisane sisteme, važi da nije poželjno skladištiti u njima prave informacije, već radije samo identifikatore kojima možemo doći do pravih informacija iz nekog izvora podataka na serveru.

Sesije su bezbednosno dosta „čvrste”, ali ne i „neuništive” (recimo, pomenutom tehnikom slanja ID-ja sesije kroz query string moguće je pogađanjem doći do tuđe sesije, pa tako i do tuđih podataka (session hijack)).

Sve u svemu, u ovoj lekciji upoznali smo se sa osnovnim protokolima interneta i World Wide Weba i stekli neki osnovni uvid u okruženje u kojem će web aplikacija postojati. U narednoj lekciji prelazimo na praktično kreiranje web aplikacija, a u sledećem modulu ćete imati prilike da vidite konkretne primere sva tri načina kojima se rukuje stanjem u Java web aplikacijama.  

Kako se naziva osnovni protokol na kojem počiva internet?

  

## MULTIMEDIJA

---

[00:17:42 ![](https://multimedia.dizajn-akademija.com/sr/Java_Web_Application_Development/multimedijaFinal/JWAD1_04.thb) JWAD1\_04.mp4](https://www.link-elearning.com/linkdl/portal/?c=main&pk=ebdd8fd28e415a15a48173a8b560d682_ita_23# "JWAD1_04.mp4")

| [  Prethodna jedinica  ](https://www.link-elearning.com/linkdl/portal/index.php?pk=ebdd8fd28e415a15a48173a8b560d682_ita_23&IDJedinica=1434714&c=jedinice) | [  Sledeća jedinica  ](https://www.link-elearning.com/linkdl/portal/index.php?pk=ebdd8fd28e415a15a48173a8b560d682_ita_23&IDJedinica=1434716&c=jedinice) |
| --- | --- |

Kako Vam mogu pomoći?

[Scroll To Top](https://www.link-elearning.com/linkdl/portal/?c=main&pk=ebdd8fd28e415a15a48173a8b560d682_ita_23#)