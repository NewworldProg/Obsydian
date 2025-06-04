---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=922e2e4b7bf10954b111ef3113959a14_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434674"
author:
published:
created: 2025-04-25
description:
tags:
  - "clippings"
---
Jedinica 7 od 22

## Uvod u sintaksu Java jezika

==U prethodnim lekcijama, korišćenjem dva različita pristupa, obavljeno je kreiranje prvog Java programa, koji na izlazu ispisuje poruku *Hello World*.== Upoznali smo se sa koracima za pisanje i pokretanje takvog programa, ali još nismo u stanju da u potpunosti razumemo izvorni kod koji smo napisali. Prvi korak u razumevanju uvodnog primera jeste upoznavanje sa sintaksom Java jezika. Lekcija pred vama biće posvećena upravo osnovnim načelima sintakse ovog jezika.  
  

### Šta je sintaksa nekog programskog jezika?

Sintaksa programskih – ali i bilo kog govornog jezika – predstavlja ==skup pravila koja učesnik u komunikaciji mora da ispoštuje kako bi ostali korisnici tog jezika mogli da ga razumeju.==== Drugim rečima, sintaksa predstavlja skup pravila kojih se svi korisnici jezika moraju pridržavati kako bi bili u stanju da komuniciraju. ==Kršenjem nekog od sintaksnih pravila komunikacija postaje otežana ili u potpunosti nemoguća.==

Dakle, baš kao i svaki govorni jezik, i programski jezici poseduju svoju sintaksu, a može se reći da kod programskih jezika sintaksa igra možda i značajniju ulogu nego kod govornih. Naime, u svakodnevnoj pisanoj ili govornoj komunikaciji često se može primetiti veliki broj sintaksnih grešaka, ali se učesnici u komunikaciji i pored njihovog postojanja vrlo dobro razumeju. Kod programskih jezika, situacija je značajno drugačija. ==Postojanje i najmanje sintaksne greške u komunikaciji između programera i kompjutera znači nemogućnost prevođenja izvornog koda.== Upravo zbog toga je striktno pridržavanje sintaksnih pravila prilikom pisanja programskog koda nekog jezika veoma važno.  
  

### Struktura Java programa

Programski jezik Java, kao i većina drugih modernih jezika, ==najveći deo sintakse preuzima iz jezika C++==, odnosno C. Naime, jezik C++ je u trenutku nastanka Jave bio najrasprostranjeniji programski jezik, pa takav odabir tvoraca Jave uopšte ne čudi.

