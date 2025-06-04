---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=922e2e4b7bf10954b111ef3113959a14_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434673"
author:
published:
created: 2025-04-25
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 6 od 22

## IntelliJ IDEA

Prethodna lekcija je bila posvećena pisanju, prevođenju i pokretanju jednog Java programa korišćenjem osnovnih pristupa koji podrazumevaju direktnu upotrebu alata koji se nalaze unutar preuzetog JDK-a. Pri tome je ==za pisanje koda korišćen najjednostavniji tekst editor. Ipak, u praksi se za razvoj Java programa koriste specijalizovani alati== koji se drugačije nazivaju razvojna okruženja. Na početku smo se upoznali sa bazičnim pristupima za pisanje, prevođenje i pokretanje, kako biste razumeli kako Java funkcioniše na osnovnom nivou. ==Lekcija pred vama biće posvećena razvojnim okruženjima.==  
  

### Pojam razvojnog okruženja

Razvojno okruženje je ==program koji je specijalno namenjen za razvoj drugih programa==. To ne moraju biti Java programi, pa tako postoji veliki broj različitih razvojnih okruženja koja je moguće koristiti za pisanje programa korišćenjem različitih programskih jezika. Neka razvojna okruženja omogućavaju kreiranje programa korišćenjem jednog jezika, dok druga omogućavaju upotrebu većeg broja programskih jezika.

Razvojna okruženja obezbeđuju brojne pogodnosti prilikom pisanja programa. Ona ne olakšavaju samo pisanje izvornog koda već i sve ostale aspekte razvoja. To praktično znači da je ==korišćenjem razvojnog okruženja moguće obaviti sve one operacije koje smo u prethodnoj lekciji obavili korišćenjem Notepada i direktnom upotrebom javac i java alata kroz konzolu.==

Kada je reč o programskom jeziku Java, postoji nekoliko popularnih razvojnih okruženja koja su ==u širokoj upotrebi: **NetBeans**, **Eclipse** i **IntelliJ IDEA==****.** Sva tri razvojna okruženja napisana su korišćenjem Java programskog jezika. Poslednjih godina, posebno kod profesionalnih razvojnih timova, ==prednost ima razvojno okruženje IntelliJ IDEA==. To praktično znači da postoje velike šanse da u budućnosti, na vašoj prvoj radnoj poziciji, koristite upravo IntelliJ IDEA razvojno okruženje. Upravo zbog toga smo se i mi odlučili da u ovom kursu koristimo spomenuto razvojno okruženje.  
  

### IntelliJ IDEA

IntelliJ IDEA je razvojno okruženje koje je kreirala češka kompanija JetBrains, 2001. godine. Reč je o kompaniji specijalizovanoj za kreiranje razvojnih okruženja. IntelliJ IDEA bilo je prvo razvojno okruženje ove kompanije, na čijim osnovama su nastala i brojna druga razvojna okruženja, namenjena korišćenju ostalih popularnih programskih jezika i tehnologija. IntelliJ IDEA ==iskoristila je i kompanija Google za kreiranje svog razvojnog okruženja Android Studio.==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_01.png)

*Slika 6.1. IntelliJ IDEA logo (izvor:* *[https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/\)))*[  
  
](https://www.jetbrains.com/idea/\))

IntelliJ IDEA je razvojno okruženje primarno namenjeno za razvoj programa ==korišćenjem Java programskog jezika, ali opciono i drugih jezika koji za svoje izvršavanje koriste Java virtuelnu mašinu (Groovy, Kotlin, Scala...).==

IntelliJ IDEA postoji u dve varijante:

- komercijalnoj, koja nosi naziv IntelliJ IDEA Ultimate;
- besplatnoj, koja je otvorenog koda i nosi naziv IntelliJ IDEA Community.

Mi ćemo u ovom kursu koristiti **IntelliJ IDEA Community** ediciju, čija upotreba je moguća na Windows, macOS i Linux operativnim sistemima, bez ikakve naknade.

Besplatna, open-source verzija IntelliJ IDEA razvojnog okruženja zove se:

  

### Instalacija IntelliJ IDEA Community razvojnog okruženja

Preuzimanje IntelliJ IDEA Community razvojnog okruženja može se obaviti sa zvaničnog sajta:

[https://www.jetbrains.com/idea/download  
  
](https://www.jetbrains.com/idea/download)

Na navedenoj adresi je prvo potrebno odabrati operativni sistem koji koristite, a zatim dugme *Download*, pod sekcijom *Community* (slika 6.2).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_02a.png)

*Slika 6.2. Preuzimanje IntelliJ IDEA razvojnog okruženja  
  
*

Nakon preuzimanja, potrebno je da pokrenete preuzeti instalacioni fajl i da pratite uputstva za instalaciju.

Prvi korak jeste klik na dugme **Next** (slika 6.3).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_03.png)

