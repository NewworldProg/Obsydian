---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=fad91bd38285ec05615170e3a6aa0ed2_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434686"
author:
published:
created: 2025-05-08
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 19 od 22

## Brojevi

O radu sa brojevima u Java jeziku već dosta toga znamo iz lekcija koje su za nama. Ipak, nakon priče o promenljivama, prostim i složenim tipovima podataka, objektima i klasama, možemo na mnogo bolji način da se posvetimo radu sa brojevima u Java programu. Pored svega, moć svakog programa se izražava u mogućnosti obrade podataka, a numerički podaci spadaju među osnovne čijom obradom treba da ovladamo kako bismo bili u mogućnosti da pišemo složenije Java programe. Stoga će u lekciji pred vama biti sumirane tehnike za rad sa brojevima u Javi. Neke od takvih tehnika već smo imali prilike da vidimo, ali će pored njih ova lekcija doneti i neke pristupe sa kojima se još uvek nismo susretali.  
  

### Prosti numerički tipovi

Za predstavljanje brojeva u Java programu može se koristiti šest prostih tipova, koji su prikazani tabelom 19.1.

| **Tip podatka** | **Značenje** | **Veličina u bajtovima** | **Opseg vrednosti** |
| --- | --- | --- | --- |
| byte | 8-bitna celobrojna vrednost | 1 bajt | Od -128 do 127 |
| short | celobrojna vrednost smanjenog opsega | 2 bajta | od -32768 do 32767 |
| int | celobrojna vrednost standardnog opsega | 4 bajta | od -2147483648 do 2147483647 |
| long | celobrojna vrednost proširenog opsega | 8 bajtova | od -9223372036854775808L do 9223372036854775807L |
| float | decimalna vrednost | 4 bajta | ±3.40282347 E+38F |
| double | decimalna vrednost, duple preciznosti | 8 bajtova | ±1.79769313486231570 E+308 |

  
*Tabela 19.1. Prosti numerički tipovi  
  
*

Prosti numerički tipovi se mogu podeliti na:

- celobrojne tipove – byte, short, int, long;
- tipove za predstavljanje brojeva sa decimalom – float, double.

Takođe, tipovi prikazani tabelom 19.1. se međusobno razlikuju po količini memorije koju zauzimaju, što direktno diktira njihov opseg, odnosno minimalnu i maksimalnu vrednost koja se njima može predstaviti. Stoga odabir odgovarajućeg tipa zavisi od dva faktora:

- veličine broja koji je potrebno prikazati;
- tipa broja, odnosno toga da li je potrebno rukovati celim brojem ili brojem sa decimalom.

Primer predstavljanja jednog celog broja korišćenjem prostog int tipa može da izgleda ovako:

```java
intx = 16;
```

  
Primer ilustruje definisanje celobrojne numeričke vrednosti, koja se čuva unutar promenljive tipa int. Numeričku vrednost je moguće definisati u nekoliko različitih oblika:

- dekadni (decimalni);
- oktalni;
- heksadecimalni;
- binarni

Dekadni, odnosno decimalni oblik je podrazumevan. Ostali oblici se definišu korišćenjem specifičnih prefiksa koji se dodaju na vrednosti:

int decVal = 26;  
int octVal = **0** 32; // 2 \* 8^0 + 3 \* 8^1 = 2 + 24 = 26  
int hexVal = **0x** 1a; // 10 \* 16^0 + 1 \* 16^1 = 10 + 16 = 26  
int binVal = **0b** 11010; // 2^1 + 2^3 + 2^4 = 2 + 8 + 16 = 26  
  

Kod ilustruje definisanje četiri pojedinačne celobrojne vrednosti, korišćenjem različitih oblika i to po redosledu definisanja: dekadni, oktalni, heksadecimalni, binarni. Svakim oblikom se zapravo definiše identična vrednost (26), a u komentarima koji su definisani u nastavku naredbi možete videti matematiku koja se koristi za pretvaranje konkretne vrednosti u dekadni oblik. Različiti oblici za definisanje numeričkih vrednosti imaju sledeće karakteristike:

- oktalna vrednost se karakteriše karakterom nula (0) na početku vrednosti;
- heksadecimalna vrednost se karakteriše prefiksom 0x;
- binarna vrednost se karakteriše prefiksom 0b.

