---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=534997ee6090c46fdc29860655676b49_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434679"
author:
published:
created: 2025-04-29
description:
tags:
  - "clippings"
---
Jedinica 12 od 22

## Switch

U prethodnoj lekciji ilustrovan je jedan način za postizanje uslovnog izvršavanja, grananja, odnosno selekcije. Pristup je podrazumevao upotrebu if, else if i else naredbi, odnosno uslovnih blokova koji se korišćenjem ovih ključnih reči formiraju. U ovoj lekciji nastavljamo priču o načinima za postizanje uslovnog izvršavanja. Tako je na redu priča o naredbi switch.  
  

### Šta je switch?

switch je još jedna naredba za kontrolisanje toka koja postoji unutar Java jezika. Ova naredba omogućava kontrolisanje toka, baš kao što je to bio slučaj i sa if, else if i else naredbama. Ipak, switch to obavlja na nešto drugačiji način:

```java
switch(expression) {
    caselabel_1:
        statements_1
        break;
    caselabel_2:
        statements_2
        break;
    default:
        statements_def
        break;
}
```

  
switch naredba poredi expression vrednost sa vrednostima case klauzula. U prikazanom primeru, vrednosti case klauzula su obeležene sa label\_1, label\_2 itd.

==Kada se utvrdi podudaranje expression vrednosti sa nekom od case klauzula, izvršavanje programa se preusmerava na taj blok==. U slučaju da se ne pronađu podudaranja, izvršava se opcioni default blok.

Logika switch naredbe ilustrovana je slikom 12.1.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_12_01.png)

Slika 12.1. Switch naredba  
  

### Primer korišćenja switch naredbe

Praktičan primer upotrebe switch naredbe može da izgleda ovako:

```java
intx = 1;
switch(x) {
    case0:
        System.out.println("zero");
        break;
    case1:
        System.out.println("one");
        break;
    default:
        System.out.println("unknown value");
        break;
}
```

  
U prikazanom primeru, kreirana je jedna switch naredba koja u zavisnosti od vrednosti promenljive x obavlja emitovanje određene tekstualne vrednosti. Kada je vrednost promenljive x jednaka 0, na izlazu se ispisuje zero. Kada je vrednost promenljive x jednaka 1, na izlazu se ispisuje one. Na kraju, ukoliko je vrednost promenljive x bilo šta osim brojeva 0 i 1, na izlazu se ispisuje tekst unknown value.

Unutar switch naredbe obavlja se utvrđivanje jednakosti kontrolne vrednosti (što je u primeru x) sa vrednostima pojedinačnih case blokova (to su vrednosti nakon ključnih reči case). Drugim rečima, switch dozvoljava kreiranje logičkih uslova u kojima se proverava jednakost, ali ne i ostali logički uslovi (veće, manje, nejednako...).

| **Tip kontrolne vrednosti kod switcha**  U upravo prikazanom primeru ste mogli da vidite da je kontrolna vrednost koju switch dobija int tipa (reč je o vrednosti koja se navodi u zagradama nakon ključne reči switch i na osnovu koje se odlučuje koji će slučaj biti aktiviran). Nije obavezno da kontrolna vrednost bude int tipa. Tako je dozvoljeno korišćenje sledećih tipova: char, byte, short, int, Character, Byte, Short, Integer, String, enum. Svi navedeni tipovi su nam poznati, osim poslednjeg, enum tipa. O njemu će biti reči tokom izlaganja o naprednim osobinama Java jezika. |
| --- |

| **Napomena**  Default blok koda se, po konvenciji, postavlja na kraj switch naredbe, ali to ne mora biti pravilo. Ovaj deo koda je moguće postaviti bilo gde unutar switch -a |
| --- |

### Svaki od switch slučajeva se mora završiti break naredbom

Svaki od slučajeva (case) unutar switch naredbe na kraju poseduje ključnu reč **break**. Uloga ključne reči break je da izvede izvršavanje koda izvan switch naredbe. Kada izvršno okruženje naiđe na ovu naredbu, završava se izvršavanje switch naredbe. Ukoliko zaboravite da navedete ovu naredbu na kraju slučajeva switch konstrukcije, switch neće funkcionisati ispravno:

```java
intx = 0;
 
switch(x) {
    case0:
        System.out.println("zero");
    case1:
        System.out.println("one");
        break;
    default:
         System.out.println("unknown value");
         break;
}
```

  
U ovakvoj situaciji, s obzirom na to da je vrednost promenljive x jednaka 0, očekivano je da se na izlazu dobije ispis zero. Ipak, ispis je sledeći:

zero  
one

  
Iako prikazani kod ne poseduje sintaksnu grešku, već se prevodi i izvršava, rezultat nije očekivan. Neočekivani rezultat smo dobili zato što smo zaboravili da na kraju prvog slučaja postavimo break naredbu. Zato Java izvršno okruženje, i pored toga što je vrednost x jednaka 0, ulazi u naredni slučaj i izvršava njegovu logiku (ispis poruke one). S obzirom na to da drugi slučaj na svom kraju poseduje break naredbu, izvršavanje se tu zaustavlja. Zbog ovakve osobine switch konstrukcije kaže se da svaki case na svom kraju mora imati break naredbu.