*Slika 6.3. Uvodni korak IntelliJ IDEA instalacije  
  
*

Drugi prozor čarobnjaka omogućava odabir putanje na kojoj će biti smešteni fajlovi IntelliJ IDEA razvojnog okruženja (slika 6.4).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_04.png)*

*Slika 6.4. Odabir instalacione putanje  
  
*

Preporuka je da IntelliJ IDEA razvojno okruženje instalirate na podrazumevanoj putanji.

Treći prozor čarobnjaka za instalaciju donosi opcije za konfigurisanje (slika 6.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_05.png)

*Slika 6.5. Opcije za konfigurisanje instalacije  
  
*

Ponuđene opcije se odnose na sledeće:

- *Create Desktop Shortcut* – kreiranje prečice za pokretanje programa sa desktopa;
- *Update context menu* – unutar kontekstnog menija koji se dobija desnim klikom na neki folder, dodaje opciju za otvaranje takvog foldera kao projekta unutar razvojnog okruženja;
- *Create Associations* – omogućava da se određeni tipovi fajlova automatski otvaraju pomoću IntelliJ IDEA razvojnog okruženja;
- *Update PATH variable* – dodaje putanju na kojoj se nalazi instalacioni IntelliJ IDEA folder unutar sistemske Path promenljive, što omogućava da se razvojno okruženje pokrene korišćenjem konzole/terminala.

Mi smo se odlučili samo za prečicu za pokretanje programa sa desktopa.

Klikom na dugme **Install** unutar sledećeg prozora čarobnjaka (slika 6.6), započinje instalacija IntelliJ IDEA razvojnog okruženja (slika 6.7).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_06.png)

*Slika 6.6 - Pokretanje instalacije  
  
*

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_07.png)

*Slika 6.7. Instalacija u toku  
  
*

Uspešan završetak instalacije propraćen je prozorom poput onog na slici 6.8.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_08.png)

*Slika 6.8. Uspešan završetak IntelliJ IDEA instalacije  
  
*

Opcija *Run* *IntelliJ IDEA Community Edition* omogućava pokretanje razvojnog okruženja klikom na dugme **Finish**. U svakom trenutku, razvojno okruženje možete pokrenuti klikom na ikonicu koja je kreirana na desktopu (slika 6.9).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_09.png)

*Slika 6.9. Ikonica za pokretanje IntelliJ IDEA razvojnog okruženja  
  
*

### Prvo pokretanje IntelliJ IDEA okruženja

Prilikom prvog pokretanja IntelliJ IDEA razvojnog okruženja, dočekaće vas nekoliko prozora za inicijalno konfigurisanje. Prvo će biti prikazan prozor za odabir teme (slika 6.10).

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_10.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_10-original.png)

*Slika 6.10. Mogućnost odabira teme  
  
*

Tema se prevashodno odnosi na boje kojima će biti predstavljeni različiti vizuelni elementi unutar okruženja. ==Razvojno okruženje tokom inicijalnog pokretanja omogućava odabir jedne tamne (Darcula) i jedne svetle (Light) teme.== U zavisnosti od ličnih preferencija, možete odabrati temu koja vam više odgovara. Tamne teme su bolje prilikom rada u prostorijama sa malo svetlosti, a svetle teme za rad u visoko osvetljenim prostorima ili napolju. Naravno, ovo nisu jedine teme koje IntelliJ IDEA poseduje, pa je temu moguće promeniti i kasnije, u bilo kom trenutku.

