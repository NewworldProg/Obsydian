---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/portal/?pk=308084e345d485b3b03a12c2a822523a_ita_23#?pk=308084e345d485b3b03a12c2a822523a_ita_23&IDJedinica=1434712&c=jedinice"
author:
published:
created: 2025-06-08
description:
tags:
  - "clippings"
---
---

+ Rezime

### Uvod u Java EE

00:34:39

Jedinica: 1 od 17

U kursu koji je pred vama, moći ćete da se upoznate sa pristupima za razvoj web aplikacija korišćenjem programskog jezika Java. Kroz nekoliko logičkih celina (modula), imaćete prilike da čitate o različitim aspektima razvoja web aplikacija. Ipak, s obzirom na to da web razvoj predstavlja veoma kompleksnu oblast softverskog razvoja, na početku će biti neophodno definisati sam pojam web aplikacija.  
  

### Šta su web aplikacije?

Nekada, tokom prvih godina razvoja, na webu su postojali samo jednostavni web sajtovi. Oni su po svojim sposobnostima bili vrlo ograničeni, tako da su korisnicima omogućavali jednostavan uvid u različite vrste podataka. Prevashodno su to bili tekstualni podaci sa ponekom slikom, grafikom ili ilustracijom. Ipak, razvojem tehnologije, a prevashodno interneta, vremenom su web sajtovi postajali sve moćniji i kompleksniji, pa su korisnicima počeli da omogućavaju mnogo viši stepen interaktivnosti. Web sajtovi su postali mesta na kojima je moguće rezervisati kartu za let, obaviti kupovinu ili plaćanje, pogledati najnoviji film ili seriju, komunicirati sa drugim ljudima... Tako su web sajtovi lagano poprimali osobine pravih kompjuterskih programa, odnosno aplikacija. Stoga se danas veoma često može čuti termin *web aplikacija*.

Web aplikacije su zapravo web sajtovi čiji podaci nisu statični i koji po pravilu korisniku omogućavaju znatno viši stepen interaktivnosti. Društvene mreže su svakako jedan od primera web aplikacija. Svaki korisnik neke društvene mreže dobija različit, personalizovan sadržaj. Takođe, korisnik ima i mogućnost da na takav sadržaj utiče, odnosno da kreira novi ili menja postojeći.

Klasični primeri web aplikacija su i brojni poslovni sistemi koje koriste različite kompanije. Na primer, radnici u bankama na svojim poslovnim kompjuterima sasvim sigurno koriste neku vrstu web aplikacije koja im omogućava da obavljaju svakodnevne poslove.  
  

### Frontend i backend

U prvim godinama razvoja, web je prevashodno bio sačinjen iz jednostavnih, statičkih sajtova. Ipak, situacija se tokom godina rapidno menjala, tako da je danas veoma teško pronaći sajt koji je u potpunosti statičan, i kod koga barem neki delovi nemaju osobine web aplikacija.

Zbog rapidnih promena do kojih je godinama dolazilo na polju razvoja web sajtova, skovani su pojmovi: *frontend* i *backend* (često i: *front-end* i *back-end*).

Uprošćeno rečeno, frontend je pojam koji se odnosi na sve ono što korisnik vidi prilikom korišćenja nekog web sajta. Sa druge strane, pojam backend se odnosi na sve ono što je tokom funkcionisanja nekog web sajta skriveno od korisnika. Ove dve oblasti razvoja današnjih sajtova ilustrativno se mogu predstaviti kao na slici 1.1.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_01-novo.png)

*Slika 1.1. Frontend i backend  
  
*

Slika 1.1, kroz analogiju sa santom leda, uprošćeno dočarava razlike između frontend i backend razvoja. Na slici se onaj vidljivi deo sante poistovećuje se frontend slojem web aplikacija, a deo koji je skriven ispod površine vode sa backend slojem.

Kao primer koji nam može pomoći u boljem razumevanju frontend i backend delova, poslužiće društvena mreža Facebook. Sve ono što unutar svog web pregledača vidite dok koristite Facebook, može se nazvati prezentacionim, odnosno frontend delom Facebook web sajta. Međutim, kada na društvenoj mreži Facebook kreirate neki post, proces njegove objave u potpunosti je skriven od vas. Može se reći da se takav posao obavlja *iza kulisa*, pa samim tim pripada backend delu Facebook web aplikacije.

Ukoliko govorimo o jednom bankarskom sistemu, frontend bi predstavljao ono što zaposleni vidi na displeju kompjutera tokom obavljanja radnih zadataka. Sa druge strane, način na koji se u pozadini zaista obavlja prenos novca sa jednog računa na drugi, jedan je od klasičnih primera operacije koja se sprovodi u okviru backend sloja jedne web aplikacije.