| **Korišćenje karaktera donja crta prilikom definisanja numeričkih vrednosti**  Za razdvajanje grupa cifara u okviru jedne brojčane vrednosti može se koristiti karakter donja crta. Tako nešto može poboljšati preglednost i čitljivost koda. Donja crta neće biti tretirana od strane prevodioca, te će broj imati istu vrednost koju je imao i bez donjih crta. Evo primera upotrebe donje crte u brojčanim vrednostima:     Donja crta se može postaviti samo između cifara. Na sledeće pozicije se ne može postaviti donja crta:  - na početak ili kraj broja; - pored decimalne tačke; - pre **F** ili **L** sufiksa.  Redosledom kojim su prikazane, ovakve numeričke vrednosti izgledaju kao na slici 19.1.  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_19_01.png)  *Slika 19.1. Stvarna vrednost numeričkih vrednosti bez karaktera donja crta, koji se koriste za formatiranje* |
| --- |

Koji prosti numerički tip se može koristiti za predstavljanje brojeva sa decimalom?

  

### Složeni numerički tipovi

Pored prostih tipova, u Java programima se brojevi mogu predstaviti i korišćenjem složenih tipova, odnosno objekata nekoliko ugrađenih klasa. Takve klase se veoma često nazivaju i omotači primitivnih tipova, a u Javi ih ima šest, odnosno za svaki prosti tip po jedna:

- Integer
- Short
- Byte
- Float
- Long
- Double

Svi složeni numerički tipovi imaju identičnu roditeljsku klasu. Reč je o klasi Number (slika 19.2).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_19_02.png)

*Slika 19.2. Klase omotači prostih numeričkih tipova  
  
*

Unutar klase Number objedinjuju se osnovne funkcionalnosti koje su zajedničke za sve upravo prikazane klase numeričkih tipova. U jednoj od prethodnih lekcija, omotači prostih tipova su nam pomogli da razumemo osnovne osobine složenih tipova podataka, a u nastavku ove lekcije upoznaćemo se sa njihovim najznačajnijim osobinama, koje ih izdvajaju od primitivnih numeričkih tipova.  
  

### Boxing i unboxing

Numerička vrednost se korišćenjem ugrađenih složenih tipova može definisati baš kao da je reč o vrednosti prostog tipa:

```java
Integer myNumber = 16;
```

  
Ipak, Integer je jedan od složenih tipova u Java jeziku. Drugim rečima, Integer je klasa, a iz prethodnih lekcija znate da se objekti klasa kreiraju korišćenjem ključne reči new, nakon koje se navodi poziv konstruktorske metode. Upravo ovako:

```java
Integer myNumber = newInteger(16);
```

  
Ukoliko ovako nešto unesete u IntelliJ IDEA razvojnom okruženju, desiće se nešto zanimljivo (slika 19.3).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_19_03.png)

*Slika 19.3. Informacija koja se dobija kada se klase omotači instanciraju kao regularni objekti*

  
Sa slike 19.3. se može videti da tradicionalno instanciranje klase Integer stvara zanimljiv prikaz unutar IntelliJ IDEA okruženja. Kompletna logika za inicijalizaciju je markirana, konstruktor je precrtan i prikazano je nekoliko poruka. Razvojno okruženje nas obaveštava da ovakvo instanciranje nije potrebno, zato što pozivanje konstruktora sa definisanom vrednošću za nas obavlja Java kompajler. Drugim rečima, dve prikazane naredbe su ekvivalentne, zato što prilikom korišćenja složenih numeričkih tipova kreiranje objekta za nas obavlja Java kompajler.

Funkcionalnost jezika koja omogućava da se promenljivama Integer tipa vrednosti dodeljuju kao da je reč o prostim tipovima naziva se **Boxing**:

```java
Integer myNumber = 16;
```

  
Ovo je naredba koja ilustruje boxing. Boxing je zapravo proces kojim se vrednost prostog tipa konvertuje u odgovarajući tip složenog omotača. Kada Java kompajler dođe do ovakve naredbe, on u pozadini automatski poziva konstruktor Integer klase i njemu prosleđuje primitivnu vrednost.

Potpuno očekivano, suprotan proces od upravo predstavljenog boxinga naziva se **unboxing**. Unboxing se odnosi na konvertovanje složenog tipa omotača nazad u primitivni tip. Drugim rečima, unboxing se odnosi na proces izvlačenja primitivne vrednosti iz objektnog tipa omotača.

Unboxing se takođe obavlja automatski od strane Java kompajlera i to u sledećim situacijama:

- kada se objekat omotača prosleđuje nekoj metodi koja zahteva vrednost prostog tipa;
- kada se objekat omotača koristi za postavljanje vrednosti neke promenljive primitivnog tipa.

Evo najprostijeg primera unboxinga:

```java
Integer myNumber = 16;
intmyPrimitiveNumber = myNumber;
```

  
U ovom slučaju, Java kompajler samostalno izvlači prostu vrednost iz myNumber objekta i nju dodeljuje promenljivoj myPrimitiveNumber.  
  

### Najznačajnije funkcionalnosti numeričkih omotača

Osnovna prednost numeričkih omotača jeste postojanje određenih funkcionalnosti koje je moguće koristiti nad numeričkim vrednostima. Najznačajnije takve funkcionalnosti koje su dostupne nad instancama prikazane su tabelom 19.2.

| **Metoda** | **Opis** |
| --- | --- |
| compareTo() | poredi numeričke vrednosti; kada je prosleđena vrednost veća od one nad kojom se poziva, metoda emituje vrednost -1; kada je prosleđena vrednost manja, metoda emituje vrednost 1; kada je prosleđena vrednost jednaka onoj nad kojom se poziva, povratna vrednost je 0 |
| byteValue()   shortValue()   intValue()   longValue()   floatValue()   doubleValue() | metode koje se koriste za dobijanje proste (primitivne) vrednosti iz objekta omotača |

*  
Tabela 19.2. Objektne metode numeričkih omotača prostih tipova  
  
*

Metoda compareTo() koristi se na sledeći način:

```java
Integer myNumber1 = 15;
Integer myNumber2 = 16;
System.out.println(myNumber1.compareTo(myNumber2));
```

  
Nakon izvršavanja prikazanog koda, na izlazu će biti ispisana vrednost -1, zato što je broj koji se prosleđuje metodi compareTo() veći od onog nad kojim se ova metoda poziva.

Nešto ranije ste mogli da vidite da se u većini slučajeva unboxing obavlja automatski. Ipak, ukoliko to želimo samostalno da uradimo, dovoljno je iskoristiti neku od metoda iz tabele 19.2:

```java
Integer myNumber1 = 15;
intmyNumber2 = myNumber1.intValue();
```

  
Na ovaj način se eksplicitno obavlja izvlačenje primitivne vrednosti iz složenog tipa omotača.

Pored ovih metoda koje se mogu pozvati nad vrednostima, složeni tipovi omotača poseduju i određen broj statičkih metoda koje su dostupne nad svim nešto ranije spomenutim klasama (Integer, Double, Float...). Takve funkcionalnosti ilustrovane su tabelom 19.3.

| **Metoda** | **Opis** |
| --- | --- |
| compare(int x, int y) | poredi dve prosleđene numeričke vrednosti; kada je prva vrednost veća od druge, emituje povratnu vrednost 1; kada su vrednosti jednake, emituje vrednost 0; kada je druga vrednost veća, povratna vrednost je -1 |
| min(int a, int b) | utvrđuje koja od dve prosleđene vrednosti je manja |
| max(int a, int b) | utvrđuje koja od dve prosleđene vrednosti je veća |
| sum(int a, int b) | sabira dve prosleđene vrednosti |

*  
Tabela 19.3. Statičke metode numeričkih omotača prostih tipova  
  
*

Primeri korišćenja upravo prikazanih statičkih metoda izgledaju ovako:

```java
System.out.println(Integer.compare(17, 16));
System.out.println(Integer.sum(17, 16));
System.out.println(Integer.max(17, 16));
System.out.println(Integer.min(17, 16));
```

  
Rezultat ovakvog koda je sledeći:

1  
33  
17  
16  
  

### Klasa Math

Pored funkcionalnosti koje postoje unutar ugrađenih klasa koje predstavljaju omotače primitivnih tipova, za rad sa brojevima je moguće koristiti i metode koje se nalaze u jednoj specijalnoj ugrađenoj klasi. Reč je o klasi Math.

Najznačajnije funkcionalnosti koje postoje unutar klase Math ilustrovane su tabelom 19.4.