==Pored mogućnosti odabira teme, IntelliJ IDEA poseduje još nekoliko prozora za konfigurisanje razvojnog okruženja,== sa opcijama za odabir različitih dodataka koji će biti dostupni za korišćenje unutar razvojnog okruženja. Takve opcije ćete videti ukoliko odaberete dugme *Next: Default Plugins*.

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_11.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_11-original.png)

*Slika 6.11. Opcije za podešavanje dodataka (1)  
  
*

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_12.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_12-original.png)

*Slika 6.12. Opcije za podešavanje dodataka (2)  
  
*

U ovom trenutku nećemo se baviti podešavanjem dodataka, s obzirom na to da je pred nama dug put upoznavanja sa osnovim opcijama IntelliJ IDEA razvojnog okruženja. Svi dodaci se mogu aktivirati i konfigurisati i naknadno, pa ćemo različite dodatke obrađivati kada se za njihovim korišćenjem javi potreba.

==Na kraju, klikom na dugme *Start using IntelliJ IDEA* završava se proces inicijalne konfiguracije i otvara se početni prozor IntelliJ IDEA razvojnog okruženja== (slika 6.13).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_13a.PNG)

*Slika 6.13. Početni prozor IntelliJ IDEA razvojnog okruženja  
  
*

### Kreiranje novog IntelliJ IDEA projekta

Mogućnosti IntelliJ IDEA razvojnog okruženja su zaista velike i sa njima ćemo se upoznavati postepeno, u lekcijama koje slede, kada određenu funkcionalnost razvojnog okruženja budemo mogli da potkrepimo praktičnim primerima. Za početak, iskoristićemo IntelliJ IDEA razvojno okruženje za pisanje i pokretanje svog prvog Java programa, koji smo u prethodnoj lekciji napisali korišćenjem Notepada, a preveli i pokrenuli direktnom upotrebom alata koji pripadaju Java ekosistemu. Na takvom primeru, moći ćete veoma lako da uvidite neke osnovne prednosti koje donosi korišćenje razvojnih okruženja.

Unutar početnog prozora, koji je prikazan slikom 6.13, potrebno je odabrati opciju **New Project**.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_14a.PNG)

*Slika 6.14. Prozor za podešavanje novog projekta  
  
*

| **IntelliJ IDEA tip**  Unutar IntelliJ IDEA razvojnog okruženja, projekti se koriste za organizaciju koda koji pišemo. Realne aplikacije se uglavnom sastoje iz velike količine koda, koji je podeljen u različite celine. Pored izvornog koda, realne aplikacije se sastoje i iz mnoštva dodatnih elemenata, kao što su resursi, konfiguracioni fajlovi i instrukcije za izgradnju. IntelliJ IDEA projekti se koriste da sve takve elemente grupišu u jednu logičku celinu. |
| --- |

Na slici 6.14. možete videti prozor za kreiranje novog IntelliJ IDEA projekta. Kako bi se kreirao projekat za razvoj nove Java aplikacije, u panelu sa leve strane je potrebno odabrati *New Project*, za *Language* izabrati *Java*, a *Build System* treba da bude *IntelliJ*. Kreiranje projekta za razvoj Java programa zahteva i postojanje JDK-a na razvojnom kompjuteru. U jednoj od prethodnih lekcija je već prikazan kompletan proces za preuzimanje i konfigurisanje OpenJDK distribucije. Ukoliko ste uspešno ispratili uputstvo iz te lekcije, IntelliJ IDEA će automatski prepoznati konfigurisani JDK. To možete videti i na slici 6.14, gde je pod stavkom *JDK* automatski odabran OpenJDK koji smo preuzeli i konfigurisali u jednoj od prethodnih lekcija.

Tekući prozor donosi i opcije za definisanje naziva projekta i lokacije na kojoj će se naći njegovi fajlovi (slika 6.15).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_15a.PNG)

