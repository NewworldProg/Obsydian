---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=b8a0749eb05974970936e741e36dd8ca_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434682"
author:
published:
created: 2025-05-01
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 15 od 22

## Paketi

U prethodnoj lekciji mogli ste da se uverite u moć klasa i objekata, centralnih figura Java jezika. Ipak, priča o klasama ne može proći bez još jednog veoma značajnog elementa Java jezika, koji se koristi za uspostavljanje klasne hijerarhijske strukture u Java programima. Reč je o pojmu paketa. Njima će biti posvećena lekcija pred vama.  
  

### Šta su paketi?

Paketi se u Java jeziku koriste za ==grupisanje većeg broja srodnih klasa==, odnosno za uspostavljanje određene vrste hijerarhijske strukture. Uopšteno govoreći, hijerarhijska struktura se koristi kako bi se elementi organizovali u skladu sa relacijama i vezama koje postoje između takvih elemenata. ==Dobar primer takve hijerarhijske strukture je [fajl sistem](https://www.link-elearning.com/linkdl/opisPojma.php?id=160461 "fajl sistem"). Fajl sistem predstavlja hijerarhijsku organizaciju foldera== u okviru nekog skladišta podataka. Na taj način se olakšava snalaženje u okviru velike količine podataka. Na isti način se može razmišljati i o paketima u Javi. Oni predstavljaju sistem za tipiziranu klasifikaciju klasa.

U prethodnoj lekciji smo obavili kreiranje svoje prve klase. Bila je to klasa Car. Ukoliko unutar IntelliJ IDEA razvojnog okruženja otkucamo naziv ove klase, možemo da dobijemo jednu vrlo zanimljivu informaciju od ovog razvojnog okruženja (slika 15.1).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_01.png)*

*Slika 15.1. Klasa Car se nalazi u podrazumevanom paketu (default package)  
  
*

Na slici 15.1. u okviru panela sa predlozima koje dobijamo od razvojnog okruženja možete videti da nakon klase Car stoji natpis *default package*. Takođe, i pored svih ostalih klasa čiju upotrebu nam okruženje nudi stoje različiti natpisi kao što su ==java.awt, java.swing.text, java.net itd. Sve su ovo primeri paketa, na osn==ovu čega možemo da zaključimo da n==e postoji Java klasa koja ne pripada nekom paketu. Čak i naša klasa koju smo kreirali u prethodnoj lekciji pripada jednom paketu, iako ga nismo eksplicitno kreirali.==  
  

### Podrazumevani paket

Svaka Java klasa mora pripadati nekom paketu. U skladu sa tim, podrazumevani paket se koristi za klase koje nisu eksplicitno dodate unutar nijednog paketa, baš kao što je to slučaj u primeru iz prethodne lekcije. ==Sve klase koje se nalaze direktno unutar src foldera pripadaju podrazumevanom paketu.==

Iako je potpuno legitimno imati klase unutar podrazumevanog paketa, savetuje se kreiranje sopstvenog, pa čak i onda kada nam je potreban samo jedan paket i kada naš projekat ima mali broj klasa.

### Kreiranje paketa

Paketi nisu ništa drugo do folderi na fajl sistemu. U to se možete uveriti ukoliko unutar src foldera IntelliJ IDEA projekta na kome radimo napravite novi folder. ==Folder možete da napravite korišćenjem bilo koje odgovarajuće opcije koju poseduje operativni sistem na kome radite. Nakon što napravite folder unutar src foldera, IntelliJ IDEA okruženje će ga automatski prepoznati== kao novi paket (slika 15.2).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_02.png)*

*Slika 15.2. Okruženje IntelliJ IDEA je prepoznalo folder kao novi paket  
  
*

Naravno, i IntelliJ IDEA poseduje funkcionalnost za kreiranje paketa, pa je savet da upravo kreirani paket obrišete, kako bismo njegovo kreiranje obavili korišćenjem razvojnog okruženja.

| **IntelliJ IDEA Tip**  **Kreiranje paketa**  Korišćenjem IntelliJ IDEA razvojnog okruženja, paketi se kreiraju slično kao i klase. Iz kontekstnog menija koji se dobija desnim klikom na folder src, potrebno je odabrati opciju **New -> Package** (slika 15.3).  [*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_03-ispravka.png)*](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_03-original.png)  *Slika 15.3. Opcija za kreiranje paketa u IntelliJ IDEA okruženju      *  Odabirom opcije za kreiranje novog paketa, otvara se prozor za unos njegovog imena (slika 15.4).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_04.png)  *Slika 15.4. Unos naziva novog paketa      *  Nakon unosa imena paketa, kreiranje možete da potvrdite pritiskom na taster Enter na tastaturi. |
| --- |