| **Metoda** | **Opis** |
| --- | --- |
| Math.abs() | vraća apsolutnu vrednost prosleđenog broja |
| Math.max() | vraća veću od dve prosleđene vrednosti |
| Math.min() | vraća manju od dve prosleđene vrednosti |
| Math.sqrt() | vraća kvadratni koren prosleđenog broja |
| Math.pow() | stepenuje prvi parametar drugim |
| Math.signum() | utvrđuje znak (pozitivno/negativno) prosleđenog broja |
| Math.random() | vraća nasumičnu double vrednost veću ili jednaku od nule, a manju od 1.0 |
| Math.round() | zaokružuje vrednost na najbliži ceo broj |
| Math.ceil() | zaokružuje vrednost na prvi veći ceo broj |
| Math.floor() | zaokružuje vrednost na prvi manji ceo broj |

*  
Tabela 19.4. Metode klase Math  
  
*

Evo primera koji oslikava korišćenje prvih sedam metoda iz tabele 19.4:

```java
System.out.println(Math.abs(-17));
System.out.println(Math.min(17, 23));
System.out.println(Math.max(17, 23));
System.out.println(Math.sqrt(16));
System.out.println(Math.pow(4, 2));
System.out.println(Math.signum(-17));
System.out.println(Math.random());
```

  
Rezultat koji se dobija je sledeći:

17  
17  
23  
4.0  
16.0  
\-1.0  
0.30804591195596465

  
Evo kako su dobijene prikazane vrednosti, redosledom kojim su ispisane:

- 17 je apsolutna vrednost vrednosti -17
- 17 je manje od 23
- 23 je veće od 17
- koren iz 16 je jednako 4.0
- 4 na drugi je jednako 16.0
- broj -17 je negativan, pa otuda vrednost -1
- vrednost 0.30804591195596465 je proizvoljna vrednost koja se dobija od metode Math.random(); sa svakim pokretanjem programa, ova vrednost će biti drugačija, pa je gotovo izvesno da će ona kod vas biti drugačija nego što je to slučaj u ovoj lekciji

Evo kako funkcioniše metoda round za zaokruživanje vrednosti:

```java
System.out.println(Math.round(5.4));
System.out.println(Math.round(5.5));
System.out.println(Math.round(5.6));
```

  
Na početku, prikazane su tri naredbe u kojima se koristi metoda round. U svakoj naredbi, ovoj metodi se prosleđuje nešto drugačija vrednost. Metoda round zaokružuje vrednost na najbliži ceo broj. Stoga su vrednosti koje se dobijaju sledeće:

5  
6  
6  
  

Vrednost 5.4 je najbliža celoj vrednosti 5. Vrednost 5.6 je bliža celom broju 6. Kada je vrednost koja se prosleđuje metodi round podjednako udaljena od dva cela broja (5.5) zaokružuje se na prvi veći ceo broj (6).

Naredna metoda za zaokruživanje sa kojom ćemo se upoznati je metoda floor:

```java
System.out.println(Math.floor(5.4));
System.out.println(Math.floor(5.5));
System.out.println(Math.floor(5.6));
```

  
Na ovaj način se dobija sledeće:

5.0  
5.0  
5.0  
  

S obzirom na to da zaokružuje broj na prvi manji, metoda floor u svim situacijama proizvodi vrednost 5.0.

Nešto drugačije funkcioniše metoda ceil:

```java
System.out.println(Math.ceil(5.4));
System.out.println(Math.ceil(5.5));
System.out.println(Math.ceil(5.6));
```

  
Ovoga puta se na izlazu dobija:

6.0  
6.0  
6.0  
  

Ovoga puta, sve tri naredbe proizvode vrednost 6, odnosno vrednosti se zaokružuju na prvi veći ceo broj.

Pored prikazanih metoda, unutar klase Math definisane su i dve matematičke konstante koje se veoma često koriste:

- Math.PI
- Math.E

**Vežba**

Napisati program koji od korisnika prihvata jedan parametar. Parametar se odnosi na poluprečnik kruga. Nakon unosa vrednosti, program treba da izračuna obim i površinu kruga i rezultate prikaže na izlazu.

**  
Rešenje**

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        Scanner scanner = newScanner(System.in);
 
        System.out.println("Please, enter radius:");
 
        doubleradius = scanner.nextDouble();
 
        doublecircumference = 2* radius * Math.PI;
        doublearea = radius * radius * Math.PI;
 
        System.out.println("Circumference is: "+ circumference);
        System.out.println("Area is: "+ area);
 
    }
 
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_19.thb) JCPR1\_19.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_19.Mp4")

Kako Vam mogu pomoći?