*Slika 6.15. Predhodni prozor sa definisanim nazivom projekta i putanjom na kojoj će se on naći  
  
*

Za naziv projekta postavljeno je *MyFirstJavaProgram*, a za lokaciju na kojoj će se naći njegovi fajlovi odabran je nešto ranije kreirani folder java\_programs. Unutar njega ==biće kreiran jedan novi folder,== koji će imati identičan naziv kao naš prvi projekat.

Kada kliknemo na dugme **Create**, IntelliJ IDEA će za nas kreirati projektni folder; ovo je ujedno i poslednji korak u procesu kreiranja novog projekta.

Nakon kreiranja novog projekta, on će automatski biti otvoren, pa će vas dočekati prozor kao na slici 6.16.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_18a.png)

*Slika 6.16. Početni prozor IntelliJ IDEA projekta  
  
*

| **Napomena**  Ukoliko prilikom kreiranja novog projekta (slika 6.15) ostavite čekiranu opciju **Add sample code** dobićete gotov testni primer Java programa (slika 6.22), a ukoliko tu pociju isključite dobićete prazan projekat (slika 6.17). |
| --- |

### IntelliJ IDEA projektna struktura

==Prilikom kreiranja projekata korišćenjem IntelliJ IDEA razvojnog okruženja, automatski se dobija određena projektna struktura==. Drugim rečima, IntelliJ IDEA za nas automatski kreira određene fajlove i foldere. U to se možete uveriti i ukoliko posetite folder koji ste definisali kao koreni folder projekta (u ovoj lekciji je to C:\\java\_programs\\MyFirstJavaProgram).

Projektnu strukturu je mnogo jednostavnije sagledati korišćenjem IntelliJ IDEA razvojnog okruženja. Dovoljno je kliknuti na dugme **Project** koje se nalazi unutar leve vertikalne trake i otvara se panel sa projektnom strukturom (slika 6.17).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_17a.png)

*Slika 6.17. Pregled projektne strukture IntelliJ IDEA projekta  
  
*

==Uvidom u projektnu strukturu, može se zaključiti da IntelliJ IDEA za nas kreira određene foldere i fajlove:==

- **.==idea** – folder unutar koga se smeštaju podešavanja projekta== koja se koriste od strane samog razvojnog okruženja;
- ==**src** – folder unutar koga se smešta izvorni kod== naše Java aplikacije;
- ==**MyFirstJavaProgram.iml** – fajl sa podešavanjima jednog IntelliJ IDEA modula;== moduli su još jedna ==tvorevina samog razvojnog okruženja i nemaju veze sa samim Java jezikom.==

| **Napomena**  Na Linux i macOS operativnim sistemima, folder .idea je podrazumevano skriven. Kako biste ga videli, neophodno je u podešavanjima aktivirati prikaz skrivenih fajlova i foldera. |
| --- |

Na osnovu ovog kratkog izlaganja o strukturi IntelliJ IDEA projekta, može se zaključiti da su ==.iml fajl i .idea folder tvorevine samog razvojnog okruženja==, koje se k==oriste za konfigurisanje projekta==. Konfigurisanje obavlja samo razvojno okruženje, pa će se tako veoma retko javiti potreba za ručnom intervencijom nad ovim fajlovima.

==Folder koji nas u ovom trenutku najviše zanima jeste src.== Reč je o folderu koji je trenutno prazan, a unutar koga je ==potrebno smeštati fajlove sa izvornim Java kodom==. Stoga se sledeći korak u ovoj lekciji tiče upravo ovog foldera.  
  

### Kreiranje Java klase korišćenjem IntelliJ IDEA razvojnog okruženja

U prethodnoj lekciji imali ste prilike da vidite da se Java programska logika piše unutar fajlova sa ekstenzijom .java, a grupiše unutar kategorije koja se naziva klasa. Stoga će ==naš sledeći korak biti kreiranje jednog novog fajla unutar koga će postojati jedna Java klasa.== To se korišćenjem ==IntelliJ IDEA== razvojnog okruženja obavlja odabirom opcije ==**New -> Java Clas==s**, koja se može pronaći unutar kontekstnog menija koji se dobija desnim klikom na folder src (slika 6.18).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_18a.png)