Paketi se, po nepisanom pravilu, imenuju korišćenjem malih slova, bez ikakvog karaktera za razdvajanje reči.  
  

### Dodavanje klase u paket

Paket koji smo upravo kreirali je prazan. Kako bi se unutar njega dodala neka klasa, potrebno je uraditi sledeće:

- klasu je potrebno smestiti unutar foldera koji predstavlja paket;
- na početak fajla u kome se nalazi klasa je potrebno dodati jednu posebnu naredbu za smeštanje klase u paket.

Stoga, ==ukoliko bismo želeli da našu klasu Car dodamo u upravo kreirani paket, bilo bi potrebno da je prebacimo u folder== koji predstavlja paket i na njen sam početak postavimo sledeću liniju koda:

```java
packagemypackage;
 
publicclassCar {
 
}
```

  
Naredba za smeštanje klase unutar paketa definiše se korišćenjem ključne reči **package** nakon koje se navodi naziv paketa.

Da bi se klasa smestila u određeni paket, koristi se ključna reč:

  

### Korišćenje klase iz nekog drugog paketa

Sve klase koje se nalaze u jednom paketu uzajamno su vidljive bez eksplicitnog naglašavanja. Ipak, ==klasa iz jednog paketa nije u stanju da vidi klase i njihove članove iz nekih drugih paketa==. Takvu situaciju sada imamo i unutar našeg primera (slika 15.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_05.png)

*Slika 15.5. Klasa Car više nije vidljiva unutar main metode glavne klase  
  
*

Naša glavna klasa MyFirstProgram nalazi se unutar podrazumevanog paketa. Unutar main metode pokušavamo da pristupimo klasi Car, koja je sada deo posebnog paketa – mypackage. ==Razvojno okruženje jasno signalizira da ne može da pronađe klasu Car.==

Jedan od načina za korišćenje klasa iz drugih paketa jeste navođenje njihovog punog kvalifikovanog naziva (***Fully Qualified Class Name***):

```java
mypackage.Car car = newmypackage.Car();
car.startEngine();
```

  
==Pun naziv jedne klase sastoji se iz naziva paketa i naziva klase,== koji su međusobno razdvojeni karakterom tačka, baš kao u prikazanom primeru. Ipak, ovakvo rešenje, iako funkcionalno, ne smatra se elegantnim, pogotovu ukoliko je klasu potrebno instancirati veliki broj puta.

Umesto prikazanog pristupa, ==u praksi se najčešće pribegava procesu koji se naziva **uvoz ili importovanje**== (import) klase iz jednog paketa u klasu koja se nalazi u nekom drugom paketu. Posao importovanja se obavlja korišćenjem ključne reči **import**:

```java
importmypackage.Car;
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        Car car = newCar();
        car.startEngine();
    }
}
```

Sada je na samom početku dodata naredba za uključivanje klase Car u tekući dokument. Nakon takve naredbe, ==klasu Car je moguće koristiti kao da je deo aktuelnog paketa.==

==Ponekad== će se javiti ==potreba za importovanjem većeg broja klasa iz jednog paketa:==

```java
importmypackage.MyClass;
importmypackage.MyClass1;
importmypackage.MyClass2;
```

  
Ukoliko je potrebno importovati sve klase koje nalaze u jednom paketu, nakon naziva paketa navodi se karakter tačka i nakon njega zvezdica:

```java
importmypackage.*;
```

### Više klasa sa identičnim nazivom

Paketi, između ostalog, omogućavaju da unutar jednog Java programa postoji veći broj klasa sa identičnim nazivom. ==Unutar jednog paketa, sve klase moraju imati jedinstvene nazive==, ali ==dve klase koje se nalaze u različitim paketima mogu imati identična imena==. To ćete moći da vidite u narednim redovima.

U dosadašnjem toku lekcije kreiran je paket mypackage. Ponovimo sada proces kreiranja paketa, tako da dobijemo još jedan paket sa nazivom yourpackage. Struktura našeg projekta će zatim izgledati kao na slici 15.6.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_06.png)*

*Slika 15.6. Java projekat sa dva paketa  
  
*

Kreirajmo sada u svakom od paketa po jednu klasu, sa identičnim nazivom – MyClass.