Pojmovi frontend i backend poseduju i svoje odgovarajuće skupove tehnologija i jezika. Jezici HTML, CSS i JavaScript osnovni su alati frontend razvoja. Sa druge strane, kreiranje pozadinske logike web aplikacija može se obaviti korišćenjem različitih programskih jezika, kao što su C#, Java, PHP, Python itd. Pored jezika, backend veoma često podrazumeva i korišćenje različitih softverskih okvira i skupova tehnologija. Kada se govori o Java programiranju, to su tehnologije Java/Jakarta EE i softverski okviri Spring MVC, JSF, Google Web Toolkit i drugi.

| **Napomena**  Pored pojmova *frontend* i *backend*, postoji i pojam *full stack*. Full stack programer je osoba koja podjednako dobro poznaje i frontend i backend razvoj web aplikacija. |
| --- |

Web aplikacije sastavni su deo specifičnog internet servisa koji se naziva *web*, što je zapravo skraćenica za World Wide Web. Stoga je to naša sledeća tema.  
  

### Šta je World Wide Web?

Većina svakodnevnih, običnih korisnika internet poistovećuje sa pregledom web sadržaja. Ipak, kada otvorite neki od programa za pregled web sadržaja (Chrome, Firefox, Safari...), vi ste zapravo pristupili samo jednom od servisa koji postoji na internetu. Reč je o servisu koji se naziva World Wide Web (skraćeno **WWW** ili jednostavno **web**).

Bitno je razumeti da je internet mnogo više od pregleda sadržaja različitih sajtova, omiljenih društvenih mreža ili čitanja elektronskih vesti. Ipak, World Wide Web servis je uspeo da stekne status najpoznatijeg i najkorišćenijeg servisa čije postojanje je direktno uslovljeno postojanjem svetske globalne mreže – interneta.

World Wide Web se definiše kao skup dokumenata (resursa), pri čemu je svaki takav dokument identifikovan korišćenjem specijalne adrese. Svi takvi dokumenti su međusobno povezani vezama koje se nazivaju hiperlinkovi i dostupni preko interneta.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_02-novo.png)

*Slika 1.2. World Wide Web  
  
*

Za pregled dokumenata WWW servisa, koriste se specijalni programi koji se nazivaju web pregledači (*web browser*).

Tvorac weba je Tim Berners-Lee, koji je 1989. godine, radeći u organizaciji CERN, kreirao prvi dokument kojim je predstavio ideju o novom internet servisu. Tim Berners-Lee je 1990. godine napisao i prvi web pregledač i tako postavio temelje daljeg razvoja WWW servisa.

Svoje funkcionisanje WWW servis direktno zasniva na HTTP, odnosno HTTPS protokolima. Zbog toga je za adekvatno razumevanje WWW-a neophodno razumeti osnovna pravila HTTP protokola.  
  

### Šta je HTTP?

WWW i HTTP protokol su nerazdvojivi pojmovi. Jednostavno, HTTP protokol razvijen je specijalno za potrebe WWW servisa, što znači da web ne bi postojao bez ovog protokola. Dalje, WWW i HTTP imaju identičnog tvorca. Radeći na novom internet servisu (WWW), Tim Berners-Lee i njegov tim kreirali su i osnovne nacrte HTTP protokola.

HTTP je jedan od protokola aplikativnog sloja internet modela. To praktično znači da je reč o protokolu najvišeg nivoa, koji korisnici direktno upošljavaju. Da je to tako, verovatno ste i sami već primetili, korišćenjem nekog web pregledača. Jednostavno, prilikom posete nekog web sajta, verovatno ste primetili da adresa sajta započinje sa http ili https:

https://www.google.com/

Upravo je prikazana adresa jednog od najpopularnijih sajtova današnjice. Možete da primetite da ona započinje odrednicom https, što govori da se za komunikaciju koristi HTTP odnosno HTTPS protokol (u suštini je reč o istom protokolu, pri čemu HTTPS predstavlja sigurniju verziju HTTP protokola; sve što u nastavku bude rečeno odnosi se na obe varijante protokola).

HTTP je takozvani **request–response** protokol, što znači da njegov način funkcionisanja počiva na međusobnom smenjivanju zahteva i odgovora između dva kompjutera. Pri tome, dva kompjutera koja komuniciraju korišćenjem HTTP protokola nisu ravnopravna, već se jedan naziva **server**, a drugi **klijent**. Klijentski kompjuter je onaj sa koga je korišćenjem nekog web pregledača upućen zahtev. Server je kompjuter koji takav zahtev prihvata, obrađuje i na kraju odgovara isporukom određene poruke ili resursa.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_03-novo.png)

*Slika 1.3. Klijent–server komunikacija  
  
*