| **Java i ostali programski jezici**  S obzirom na to da većinu sintakse preuzima iz jezika C++, odnosno C, izvorni kod Jave je vrlo sličan spomenutim jezicima. Pošto i ostali moderni programski jezici (PHP, Python, C#...) imaju iste uzore, može se reći da je većina modernih programskih jezika veoma slična. To praktično znači da ćete učenjem sintakse Jave naučiti i dobar deo sintaksnih pravila ostalih modernih programskih jezika. |
| --- |

Osnovni ==elementi od kojih se može sastojati izvorni kod Java programa su sledeći:==

- ==izjave== (naredbe);
- ==blokovi==;
- ==rezervisane (ključne) reči;==
- ==identifikatori==;
- ==literali==;
- ==komentari==;
- ==prazni== prostori.

Za ==svaki od upravo nabrojanih elemenata Java programa postoje jasna pravila za njegovo kreiranj==e. Sa takvim pravilima ćemo se u nastavku upoznati na primeru prvog programa koji smo kreirali u lekcijama za nama. Izvorni kod takvog programa izgledao je ovako:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        System.out.println("Hello World");
    }
}
```

==U izvornom kodu našeg prvog Java programa postoje gotovo svi nešto ranije nabrojani osnovni elementi== Java programa. Stoga ćemo krenuti redom i pomoću izvornog koda našeg prvog programa pokušati da se upoznamo sa osnovnom strukturom Java programa.  
  

### Izjave (naredbe)

==Izjava (naredba) predstavlja najmanji samostalni deo== jednog programa. Izjava se može uporediti i sa jednom rečenicom u svakodnevnim govornim/pisanim jezicima. U izvornom kodu našeg prvog Java programa postoji ==sledeća izjava:==

```java
System.out.println("Hello World");
```

  
Ovo je jedna izjava, odnosno naredba kojom se postiže ispis poruke *Hello World*. Nešto ranije je rečeno da je izjava najmanji samostalni deo jednog programa, a to sada možemo videti i u praksi. ==Prikazana izjava proizvodi efekat ispisa jedne poruke.==

==Na kraju upravo prikazane izjave možete primetiti karakter tačka i zapeta.== Baš kao što se ==u pisanim jezicima rečenica završava tačkom==, ==u programskom jeziku Java izjava se mora okončati karakterom tačka i zapeta (;)==.

| **Karakter tačka i zapeta (;)**  U programskom jeziku Java, svaka izjava se mora završiti karakterom tačka i zapeta. |
| --- |

Nepostojanje karaktera tačka i zapeta na kraju izjave u programskom jeziku Java se smatra sintaksnom greškom. Tako smo se u ovom trenutku prvi put susreli sa pojmom sintaksne greške.

| **Sintaksne greške**  Bilo koje nepoštovanje sintaksnih pravila jezika Java proizvodi sintaksnu grešku. Izvorni kod sa sintaksnom greškom nije validan i ne može se kompajlirati u bytecode. Stoga je preduslov za kompajliranje izvorni kod bez ijedne sintaksne greške. |
| --- |

| **IntelliJ IDEA Tip**  **Sintaksne greške**  Mi smo se do sada upoznali samo sa jednom sintaksom greškom u jeziku Java - izostanak karaktera tačka zapeta na kraju izjave. Ipak, to nam je dovoljno kako bismo se upoznali sa jednom značajnom osobinom IntelliJ IDEA razvojnog okruženja. Reč je o detekciji sintaksnih grešaka. Detekcija sintaksnih grešaka je samo jedna od pogodnosti razvojnog okruženja IntelliJ IDEA, koje olakšavaju razvoj Java programa. Naime, IntelliJ IDEA okruženje poseduje sistem za detekciju i jasno markiranje sintaksnih grešaka (slika 7.1).  [![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_01.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_01-original.png)  *Slika 7.1. Markiranje sintaksne greške unutar IntelliJ IDEA razvojnog okruženja      *  Na slici 7.1. možete videti kako izgleda izvorni kod Java programa sa jednom sintaksom greškom unutar IntelliJ IDEA razvojnog okruženja. Sve što je potrebno uraditi kako bi se dobio ovakav prikaz jeste uklanjanje karaktera tačka zapeta sa kraja naredbe našeg prvog programa. Odmah nakon uklanjanja tog karaktera, IntelliJ IDEA na nekoliko različitih načina signalizira postojanja sintaksne greške:  - mesto na kome treba da postoji karakter tačka i zapeta podvučeno je crvenom talasastom linijom; kada preko tog mesta postavite kursor miša, dobija se poruka da se na tom mestu očekuje karakter tačka i zapeta; - u gornjem desnom uglu radne površine (površine za pisanje koda) pojavljuje se uzvičnik sa ukupnim brojem sintaksnih grešaka unutar celog dokumenta; - naslov tekućeg dokumenta je podvučen crvenom talasastom linijom; - unutar projekte strukture (Project panel), nazivi projekta i klase sa sintaksnom greškom takođe su podvučeni crvenom bojom. |
| --- |

Pre nego što se posvetimo narednom važnom elementu Java programa, osvrnućemo se ukratko i na jednu činjenicu koja se često pogrešno interpretira. Reč je o pojmu *linija koda*.

| **Izjave i linije**  Veoma često se može čuti da se veličina nekog programa meri u linijama, pa se tako može naići npr. na *100 linija koda*, *1245 linija koda* ili *na 128. liniji koda se nalazi sintaksna greška*. Ipak, bitno je znati da pojam linije nije isto što i pojam izjave, odnosno naredbe. Najčešća praksa je da se jedna izjava piše unutar jedne linije koda:  ```java System.out.println("Hello World"); ```     Ovo je jedna naredba, ali ujedno i jedna linija koda. Ipak, nije obavezno da svaka naredba mora biti u zasebnoj liniji koda:  ```java System.out.println("Hello World");System.out.println("Hello World"); ```     Ovo je sada primer koji ilustruje dve naredbe koje su napisane u jednoj liniji, pa tako imamo dve naredbe i jednu liniju koda, što je u potpunosti sintaksno ispravan kod. Ipak, u praksi se zbog preglednosti najčešće pribegava smeštanju svake naredbe u zasebnu liniju:  ```java System.out.println("Hello World"); System.out.println("Hello World"); ```     Ovo su sada dve naredbe i dve linije koda. |
| --- |

### Blokovi

Blok koda ==predstavlja== ==način za grupisanje izjava, odnosno naredbi u jednu logičnu celinu==. U primeru prve Java aplikacije prikazane na početku ove lekcije postoje dva bloka koda. Njih je veoma lako ==prepoznati po otvorenim i zatvorenim vitičastim zagradama – {}.==

Prvi blok iz naše Java aplikacije izgleda ovako:

```java
publicclassMyFirstProgram {
 
}
```

  
Ovo je ==blok koda koji se koristi za kreiranje jedne klase.==

==Drugi blok== iz naše Java aplikacije je sledeći:

```java
publicstaticvoidmain(String[] args) {
    System.out.println("Hello World");
 
}
```

  
Ovo je blok kojim se ==kreira jedna metoda.==

| **Vitičaste zagrade**  U programskom jeziku Java, blokovi se kreiraju upotrebom vitičastih zagrada – {}. { označava početak bloka, a } završetak bloka. **Svaki blok koji se otvori mora se i zatvoriti.** Stoga, svaka otvorena vitičasta zagrada mora posedovati i pripadajuću zatvorenu vitičastu zagradu. |
| --- |

Na osnovu ova dva primera može se zaključiti da se blokovi u programskom jeziku Java koriste za kreiranje različitih jezičkih elemenata. U primeru su prikazane klase i metode, a takom kursa ćemo se susretati sa brojnim drugim jezičkim elementima koji se kreiraju korišćenjem blokova. Za sada je dovoljno da znate da se ==blokovi koriste za kreiranje jedne celine koda, unutar koje se može naći jedna ili više naredbi, i da se blokovi karakterišu upotrebom vitičastih zagrada.==

Na kraj bloka ne stavlja se karakter tačka zapeta.  
  

### Ključne reči

==Izvorni kod== našeg prvog Java programa sa početka ove lekcije ==poseduje izvestan broj specijalnih== reči – ==public, class, void.==.. Reč je elementima jezika koji se nazivaju ==ključne reči.==

Ključne reči su reči koje su rezervisane od strane jezika, pa tako za Java kompajler imaju posebno značenje. Tako, na primer, kada kompajliranje izvornog koda dođe do reči class, kompajler zna da je naša namera da kreiramo novu Java klasu.

Ja==va jezik poseduje veliki broj ključnih reči. One su prikazane tabelom== 7.1.

| abstract | assert | boolean | break | bytte | case |
| --- | --- | --- | --- | --- | --- |
| catch | char | class | const | continue | default |
| double | do | else | enum | extends | false |
| final | finally | float | for | goto | if |
| implements | import | instanceof | int | interface | long |
| native | new | null | package | private | protected |
| public | return | short | static | strictfp | super |
| switch | synchronized | this | throw | throws | transient |
| true | try | void | volatile | while |  |

*  
Tabela 7.1. Rezervisane (ključne) reči jezika Java  
  
*

==Sa različitim ključnim rečima Java jezika ćemo se upoznavati postepen==o, prilikom obrađivanja jezičkih elemenata koji se korišćenjem takvih ključnih reči kreiraju. Tako ćemo, na primer, o ključnim rečima public, static i class govoriti kada bude bilo reči o klasama, a o ključnoj reči void prilikom upoznavanja sa pojmom metoda.

| **IntelliJ IDEA Tip**  **Syntax highlighting**  Još jedna od funkcionalnosti koju poseduje većina razvojnih okruženja, pa i IntelliJ IDEA, jeste specijalno markiranje izvornog koda koji pišemo. Takva funkcionalnost se naziva *Syntax highlighting*, odnosno markiranje koda na osnovu sintakse jezika. Sada kada smo započeli izučavanje osnovnih sintaksnih pravila Java jezika, možemo razumeti ovakvu značajnu osobinu razvojnog okruženja (slika 7.2).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_02.png)  *Slika 7.2. Syntax highlighting funkcionalnost razvojnog okruženja      *  Slika 7.2. predstavlja isečak IntelliJ IDEA radne površine, odnosno površine za pisanje koda.  Odmah možete da primetite da su različiti delovi izvornog koda obojeni različitim bojama. Na primer, ključne reči, o kojima je upravo bilo reči, obojene su narandžastom bojom.  Skup boja za označavanje sintaksnih elemenata koda deo je šeme boja koja se može menjati iz prozora za podešavanja koji se dobija odabirom opcije **File -> Settings** (slika 7.3).  [*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_03.png)*](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_03-original.png)  *Slika 7.3. Prozor za podešavanje šeme boja      *  U prozoru za podešavanje potrebno je odabrati opciju **Editor -> Color Scheme**, a zatim iz padajućeg menija **Scheme** odabrati odgovarajuću šemu, baš kao na slici 7.3. |
| --- |

### Identifikatori

U prethodnim redovima definisan je pojam ključnih reči Java jezika, odnosno reči čiji su oblik i značenje unapred utvrđeni pravilima jezika. ==Prilikom pisanja Java koda, programer ima mogućnost i da samostalno formira nazive određenih jezičkih elemenata==. To se postiže korišćenjem identifikatora. Jednostavno, određeni ==jezički elementi, kao što su klase i metode, moraju da budu imenovani.== Upravo zbog toga u programskom jeziku Java postoje identifikatori.

U primeru našeg prvog programa postoji nekoliko identifikatora. Za početak, ==naziv klase== je jedan ==primer identifikatora:==

```java
publicclassMyFirstProgram {
 
}
```

  
Ovde je MyFirstProgram identifikator.

Takođe, ==naziv metode== je još jedan ==primer identifikatora:==

```java
publicstaticvoidmain(String[] args) {
    System.out.println("Hello World")
}
```

  
Sada je ==primer identifikatora reč main.==

| **Pravila za definisanje identifikatora**  Bitno je razumeti da identifikatori nisu nešto što je unapred definisano jezikom. Drugim rečima, programer sam smišlja njihove nazive. Zato je veoma bitno znati da je prilikom definisanja identifikatora potrebno poštovati nekoliko pravila za njihovo pisanje:  - identifikatori mogu biti sastavljeni od slova, brojeva i karaktera donja crta i dolar; - identifikatori moraju sadržati makar jedan karakter; - identifikatori ne smeju početi brojem; - identifikatori su osetljivi na velika i mala slova (*case sensitive*), tako da myClass i MyClass nije isto; - ključne reči se ne mogu koristiti kao identifikatori. |
| --- |

==Pravila za definisanje identifikatora su veoma značajna==, jer se identifikatori koriste za imenovanje brojnih jezičkih elemenata, o kojima će biti reči u lekcijama koje slede – promenljive, konstante, klase...

Jedan ==primer validnog identifikatora,== koji predstavlja naziv klase, može da izgleda ovako:

```java
classJavaClass
{
}
```

  
Sa druge strane, ==primer sintaksno netačnog identifikatora== može da izgleda ovako:

```java
class5Class
{
}
```

  
Identifikator sada započinje brojem, što je sintaksno nevalidno.

Još jedan primer ==ispravnog identifikatora== može biti ovakav naziv jedne metode:

```java
voidmethod_name()
{
}
```

  
Sintaksno ==nevalidan naziv== metode može da izgleda ovako:

```java
voidclass()
{
}
```

  
Za naziv metode je upotrebljena jedna od rezervisanih reči jezika, što je sintaksno nedopustivo.  
  

### Literali

Pored identifikatora, p==rogramer ima mogućnost da proizvoljno, odnosno samostalno definiše još jedan jezički element== – reč je o literalima, odnosno vrednostima. Literali predstavljaju način za ==predstavljanje vrednosti unutar programa==. ==U primeru== našeg prvog Java programa postoji jedan literal. Reč je o ==tekstu koji naš program ispisuje== kao svoj rezultat:

```java
System.out.println("Hello World");
```

  
Unutar ovakve izjave, odnosno naredbe, tekst "Hello World" je primer literala. Ovim literalom se u programu predstavlja jedna tekstualna vrednost koju program ispisuje na izlazu. Pored tekstualnih vrednosti, prilikom razvoja Java programa moguće je kreirati i razne druge tipove vrednosti, pa se tako literali koriste za predstavljanje brojeva, teksta, logičkih vrednosti...

Pojam literala je tesno p==ovezan sa pojmom promenljivih i tipovima podataka.== Stoga će već u narednom modulu ovog kursa sa posebnom pažnjom biti nastavljena priča o literalima.  
  

### Komentari

Prilikom pisanja Java koda moguće je napisati i tekst koji nema nikakvo značenje za kompajler. Na taj način je moguće napisati neku dodatnu informaciju o kodu koja će poslužiti kao uputstvo ili naznaka za lakše snalaženje programera. Takve dodatne informacije se nazivaju **komentari**.

Komentari se u jeziku Java ==mogu formirati na dva načina, u zavisnosti od toga koliko linija teksta obuhvataju (slika 7.4).==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_04.png)

*Slika 7.4 – Primer jednolinijskih i višelinijskih komentara  
  
*

Slika 7.4. ilustruje primer jednolinijskog i višelinijskog komentara. Potpuno razumljivo, jednolinijski komentar je onaj koji obuhvata jednu liniju teksta. Formira se korišćenjem dva karaktera kosa crta. Ukoliko je pod komentar potrebno postaviti više linija teksta, koristi se nešto drugačiji pristup za formiranje komentara: ==/\* za njegov početak i \*/ za njegov završeta==k.

Izvorni kod našeg prvog Java programa ne poseduje nijedan komentar, ali komentar možemo vrlo lako dodati:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        
        System.out.println("Hello World");
    }
}
```

  
U izvorni kod našeg programa sada je dodata još jedna linija koda, pre izjave kojom se ispisuje *Hello World* poruka. Reč je o jednolinijskom komentaru, koga možete prepoznati na osnovu dva karaktera kosa crta (*slash*).

