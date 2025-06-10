---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/portal/index.php?c=main&pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23#?pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23&IDJedinica=1434713&c=jedinice"
author:
published:
created: 2025-06-09
description:
tags:
  - "clippings"
---
Ono malo što znam zahvaljujem svom neznanju. **Johann Wolfgang von Goethe**

---

---

+ Rezime

### ==Kreiranje prve web aplikacije==

00:24:17

Jedinica: 2 od 17

U ovoj lekciji pozabavićemo se kreiranjem prve Java web aplikacije. ==Kreiraćemo jednu jednostavnu web aplikaciju koja će na izlazu prikazivati poruku *Hello World*==. Pod izlazom se ovde podrazumeva web stranica, pa će ==efekti naše aplikacije biti vidljivi pri pokretanju u nekom od pregledača==. ==Preduslov== za uspešno praćenje ove lekcije je instalirano razvojno okruženje ==IntelliJ IDEA Community Edition.==  
  

### ==Kreiranje projekta za Java web aplikaciju==

Java web aplikaciju je moguće kreirati na mnogo načina. Za njeno kreiranje mi ćemo koristiti ==IntelliJ IDEA razvojno okruženje i jedan od Maven šablona== koji nam omogućava da automatski dobijemo Java web aplikaciju sa određenom projektnom strukturom. Za obavljanje takvog posla prvo je potrebno odabrati opciju za kreiranje novog projekta – ==**New Project** (slika 2.1).==

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_01-novo.png)

*Slika 2.1. Kreiranje novog IntelliJ IDEA projekta  
  
*

Unutar prozora za konfigurisanje novog projekta, potrebno je ==odabrati **Maven Archetype**== iz liste generatora projekta, a onda projekat ==konfigurisati kao na slici 2.2==.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_02-novo.png)

*Slika 2.2. Konfigurisanje Java web projekta  
  
*

Na prikazan način kreira se jedan projekat koji će kao svoj sistem izgradnje koristiti Maven. Stoga je odmah na početku potrebno odgovoriti na dosta pitanja čiji odgovori u ovom trenutku za vas mogu biti nepoznanice – ==*na šta se odnosi proces izgradnje aplikacija; šta je pakovanje i šta su to automatizovani sistemi za izgradnju u koje se svrstava i spomenuti Maven*?==