Nakon kreiranja klasa MyClass u svakom od paketa, sadržaje oba naša paketa možemo importovati unutar glavne klase na sledeći način:

```java
importmypackage.*;
importyourpackage.*;
```

  
Ukoliko sada pokušamo da instanciramo klasu MyClass, doći će do sledećeg problema (slika 15.7).

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_07.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_07-original.png)

*Slika 15.7. Problem koji nastaje usled postojanja dve klase sa istim imenima u dva različita importovana paketa  
  
*

Razvojno okruženje jasno signalizira da je naziv klase MyClass dvosmislen, s obzirom na to da klasa sa ovim nazivom postoji u oba uključena paketa. U ovakvim situacijama mora se pribeći definisanju punog naziva klasa prilikom njihovog korišćenja u kodu:

```java
mypackage.MyClass mc = newmypackage.MyClass();
yourpackage.MyClass mc2 = newyourpackage.MyClass();
```

### Paketi unutar paketa

Pored klasa, sadržaj paketa mogu biti i drugi paketi. Tako je ==moguće napraviti paketnu strukturu dublju od jednog nivoa. Paket unutar paketa== se može kreirati na već prikazan način, aktiviranjem opcije **New -> Package**. Ipak, kontekstni meni je potrebno aktivirati nad već kreiranim paketom (slika 15.8).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_08.png)

*Slika 15.8.* *Kreiranje potpaketa  
  
*

Unutar IntelliJ IDEA razvojnog okruženja, različiti nivoi paketa se odvajaju karakterom tačka. Kada pokrenemo opciju za kreiranje potpaketa, unutar prozora za unos njegovog naziva već dobijemo pripremljen prefiks (slika 15.9).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_09.png)

*Slika 15.9.* *Unos naziva potpaketa  
  
*

Na nama je samo da unesemo naziv potpaketa, što je u primeru subpackage. IntelliJ IDEA će obaviti kreiranje novog foldera sa nazivom subpackage, koji će postaviti unutar foldera mypackage.

Ukoliko sada našu klasu Car premestimo u potpaket subpackage, bitno je da primetite zanimljivu osobinu. U==koliko pokušamo da importujemo sve članove mypackage paketa, nećemo biti u mogućnosti da koristimo našu klasu Car==:

```java
importmypackage.*;
```

  
Iako se možda čini da se na ovaj način automatski importuju i sve klase potpaketa subpackage, to nije slučaj. ==Sadržaj takvog paketa moramo eksplicitno importovati:==

```java
importmypackage.*;
importmypackage.subpackage.*;
```

### Ugrađeni paketi u jeziku Java

