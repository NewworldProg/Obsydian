---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=4301ba98f5ab3d9013441c8436f489db_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434681"
author:
published:
created: 2025-04-30
description:
tags:
  - "clippings"
---
Jedinica 14 od 22

## Klase i objekti

Više puta u dosadašnjem toku ovog kursa rečeno je da je Java objektno orijentisan programski jezik. To praktično znači da su klase i objekti njegova centralna figura. Takođe, rečeno je i da nećemo biti u mogućnosti da u potpunosti razumemo kompletan kod primera koji su do sada kreirani sve dok se ne upoznamo sa pojmom objekata i klasa. Stoga će kompletan modul pred vama biti posvećen tim veoma važnim pojmovima Java programiranja.  
  

### Šta su klase i objekti?

Objekti su način da se unutar Java programa predstave podaci po uzoru na pojmove iz realnog sveta. Na primer, ukoliko unutar Java programa želimo da predstavimo podatke studenata, svaki student bi predstavljao jedan objekat u našem programu. Po istom principu, ukoliko bismo želeli unutar našeg programa da predstavimo podatke različitih automobila, svaki pojedinačni automobil bi bio jedan objekat. Stoga se može reći i to da je objekat instanca, odnosno jedan primerak nečega (slika 14.1).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_01.png)

*Slika 14.1. Primer različitih automobila koji se u programu mogu predstaviti objektima  
  
*

Na slici 14.1. prikazana su tri različita automobila, pri čemu svaki od ovakvih automobila unutar Java programa može biti po jedan objekat.

Objekti se kreiraju na osnovu određenog šablona, odnosno modela. U objektno orijentisanom programiranju takvi šabloni se drugačije nazivaju **klase** (slika 14.2).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_02.png)*

*Slika 14.2. Objekti se kreiraju na osnovu klasa  
  
*

Slika 14.2. dočarava odnos između klasa i objekata. Klasa je šablon, odnosno model na osnovu koga nastaju objekti. Na osnovu jedne klase se može stvoriti proizvoljan broj objekata, pri čemu svaki objekat može imati različite osobine. Tako su svi objekti sa slike 14.2. automobili, ali automobili različitih osobina. Jedan se zove *Renault 4L* i plave je boje, drugi se zove *Geely TX4* i ima žutu boju, dok je treći crni *Ford Crown Victoria*.  
  

### Kreiranje klasa

U objektno orijentisanom programiranju, klasa se može doživeti kao kalup, a objekti kao kolači koji se na osnovu takvog kalupa izlivaju. Kao što nije moguće napraviti takav kolač bez kalupa, ni objekat se ne može kreirati bez klase.

Klasa se kreira na sledeći način:

```java
classCar {
 
}
```

  
Struktura klase u Java jeziku može se predstaviti kao na slici 14.3.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_03.png)*

*Slika 14.3. Osnovna struktura klase  
  
*

U programskom jeziku Java, klase se kreiraju korišćenjem ključne reči **class**, nakon koje sledi naziv klase. U prikazanom primeru, naziv klase je **Car**. Ključna reč class i naziv klase zajednički se nazivaju **zaglavlje klase**. Nakon zaglavlja, sledi **telo klase**, koje je oivičeno vitičastim zagradama. Tako je telo Java klase jedna vrsta bloka koda u sintaksnoj hijerarhiji jezika.

| **Klase u dosadašnjem toku ovog kursa**  Pojam klasa za nas nije potpuna nepoznanica, zato što smo se sa njima već više puta susretali. Za početak, prilikom kreiranja našeg prvog Java programa, bili smo u obavezi da kreiramo jednu Java klasu. Takođe, u prethodnim lekcijama koristili smo i neke klase koje su ugrađene u sam Java jezik – String, Integer... |
| --- |

| **IntelliJ IDEA Tip**  **Kreiranje nove klase**  Korišćenjem IntelliJ IDEA razvojnog okruženja, kreiranje nove klase se može obaviti praćenjem sledećih koraka. Iz kontekstnog menija koji se dobija desnim klikom na folder src potrebno je odabrati opciju **New -> Java Class** (slika 14.4).  [![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_04.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_04-original.png)  *Slika 14.4. Opcija za kreiranje nove klase      *  U prozoru koji se zatim otvara potrebno je uneti naziv klase (slika 14.5).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_05.png)  *Slika 14.5. Prozor za kreiranje nove klase      *  Kreiranje klase se može pokrenuti duplim klikom na opciju *Class* ili odabirom tastera Enter na tastaturi. IntelliJ IDEA će na ovaj način unutar foldera src kreirati novi fajl sa imenom klase, i unutar njega sledeći kod:  ```java publicclassCar {   } ``` |
| --- |

