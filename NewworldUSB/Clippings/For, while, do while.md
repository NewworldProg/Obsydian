---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=534997ee6090c46fdc29860655676b49_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434680"
author:
published:
created: 2025-04-29
description:
tags:
  - "clippings"
---
Jedinica 13 od 22

## For, while, do while

Prethodne lekcije ilustrovale su jedan od osnovnih mehanizama za postizanje kontrole toka – uslovno izvršavanje, odnosno grananje. Pored grananja, petlje su jedan od osnovnih elemenata za postizanje kontrole toka. Stoga će lekcija pred vama biti posvećena upoznavanju pojma petlji u Java jeziku.  
  

### Pojam petlji

Petlje imaju nešto drugačije osobine nego uslovno izvršavanje (grananje). Da bi se njihove osobine na najbolji način razumele, biće razmotreno sledeće pitanje:

==*Na koji način se jedna ista naredba Java koda može izvršiti više puta?*==

Na primer, potrebno je pet puta ispisati jednu istu poruku. Najjednostavnije rešenje za postizanje opisanog ponašanja jeste navođenje pet sukcesivnih naredbi za ispis:

```java
System.out.println("Hello World");
System.out.println("Hello World");
System.out.println("Hello World");
System.out.println("Hello World");
System.out.println("Hello World");
```

  
Ovakav kod će na izlazu proizvesti sledeći ispis:

Hello World  
Hello World  
Hello World  
Hello World  
Hello World

  
Željeni rezultat je postignut, ali šta da je bilo potrebno Hello World poruku ispisati 1000 puta? ==Navođenje 1000 identičnih naredbi je vrlo nepraktično== i zamorno. Ono što je potrebno uraditi kako bi se nastali problem razrešio jeste iznaći način da se izvršnom okruženju kaže: *izvrši naredbu za ispis poruke* *tačno 1000 puta*. Upravo su petlje način da se jedna takva logika formuliše u programski kod Java jezika.

Osnovna ==logika petlji ilustrovana je slikom== 13.1.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_01.png)*

*Slika 13.1. Petlja  
  
*

Sa slike 13.1. se može zaključiti da u svetu programiranja petlje omogućavaju da se određeni deo koda izvrši više puta tako što se tok izvršavanja ciklično vraća unazad.

U osnovi svake petlje jeste proces ponavljanja. Svako ponavljanje se drugačije naziva **iteracija**. Tako su petlje zapravo sačinjene iz iteracija. Petlja započinje prvom iteracijom, a završava se nakon poslednje iteracije. Broj iteracija jedne petlje može biti proizvoljan, od nula do beskonačno. Petlja sa beskonačnim brojem iteracija nema svoj kraj, pa se drugačije naziva **mrtva petlja**.  
  

### Petlje u Java jeziku

==Java poznaje nekoliko naredbi koje omogućavaju kreiranje petlji:==

- ==for==
- ==while==
- ==do…while==

Takođe, Java poseduje i ==dve naredbe za kontrolu izvršavanja petlji:==

- ==break==
- ==continue==

Navedene naredbe biće tema lekcije pred vama.  
  

### For petlja

For petlja omogućava da se određeni blok koda izvrši tačan broj puta. U uvodnom delu ove lekcije postavljeno je pitanje:

*Kako ispisati jednu istu poruku određeni broj puta?*

Odgovor na ovo pitanje leži upravo u korišćenju for petlje:

```html
for (int i = 0; i < 5; i++) {
    System.out.println("Hello World");
}
```

  
Rezultat prikazanog koda je identičan kao i u uvodnom primeru:

Hello World  
Hello World  
Hello World  
Hello World  
Hello World

  
Da bismo razumeli kako je ovako nešto postignuto, neophodno je upoznati se sa ==sintaksom for petlje:==

```java
for(initialization; condition; final-expression)              
   statement
```

  
Kada se ovakav [pseudokod](https://www.link-elearning.com/linkdl/opisPojma.php?id=160486 "pseudokod")  predstavi korišćenjem algoritma, struktura for petlje je kao na slici 13.2.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_02.png)*

*Slika 13.2. Logika for petlje  
  
*

For petlja kreira se ==korišćenjem ključne reči for==. Nakon ove ključne reči, u zagradama se navode tri izjave (naredbe):

1. **==initialization== (==inicijalizacija==)** – p==očetna naredba koja se izvršava samo jednom, na početku izvršavanja petlje==; koristi se za inicijalizaciju jednog ili više brojača petlje; u prikazanom primeru to je int i = 0;
2. **==condition== (==uslov==)** – naredba kojom se utvrđuje istinitost uslova; ==ukoliko je uslov ispunjen, prelazi se na izvršavanje tela petlje==; ovo je naredba koja se izvršava pre svake iteracije; u prikazanom primeru je to i < 5;
3. ==**final-expression**== – ==naredba koja se izvršava nakon svake iteracije==; uglavnom se koristi za uvećanje ili smanjenje vrednosti brojača; u primeru je to i++

Nakon zagrada u kojima se nalaze tri upravo opisane naredbe, sledi telo petlje koje započinje otvorenom, a završava se zatvorenom vitičastom zagradom. ==Unutar bloka petlje može se naći proizvoljan broj naredbi koje se ponavljaju== svakom iteracijom. Baš kao i kod uslovnih blokova, vitičaste zagrade za formiranje bloka for petlje je moguće izostaviti ukoliko telo petlje poseduje samo jednu naredbu.

==Kompletna upravo opisana struktura for petlje iz prvog prikazanog primera može se ilustrovati kao na slic==i 13.3.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_03.png)*