U dosadašnjem toku lekcije bavili smo se pojmom paketa na primeru onih koje smo samostalno kreirali. Ipak, kao što već znate, sastavni deo Java platforme je i velika količina gotovih funkcionalnosti koje su nam dostupne za korišćenje. Takve funkcionalnosti strukturirane su korišćenjem paketa, pa se zbog toga kaže da, pored paketa koje samostalno možemo da kreiramo, ==postoje i [ugrađeni](https://www.link-elearning.com/linkdl/opisPojma.php?id=160439 "ugrađeni") paketi==. Standardni paketi koji su ugrađeni u programski jezik Java organizovani su u hijerarhijsku strukturu kao na slici 15.10.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_10.png)

*Slika 15.10.* *Struktura ugrađenih paketa  
  
*

Na slici 15.10. možete videti da su koreni ugrađeni paketi **java** i **javax***.* Neko opšte pravilo je da su java paketi bazni, a javax paketi nadogradnje. Takođe, ==ugrađeni paketi imaju i svoje potpakete. Na primer, potpaket paketa java je awt, dok awt ima svoj potpaket event*.*==

==Neki od najznačajnijih ugrađenih Java paketa i njihovi kratki opisi prikazani su u tabeli== 15.1.

| **Naziv paketa** | **Opis** |
| --- | --- |
| java.lang | osnovne funkcionalnosti jezika Java, kao što su ugrađeni tipovi |
| java.util | kolekcije, događaji, internacionalizacija |
| java.io | rad sa ulaznim i izlaznim tokovima podataka |
| java.math | BigInteger, BigDecimal |
| java.nio | rad sa baferima |
| java.net | podrška za mrežu, URL, socket programiranje, IP adrese |
| java.security | podrška sigurnosti, enkripcija, dekripcija, generisanje ključeva |
| java.sql | podrška za rad sa bazama podataka |
| java.awt | integrisani set klasa za stvaranje korisničkog interfejsa |
| java.applet | podrška za kreiranje appleta |
| java.time | rukovanje datumom i vremenom |

*  
Tabela 15.1. Pregled najznačajnijih ugrađenih Java paketa  
*  

==Jedini ugrađeni paket koji ne zahteva prethodno importovanje je **java.lang**.== Ovaj paket se automatski importuje u svaki Java program. Svi ostali paketi zahtevaju importovanje, odnosno referenciranje u okviru klase u kojoj se koriste. Na primer, ukoliko bismo želeli da iskoristimo klasu Rectangle koja se nalazi u paketu java.awt, ne bi bilo dovoljno da napišemo samo ovako:

```java
Rectangle rectangle = newRectangle();
```

  
Pod uslovom da u našem programu nema klase sa ovim nazivom koju smo samostalno kreirali, kompajler neće moći da zna gde je potrebno da potraži klasu sa nazivom Rectangle. Stoga mu mi to moramo reći:

```java
importjava.awt.*;
```

  
Na ovaj način smo obavili importovanje svih klasa koje se nalaze unutar paketa java.awt. Klasu Rectangle smo mogli importovati i pojedinačno:

```java
importjava.awt.Rectangle;
```

| **IntelliJ IDEA Tip**  **Automatsko importovanje**  IntelliJ IDEA razvojno okruženje poseduje nekoliko načina na koje samostalno, umesto nas, može da obavi dodavanje neophodne naredbe za importovanje klasa koje se nalaze u nekim drugim paketima.  Prvi način je da prilikom pisanja naredbe za instanciranje klase odaberete odgovarajuću klasu iz prozora sa ponuđenim tipovima (slika 15.11).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_11.png)*  *Slika 15.11. Odabirom ponuđenog tipa, automatski se dodaje i naredba za uvoz, ukoliko je potrebno      *  Kada unesete naziv Rectangle, razvojno okruženje će vam ponuditi sve klase koje u svom nazivu poseduju unetu reč. Potrebno je da se pozicionirate na Rectangle klasu iz paketa java.awt i pritisnete Enter. IntelliJ IDEA će automatski na početak dokumenta dodati naredbu za import:  ```java importjava.awt.*; ```     Drugi način za automatsko dodavanje import naredbe jeste odabir opcije *Import class*, koja se može naći u panelu koji se otvara kada pokazivač miša pozicionirate preko klase koja još nije importovana (slika 15.12).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_12.png)*  *Slika 15.12. Opcija za import      *  Pod uslovom da IntelliJ IDEA može da detektuje gde se takva klasa nalazi, obaviće automatsko importovanje. |
| --- |

### Vežba

Potrebno je napraviti Java program koji od korisnika može da preuzme ime i da mu zatim uputi pozdravnu poruku koja će sadržati ime koje je korisnik uneo u program. Za obavljanje ovakvog posla potrebno je koristiti klasu Scanner, koja se nalazi unutar paketa java.util.

**  
Rešenje**

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        Scanner scanner = newScanner(System.in);
        System.out.println("Please, enter your name:");
 
        String username = scanner.nextLine();
        System.out.println("Hello: "+ username);
 
    }
 
}
```

**  
Objašnjenje:**

Prikazani primer je vrlo jednostavan, ali i pored toga omogućava nam da u nastavku kreiramo mnogo naprednije Java programe. Sa razlogom smo sačekali sve do sada kako bismo u priču o Java programiranju uveli pojam klase Scanner. Klasa Scanner je jedna od ugrađenih funkcionalnosti Java platforme i nalazi se unutar java.util paketa. Stoga, kako bi se koristila, neophodno je obaviti njen import, što je u prikazanom primeru i učinjeno.

Nakon uvoza, obavljano je instanciranje klase Scanner, pa smo na taj način dobili objekat ove klase. Nad objektom klase Scanner je pozvana metoda nextLine, koja čini da se program zaustavi u takvoj naredbi i da čeka korisnički unos. Stoga, kada korisnik unese svoje ime i pritisne Enter, takva vrednost će biti smeštena unutar promenljive username, pa nama preostaje samo da je uvrstimo unutar poruke koju emitujemo na izlazu (slika 15.13).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_15_13.png)*

*Slika 15.13. Primer funkcionisanja programa*

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_15.thb) JCPR1\_15.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_15.Mp4")

Kako Vam mogu pomoći?