### Osnovni klasni članovi

Telo upravo kreirane klase je prazno, zato što između otvorene i zatvorene vitičaste zagrade nema ničega. Unutar tela klase, može se naći izvorni kod kojim se kreiraju dva osnovna tipa njenih članova:

- svojstva (polja);
- metode

**Svojstva** su zapravo promenljive koje se deklarišu direktno unutar klasa:

```java
classCar {
    String make;
    String model;
}
```

  
Unutar klase Car sada smo definisali dva svojstva. To su zapravo dve promenljive tipa String, unutar kojih će se čuvati informacije o proizvođaču i modelu automobila.

Pored svojstava, unutar klasa se mogu naći i **metode**. Metodama se definišu funkcionalnosti koje su vezane za namenu klase:

```java
classCar {
    String make;
    String model;
 
    voidstartEngine(){
        System.out.println("Engine started...");
    }
}
```

  
Unutar klase Car sada je dodata i jedna metoda. Iz sintaksnog ugla jezika, reč je o jednom bloku, unutar koga se objedinjuje kod koji treba da obavi neku operaciju. Stoga je upravo kreirana metoda slikovita – ona treba da pokrene motor jednog automobila.  
  

### Kreiranje objekata

Sada kada imamo klasu koju smo samostalno definisali, nju možemo iskoristiti za kreiranje objekata. Jedan objekat na osnovu klase Car se može kreirati na sledeći način:

```java
Car myCar = newCar();
```

  
Upravo prikazanu naredbu je potrebno da postavite unutar main metode Java programa. Korišćenjem ovakve naredbe obavlja se kreiranje objekta. Objekat se kreira upotrebom ključne reči **new**, nakon koje se navode naziv klase i zagrade.

Prikazanom naredbom zapravo se obavlja deklarisanje i inicijalizovanje jedne promenljive. Stoga je prikazanu naredbu bilo moguće razdvojiti na dva dela:

```java
Car myCar;
myCar = newCar();
```

  
Ovo je sada primer koji podrazumeva odvojenu deklaraciju i inicijalizaciju jedne promenljive preko koje će u programu biti dostupan kreirani objekat.

| **Korisnički definisani tipovi podataka**  Bitno je da primetite razliku između upravo prikazanog primera deklaracije promenljive i onih iz prethodnih lekcija ovog kursa. Naime, na mestu na kome se definiše tip promenljive stoji reč Car. Iz ovoga možemo da zaključimo da je tip promenljive myCar – Car. To na kraju znači da smo kreiranjem klase Car prvi put obavili kreiranje jednog korisnički definisanog tipa. Kada se za neki tip kaže da je korisnički definisan, to znači da on ne postoji kao deo Java jezika. Drugim rečima, mi smo ga samostalno kreirali. Tako se može reći da u Javi postoje dve vrste tipova:  - ugrađeni (int, float, String, Integer...); - korisnički (programer ima mogućnost da samostalno kreira proizvoljan broj sopstvenih tipova). |
| --- |

Proces kreiranja objekata drugačije se naziva **instanciranje klase**. Instanciranjem klase kreira se jedna njena instanca, odnosno objekat, koji u kodu postaje dostupan kroz promenljivu. Na osnovu jedne klase moguće je napraviti proizvoljan broj objekata:

```java
Car myCar = newCar();
Car myCar2 = newCar();
```

  
Ovo su sada dva objekta kreirana instanciranjem jedne iste klase. Na identičan način je moguće kreirati proizvoljan broj objekata. Zajedničko za sve kreirane objekte je da unutar njih postoje svojstva i metode koji su definisani unutar klase. Kreiranim svojstvima i metodama je moguće pristupiti navođenjem naziva promenljive i karaktera tačka (slika 14.6).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_06.png)*

*Slika 14.6. Pristup svojstvima i metodama  
  
*

S obzirom na to da su svojstva zapravo promenljive koje se definišu unutar klasa, njima je moguće operisati korišćenjem pristupa koji su već ilustrovani:

```java
Car myCar = newCar();
myCar.make = "Honda";
myCar.model = "Accord";
```

  
Ovakvim kodom definisane su vrednosti svojstava make i model objekta koji je kreiran na osnovu klase Car. Na ovaj način, objekat jednog automobila u našem programu počinje da dobija svoj oblik.