Slika 1.3. ilustruje uprošćenu komunikaciju između klijenta i servera posredstvom HTTP protokola. Sliku možete poistovetiti sa svakodnevnim korišćenjem weba. Na primer, prilikom otvaranja nekog web sajta, korišćenjem web pregledača (npr. Chromea), vaš kompjuter se ponaša kao HTTP klijent. Kompjuter na kome se nalazi sajt kome pokušavate da pristupite naziva se HTTP server.

HTTP klijent se serveru obraća pomoću obrasca koji se naziva HTTP zahtev, dok server njemu uzvraća odgovor, koji se drugačije naziva HTTP odgovor. Smenjivanje HTTP zahteva i odgovora osnova je komunikacije između klijenata i servera na webu.

Kada je reč o web aplikacijama, klijenti i serveri su primarne pozornice za izvršavanje aplikativnog koda. Kod koji se izvršava na klijentu se naziva klijentski kod, dok je serverski kod onaj koji se izvršava na serveru.

Kada pristigne zahtev od klijenta, server analizira njegovo zaglavlje i čita adresu traženog dokumenta. Server pronalazi traženi dokument, a zatim utvrđuje da li unutar njega postoji neki serverski kod. Ukoliko postoji, dokument se prosleđuje Java virtuelnoj mašini, koja izvršava serverski kod, a zatim rezultat prosleđuje klijentu. Ukoliko unutar traženog dokumenta nema serverskog koda, može se konstatovati da je reč o statičkom resursu koji se direktno prosleđuje klijentu.  
  

### Resursi na webu

Kao što i sami znate, web je preplavljen sadržajem različitih vrsta. Tekst, slike, audio i video zapisi i razni dokumenti su samo neki od sadržaja koji se nalaze na webu. Svi oni se objedinjeno nazivaju *resursi*. To praktično znači da kada npr. pokušavate da pogledate neki snimak sa YouTubea, vi zapravo upućujete zahtev za pristup određenom web resursu. U opisanoj situaciji, taj resurs je video-zapis.

Svi resursi na webu su jednoznačno određeni specijalnim adresama. Takve adrese omogućavaju razlikovanje resursa, a korisnicima obezbeđuju sistem za pristup. Recimo, https://www.google.com jeste primer jedne adrese web resursa.

| **Uniform Resource Locator (URL)**  Adresa jednog web resursa se drugačija naziva *Uniform Resource Locator* ili skraćeno URL. Prosto rečeno, URL je ono što kucate u web pregledaču kada pokušavate da pristupite nekom sajtu. Po svojoj strukturi, URL je hijerarhijska sekvenca komponenata (slika 1.4).  ![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_04-novo.png)  *Slika 1.4. Struktura URL adrese      *  Slika 1.4. ilustruje različite delove od kojih može biti sačinjen jedan URL:  - **scheme –** naziv protokola koji se koristi za komunikaciju; - **fully qualified domain name (FQDN) –** definiše preciznu lokaciju kompjutera (hosta) unutar mreže; - **port number –** oznaka koja definiše određeni proces ili servis koji se izvršava na kompjuteru povezanom na mrežu; - **path –** putanja do određenog resursa na serverskom računaru; - **resource –** naziv resursa koji se od servera zahteva; - **query string –** opcioni parametri koji se u formi parova ključeva i vrednosti mogu proslediti serveru.  Određeni delovi URL-a su opcioni. Tako je potpuno legitimno napisati samo:  http://www.mysite.com  ili:  https://www.google.com  Obe prikazane URL adrese potpuno su legitimne, dok se preostali delovi URL-a koji su prikazani slikom 1.4 mogu koristiti kada se za tim javi potreba, kako bi se pristupilo specifičnom resursu unutar nekog hosta. |
| --- |

Prethodne redove smo iskoristili kako bismo napravili uvertiru za priču koja će uslediti u nastavku, a koja u ovom trenutku nas najviše zanima. Stoga ćemo u nastavku pokušati da odgovorimo na pitanje kako se u svetu Java programiranja obavlja kreiranje web aplikacija. Prvi pojam do koga u takvoj situaciji dolazimo jeste Java EE.

### Šta je Java EE?

Priča o Java web programiranju jeste zapravo priča o Java EE specifikaciji. *Java Enterprise Edition* (skraćeno *Java EE*; nekada se koristilo i *J2EE* ili *Java 2 Enterprise Edition*) jeste skup specifikacija namenjenih serverskom Java programiranju.

Iz naziva Java EE specifikacije stiče se utisak da je reč o tehnologijama namenjenim za razvoj poslovnih (*enterprise*) aplikacija. Za početak je potrebno razjasniti šta predstavlja pojam poslovnih aplikacija.