Naredba koja se koristi za bezuslovno napuštanje switch konstrukcije je:

  

### Višestruko poklapanje kod switch naredbe

Prethodni primer oslikavao je ispunjenje samo jednog uslova. Na primer, ukoliko je x jednako 1 i samo 1, izvršava se određeni blok koda. Ukoliko je x jednako 2 i samo 2, izvršava se drugi blok koda. Ali šta ukoliko je potrebno da se neki blok koda izvrši ukoliko x ima bilo koju od vrednosti 1 ili 2? U takvoj situaciji mora se pribeći definisanju višestrukih uslova.

Postavka primera će izgledati ovako:

*Potrebno je napraviti switch strukturu koja će testirati vrednost promenljive x. Ako x ima vrednost 1 ili 2, na izlazu je potrebno ispisati „YES”, dok za svaku drugu vrednost promenljive x treba ispisati „NO”.*

```java
intx = 1;
 
switch(x) {
    case1:
    case2:
        System.out.println("YES");
        break;
    default:
         System.out.println("NO");
         break;
}
```

  
Na ovaj način, prvi blok koda će se izvršiti kada promenljiva x ima vrednost 1 ili 2. Za sve ostale vrednosti, izvršava se default blok koda.  
  

### Unapređeni switch

Prethodni primeri ilustrovali su korišćenje standardne switch konstrukcije, kakva postoji i u većini ostalih programskih jezika. Ipak, Java jezik dodatno unapređuje switch naredbu, pa je nju moguće koristiti i na nešto drugačiji, kompaktniji način. Takav switch se naziva *unapređeni switch*.

Za početak ćemo videti kako se prvi primer switch konstrukcije iz ove lekcije može transformisati korišćenjem unapređenog switch -a. Takav primer je izgledao ovako:

```java
intx = 1;
     switch(x) {
          case0:
                System.out.println("zero");
                break;
          case1:
                 System.out.println("one");
                 break;
          default:
                 System.out.println("unknown value");
                 break;
}
```

  
Ovakav kod se može unaprediti na sledeći način:

```java
intx = 1;
 
    switch(x) {
        case0-> System.out.println("zero");
        case1-> System.out.println("one");
        default-> System.out.println("unknown value");
}
```

Čak i na prvi pogled, jasno je da je upravo prikazani kod znatno kompaktniji od onog iz prethodnog primera. Karakteri dve tačke (:), koji su razdvajali kontrolne vrednosti slučajeva od njihove logike, zamenjeni su karakterima **\->**. Takođe, unapređeni switch nas oslobađa potrebe za definisanjem break naredbe na kraju svakog slučaja, što je ogromna prednost. Jednostavno, nešto ranije ste mogli da vidite da izostavljanje break naredbe može proizvesti velike probleme. Zbog toga je ovaj unapređeni način kreiranja switch -a velika pogodnost Java jezika.

| **IntelliJ IDEA Tip**  **Unapređeni (enhanced) switch**  *Unapređeni switch* je korišćenjem IntelliJ IDEA razvojnog okruženja moguće kreirati na vrlo jednostavan način. Naime, ovo razvojno okruženje obezbeđuje opcije za automatsko konvertovanje standardnog u *unapređeni (enhanced) switch* (slika 12.2).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_12_02.png)  *Slika 12.2. Konvertovanje standardnog u unapređeni switch      *  Dovoljno je da kliknete na opciju **Replace with enhanced 'switch' statement** i konverziju će za vas obaviti IntelliJ IDEA. |
| --- |

*Unapređeni switch* donosi olakšice i kada je potrebno kreirati višestruko poklapanje. Primer višestrukog poklapanja je izgledao ovako:

```java
intx = 1;
 
switch(x) {
    case1:
    case2:
        System.out.println("YES");
        break;
    default:
        System.out.println("NO");
        break;
}
```

  
Višestruko poklapanje se ogleda u postojanju zajedničke logike za prva dva slučaja. Drugim rečima, za vrednosti 1 i 2 aktiviraće se identična logika. Ovakav switch je moguće unaprediti na sledeći način:

```java
intx = 1;
 
switch(x) {
    case1, 2-> System.out.println("YES");
    default-> System.out.println("NO");
}
```

  
Opet je jasno da je reč o znatno kompaktnijoj sintaksi. Nema potrebe za ponavljanjem ključne reči case, već se pojedinačne vrednosti (1, 2) jednostavno razdvajaju karakterom zapeta. Takođe, kao i u prethodnom primeru, ni ovde nije potrebno postavljati break naredbu.  
  

### switch kao izraz

switch je u svojoj osnovi izjava, odnosno naredba, pa se stoga u svom izvornom obliku ne može koristiti unutar izraza. Ovde se prevashodno misli na mogućnost dodeljivanja vrednosti u zavisnosti od nekog uslova, direktno iz switch konstrukcije. Kako biste razumeli o čemu je reč, podsetićemo se priče iz prethodne lekcije:

```java
intage = 19;       
String message = "";
 
if(age < 18) {
    message = "You can't enter";
} else{
    message = "Welcome";
}
```

  
Ovo je kod kojim se uz pomoć if...else naredbe obavlja uslovno dodeljivanje vrednosti promenljivoj message. Ipak, ni if...else naredba se ne može koristiti unutar izraza. Sa druge strane, ternarni operator ilustrovan u prethodnoj lekciji može, pa se korišćenjem njega prikazani kod može transformisati u izraz:

```java
intage = 19;
String message = (age < 18) ? "You can't enter": "Welcome";
```

  
Rezultat je identičan kao i u prethodnom primeru, ali se ovoga puta koristi ternarni operator, koji omogućava da se uslovno izvršavanje upakuje u izraz za dodeljivanje vrednosti promenljivoj.

Ovi primeri su prikazani kao uvertira koja će vam olakšati da razumete ono što ćete videti u nastavku. Za početak, ni standardna switch naredba, baš kao ni if...else, ne može se koristiti unutar izraza:

```java
intvalue = 1;
String stringValue = "";
 
switch(value) {
    case0:
        stringValue = "NO";
        break;
     case1:
        stringValue = "YES";
        break;
      default:
        System.out.println("Invalid value");
}
```

  
Ovo je primer u kome se korišćenjem switch konstrukcije vrednost promenljive stringValue postavlja na osnovu vrednosti promenljive value. Java jezik omogućava da se ovakve situacije značajno olakšavaju, tako što će se switch upotrebiti unutar samog izraza:

```java
intvalue = 0;
String stringValue = switch(value) {
    case0:
        yield  "NO";
    case1:
       yield "YES";
    default:
       yield "";
};
```

  
Ovoga puta je switch iskorišćen direktno unutar izraza. Takođe, switch je delimično izmenjen. Unutar pojedinačnih slučajeva koristi se ključna reč **yield** za definisanje vrednosti koja će biti dodeljena promenljivoj stringValue. Takođe, korišćenje ključne reči yield oslobađa nas potrebe za definisanjem ključne reči break.  
  

### Vežbe

**Vežba1**

Potrebno je napraviti program koji na osnovu vrednosti jedne numeričke promenljive, koja može biti između 1 i 7, ispisuje naziv dana u sedmici.

**Vežba 2**

U program ulaze sledeći podaci:

```java
intx = 523134;
inty = 325423;
```

  
Potrebno je izvršiti proveru ostatka deljenja x i y. Ukoliko ne postoji ostatak, prikazati poruku da ostatak ne postoji; u suprotnom, proveriti da li je ostatak veći ili manji od hiljadu i dati odgovarajuću poruku.

**Vežba 3**

Dati su sledeći ulazni podaci za jedno vozilo:

```java
String carMake = "Ford";
intdoors = 4;
```

  
Potrebno je napraviti uslovnu konstrukciju koja će proveravati da li je proizvođač automobila Ford, i ukoliko jeste, u zavisnosti od broja vrata prikazati odgovarajuću poruku.

### Rešenja:

**Vežba 1**

```java
intday = 3;
 
switch(day) {
    case1-> System.out.println("Monday");
    case2-> System.out.println("Tuesday");
    case3-> System.out.println("Wednesday");
    case4-> System.out.println("Thursday");
    case5-> System.out.println("Friday");
    case6-> System.out.println("Saturday");
    case7-> System.out.println("Sunday");
    default-> System.out.println("Unknown value");
}
```

**  
Vežba 2**

```java
intx = 523134;
inty = 325423;
 
intremainder = x % y;
 
switch(remainder)   {
 
        case0:
            System.out.println("division without remainder");
            break;
 
        default:
            if(remainder > 1000)
                      System.out.println("remainder over 1000");
                  else
                      System.out.println("remainder below 1000");
             break;
}
```

**  
Vežba 3**

```java
String carMake = "Ford";
intdoors = 4;
 

 
    
 
        
        
 
            
                
                
 
            
                
                
 
            
                
                
        
        
 
    
        System.out.println("We're sorry. You do not drive a Ford car.");
        break;
}
```

**  
Objašnjenje:**

Prikazani zadatak realizovan je korišćenjem jednog zanimljivog pristupa. Naime, možete videti da je u rešenju upotrebljena jedna switch konstrukcija koja se nalazi unutar drugog switch bloka. Iako ovo možda deluje kompleksno, zapravo nije. Sve uslovne blokove je moguće smeštati jedan unutar drugog i na taj način dobijati složene uslovne blokove sa više nivoa.

U prikazanom primeru zapravo imamo spoljašnji i unutrašnji switch. Spoljašnji switch poseduje samo dva slučaja, pri čemu se unutar prvog slučaja nalazi novi, unutrašnji switch. To praktično znači da će se drugi, unutrašnji switch aktivirati samo ukoliko je vrednost promenljive carMake Ford.

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_12.thb) JCPR1\_12.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_12.Mp4")

Kako Vam mogu pomoći?