| ==**Pojam *izgradnje* aplikacije**==  Izgradnja Java aplikacije ==podrazumeva== ==prevođenje== ==Java programa (pomoću Java kompajlera) i svih njegovih komponenata,== kao i eventualno ==pakovanje u neku kompozitnu formu==. Često prevođenjem nazivamo prevod jednog fajla, dok je izgradnja prevođenje više fajlova u jednom koraku.  ==Prevođenje==:  - prevodi se ==jedan ili više .java fajlova u bajtkod;== - ==finalni proizvod su .class fajlovi==.  ==Izgradnja==:  - prevodi se j==edan ili više .java fajlova u bajtkod==; - prikupljaju se i obrađuju prateće komponente programa; - prevedeni ==fajlovi raspoređuju se u odgovarajuće foldere; - finalni proizvod ne moraju biti .class fajlovi==.  I u slučaju prevođenja i slučaju izgradnje, ==glavnu ulogu ima program **javac**==.  **Pakovanje Java aplikacija**  Krajnji korisnici generalno ne vole programe koje moraju da podešavaju da bi funkcionisali. Čak ni ako smo sami krajnji korisnici sopstvene aplikacije, neće nam biti drago da je svaki put startujemo na specifičan način. Zato se ==Java aplikacije najčešće pakuju u pakete, a zatim startuju pomoću takvih paketa==. Spomenuti paketi najčešće su ==tipa JAR== (za samostalne aplikacije), ==WAR== (za web aplikacije) ili ==APK== (za Android aplikacije). ==Svaki od spomenutih paketa nije ništa drugo do ZIP== arhiva sa specifičnom ekstenzijom.  ==**Šta je problematično kod direktne izgradnje i pakovanja?**==  Do sada smo obavljali prevođenje i pakovanje jednostavnih aplikacija. Očigledno je da bi ==za komplikovaniju aplikaciju bilo potrebno više podešavanja, te da bi sama njena izgradnja bila komplikovanija==. Kompletna procedura izgradnje i pakovanja zapravo podrazumeva nekoliko koraka, što dramatično usporava proces proizvodnje ukoliko imamo potrebe za čestim proverama funkcionisanja aplikacije. Ručna izgradnja i pakovanje posebno otežavaju i testiranje, a u celoj toj priči ne sme se izostaviti ni rukovanje zavisnostima, odnosno pridruživanje dodatnih biblioteka koje će našim aplikacijama biti potrebne za nesmetano izvršavanje. ==Zbog svega toga, postoje posebni alati koji su namenjeni izgradnji projekata.==  **Šta su to alati za izgradnju projekata?**  ==Alat za izgradnju automatizuje sve što je povezano sa izgradnjom softverskog projekta==. Izrada softverskog projekta obično uključuje jednu od sledećih aktivnosti ili više njih:  - ==generisanje izvornog koda== (==ako se u projektu koristi automatski generisani kod==); - ==generisanje dokumentacije== iz izvornog koda; - ==kompajliranje izvornog koda==; - ==pakovanje== kompajliranog koda ==u JAR, WAR, ZIP== ili neku drugu vrstu arhive; - instaliranje zapakovanog koda na server, u repozitorijum ili na neko drugo mesto.  ==Automatizacija procesa izgradnje smanjuje rizik od pojave ljudske greške== prilikom ručne izgradnje softvera. Pored toga, automatizovani alat za izgradnju je obično brži od čoveka koji bi izvodio iste korake ručno.  **Alati za izgradnju Java aplikacija**  ==Tri najpoznatija alata koja se koriste u svetu Java programiranja su:==  - ==Apache Ant + Ivy== (https://ant.apache.org/ivy/); - ==Apache Maven== (https://maven.apache.org/); - ==Gradle== (https://gradle.org/).  ==Ant je najstariji== od tri spomenuta alata. Jednostavan je za rukovanje i ==bazira se na XML-u==.  ==Maven== je ==najpopularniji== alat za izgradnju Java aplikacija. ==Bazira se na XML-u==, baš kao i Ant. Jedna od najvećih ==prednosti Maven alata u odnosu na Ant jeste postojanje sistema za automatsko rukovanje zavisnostima==. Takav sistem ==podrazumeva dinamičko preuzimanje i učitavanje eksternih biblioteka koje se koriste u projektu== na kome se radi.  ==Gradle== obavlja identičan posao ==kao Ant i Maven==, ali je reč o ==najmlađem alatu==, zbog čega on ==nudi najveći broj mogućnosti== kojima se prevazilaze problemi koji postoje u Ant i Maven alatima. Osnovna osobenost Gradle alata jeste korišćenje [Groovy](https://www.link-elearning.com/linkdl/opisPojma.php?id=171189 "Groovy") jezika za konfigurisanje projekta. Gradle je atraktivan alat za izgradnju, sa veoma dobrom perspektivom.  **Maven**  Maven je jedan od najpopularnijih alata za automatizaciju izgradnje projekata koji koriste Java programski jezik. Iako se ==najčešće koristi== u svetu Java programiranja, ==moguće ga je upotrebljavati i na projektima u kojima se koriste C#, Ruby, Scala i drugi programski jezici.==  Maven je 2002. godine kreirao Jason van Zyl (Džejson Van Zil), da bi projekat već 2004. godine prešao pod okrilje Apache softverske fondacije (Apache Software Foundation). Maven je primarno ==usmeren na standardizaciju i automatizaciju sledećih procesa:== ==izgradnja==, ==dokumentovanje==, ==rukovanje zavisnostima,== ==generisanje izveštaja==, ==distribucija==, ==objavljivanje==...  Maven je alat koji se može koristiti za izgradnju i upravljanje za bilo koji projekat zasnovan na Javi. Maven umnogome olakšava svakodnevni rad Java programera i generalno pomaže u razumevanju bilo kog Java baziranog projekta.  IntelliJ IDEA podržava potpuno funkcionalnu integraciju sa Maven alatom, koja pomaže da se proces izgradnje automatizuje. Može se jednostavno kreirati novi Maven projekat, otvoriti i sinhronizovati postojeći, dodati Maven podrška bilo kom postojećem IntelliJ IDEA projektu, konfigurisati i kontrolisati projekat sa više modula...  **Maven Archetype**  Na kraju, dolazimo i do pojma koji smo direktno upotrebili prilikom kreiranja prvog Java web projekta, što možete videti na slici 2.2. *Maven Archetype*.  Maven Archetype je osnovni sistem za projektne šablone kada se za izgradnju koristi Maven. Šta to praktično znači? To praktično znači da nam Maven omogućava da prilikom kreiranja projekata dobijemo određenu unapred pripremljenu strukturu koja u svom sastavu poseduje i određene fajlove sa automatski napisanom osnovnom logikom. |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

Prethodni redovi, u kojima smo skrenuli sa glavne teme ove lekcije, bili su neophodni kako biste bolje razumeli samu pozadinu korišćenja Maven sistema za izgradnju i arhetipova koji nam omogućavaju da brzo dobijemo potrebnu projektnu strukturu. Sve to praktično znači da, kada se koristi **maven-archetype-webapp**, baš kao što smo to mi uradili, dobijamo kostur jedne Java web aplikacije, što podrazumeva kreiranu fajl strukturu, fajlove za konfigurisanje takvog projekta, pa čak i jedan fajl koji predstavlja stranicu naše nove web aplikacije. To će zapravo da bude projekat koji ćemo odmah moći da upotrebimo za pokretanje i testiranje.

Na kraju, nakon odabira arhetipa i klika na dugme **Create** (slika 2.2.), IntelliJ IDEA će za nas obaviti kreiranje projekta.  
  

### Struktura Maven Java web aplikacije

IntelliJ IDEA, odnosno preciznije Maven sistem za izgradnju, prilikom kreiranja projekta automatski uspostavlja određenu strukturu fajlova i foldera. Nju možete da vidite na slici 2.3.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_03-novo.png)