*Slika 13.3. Struktura jedne for petlje  
  
*

Na kraju ćemo još jednom rezimirati kompletnu logiku prikazanog primera. Kreiranje petlje započinje navođenjem ključne reči for. Nakon toga, u zagradama se definišu inicijalizacija, uslov i završna naredba.

Prvo se deklariše i inicijalizuje jedna promenljiva sa nazivom i:

```java
inti = 0;
```

  
Ova promenljiva ima početnu vrednost 0, a unutar for petlje služi kao **brojač**.

Nakon inicijalizacije, sledi deo kojim se definiše uslov:

```java
i < 5;
```

  
Na ovaj način je rečeno da će se telo petlje izvršavati sve dok je vrednost promenljive i manja od 5.

Na kraju, definiše se i završna naredba, koja je u prikazanom primeru realizovana kao inkrementacija brojača:

```java
i++
```

  
Ovakvom naredbom je rečeno da se nakon svake iteracije vrednost brojača uvećava za jedan. Ovakva naredba se izvršava nakon svake iteracije, pa se upravo zbog toga i zove završna naredba.

| **Promenljiva koja predstavlja brojač postoji samo unutar for petlje**  Svaka promenljiva u Java jeziku poseduje nešto što se naziva *oblast vidljivosti*. Ovaj pojam se odnosi na sva ona mesta u programskom kodu sa kojih je jednoj promenljivoj moguće pristupiti. Blokovi, kao sintaksni elementi jezika, uvek predstavljaju jednu oblast vidljivosti. To praktično znači da se promenljive deklarisane unutar for petlje mogu koristiti samo unutar bloka petlje, a ne i izvan takvog bloka. To pravilo važi i za promenljivu koja predstavlja brojač, zato što je i ona primer promenljive koja se deklariše unutar bloka for petlje:  ```java for(inti = 0; i < 5; i++) {     System.out.println("Hello World"); }   System.out.println(i); ```     Ovakav kod će svakako da proizvode grešku, zato što promenljiva i nije vidljiva izvan for petlje. Sve ovo znači da je promenljivu sa nazivom i bez ikakvih problema moguće kreirati izvan for petlje. Ona će biti u potpunosti zasebna promenljiva i neće imati nikakve veze sa onom koja se koristi za deklarisanje brojača. |
| --- |

Upravo prikazani kod ilustruje osnovni oblik for petlje. Ipak, ona se može pojaviti u raznim drugim oblicima. Na primer, završnu naredbu je moguće formulisati i na druge načine:

```java
for(inti = 0; i < 5; i+=2) {
    System.out.println("Hello World");
}
```

  
Završna naredba, odnosno logika kojom se menja vrednost brojača, sada je izmenjena. Na kraju svake iteracije, vrednost brojača se uvećava za dva. Tako se u ovom slučaju na izlazu dobija:

Hello World  
Hello World  
Hello World

  
U ovom slučaju for petlja poseduje samo tri iteracije (za vrednosti brojača 0, 2 i 4).

Takođe, ==nije neophodno da se brojač uvećava. Njega je u svakoj iteraciji moguće i umanjivati:==

```java
for(inti = 5; i > 0; i--) {
    System.out.println("Hello World");
}
```

  
Inicijalna vrednost brojača sada je 5. U svakoj iteraciji brojač se umanjuje za jedan. Uslov je takođe izmenjen, pa se proverava da li je brojač veći od nule. Kada postane veći od nule, izlazi se iz petlje. Efekat će biti identičan, kao u jednom od prethodnih primera, odnosno, na izlazu će se pet puta ispisati poruka Hello World:

Hello World  
Hello World  
Hello World  
Hello World  
Hello World  

Prva naredba u deklaraciji for petlje odnosi se na:

  

  
  