| **Šta su poslovne (enterprise) aplikacije?**  Pojam poslovnih aplikacija je prilično rastegljiv i podložan subjektivnim interpretacijama. Ipak, može se reći da su poslovne aplikacije one koje se koriste u okviru velikih organizacija. Takvim tipom aplikacija omogućavaju se tipični poslovno orijentisani servisi, kao što su: online kupovina, plaćanje preko interneta, vođenje poslovanja, izveštavanje, praćenje, interaktivni katalozi i slično.  Za razliku od jednokorisničkih aplikacija, koje se izvršavaju isključivo na korisničkom računaru, poslovne aplikacije se izvršavaju na serveru i istovremeno uslužuju veliki broj korisnika. Zbog toga su poslovne aplikacije gotovo uvek i distribuirane, što znači da se izvršavaju na većem broj kompjutera.  Neke od najvećih kompanija koje se bave razvojem poslovnih aplikacija su IBM, Oracle Corporation, Microsoft Corporation, Adobe Systems, SAP, Salesforce...  Poslovne aplikacije nisu samo one koje koriste velike korporacije, agencije i vlade. Danas, u sve umreženijem svetu, poslovne aplikacije su neophodne i manjim organizacijama, a nekada čak i pojedincima. |
| --- |

Iako se pri definisanju Java EE specifikacije koristi pojam *poslovne aplikacije*, bitno je razumeti da je reč više o marketinškom nazivu koji nije potrebno doživeti kao određujući faktor. Tako je Java EE moguće upotrebiti za razvoj bilo kog tipa aplikacija, bilo da je reč o zabavnom, poslovnom, edukativnom ili nekom drugom tipu softvera.

Do sada je više puta rečeno da je Java EE *specifikacija*. To praktično znači da Java EE samo propisuje i utvrđuje načine na koje je potrebno da funkcionišu različite komponente web aplikacija napisanih programskim jezikom Java. S obzirom na to da je reč o specifikaciji, njom se definišu brojni aspekti funkcionisanja web aplikacija: obrada zahteva, validacija, parsiranje, transakcije, povezivanje...

| **Zbog čega nam je potreban Java EE?**  Iz uvodnih kurseva u kojima je obrađivan Java SE, već znate da, kada se javi potreba za kolekcijom podataka, u najvećem broju slučajeva nećemo pribeći kreiranju sopstvenog tipa podataka, već ćemo koristiti neku postojeću Java kolekcija (ArrayList, npr.). Na isti način, kada je potrebno napraviti sigurnu, robusnu, distribuiranu web aplikaciju, nećemo bespotrebno pisati funkcionalnosti niskog nivoa, već ćemo jednostavno upotrebiti Java EE.  Baš kao što Java SE poseduje funkcionalnosti za rad sa kolekcijama, tako i Java EE poseduje funkcionalnosti i specifikacije za rad sa transakcijama, servisnim porukama, skladištima i perzistentnim objektima, web servisima, tj. svim onim što može da bude potrebno jednoj web aplikaciji kako bi odgovorila na širok spektar zahteva. |
| --- |

### Razvoj Java EE

Java EE je tokom godina prošla kroz veliki broj iteracija. Svako novo izdanje Java jezika pratilo je i predstavljanje nove Jave EE verzije. Ranije verzije Java EE tehnologije karakterisale su velika kompleksnost i obaveza korišćenja komplikovanih šablona za definisanje klasa. Danas je Java EE dobro dokumentovana platforma sa velikom zajednicom iskusnih programera i velikim brojem realizovanih aplikacija različitog tipa.

U septembru 2017. godine, Oracle je odlučio da ustupi prava na korišćenje Java EE tehnologije fondaciji Eclipse. Ipak, programski jezik Java kao brend je i dalje ostao u vlasništvu Oraclea. Zbog toga je Eclipse fondacija morala da preimenuje Java EE, kako bi izbegla komplikacije u vezi sa korišćenjem imena Java, nad kojim nema prava. Kao novo ime zajednica je izabrala **Jakarta EE**. U nastavku ovog kursa, potpuno ravnopravno ćemo koristiti nazive Java EE i Jakarta EE, kao sinonime.  
  

### Od čega se sastoji Java EE?

Za Java EE se kaže da je *skup specifikacija*, zato što u svom sastavu objedinjuje veliki broj pojedinačnih specifikacija, namenjenih rešavanju izolovanih problema prilikom kreiranja web aplikacija. Najznačajnije takve specifikacije su:

- **Jakarta Servlet** – specifikacija za implementiranje Java klasa koje mogu da odgovaraju na klijentske zahteve upućene posredstvom HTTP protokola;
- **Jakarta Server Pages (JSP)** – specifikacija za generisanje dinamičkog HTML sadržaja korišćenjem Java programskog koda;
- **Jakarta Standard Tag Library (JSTL)** – specifikacija koja proširuje HTML jezik, uvođenjem dodatnih tagova koje je moguće koristiti u okviru JSP stranica;
- **Jakarta Faces (JSF)** – specifikacija za kreiranje korisničkih okruženja Java web aplikacija, koja su sačinjena iz komponenata;
- **Jakarta Expression Language (EL)** – specifikacija koja opisuje poseban programski jezik kojim je moguće obaviti umetanje i izvršavanje izraza unutar web stranica;
- **Jakarta Enterprise Beans (EJB)** – specifikacija za kreiranje komponenata kojima se modeluju entiteti, odnosno poslovna aplikativna logika;
- **Jakarta Persistence (JPA)** – specifikacija koja definiše način upravljanja relacionim podacima u okviru Java web aplikacija;
- **Jakarta Transactions (JTA)** – specifikacija koja opisuje način realizacije transakcija, odnosno nedeljivih celina sačinjenih iz više operacija koje se moraju završiti uspešno (*commit*) ili se ne izvršiti uopšte (*rollback*);
- **Jakarta Contexts and Dependency Injection (CDI)** – specifikacija koja definiše način realizacije DI (*dependency injection*) softverskog šablona.

Navedene Jakarta EE specifikacije ćemo aktivno koristiti u procesu kreiranja Java web aplikacija u lekcijama koje slede.  
  

### Troslojna softverska arhitektura i Java EE

Svetom softverskog razvoja dominira troslojna softverska arhitektura. Reč je o načinu na koji se jedan softverski proizvod strukturira i organizuje. Svaki sloj jednog softverskog sistema predstavlja izolovano, funkcionalno područje. Više slojeva međusobnom komunikacijom čine sistem funkcionalnim.

Troslojna softverska arhitektura podrazumeva klijentski sloj, srednji sloj i sloj podataka. Klijentski sloj šalje zahteve srednjem sloju. Srednji sloj obrađuje zahteve klijenata i rukuje podacima koje trajno čuva na trećem sloju, sloju podataka.

Troslojna softverska arhitektura je posebno značajna i za web razvoj, zato što gotovo svaka web aplikacija poseduje upravo tri sloja. Izuzetak nisu ni Java web aplikacije (slika 1.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_05-novo.png)

*Slika 1.5. Troslojna struktura Java/Jakarta EE aplikacija  
  
*

Na slici. 1.5 možete videti tri sloja u arhitekturi aplikacija koje se kreiraju korišćenjem Java EE tehnologije. Prvi sloj je sloj prezentacije i to su zapravo web stranice koje se prikazuju korisnicima. Na drugom sloju se nalazi Java EE server, dok je treći sloj – sloj podataka ili sloj servera baze podataka. Komponente klijentskog sloja funkcionišu na klijentskim mašinama, komponente srednjeg sloja na Java/Jakarta EE serveru, dok se podaci nalaze na serveru baza podataka.

Java EE se odnosi primarno na srednji sloj, ali jedna od Java EE specifikacija omogućava da se i klijentski sloj takvih aplikacija realizuje korišćenjem Java EE tehnologije. Jedan kompletan modul ovoga kursa biće posvećen klijentskom programiranju, pa ćete tako nešto imati prilike da vidite i na praktičnim primerima.

U nastavku ćemo posebno razmotriti svaki od tri upravo ilustrovana sloja troslojne softverske arhitekture iz ugla Java web programiranja.

**Klijentski sloj**

Klijentski sloj (*client tier*) često se naziva i prezentacioni sloj. To je deo aplikacije koji omogućava korisnicima interakciju sa sistemom.