Drugi objekat koji je kreiran na osnovu klase Car može se konfigurisati na sledeći način:

```java
Car myCar2 = newCar();
myCar2.make = "Lexus";
myCar2.model = "LS500";
```

  
Naš drugi objekat kreiran na osnovu klase Car poseduje drugačije vrednosti svojstava make i model. Na ovaj način smo dobili dva objekta koji imaju isti tip (Car), ali se koriste da u našem programu predstave dva različita automobila.

| **Složeni tipovi podataka**  Tipovi podataka detaljno su obrađeni u prethodnom modulu ovog kursa. Tada ste mogli da pročitate da je osnovna podela svih tipova na proste i složene. Prethodni modul je prevashodno bio posvećen radu sa prostim tipovima. Sada, upoznavanjem sa klasama, započinjemo rad i sa složenim tipovima. Svaka klasa je primer složenog tipa podataka, zato što unutar sebe može da objedini veliki broj pojedinačnih vrednosti (svojstava) i ponašanja (metoda). To možete videti i na slici 14.6. Promenljive myCar i myCar2, unutar kojih se nalaze složeni tipovi podataka, omogućavaju pristup brojnim svojstvima i metodama, što nije bio slučaj sa promenljivama prostih tipova. |
| --- |

| **Nasleđivanje**  Na slici 14.6. možete videti još jednu zanimljivu osobinu objektno orijentisanog programiranja. Kada se nakon naziva promenljive koja pokazuje na objekat unese karakter tačka, IntelliJ IDEA prikazuje sve klasne članove koje je moguće koristiti nad takvim objektom. Na početku su tu klasni članovi koje smo samostalno kreirali – make, model i startEngine(). Pored ovih članova, na slici 14.6. možete videti i brojne druge, koje nismo samostalno kreirali. Kao logično se nameće pitanje – odakle oni tu?  Jedna od osnovnih osobina objektno orijentisanog programiranja jeste i nasleđivanje. Nasleđivanje je pojam koji omogućava da jedna klasa nasledi osobine od neke druge klase. Upravo je nasleđivanje „krivac” zbog koga je pomoću promenljive sa slike 14.6. moguće pristupiti određenim klasnim elementima koje nismo kreirali u klasi Car. Svi takvi elementi potiču iz osnovne klase Java jezika. Reč je o klasi Object.  Sve klase u Java programskom jeziku, bez obzira na to da li je reč o ugrađenim klasama ili klasama koje mi samostalno kreiramo, nasleđuju klasu Object. Upravo to je razlog zbog koga objekti naše klase Car poseduju elemente koje mi nismo eksplicitno definisali u samoj klasi.  O nasleđivanju će više reči biti u jednoj od narednih lekcija. |
| --- |

### Metode

U prethodnim redovima ste mogli da pročitate da su, pored svojstava, metode osnovni klasni članovi. Metode su način za grupisanje određene funkcionalnosti u jednu celinu. Stoga se metode u drugim programskim jezicima često nazivaju i funkcije. Ipak, zbog objektne orijentacije Java jezika, funkcije imaju naziv metode, što označava da se one nalaze unutar klasa. Drugim rečima, u Javi nije ni moguće napraviti funkciju/metodu koja se nalazi izvan neke klase. U jezicima u kojima je to moguće, sve funkcionalnosti su funkcije, a one unutar klasa se nazivaju metode. Stoga ćemo ovde nastaviti da koristimo isključivo pojam *metoda*.

Metoda je specijalni blok koda, zadužen za izvršenje određene logike. Metoda prilikom izvršavanja logike može da koristi određene vrednosti, koje se nazivaju **ulazni parametri**, a može i emitovati svoj rezultat kao **povratnu vrednost** (slika 14.7).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_07.png)*

*Slika 14.7. Metoda  
  
*

Na slici 14.7, slovom x je označen ulazni parametar, odnosno vrednost koju metoda dobija na obradu. Nakon obrade, metoda emituje rezultat izvršavanja. Ipak, nije obavezno da metoda ima ulazne i uzlazne parametre.

U nešto ranije kreiranoj Java klasi, prvoj koju smo kreirali, nalazila se i jedna metoda:

```java
voidstartEngine() {
    System.out.println("Engine started...");
}
```

  
Ovo je primer metode koja nema ulaznih ni izlaznih parametara. Sve što ona obavlja jeste ispis jedne poruke na izlazu. Ključna reč **void** označava da metoda nema povratnu vrednost, a na osnovu praznih zagrada nakon njenog naziva može se zaključiti da ona nema ulaznih parametara.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_08.png)