| **IntelliJ IDEA Tip**  **Brzo kreiranje for petlje**  IntelliJ IDEA razvojno okruženja poseduje prečicu koja omogućava brzo kreiranje for petlje. U editoru je dovoljno uneti **fori**, i kompletna for petlja sa standardnim elementima će biti generisana (slika 13.4).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_04.png)  *Slika 13.4. Prečica za kreiranje for petlje u IntelliJ IDEA razvojnom okruženju* |
| --- |

### Petlja unutar petlje

Jednu for petlju je moguće smestiti unutar druge for petlje i na taj način dobiti jednu zanimljivu strukturu. Takav pristup se veoma ==često koristi u kompleksnijim programima==, a i mi ćemo ga u nastavku ovoga kursa praktično primeniti, kada se budemo upoznali sa pojmom nizova u Java jeziku. Do tada, pokušaćemo da se ==načelno upoznamo sa načinom na koji funkcionišu petlje unutar petlji.==

Evo kako izgleda jedna struktura koja podrazumeva petlju unutar petlje:

```html
for (int i = 0; i < 4; i++) {
    for (int j = 0; j < 3; j++) {
        System.out.println(j);
    }
}
```

  
Najlakše je da ovakvu strukturu posmatrate iznutra, odnosno počevši od unutrašnje petlje. Ona ima brojač imenovan nazivom j i unutar tela petlje se obavlja ispis vrednosti brojača. Ova unutrašnja petlja će se izvršiti tri puta, što znači da će na izlaz ispisati vrednosti 0, 1, 2. Kada ne bi bilo spoljašnje for petlje, to bi bio i jedini ispis koji bismo dobili od ovakvog programa. Ipak, spoljašnja petlja čini da se izvršavanje unutrašnje petlje ponovi četiri puta, pa se na kraju na izlazu dobija sledeće:

0  
1  
2  
0  
1  
2  
0  
1  
2  
0  
1  
2

  
Bitno je da primetite da svaka petlja poseduje brojač sa jedinstvenim nazivom. S obzirom na to da unutrašnja petlja pripada bloku spoljašnje petlje, neophodno je da se za brojač koristi promenljiva jedinstvenog naziva.

### while petlja

Pored for petlje, Java poznaje još nekoliko načina da se određeni kod izvrši više puta. Jedan od njih jeste while petlja.

==while petlja izvršava određeni blok koda sve dok je ispunjen uslov za izvršavanje petlje==. To praktično znači da ova vrsta petlje nema unapred definisan broj iteracija. Sintaksa while petlje je sledeća:

```java
while(condition) {
    statement
}
```

  
Sve dok je uslov (condition) ispunjen, izvršava se blok koda, odnosno telo petlje. Logika while petlje može se ilustrovati slikom 13.5.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_05.png)*

*Slika 13.5. while petlja  
  
*

Primer upotrebe while petlje je sledeći:

```java
intx = 0;
while(x < 5) {
    System.out.println("Hello World");
    x = x + 1;
}
```

  
Na početku se deklariše i inicijalizuje promenljiva x, sa vrednošću 0. while petlja se kreira korišćenjem ključne reči while, a nakon nje, unutar zagrada se definiše uslov:

x<5

Ovo praktično znači da će se petlja izvršavati sve dok je vrednost promenljive x manja od 5.

Telo petlje definisano je vitičastim zagradama. Unutar tela petlje vrši se ispisivanje poruke Hello World, ali i uvećavanje vrednosti promenljive x za jedan. Da kojim slučajem ova inkrementacija nije navedena, uslov za izvršavanje ove petlje uvek bi bio ispunjen. Na taj način bi se stvorila jedna **beskonačna petlja**, odnosno petlja koja nikada ne bi prestala da se izvršava.

Upravo prikazanim primerom while petlje dobija se identičan efekat kao i nešto ranije, kada smo koristili for petlju:

Hello World  
Hello World  
Hello World  
Hello World  
Hello World  
  

### do…while petlja

Upravo opisana while petlja ni na koji način ne garantuje da će se njeno telo uopšte i izvršiti. J==ednostavno, ukoliko uslov nije ispunjen, telo petlje se neće izvršiti nijednom:==

```java
intx = 6;
 
while(x < 5) {
     System.out.println("Hello World");
     x = x + 1;
}
```

  
U primeru, vrednost promenljive x je veća od 5, tako da uslov za izvršavanje while petlje nije ispunjen, te se kod unutar tela while petlje neće izvršiti nijednom. Ali šta ukoliko je potrebno osigurati da se petlja izvrši makar jednom, bez obzira na ispunjenje uslova?

Tako nešto moglo bi se postići ukoliko bi se provera ispunjenosti uslova smestila nakon bloka koda koji je potrebno izvršiti. Upravo to je osnovna osobina petlje do…while.