Ovo je klasičan primer korišćenja komentara za pružanje nekih dodatnih informacija o samom kodu. Jednostavno, komentarom je opisan efekat naredbe koja sledi.

Kao što je rečeno, komentari nemaju uticaj na izvršavanje koda, pa će tako naš program funkcionisati na identičan način kao i do sada. Još jedna veoma česta namena komentara jeste isključivanje određenih delova koda. U takvom slučaju, komentari zapravo utiču na izvršavanje programa:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        
        
    }
}
```

  
Sada je bitno da primetite da je i naredba kojom se ispisuje poruka *Hello World* pretvorena u komentar. Stoga to više nije naredba, već običan jednolinijski komentar; pošto kompajler ignoriše komentare, ovakav program neće proizvesti nikakav efekat, zato što će za kompajler on biti identičan kao i program koji poseduje potpuno praznu main metodu:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
    }
}
```

  
Ovaj i prethodni primer su identični po efektu koji proizvode.

Identičan efekat je mogao biti postignut i korišćenjem višelinijskog komentara:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        
        
    }
}
```

  
Ovaj i prethodna dva primera imaju identičan efekat.

| **Javadoc**  Pored standardnih komentara, o kojima je bilo reči u dosadašnjem toku lekcije, za programski jezik Java karakteristična je još jedna vrsta komentara. Može se reći da je reč o jednoj vrsti specijalnih komentara. Naime, Java poseduje ugrađen mehanizam za generisanje dokumentacije o kodu koji se piše. Ovaj mehanizam se naziva **Javadoc**.  Javadoc komentari počinju kosom crtom, nakon čega slede dve zvezdice (**/\*\***), a završavaju se zvezdicom i kosom crtom (**\*/**). Iz ovoga se može zaključiti da je razlika u odnosu na standardne višelinijske komentare samo u jednom karakteru zvezdica više prilikom otvaranja Javadoc komentara:  ```java /**       * this is example       * of Javadoc comment       */ ```     Jedan realan primer Javadoc komentara bi mogao da izgleda ovako:  ```java /**           * This is my test class.          * @author      John Lord <john.lord@example.com>          * @version     1.8          * @since       1.4          */             publicclassTest {                             } ```     Prikazanim Javadoc komentarom definišu se neke osnovne informacije o programu, koje primarno pomažu drugim programerima da razumeju čemu je namenjen kod koji se nalazi unutar Test klase.  Bitno je da primetite i da svaka linija unutar Javadoc komentara započinje karakterom zvezdica. Tako nešto nije pravilo, već samo konvencija, odnosno preporuka, zbog bolje preglednosti i čitljivosti.  Sve gotove funkcionalnosti koje su deo Java platforme poseduju Javadoc komentare. To je veoma važna činjenica, koja će nam u nastavku učenja Jave biti od velike koristi. Naime, s obzirom na to da ćemo se u nastavku upoznati sa velikim brojem različitih ugrađenih funkcionalnosti jezika, u svakom trenutku možemo da dobijemo neke osnovne informacije o njima upravo korišćenjem Javadoca. Dobra stvar je i to što IntelliJ IDEA razvojno okruženje značajno olakšava pristup takvoj dokumentaciji. Dovoljno je postaviti kursor miša iznad neke ugrađene funkcionalnosti Java platforme i dobija se Javadoc tekst (slika 7.5).  [![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_05.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_07_05-original.png)  *Slika 7.5. Pregled Javadoc komentara korišćenjem IntelliJ IDEA okruženja      *  Na slici 7.5. možete videti Javadoc komentare za jednu od ugrađenih klasa koja nosi naziv System. Postavljanjem pokazivača miša preko nje, dobija se panel sa Javadoc tekstom, odnosno opisom osnovne namene ove klase. |
| --- |

### Prazna mesta

Analizom izvornog koda našeg prvog Java programa može se primetiti da je u njegovom formiranju iskorišćeno specifično formatiranje koda. Kod je smešten u određeni broj novih redova (linija), ==neki elementi su razdvojeni praznim mestima, dok su određene linije uvučene u odnosu na ostatak koda.== Sve ovo je urađeno kao bi se dobio pregledniji i čitljiviji kod. Prazna mesta (*white spaces*) koja su u te svrhe korišćena su:

- ==razmaci;==
- ==tabulatori;==
- ==prelasci u novi red.==

Primenom specifičnog formatiranja koje poboljšava čitljivost koda, dobijaju se linije. Veoma je bitno znati da ==za Java kompajler pojam linije, baš kao ni pojam praznih mesta, nema nikakvo značenje. Naime, potpuno je legitimno napisati kod kompletnog programa u jednoj liniji:==

```java
publicclassMyFirstProgram { publicstaticvoidmain(String[] args) { System.out.println("Hello World"); }}
```

  
Efekat ovakvog koda je identičan onom sa početka lekcije. ==Ipak, ovako nešto se ne praktikuje jer== veoma ==loše utiče na čitljivost.==

Koji od sledećih primera oslikava pravilnu upotrebu komentara u jeziku Java?

  

**Vežba 1**

Data je sledeća naredba:

```java
int1myNumber = 800;
```

  
==Prikazana naredba poseduje sintaksu grešku. Potrebno je ispraviti tu grešku.==

==**Rešenje**==

==*Identifikatori u Javi ne smeju početi brojem:*==

```java
intmyNumber = 800;
```

**  
Vežba 2**

Dat je sledeći Java program:

```java
publicclassMyFirstProgram {
 
    publicstaticvoidmain(String[] args) {
        System.out.println("Hello World");
}
```

  
Prikazani kod poseduje sintaksu grešku. Potrebno je pronaći i ukloniti tu grešku.

**Rešenje**

==*Blok koda koji predstavlja telo* *main* *metode nije zatvoren==. Stoga je potrebno dodati jednu zatvorenu vitičastu zagradu:*

```java
publicclassMyFirstProgram {
 
    publicstaticvoidmain(String[] args) {
        System.out.println("Hello World");
    }
 
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_07.thb) JCPR1\_07.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_07.Mp4")