*Slika 14.8. Osnovna struktura metode bez parametara  
  
*

Sa slike 14.8. možete da vidite osnovnu strukturu metoda u Java jeziku. Metode se sastoje iz potpisa i tela. Potpis obuhvata:

- tip povratne vrednosti (u primeru void);
- naziv metode (u primeru startEngine);
- eventualne ulazne parametre koji se navode unutar zagrada, nakon naziva metoda (u primeru ()).

Telo metode se definiše upotrebom vitičastih zagrada. Unutar njih se definiše logika metode.

Kako bi se aktivirao kod koji se nalazi unutar neke metode, nju je potrebno pozvati. **Poziv metode** obavlja se navođenjem njenog naziva i zagrada:

```java
Car myCar = newCar();
myCar.startEngine();
```

Ovo je kod koji ilustruje način na koji se poziva metoda startEngine koja se nalazi unutar klase Car. Efekat ovakvog koda jeste ispis poruke Engine started..., što je produkt koda koji se nalazi unutar tela metode.

Evo kako može izgledati jedna metoda koja poseduje i ulazne i izlazne parametre:

```java
doublekwToHp(intkw) {
  doubleresult = kw / 0.745699872;
  returnresult;
}
```

  
Struktura ove metode predstavljena je slikom 14.9.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_09.png)

*Slika 14.9. Osnovna struktura metode sa ulaznim i izlaznim parametrima  
  
*

Ovo je metoda koja je namenjena konverziji snage motora iz kilovata u konjske snage. Metoda prihvata jedan parametar tipa int (kw), što je zapravo snaga motora u kilovatima. Ulazni parametar možete videti unutar zagrada, nakon naziva metode. Unutar tela metode, obavlja se računanje vrednosti, koja se postavlja za vrednost promenljive result. Na kraju se vrednost takve promenljive emituje kao povratna. Emitovanje povratne vrednosti se postiže upotrebom ključne reči return, dok je tip povratne vrednosti definisan unutar potpisa metode.

Ovakva metoda je mogla biti jednostavnije formulisana na sledeći način:

```java
doublekwToHp(intkw){
  returnkw / 0.745699872;
}
```

  
Sada je izbegnuto deklarisanje promenljive unutar tela metode, pa se vrednost računanja direktno emituje kao povratna. Efekat je identičan.

Metoda kwToHp se može pozvati na sledeći način:

```java
Car myCar = newCar();
myCar.kwToHp(147);
```

  
Nad promenljivom kojom se predstavlja jedan objekat automobila pozvana je metoda kwToHp i tom prilikom joj je prosleđena vrednost 147. Može se reći da je 147 ulazni parametar ove metode. Ovakav kod će se izvršiti i metoda kwToHp će svoj rezultat isporučiti kao povratnu vrednost. Ipak, ukoliko želimo da dobijemo takav rezultat, neophodno je da ga smestimo unutar promenljive:

```java
doublehpPower = myCar.kwToHp(147);
System.out.println(hpPower);
```

Naredba u kojoj se poziva metoda kwToHp sada je neznatno izmenjena, deklaracijom promenljive hpPower. Ova promenljiva se inicijalizuje povratnom vrednošću metode kwToHp.

### Konstruktori

Nešto ranije ste videli na koji način se obavlja instaciranje klase:

```java
Car myCar = newCar();
```

  
Do sada je rečeno da instanciranje podrazumeva upotrebu ključne reči new, ali se do sada nismo posebno bavili onim što dolazi nakon ove ključne reči. Nakon ključne reči možete videti nešto što podseća na poziv metode čije je ime Car. Zapravo, deo nakon ključne reči new i jeste poziv metode, ali jedne specijalne metode koja se naziva konstruktor.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_10.png)

*Slika 14.10. Osnovna struktura naredbe za pozivanje konstruktora  
  
*

Konstruktor je specijalna metoda unutar klase, koja se poziva prilikom kreiranja objekata. Svaka klasa može imati jedan ili više konstruktora. Drugim rečima, ne postoji klasa bez konstruktora. Možda se u ovom trenutku pitate zbog čega onda u klasi koju smo kreirali ne postoji konstruktor. Odgovor je vrlo jednostavan: kada se konstruktor ne napiše eksplicitno, Java kompajler kreira konstruktor koji se naziva podrazumevani. Reč je zapravo o metodi koja ima isto ime kao i klasa, nema ulaznih ni izlaznih parametara, a telo joj je prazno. Takav konstruktor izgleda ovako:

```java
classCar {
    Car() {
    }
}
```

  
Ukoliko objekte kreiramo na način na koji je to obavljeno u jednom od prethodnih poglavlja, nema nikakve potrebe da konstruktor samostalno definišemo. Ipak, ukoliko želimo da na neki način prilagodimo proces kreiranja objekata, moguće je samostalno definisati konstruktor:

```java
classCar {
 
    String make;
    String model;
 
    Car(String _make, String _model) {
        make = _make;
        model = _model;
    }
}
```

  
Ovo je sada klasa u kojoj smo samostalno definisali konstruktor. Možete da vidite da je konstruktor uistinu metoda, koja u ovom primeru prihvata dva ulazna parametra i njihove vrednosti dodeljuje svojstvima make i model.

Klasa sa ovakvim konstruktorom više se ne može instancirati kao do sada. Tokom instanciranja, konstruktoru je neophodno proslediti ulazne parametre:

```java
Car myCar = newCar("Honda", "Accord");
```

  
Samostalnim definisanjem konstruktora, podrazumevani prestaje da postoji. Stoga je jedini konstruktor koji u ovom trenutku postoji u našoj klasi onaj koji prihvata dva parametra. Ipak, kao što je već rečeno, jedna klasa može imati veći broj konstruktora:

```java
classCar {
 
    String make;
    String model;
 
    Car(){
 
    }
    Car(String _make, String _model) {
        make = _make;
        model = _model;
 
    }
}
```

  
Klasa Car sada poseduje dva konstruktora. Jedan je bez parametara i bilo kakve logike, dok drugi, kao i u prethodnom primeru, prihvata dva parametra. U ovakvim situacijama je moguće birati način za obavlja instanciranja:

```java
Car myCar = newCar("Honda", "Accord");
Car myCar2 = newCar();
```

  
Obe naredbe za kreiranje objekata su validne, zato što klasa Car sada poseduje dva konstruktora.

| **Overloading**  Upravo prikazani slučaj postojanja dva konstruktora sa različitim ulaznim parametrima primer je osobine Java jezika koja se naziva *overloading*. *Overloading* je zapravo mogućnost preklapanja metoda, odnosno postojanja metoda sa istim nazivom, ali različitim sklopom ulaznih parametara. O ovom pojmu će više reči biti u jednoj od narednih lekcija. |
| --- |

### this

Nešto ranije, prilikom samostalnog definisanja konstruktora sa parametrima, napisali smo ovako nešto:

```java
classCar {
 
    String make;
    String model;
 
    Car(String _make, String _model) {
        make = _make;
        model = _model;
    }
}
```

  
Obratite pažnju na to da smo parametre koje prihvata konstruktor imenovali sa početnim karakterom donja crta, kako bi se njihova imena razlikovala od svojstava definisanih unutar klase. Svakako, bilo bi najbolje da i oni imaju identičan naziv:

```java
Car(String make, String model) {
        make = make;
        model = model;
}
```

  
Iako ovakav kod ne bi proizveo sintaksu grešku, efekat ne bi bio očekivan. Na ovaj način uopšte i ne bi bile postavljene vrednosti klasnih svojstava make i model, zato što se u ovakvoj situaciji nazivi make i model odnose na parametre konstruktora. Kako bi kod obavio ono što želimo bez izmene naziva parametara, neophodno je da iskoristimo jednu do sada nepoznatu mogućnost jezika. To je ključna reč **this**.

Ključna reč this omogućava pristup objektu unutar metoda i konstruktora klase. Izvan klase, kao što ste već mogli da vidite, nakon njenog instanciranja, objekat se reprezentuje kroz promenljivu. Ipak, ukoliko je to isto potrebno uraditi unutar klase, pribegava se korišćenju ključne reči this.

Ključna reč this nam omogućava i da učinimo da kod iz našeg konstruktora obavlja ono što smo zamislili:

```java
Car(String make, String model) {
        this.make = make;
        this.model = model;
}
```

  
Promenljive sa istim nazivima sada se razlikuju pomoću ključne reči this. Svojstvima make i model pristupili smo pomoću ključne reči this, na identičan način kao i korišćenjem promenljive izvan klase.