Svaki server zahteva postojanje [klijenta](https://www.link-elearning.com/linkdl/opisPojma.php?id=161727 "klijenta") koji opravdava njegovo postojanje, pa je tako i sa Java web aplikacijama. Klijentski sloj je gotovo uvek krajnja tačka izvršavanja web aplikacije. On sadrži logiku koja je u stanju da pošalje zahtev serveru i da preuzme i adekvatno pročita odgovor. Web pregledači (Mozilla, Chrome, Internet Explorer, Opera, Safari, Edge...) najčešći su oblik klijentskih web aplikacija, ali krajnji korisnici web aplikacija ne moraju obavezno biti web pregledači, već to može biti i bilo koja aplikacija koja tokom svog izvršavanja obavlja komunikaciju sa web serverom.

**Srednji sloj**

Srednji sloj troslojne softverske arhitekture sadrži logiku za obradu web zahteva i rukovanje modelom podataka. Centralna figura takvog sloja jeste server koji je u mogućnosti da prihvati zahteve klijenata i da formira odgovor.

Server je program koji preuzima i obrađuje klijentske zahteve, a zatim, na osnovu parametara iz takvih zahteva, kreira odgovarajuće odgovore. Danas postoji nekoliko dominantnih web servera. Jedan od njih je [Microsoft Internet Information Services](https://www.link-elearning.com/linkdl/opisPojma.php?id=161728 "Microsoft Internet Information Services") (IIS). Takva aplikacija funkcioniše na Windows operativnim sistemima, i iako je u stanju da opslužuje različite tehnologije, najčešće se koristi za opsluživanje Microsoft web tehnologija ([ASP.NET](https://www.link-elearning.com/linkdl/opisPojma.php?id=161729 "ASP.NET")).

Druga veoma popularna web server aplikacija je [Apache](https://www.link-elearning.com/linkdl/opisPojma.php?id=161730 "Apache") web server, čije je prirodno okruženje [Linux](https://www.link-elearning.com/linkdl/opisPojma.php?id=161731 "Linux") operativni sistem. Za razliku od IIS-a, Apache postoji u verzijama za različite operativne sisteme, pa tako i za Windows. Ipak, najbolje rezultate Apache web server daje baš na Linux platformi.

Java web serveri se najčešće zasnivaju na Apache derivatima, ali mogu počivati i na drugim komercijalnim, besplatnim serverima otvorenog koda kao što su [Apache Tomcat](https://www.link-elearning.com/linkdl/opisPojma.php?id=161732 "Apache Tomcat"), [WildFly](https://www.link-elearning.com/linkdl/opisPojma.php?id=161734 "WildFly"), [Apache Geronimo](https://www.link-elearning.com/linkdl/opisPojma.php?id=161735 "Apache Geronimo"), [GlassFish](https://www.link-elearning.com/linkdl/opisPojma.php?id=161733 "GlassFish"), JBoss, Apache TomEE, Jetty... U nastavku našeg rada koristićemo Tomcat i TomEE web servere.

**Sloj podataka**

Sloj podataka jeste sloj koji se koristi za rukovanje podacima koje aplikacija koristi i skladištenje tih podataka. Za obavljanje takvog posla koristi se još jedan tip servera, odnosno sistema za rukovanje podacima. Serveri za rukovanje podacima obično se nalaze na mašini odvojenoj od aplikativnog servera i pristupaju im komponente poslovnog sloja. U produkcionim uslovima, najčešće je u upotrebi [MySQL](https://www.link-elearning.com/linkdl/opisPojma.php?id=161736 "MySQL") server baze podataka. Upravo zbog toga ćemo i mi u ovom kursu koristiti MySQL server za čuvanje podataka Java web aplikacija koje ćemo kreirati.  
  

### Arhitektura Java EE aplikacija

Java EE aplikacije podrazumevaju specifično okruženje izvršavanja. Razumevanje takvog okruženja je od presudne važnosti za uspešno praćenje lekcija koje slede. Osnovna arhitektura na kojoj počivaju Java EE aplikacije ilustrovana je slikom 1.6.

![](https://www.link-elearning.com/linkdl/coursefiles/1523/JWAD1_01_06-novo.png)

*Slika 1.6. Arhitektura Java EE aplikacija  
  
*

Na slici 1.6. možete videti da su osnovni gradivni elementi Java EE aplikacija, počevši od onih najnižih, sledeći:

- Java/Jakarta EE komponente;
- Java/Jakarta EE kontejneri;
- Java/Jakarta EE servisi.

Java/Jakarta EE komponente su samostalne, funkcionalne softverske jedinice od kojih su sačinjene Java EE aplikacije. Svaka komponenta za svoje funkcionisanje zahteva odgovarajući kontejner, koji komponentama stavlja na raspolaganje određene servise. U nastavku ćemo se pozabaviti svakom od tri upravo spomenute grupe Jakarta EE gradivnih elemenata.

**Jakarta EE komponente**

Java EE aplikacije se sastoje od komponenata. Komponenta je samostalna funkcionalna softverska jedinica koja obavlja određeni posao i tom prilikom može da komunicira i sa drugim aplikativnim komponentama. U svetu Java web razvoja postoji nekoliko vrsta takvih komponenata:

- **Servleti** – obrađuju HTTP zahteve i formiraju odgovor;
- **JavaServer Pages (JSPs)** – omogućava formiranje dinamičkog sadržaja kombinovanjem koda opisnog jezika kao što je HTML sa kodom programskog jezika Java;
- **Enterprise JavaBeans (EJBs)** – koriste se za modelovanje podataka unutar poslovnog sloja aplikacije;
- **Java Persistence API (JPA)** – predstavljaju sponu između objekata kojima se modeluju podaci i skladišta u kojima se podaci čuvaju;
- **Jakarta Faces** – omogućavaju kreiranje korisničkih okruženja web aplikacija baziranih na komponentama
- ...

**Jakarta EE kontejneri**

Jakarta EE kontejneri su celine koje upravo spomenutim komponentama obezbeđuju okruženje za izvršavanje, stavljanjem na raspolaganje različitih servisa. Takvi servisi mogu biti upravljanje bezbednošću, pristup bazi podataka, upravljanje transakcijama, rukovanje imenovanjem, ubrizgavanje zavisnosti... Na taj način kontejneri smanjuju kompleksnost, tako što skrivaju – ili, bolje reći, enkapsuliraju – logiku kojom se obavljaju neke uobičajene stvari u životu komponenata.

Postoje dve osnovne vrste kontejnera:

- **web kontejneri** (*web containers*) – obezbeđuju servise za upravljanje web komponentama i njihovo izvršavanje; ova vrsta kontejnera je odgovorna za instanciranje, inicijalizovanje i pozivanje servleta i opsluživanje HTTP i HTTPS zahteva, formiranjem odgovara koji se isporučuju klijentima;
- **EJB kontejneri** (*Jakarta Enterprise Bean containers*) – kontejneri odgovorni za rukovanje EJB komponentama koje sadrže logiku poslovnog sloja Jakarta EE aplikacije i njihovo izvršavanje; ova vrsta kontejnera je odgovorna za instanciranje EJB-ova, rukovanje njihovim životnim tokom i omogućavanje servisa za pomenute komponente.

### Jakarta servisi

Jakarta kontejneri omogućavaju komponentama da funkcionišu i izlažu im na korišćenje različite servise u zavisnosti od svog tipa. Servisi su nešto što postoji na nivou implementacije, odnosno samog servera, a web aplikacijama se stavljaju na raspolaganje posredstvom komponenata. Takvi servisi, između ostalog, komponentama omogućavaju da obavljaju sledeće:

- obrada HTTP zahteva;
- ubacivanje zavisnosti (*dependency injection*);
- upravljanje bezbednošću;
- rukovanje transakcijama;
- obrada JSON podataka;
- validacija podataka;
- obezbeđivanje sistema za razmenu poruka po modelu pretplatnik/izdavač (*subscriber/publisher*);
- perzistencija relacionih podataka.

Svaki servis koji kontejneri poseduju je prilagodljiv, što praktično znači da ga je moguće konfigurisati u zavisnosti od komponente koja ga koristi. Tako dve različite komponente mogu da koriste jedan isti servis, ali na potpuno različite načine, što ponovnu upotrebljivost podiže na najviši nivo.

Različiti serveri podržavaju različitu količinu servisa definisanih Jakarta EE specifikacijom. Zbog toga postoje tri grupe servisa, koje se drugačije nazivaju profili:

- **Core Profile** – skup sa najmanjom količinom servisa; reč je o profilu koji je namenjen razvoju aplikacija za cloud, pa zbog toga poseduje servise za rad sa [REST servisima](https://www.link-elearning.com/linkdl/opisPojma.php?id=171190 "REST servisima"), [JSON](https://www.link-elearning.com/linkdl/opisPojma.php?id=171191 "JSON") formatom i DI šablonom;
- **Web Profile** – profil koji nadograđuje Core Profile; namenjen je razvoju modernih web aplikacija, kojima uglavnom nisu potrebni svi servisi koji postoje unutar pune Jakarta EE specifikacije;
- **Full Platform** – profil koji podrazumeva kompletan skup Java EE specifikacija.

Kao što je rečeno, količina podržanih servisa direktno zavisi od implementacije, odnosno od konkretnih servera. Apache TomEE, jedan od servera koji ćemo koristiti u nastavku ovog kursa, podržava *Web Profile* skup funkcionalnosti.

Onoga trenutka kada se javi potreba za nekim od servisa koji prevazilaze *Web Profile*, neophodno je pribeći korišćenju servera koji tako nešto podržavaju. Takvi serveri nose oznaku *Jakarta EE Full platform compliant* i neki od njih su Eclipse GlassFish, JBoss, WildFly...  
  

### Objavljivanje Java EE aplikacija

Java web aplikacije postoje u okviru web kontejnera koje obezbeđuju konkretni serveri. Upravo zbog toga, pre nego što izvršavanje Java web aplikacije postane moguće, nju je neophodno smestiti na odgovarajući način unutar web servera. Java web aplikacija se mora smestiti na tačno definisano mesto u okviru web servera i njen format mora biti odgovarajući.

Java Web aplikacije pakuju se unutar posebne vrste arhivnog fajla, baš kao što je to slučaj i sa običnim Java aplikacijama. Ipak, svet Java web razvoja poznaje i dva dodatna takva formata, pa tako dolazimo do ukupno tri formata koja se mogu koristiti za pakovanje Java web aplikacija:

- Java Archive (JAR);
- Web Archive (WAR);
- Enterprise Archive (EAR).

U sva tri slučaja reč je fajlovima klasičnog .zip formata. Jednostavno, ukoliko bilo kom od navedenih fajlova promenite ekstenziju u .zip, bićete u mogućnosti da njegov sadržaj pregledate korišćenjem bilo kog programa za rad sa arhivama.

Proces izgradnje Java web aplikacije kao svoj finalni proizvod podrazumeva dobijanje jednog fajla, koji ima neki od upravo navedenih formata. Unutar takvog fajla objedinjuje se sve ono što je jednoj Java web aplikaciji potrebno za funkcionisanje u okviru nekog servera.

Tip fajla koji će biti korišćen za objavljivanje Java web aplikacije zavisi isključivo od web servera na kome će objavljivanje biti obavljeno. Većina servera podržava WAR fajlove, i uglavnom je to format koji se koristi kada se aplikacija objavljuje u okviru web servera koji podržava *Web Profile* skup funkcionalnosti.

Jakarta EE Full Profile web servis koristi EAR (Enterprise Archive) format, dok JAR arhive upotrebljavaju neki eksterni softverski okviri, kao što je Spring MVC.  
  

### Softverski okviri za razvoj Java web aplikacija

Bitno je razumeti da korišćenje Java/Jakarta EE funkcionalnosti nije jedini način za kreiranje Java web aplikacija. S obzirom na to da su ranije verzije Java EE specifikacije bile karakteristične po vrlo visokom nivou kompleksnosti, tokom vremena su razvijeni brojni softverski okviri otvorenog koda, kako bi se pojednostavio razvoj Java web aplikacija.

| **Šta su softverski okviri?**  Softverski okviri (*frameworks*) su veliki delovi unapred napisanog koda kojima dodajemo sopstveni kod kako bismo rešili neki problem. Korišćenje softverskih okvira podrazumeva pozivanje njihovih metoda, nasleđivanje unapred kreiranih tipova, korišćenje *callback objekata* i slušalaca događaja koji su sastavni deo softverskog okvira koji se koristi. Softverski okviri vrlo često diktiraju strukturu aplikacije i upravo zbog toga se i zovu softverski *okviri* – oni na neki način ukalupljuju i standardizuju posao razvoja softvera. |
| --- |

Softverski okviri se koriste kako bi se olakšao razvoj aplikacija. Identično važi i za softverske okvire koji se koriste u svetu Java programiranja. Neki od najkorišćenijih takvih okvira su: Spring MVC, JSF, Vaadin, Google Web Toolkit, Grails, Play 3, Apache Struts 1, Apache Struts 2... Svakako najpopularniji softverski okvir namenjen razvoju Java web aplikacija jeste Spring MVC i upravo zbog toga će on biti detaljno obrađen tokom trajanja ovoga kursa. Jedan kompletan modul u ovom kursu biće posvećen baš tom softverskom okviru.  
  

### Zaključak

U prethodnim redovima imali ste prilike da naučite šta je Java odnosno Jakarta EE i na koje načine je moguće razvijati web aplikacije posredstvom Java jezika. Sada preostaje da ono što smo ispričali pretočimo u praksu. Stoga ćemo već u narednoj lekciji započeti sa kreiranjem svoje prve Java web aplikacije. U tom poslu ćemo koristiti IntelliJ IDEA razvojno okruženje. Odmah nakon kreiranja prve aplikacije, nju ćemo pokušati i da pokrenemo, za šta će nam biti neophodan neki od web servera. U nastavku će biti ilustrovano uspostavljanje dva takva servera – Apache Tomcat i Apache TomEE. Nastavak kursa biće posvećen najznačajnijim Jakarta EE funkcionalnostima, Spring MVC softverskom okviru i različitim pristupima za kreiranje klijentskih komponenata Java web aplikacija.

U jednoj web aplikaciji, na kojem sloju se nalaze dinamičke HTML stranice?

  

## MULTIMEDIJA

---

[00:22:32 ![](https://multimedia.dizajn-akademija.com/sr/Java_Web_Application_Development/multimedijaFinal/JWAD1_01.thb) JWAD1\_01.mp4](https://www.link-elearning.com/linkdl/portal/?pk=308084e345d485b3b03a12c2a822523a_ita_23# "JWAD1_01.mp4")

| Prethodna jedinica | [  Sledeća jedinica  ](https://www.link-elearning.com/linkdl/portal/index.php?pk=308084e345d485b3b03a12c2a822523a_ita_23&IDJedinica=1434713&c=jedinice) |
| --- | --- |

Kako Vam mogu pomoći?

[Scroll To Top](https://www.link-elearning.com/linkdl/portal/?pk=308084e345d485b3b03a12c2a822523a_ita_23#)