*Slika 6.18. Kreiranje nove klase korišćenjem IntelliJ IDEA razvojnog okruženja  
  
*

Pokretanje opcije za kreiranje nove klase propraćeno je prozorom za unos njenog naziva (slika 6.19).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_19a.png)

*Slika 6.19. Unos naziva klase koja će biti kreirana  
  
*

Nakon unosa naziva klase, dovoljno je pritisnuti taster Enter na tastaturi i nova klasa će biti kreirana.

Kreiranje nove klase podrazumeva kreiranje novog fajla koji ima identičan naziv kao i klasa unutar njega (slika 6.20).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_20a.png)

*Slika 6.20. Kreiranjem nove klase dobija se novi fajl unutar projektne strukture  
  
*

==Fajl unutar koga se smešta kreirana klasa ima ekstenziju .java==. Iz prethodne lekcije znamo da .java ekstenzija označava fajlove sa Java izvornim kodom. Nemojte se zbuniti zbog toga što unutar IntelliJ IDEA projektne strukture upravo dobijeni fajl (MyFirstProgram) nema ekstenziju.java. Jednostavno, ==IntelliJ IDEA uprošćava prikaz fajlova i foldera, pa tako automatski skriva .java ekstenziju.==  
  

### Pisanje izvornog koda našeg prvog Java programa

Kreiranjem nove klase korišćenjem IntelliJ IDEA razvojnog okruženja automatski se dobija novi fajl i unutar njega određeni izvorni kod (slika 6.21).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_21a.png)

*Slika 6.21. Automatski generisan izvorni kod Java klase  
  
*

Izvorni kod Java klase se može videti unutar radne površine, na desnoj strani. Razvojno okruženje je za nas automatski generisalo sledeće:

```java
publicclassMyFirstProgram {
 
}
```

| **Napomena**  Ovo je kod kojim se u Java jeziku kreira jedna klasa. Za sada je dovoljno da znate da se klase koriste za grupisanje izvornog koda u jednu logičnu celinu i da nije moguće napisati funkcionalan Java kod bez klase. U nastavku ovog kursa, klase će biti jedna od centralnih tema i biće im posvećena posebna pažnja. |
| --- |