==Sintaksa do…while petlje je sledeća:==

```java
do{
    
} while(condition);
```

  
Na početak se postavlja ključna reč **do**, a nakon nje blok koda koji je oivičen vitičastim zagradama. Nakon bloka, koristi se ključna reč **while** za definisanje uslova izvršenja petlje.

Logika do...while petlje se [algoritmom](https://www.link-elearning.com/linkdl/opisPojma.php?id=160487 "algoritmom") može predstaviti kao na slici 13.6.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_13_06.png)*

*Slika 13.6. do...while petlja  
  
*

Sada se ==prethodni primer može transformisati na sledeći način:==

```java
intx = 6;
 
do{
    System.out.println("Hello World");
    x = x + 1;
} while(x < 5);
```

  
Rezultat je sledeći:

Hello World

Zaključak je da se telo petlje izvršilo jednom i pored toga što uslov nije ispunjen. Provera ispunjenosti uslova se obavlja nakon izvršavanja svake iteracije, te stoga do...while petlja uvek poseduju makar jednu iteraciju.

U okviru radnog okruženja možete testirati i primere do...while -petlji.  
  

### Naredbe break i continue

Ponekad je potrebno kontrolisati izvršavanje petlje na osnovu nekog uslova i to unutar tela petlje. U takvim situacijama je moguće koristiti naredbe break i continue.

Naredba continue prekida aktuelnu iteraciju i prelazi na sledeću.

Naredba break napušta petlju.

Sledeći primer ilustruje upotrebu naredbe continue:

```java
inti;
 
for(i = 0; i < 100; i++) {
    if(i > 50) {
        continue;
    }
 
   System.out.println(i);
}
 
System.out.println(i);
```

  
U primeru je kreirana jedna for petlja, koja će imati 100 iteracija (od 0 do 99). Ipak, unutar for petlje je definisan jedan uslov, kojim se proverava da li je brojač veći od 50. Ukoliko je brojač veći od 50, poziva se naredba continue. S obzirom na to da ova naredba odmah prelazi na izvršavanje sledeće iteracije, linija za ispis vrednosti brojača se neće izvršiti u slučaju da je brojač veći od 50. Sve ovo proizvodi sledeći rezultat:

0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50  
100

  
Analizom izlaza može se utvrditi da se linija za ispis vrednosti brojača unutar tela petlje izvršava do vrednosti 50. Petlja nastavlja da se izvršava do kraja, ali ne ispisuje vrednosti, u šta se možemo uveriti poslednjim ispisanim brojem. To je broj 100, koji je ispisan od strane linije koja se nalazi izvan petlje. Ovo praktično znači da je vrednost brojača nakon završetka petlje 100, što dokazuje da se petlja izvršila u celosti.

Za razliku od naredbe continue, koja prekida trenutnu i prelazi na sledeću iteraciju, naredba break kao svoj efekat ima izlazak iz petlje. Drugim rečima, naredba break završava petlju. Stoga pogledajte šta će se dogoditi ukoliko ključnu reč continue zamenimo ključnom rečju break:

```java
inti;
 
for(i = 0; i < 100; i++) {
    if(i > 50) {
        break;
    }
 
   System.out.println(i);
}
 
System.out.println(i);
```

  
Ovoga puta, kod proizvodi sledeći izlaz:

0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50  
51

  
Jasno se može videti razlika između naredbi continue i break. Kada brojač dostigne vrednost 51, aktivira se if uslovni blok unutar koga se nalazi naredba break. Izvršavanjem naredbe break dolazi do trenutnog izlaska iz petlje, te se prelazi na izvršavanje sledeće naredbe. Zbog toga je poslednja vrednost koja se štampa unutar for petlje 50. Nakon izvršavanja for petlje, štampa se vrednost 51.

| **Napomena**  U primerima efekata naredbi break i continue, brojači su namerno deklarisani izvan for petlji, kako bi se njihova vrednost očuvala i nakon završetka petlji. U realnim okolnostima, kao što je već rečeno nešto ranije, ovo se smatra lošom praksom. |
| --- |

### Vežbe

**Vežba 1**

Napisati Java program koji ispisuje prvih sto celih pozitivnih brojeva, počevši od broja 1.

**Vežba 2**

Napraviti program koji sabira prvih dvadeset celih pozitivnih brojeva.

### Rešenja:

**Vežba 1**

```java
for(inti = 1; i < 101; i++) {
    System.out.println(i);
}
```

**  
Vežba 2**

```java
intsum = 0;
 
for(inti = 0; i < 21; i++) {
    sum += i;
}
 
System.out.println(sum);
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_13.thb) JCPR1\_13.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_13.Mp4")

Kako Vam mogu pomoći?