*Slika 2.3. Struktura Java web Maven projekta  
  
*

Slika 2.3. ilustruje navigacioni panel IntelliJ IDEA razvojnog okruženja unutar koga je moguće videti kompletnu projektnu strukturu koja se dobija od Maven sistema za izgradnju. Koreni folder takve strukture nosi naziv javaee\_demo i to je naziv koji je formiran na osnovu imena projekta koje smo postavili u prethodnom koraku. Unutar takvog korenog foldera direktno se nalaze sledeći fajlovi/folderi:

- **.idea** – fajlovi koje koristi razvojno okruženje IntelliJ IDEA; njima se gotovo nikada nećemo baviti direktno;
- **src** – folder sa svim fajlovima od kojih je sačinjen web projekat; uključuje izvorni kod i sve ostale resurse;
- **.gitignore** – fajl koji se koristi od strane git alata za verzionisanje, kako bi se naveli fajlovi i folderi koje ne treba pratiti;
- **xml** – glavni konfiguracioni fajl Maven sistema za izgradnju.

| **Fajl za konfigurisanje Maven projekta – POM**  Svi alati za izgradnju zahtevaju postojanje specijalnog fajla koji opisuje projekat i definiše načine za njegovu izgradnju. Kada je reč o Maven sistemu, takav fajl je **pom.xml**.  POM je skraćenica za **Project Object Model**. POM sadrži sve potrebne informacije o projektu na jednom mestu i tako olakšava pronalaženje zavisnosti koje su projektu potrebne za funkcionisanje.  S obzirom na to da je sadržaj POM fajla XML, unutar njega se mogu naći brojni XML elementi. Ipak, postoji određeni broj elemenata koji se moraju pojaviti unutar POM fajla:  - project – koreni element POM fajla; - modelVersion – verzija POM XML sintakse koju dokument koristi (4.0 je trenutno podržana POM verzija); - groupId – jedinstveni naziv paketa ili organizacije koja razvija projekat (obično naziv domena napisan naopako, tj. kao com.domain.name); - artifactId – naziv projekta koji će biti izgrađen; rezultat procesa izgradnje se kod Maven sistema naziva artefakt; najčešće je to JAR, WAR ili EAR fajl, ali može biti i nešto drugo; - version – broj verzije projekta; podrazumevano se ovo polje automatski određuje.  Upravo navedeni elementi čine minimalni POM koji Maven dozvoljava. Vrednosti tri elementa groupId, artifactId i version čine podatke kojima se projekat identifikuje u svom okruženju. |
| --- |

Nakon kratke priče o POM fajlu, nastavljamo upoznavanje sa strukturom Maven projekta kada je reč o razvoju Java web aplikacija. Odlazimo jedan korak dublje u projektnoj strukturi, pa tako prelazimo na folder src. Folder **src** je onaj unutar koga ćemo provoditi najviše vremena, zato što on sadrži fajlove sa resursima i izvornim kodom aplikacije. Unutar njega postoji sledeća struktura:

- **src/main/resources** – folder za smeštanje resursa projekta; resursima se smatraju svi fajlovi koji ne sadrže izvorni programski kod;
- **src/main/webapp** – folder koji sadrži sve javne fajlove jedne web aplikacije – html, css, js dokumenta; sve što se nalazi unutar webapp foldera jeste javno dostupno, osim sadržaja WEB-INF foldera;
- **src/main/webapp** **/** **WEB-INF** – folder u kome se nalaze fajlovi koji ne treba da budu javno dostupni; u zavisnosti od afiniteta programera, u ovom folderu se mogu naći fajlovi različitih tipova; njima se ne može pristupiti spolja, direktnim navođenjem URL adrese, kao što je to slučaj sa fajlovima iz foldera webapp; ipak, njih može da koristi aplikativna logika u procesu formiranja serverskog odgovora, što ćete imati prilike da vidite u nastavku ovog kursa;
- **src/main/webapp/** **WEB-INF** **/web.xml** – konfiguracioni fajl web aplikacije, takozvani deskriptor raspoređivanja (*deployment descriptor*); unutar ovog fajla se nalaze informacije na osnovu kojih će server znati kako da tretira određene delove aplikacije;
- **src/main/webapp/** **jsp** – dokument koji predstavlja Java seversku stranicu, odnosno JSP (Java Server Pages); ovaj dokument možete da doživite kao HTML dokument sa posebnim naprednim mogućnostima, zato što je unutar njega moguće kombinovati HTML i Java kod.

Upravo spomenuti JSP dokument za nas je najzanimljiviji u ovom trenutku, zato što sadrži kod sa porukom koju ćemo videti unutar web pregledača kada pokrenemo našu aplikaciju:

```java
<html>
 
<body>
 
<h2>Hello World!</h2>
 
</body>
 
</html>
```

  
Unutar index.jsp dokumenta trenutno se nalazi čist HTML kod sa jednim naslovom (h2) koji sadrži tekst *Hello World!*. To je poruka koja će biti vidljiva unutar web pregledača nakon pokretanja naše aplikacije. Ipak, kako bismo zaista i bili u stanju da takvu poruku vidimo unutar nekog pregledača, neophodno je obaviti nekoliko koraka:

- izgradnja projekta i dobijanje WAR fajla;
- pokretanje Java EE web servera;
- objavljivanje aplikacije na web serveru.

Ovim koracima biće posvećeni nastavak ove lekcije i kompletna naredna lekcija.  
  

### Izgradnja Maven projekta

Prvi korak koji će nam omogućiti da naša aplikacija postane aktivna jeste izgradnja projekta i dobijanje fajla unutar koga će biti zapakovana kompletna aplikacija. Proces izgradnje i pakovanja se obavlja korišćenjem Maven sistema uz koordinaciju razvojnog okruženja IntelliJ IDEA. Ipak, bitno je znati da IntelliJ IDEA podrazumevano koristi izvorni (sopstveni) alat za izgradnju. Iako je reč o alatu za izgradnju koji je posebno prilagođen i u većini slučajeva brži, pogotovu ukoliko je reč o projektu koji sadrži čist Java kod, mi ćemo se u nastavku odlučiti za delegiranje svih akcija izgradnje od strane IntelliJ okruženja do Maven sistema, posebno zato što želimo da se još bolje upoznamo sa korišćenjem Maven sistema. To je moguće uraditi otvaranjem **File** **\-> Settings -> Build, Execution, Deployment -> Build tools -> Maven -> Runner** stranice za podešavanja (slika 2.4).

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_04-novo.png)

*Slika 2.4. Opcija za delegiranje izgradnje do Maven sistema  
  
*

Na slici 2.4. možete da vidite opciju **Delegate IDE build/run actions to Maven**, koju je potrebno aktivirati.

Maven je moguće uposliti korišćenjem konzole/terminala, upućivanjem odgovarajućih komandi. Osnovna komanda jeste **mvn**, nakon koje se definišu opcije, zadaci i faze koje Maven sistem treba da sprovede. Kako bismo, na primer, dobili osnovne informacije o Maven sistemu, moguće je uputiti jednu ovakvu komandu:

mvn –v

Prikazana komanda se može uputiti pomoću konzole/terminala, dok je moguće iskoristiti i ugrađeni Terminal panel IntelliJ IDEA razvojnog okruženja (slika 2.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_05-novo.png)

*Slika 2.5. Komanda za čitanje verzije Maven sistema  
  
*

Na slici 2.5. možete videti Terminal panel unutar IntelliJ IDEA okruženja koji je iskorišćen za upućivanje komande mvn -v. Ipak, bitno je da razumete da za uspešno funkcionisanje primera sa slike 2.5 morate imati samostalno instaliran Maven na svom kompjuteru. Procedura instaliranja Mavena podrazumeva njegovo preuzimanje sa adrese [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi), zatim raspakivanje, a onda smeštanje unutar sistemske PATH promenljive, kako bi komanda mvn mogla da se koristi sa bilo koje lokacije.

Nešto ranije je rečeno da IntelliJ IDEA dolazi sa sopstvenim Maven alatom i u to se lako možete uveriti iz **File** **\-> Settings -> Build, Execution, Deployment -> Build tools -> Maven** stranice sa podešavanjima (slika 2.6).

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_06-novo.png)

*Slika 2.6. Podešavanje lokacije Maven sistema koji će koristiti IntelliJ IDEA  
  
*

Sa slike 2.6. lako je moguće videti da IntelliJ IDEA koristi sopstveni (*Bundled*) Maven sistem. Naravno, to je moguće promeniti, ali za takvim nečim sada nema potrebe.

Sledeće pitanje koje se postavlja jeste kako iskoristiti Maven koji je ugrađen unutar IntelliJ IDEA okruženja. Za obavljanje tog posla može se koristiti jedan poseban panel koji IntelliJ IDEA okruženja poseduje. Reč je o panelu Maven.

| **Maven panel unutar IntelliJ IDEA razvojnog okruženja**  Razvojno okruženje IntelliJ IDEA poseduje poseban panel koji je moguće koristiti za interakciju sa ugrađenim Maven sistemom. Taj panel se može dobiti aktiviranjem opcije **View ->** **Tool Windows ->** **Maven**. Sam Maven panel možete videti na slici 2.7.  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_07-novo.png)  *Slika 2.7. Maven panel unutar IntelliJ razvojnog okruženja      *  Maven panel poseduje brojne mogućnosti. On služi za pregled dostupnih Maven projekata, preuzimanje Javadoc dokumentacije, izvršavanje Maven ciljeva i faza... Svi Maven projekti su prikazani kao čvorovi stabla, sa podstavkama Lifecycle i Plugins i Dependencies.  Kako bismo dobili informaciju o verziji Maven sistema koji je ugrađen u sam IntelliJ IDEA, dovoljno je aktivirati opciju **Execute Maven Goal** (slika 2.8).  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_08-novo.png)  *Slika 2.8. Opcija Execute Maven Goal za izvršavanje Maven ciljeva      *  Nakon aktiviranja opcije *Execute Maven Goal* otvara se panel pomoću koga je moguće formulisati novu naredbu koja će biti upućena ugrađenom Maven sistemu (slika 2.9).  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_09-novo.png)  *Slika 2.9. Upućivanje nove komande ugrađenom Maven sistemu      *  Na ovaj način će biti prikazana verzija Maven sistema koju koristi IntelliJ IDEA okruženje. Rezultat je moguće videti unutar Run panela (slika 2.10).  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_10-novo.png)  *Slika 2.10. Pregled rezultata izvršavanja Maven komande za dobijanje njegove verzije* |
| --- |

Nakon upoznavanja sa Maven panelom IntelliJ IDEA razvojnog okruženja, možemo preći na ono što smo od samog početka hteli da uradimo. Naravno, to je proces izgradnje kompletnog projekta. Izgradnju je moguće obaviti na dosta načina, u zavisnosti do toga šta sve želimo da postignemo takvim procesom. Kako bismo na pravi način razumeli komande za izgradnju, neophodno je poznavati osnovne Maven pojmove kao što su životni ciklusi, ciljevi i dodaci.

| **Maven faze životnog ciklusa, ciljevi i dodaci (lifecycle phases, goals, plugins)**  Maven proces izgradnje sastavljen je iz faza koje čine jedan životni ciklus. Životni ciklus procesa izgradnje poseduje tačan broj unapred utvrđenih faza, složenih po posebnom hronološkom redosledu. Svaka faza sačinjena je iz jednog ili više ciljeva (*goals*), dok sami ciljevi pripadaju dodacima (*plugins*). Sve to možete videti na slici 2.11.  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_11-novo.png)  *Slika 2.11 – Maven faze životnih ciklusa, ciljevi i dodaci      *  Postoje tri životna ciklusa u okviru Mavena:  - clean - site - default  Životni ciklus **clean** je namenjen brisanju svega što je izgrađeno prethodnim procesom izgradnje. Sačinjen je iz sledećih faza:  - pre-clean - clean - post-clean  Životni ciklus **site** je namenjen generisanju dokumentacije i izveštaja i sačinjen je iz sledećih faza:  - pre-site - site - post-site - site-deploy  Za nas najznačajniji životni ciklus je svakako **default,** koji se koristi za izgradnju aplikacije. Sačinjen je iz sledećih faza:  - validate – proverava da li su sve potrebne informacije za izgradnju dostupne; - compile – kompajlira izvorni kod; - test – kompajlira izvorni kod jediničnih testova i pokreće ih; - package – pakuje izvorni kod i resurse u paket odgovarajućeg formata (jar, war…); - verify – proverava da li je paket validan i da li zadovoljava kriterijume kvaliteta; - install – instalira paket u lokalni repozitorijum; - deploy – kopira paket u neki udaljeni repozitorijum.  Maven omogućava direktno izvršavanje faza navedenih životnih ciklusa. Tako je moguće napisati:  mvn package  i biće izvršena package faza, ali i sve faze koje su navedene pre nje. To je veoma bitno zapamtiti – izvršavanje Maven faze uvek podrazumeva izvršavanje i svih faza koje se nalaze pre te faze unutar životnog ciklusa. Stoga će navedenom komandom biti obavljeni validiranje, kompajliranje, testiranje i pakovanje projekta.  Nešto ranije su spomenuti i Maven ciljevi (*goals*). Svaka od Maven faza sačinjena je iz ciljeva. Ciljevi su konkretni poslovi koje Maven obavlja tokom svog funkcionisanja. Tako postoji cilj clean, koji čisti prethodnu izgradnju, ili cilj war, koji obavlja generisanje WAR paketa.  Pored toga što Maven omogućava direktno izvršavanja faza životnog ciklusa (što ste mogli da vidite u prethodnim redovima), on takođe omogućava i direktno obavljanje pojedinačnih ciljeva. Na primer:  mvn war:war  Na ovaj način je izvršen war cilj koji je sastavni deo istoimenog Maven dodatka. Stoga je bitno zapamtiti da su ciljevi sastavni deo Maven dodataka (*plugins*). |
| --- |

Obe Maven komande prikazane u prethodnim redovima mogu se koristiti za dobijanje WAR paketa unutar koga će biti upakovana naša prva Java web aplikacija.

Prilikom izgradnje, strukturi Maven projekta se pridružuje još jedan folder, pod imenom **target**, koji sadrži prevedene klase, ali i pakete (JAR, WAR...) koje je Maven generisao.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_02_12-novo.png)

*Slika 2.12. Folder target koji se dobija nakon završene izgradnje  
  
*

U target folderu se nakon izgradnje i pakovanja aplikacije nalazi jedna WAR arhiva*.* Ime tog WAR fajla definisano je unutar POM fajla, i to kao vrednost <artifactId> elementa. U našem slučaju, to je naziv javaee\_demo. Naravno, da smo pokrenuli samo izgradnju, bez pakovanja, takva WAR arhiva ne bi ni bila kreirana.

U dosadašnjem toku ovoga kursa kreirali smo projekat sa prvom Java web aplikacijom i obavili njenu izgradnju i pakovanje. Došli smo do WAR fajla koji je moguće postaviti na neki od kompatibilnih web servera i na taj način aplikaciju učiniti dostupnom. Stoga je naš sledeći korak u ovom kursu da naučimo kako se uspostavljaju serveri koji će nam omogućiti da pokrenemo svoju aplikaciju.

U kom folderu se smeštaju javni fajlovi jedne Java web aplikacije koja se gradi korišćenjem Maven sistema?

  

## MULTIMEDIJA

---

[00:18:50 ![](https://multimedia.dizajn-akademija.com/sr/Java_Web_Application_Development/multimedijaFinal/JWAD1_02.thb) JWAD1\_02.mp4](https://www.link-elearning.com/linkdl/portal/?c=main&pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23# "JWAD1_02.mp4")

| [  Prethodna jedinica  ](https://www.link-elearning.com/linkdl/portal/index.php?pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23&IDJedinica=1434712&c=jedinice) | [  Sledeća jedinica  ](https://www.link-elearning.com/linkdl/portal/index.php?pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23&IDJedinica=1434714&c=jedinice) |
| --- | --- |

Kako Vam mogu pomoći?

[Scroll To Top](https://www.link-elearning.com/linkdl/portal/?c=main&pk=2f19cbe7e44adc181f83e99aa03c4cf6_ita_23#)