Unutar kreirane klase, sada je potrebno dodati ostatak koda iz prethodne lekcije koji čini naš prvi Java program:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        System.out.println("Hello World");
    }
}
```

  
==Unutar klase== dodata je ==main metoda== i ==unutar nje== jedna ==linija koda koja obavlja ispis poruke *Hello World*==.

| **Napomena**  Ukoliko prilikom kreiranja novog projekta (slika 6.15) ostavite čekiranu opciju **Add sample code** dobićete gotov primer koji je sličan našem prvom Java programu, jedino će ime klase biti **Main** umesto **MyFirstProgram**.  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_22a.png)  *Slika 6.22. Automatski generisan izvorni kod Java klase* |
| --- |

| **Metoda main**  Metode su još jedan način za grupisanje koda u programskom jeziku Java. Ipak, za razliku od klasa, unutar metoda se grupiše izvršni kod, odnosno kod koji obavlja neki posao. Metode se smeštaju unutar klasa, a jedna klasa može imati proizvoljan broj metoda.  Metoda main je specijalna metoda koja predstavlja ulaznu tačku Java programa. Svaki Java program mora imati main metodu. To je metoda koja se automatski poziva kada se pokrene Java program. |
| --- |

### Pokretanje prvog Java programa korišćenjem IntelliJ IDEA razvojnog okruženja

U prethodnim redovima uradili smo sve što je potrebno kako bismo dobili jedan potpuno funkcionalan Java program. ==Preostalo je još da ga pokrenemo i vidimo efekat njegovog izvršavanja. Za obavljanje takvog posla, u prethodnoj lekciji smo direktno koristili alate javac i java==. Java kompajler (javac) koristili smo kako bismo dobili bytecode, a java kako bismo takav kod proslediti Java virtuelnoj mašini na izvršavanje. ==Sve takve korake sada ćemo obaviti korišćenjem razvojnog okruženja IntelliJ IDEA.==

Već je rečeno da je postojanje main metode unutar nekog programa neophodno kako bi on mogao da se izvrši. Upravo zbog toga, ==čim detektuje postojanje main metode, IntelliJ IDEA unutar radne površine (površine za pisanje koda) dodaje dugme za pokretanje takvog programa (slika 6.23).==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_23a.png)

*Slika 6.24. Opcija za pokretanje Java programa  
  
*

Klikom na zeleni trougao koji možete videti na slici 6.23. dobija se panel za odabir jednog od nekoliko različitih tipova pokretanja. U ovom trenutku iskoristićemo standardno pokretanje, odnosno opciju ==**Run** **'MyFirstProgram.main** **()'**.==

Nakon odabira opcije za pokretanje programa, ==IntelliJ IDEA obavlja nekoliko operacija:==

- u pozadini, IntelliJ IDEA koristi ==javac kako bi obavio kompajliranje== Java izvornog koda;
- kompajlirani kod, odnosno ==bytecode, IntelliJ IDEA smešta u folder out koji kreira unutar projekte strukture;==
- na kraju, IntelliJ ==IDEA prosleđuje bytecode na izvršavanje Java virtuelnoj mašini.==

Efekat izvršavanja programa je moguće videti unutar Run panela koji se pojavljuje u dnu IntelliJ IDEA prozora (slika 6.24).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_06_24a.png)

*Slika 6.24. Efekat izvršavanja Java programa  
  
*

Unutar Run panela ==najpre se može videti naredba kojom se kompajlirani bytecode upućuje na izvršavanje==. Reč je o komandi koju smo u prethodnoj lekciji pisali ručno i koja podrazumeva upotrebu java alata. Ova komanda sada izgleda nešto složenije, sa dodatnim konfiguracionim parametrima koje dodaje razvojno okruženje kako bi moglo da prati izvršavanje našeg programa.

Nakon naredbe za pokretanje, može se videti i ==efekat izvršavanja našeg programa, odnosno poruka *Hello World* koja se dobija na izlazu.==

==Poslednja linija koja se dobija unutar Run panela (*Process finished with exit code 0*) obaveštava nas== da je naša aplikacija uspešno okončala svoje izvršavanje. Uspešan završetak izvršavanja propraćen je ==izlaznim kodom 0.==

Prethodni redovi ilustrovali su samo jedan od načina na koje se može pokrenuti Java program koji se kreira korišćenjem IntelliJ IDEA razvojnog okruženja. Opcije za ==pokretanje se nalaze na velikom broju različitih mesta unutar IntelliJ IDEA okruženja:==

- unutar Run padajućeg menija;
- unutar trake sa navigacijom;
- kao sastavni deo Run panela.

### Nastavak upoznavanja sa IntelliJ IDEA okruženjem

U ovoj lekciji upoznali smo se sa osnovnim osobinama razvojnog okruženja IntelliJ IDEA, koje nam omogućavaju da pišemo i pokrećemo jednostavne Jave programe. IntelliJ IDEA je vrlo moćno razvojno okruženje, sa pregršt funkcionalnosti namenjenih profesionalnim programerima. Takve funkcionalnosti u ovom trenutku umnogome prevazilaze naše poznavanje Java jezika i programiranja uopšte. Stoga ćemo se sa njima upoznavati postepeno tokom ovog kursa, kada se za njihovo korišćenje javi opravdan razlog. Naš primarni cilj u ovom trenutku jeste potpuno razumevanje programskog koda našeg prvog Java programa. Na takvom putu, prva stepenica jeste razumevanje sintakse Java jezika, što će biti sledeća tema u ovom kursu.

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_06.thb) JCPR1\_06.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_06.Mp4")

Kako Vam mogu pomoći?