| **Prosti i složeni tipovi i čuvanje unutar memorije**  S obzirom na to da u ovom trenutku znamo što su to prosti, ali i složeni tipovi u Javi, možemo da govorimo o načinu na koji se oni smeštaju u memoriju. Naime, u jednoj od prethodnih lekcija u kojima je bilo reči o tipovima podataka, rečeno je da se složeni tipovi drugačije nazivaju i **referentni**. Kako biste razumeli odakle dolazi ovaj pojam *referentni*, neophodno je da se pozabavimo načinom na kojim se prosti i složeni tipovi smeštaju u memoriju.  Svaki podatak, bez obzira na to da li je prost ili složen, zauzima određeno mesto u memoriji. Ipak, prosti i složeni tipovi se smeštaju u različitim delovima radne memorije. Prosti tipovi se smeštaju na statički deo memorije, koji se naziva **Stack**, gde zauzimaju svoj prostor prilikom aktivacije programa. Sa druge strane, složeni tipovi se smeštaju u dinamičkom memorijskom delu, koji se naziva **Heap.** Unutar Stacka se čuva samo adresa koja pokazuje na njihovu stvarnu vrednost u dinamičkoj memoriji (slika 14.11).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_14_11.png)*  *Slika 14.11. Čuvanje prostih i složenih podataka unutar memorije      *  Slika 14.11. ilustruje uprošćen prikaz memorijske strukture programa unutar koga su definisane tri vrednosti. Dve su objekti, dok je treća celobrojna numerička vrednost. U Java programu, takve vrednosti bi mogle da izgledaju ovako:  ```java Car myCar = newCar(); intmyNumber = 16; Car myCar2 = newCar(); ```     Sa slike 14.11. možete videti da je prosta vrednost (16) direktno smeštena unutar statičkog dela memorije (*Stack*). Kod složenih tipova, na statičkom delu memorije smešta se samo referenca koja pokazuje na stvarnu vrednost koja je uskladištena unutar dinamičkog dela memorije, koji se naziva *Heap*. Upravo zbog ove činjenice se složeni tipovi nazivaju referentni, a za promenljive kaže da čuvaju samo referencu do objekta a ne stvarnu vrednost.  Razlog ovoga leži u različitoj veličini memorije koju primitivni i referentni tipovi mogu da zauzmu. Svaki primitivni tip ima unapred definisanu količinu memorije koju zauzima u memoriji. To ste, uostalom, mogli da vidite u jednoj od prethodnih lekcija, u kojoj je bilo reči o prostim tipovima. Ipak, tako nešto nije slučaj kod složenih tipova. S obzirom na to da oni mogu biti sačinjeni iz proizvoljnog broja prostih vrednosti i ponašanja, količina potrebne memorije za njihovo čuvanje nije unapred poznata. Upravo zbog toga se pribegava čuvanju složenih tipova unutar dinamičkog dela memorije. Java virtuelna mašina poseduje kompleksne mehanizme za rukovanje takvom vrstom memorije, što na kraju omogućava čuvanje vrednosti čija veličina nije unapred poznata – i to sve bez ikakve intervencije programera. Zbog toga se kaže da Java jezik poseduje ugrađene mehanizme za rukovanje memorijom koji programera oslobađaju potrebe za samostalnom [alokacijom](https://www.link-elearning.com/linkdl/opisPojma.php?id=160488 "alokacijom") i oslobađanjem memorije. |
| --- |

### Vežba

Potrebno je kreirati klasu kalkulator (Calculator). Unutar klase je potrebno da se nađu četiri metode za obavljanje osnovnih aritmetičkih operacija – sabiranja, oduzimanja, množenja i deljenja. Brojeve nad kojima će se obavljati takve operacije potrebno je smestiti unutar svojstava objekata. Takođe, potrebno je osigurati da se objekat klase Calculator ne može kreirati bez navođenja dva broja.

**Rešenje**

```java
publicclassCalculator {
 
    doublenumA;
    doublenumB;
 
    Calculator(doublenumA, doublenumB) {
        this.numA = numA;
        this.numB = numB;
    }
 
    doubleadd() {
        returnnumA + numB;
    }
 
    doublesubtract() {
        returnnumA - numB;
    }
 
    doublemultiply() {
        returnnumA * numB;
    }
 
    doubledivide() {
        returnnumA / numB;
    }
}
```

**  
Primer upotrebe:**

```java
Calculator calculator = newCalculator(15, 5);
 
System.out.println(calculator.add());
System.out.println(calculator.subtract());
System.out.println(calculator.multiply());
System.out.println(calculator.divide());
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_14.thb) JCPR1\_14.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_14.Mp4")

Kako Vam mogu pomoći?