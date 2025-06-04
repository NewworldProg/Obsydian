---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=534997ee6090c46fdc29860655676b49_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434678"
author:
published:
created: 2025-04-29
description:
tags:
  - "clippings"
---
Jedinica 11 od 22

## If, else if, else

Izvorni kod programa koje smo do sada pisali izvršavao se linearno, odnosno naredbu po naredbu, od vrha ka dnu. Drugim rečima, programi koje smo do sada kreirali nisu imali veliku mogućnost kontrole toka. To nas je i sputavalo u izvođenju nekih ozbiljnijih operacija. Stoga će modul pred vama biti posvećen različitim tehnikama koje će nam omogućiti da kontrolišemo tok izvršavanja Java programa.  
  

### Šta je kontrola toka?

Izvršavanje Java koda obavlja se ==sleva nadesno, pri čemu se napisane izjave (naredbe) izvršavaju redom, jedna za drugom==:

```java
intx = 1;
inty;
y = x;
```

  
U prikazanom primeru definisane su ==tri Java naredb==e. One će se izvršiti redom kojim su napisane, pa će tako prvo biti deklarisana i inicijalizovana promenljiva x, zatim će biti deklarisana promenljiva y i na kraju će vrednost promenljive x biti dodeljena promenljivoj y. Ilustrativno, tok izvršavanja prikazanog koda je kao na slici 11.1.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_01.png)*

*Slika 11.1. Linearni tok izvršavanja koda  
  
*

Zamislite sada situaciju u kojoj biste mogli da kontrolišete tok izvršavanja prikazanog koda. Na primer, ==želite da se nakon izvršavanja prve izjave pređe na izvršavanje treće (slika 11.2).==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_02.png)

*Slika 11.2. Primer nelinearnog izvršavanja (kontrole toka)  
  
*

Pored preskakanja, kontrola toka se može ogledati i u ponavljanju jedne ili više naredbi. Na primeru tri prikazane naredbe sa početka lekcije, takvo ponavljanje može izgledati kao na slici 11.3. ==Nakon izvršavanja poslednje, treće naredbe, izvršavanje se ponovo vraća na prvu naredbu.==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_03.png)

*Slika 11.3. Primer nelinearnog izvršavanja (kontrole toka) (2)  
  
*

Upravo prikazani scenariji spadaju u domen kontrole toka, a jezik Java omogućava različite načine za njeno postizanje:

- ==grananje (uslovno izvršavanje);==
- ==petlje (ponavljanje).==

U modulu koji je pred vama biće obrađeni osnovni postulati kontrole toka u programskom jeziku Java.  
  

### Grananje (uslovno izvršavanje)

Grananje omogućava da se ==određene naredbe izvrše samo u slučaju zadovoljenja nekog uslova==. Zbog toga je grananje usko povezano sa logičkim tipovima podataka i logičkim operatorima, što su pojmovi koji su obrađeni u lekcijama za nama. Naime, Java omogućava da se kreira više mogućih grana izvršavanja, a da sam odabir grane izvršavanja bude obavljen u zavisnosti od neke kontrolne logičke vrednosti.

==Java poznaje dve vrste== kondicionalnih (uslovnih) naredbi:

- ==if..else grupa naredbi;==
- ==switch.==

### if naredba

Osnovna naredba grananja u Java jeziku jeste naredba if. Ova naredba postoji u praktično svim programskim jezicima, a svrha joj je oslikana u samom nazivu: *ako*.

Reč if (*ako*), sama za sebe, nema baš mnogo logike u retorici, a tako je i u programiranju. Naime, pored ove ključne reči potrebno je postaviti i neki uslov od koga će zavisiti ishod ove naredbe. Tako opšta ==sintaksa if naredbe izgleda ovako:==

```java
if(condition) {
          
}
```

  
Za formiranje if naredbe, koristi se ključna reč if, nakon koje se u zagradama navodi uslov. ==U slučaju ispunjenja uslova, izvršava se blok koda== if naredbe.

Slika 11.4. ilustruje logiku izvršavanja programa kada se upotrebljava if naredba.

 *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_04.png)*

*Slika 11.4. If naredba  
  
*

Kao što se sa slike 11.4. može videti, izvršavanje programa dolazi do dela nazvanog *condition* (uslov). U ovom delu se ==proverava definisani uslov i ukoliko je on ispunjen, izvršava se kod if bloka==. ==U protivnom, if blok koda se preskače, a izvršavanje se nastavlja prvom sledećom naredbom==. Primer koji ilustruje upotrebu if naredbe je sledeći:

```java
intspeed = 9;
 
 if(speed < 10) {
    System.out.println("Too slow...");
 }
```

  
Na početku je deklarisana i inicijalizovana promenljiva sa nazivom speed i vrednošću 9. Nakon ove linije, sledi if naredba. Uslov je definisan tako da se proverava ==da li je vrednost promenljive speed manja od 10. Ukoliko je ovakav uslov ispunjen, izvršava se blok koda između vitičastih zagrada==, koji u primeru poseduje jednu naredbu.

==Da je kojim slučajem vrednost promenljive speed bila veća ili jednaka broju 10, blok koda iz primera se ne bi izvršio.==

| **Logički uslovi i logičke vrednosti**  Nešto ranije je rečeno da se unutar zagrada nakon ključne reči if navodi uslov koji diktira da li će if blok biti izvršen ili ne. Ipak, ukoliko želimo da budemo potpuno precizni, može se reći da se unutar zagrada nakon ključne reči if navodi neka logička vrednost (true ili false):  ```java if(true) {     System.out.println("Too slow..."); } ```     Naravno, ovakav blok koda uvek će se izvršiti, zato što je unutar zagrada navedena vrednost true. Tako se ovakav blok i ne može nazvati uslovnim, jer je verovatnoća njegovog izvršavanja unapred poznata. Stoga se direktno navođenje logičke vrednosti kao uslova grananja vrlo retko koristi. Ipak, bitno je znati da se grananje u svojoj biti obavlja na osnovu logičkih vrednosti true i false, pa je i nešto ovako potpuno legitimno napisati. Identično važi i za sve ostale naredbe grananja, koje će biti prikazane u nastavku. |
| --- |

**Blokovi uslovnih naredbi**

U upravo prikazanom primeru mogli ste da vidite da se if naredba sastoji iz uslova i bloka. Blok se formira kao i svaki drugi blok u jeziku Java, korišćenjem vitičastih zagrada:

```java
intspeed = 9;
if(speed < 10) {
    System.out.println("Too slow...");
}
```

  
Ipak, bitno je da znate da se zagrade za formiranje bloka mogu izostaviti ukoliko blok poseduje samo jednu naredbu:

```java
intspeed = 9;
if(speed < 10)
    System.out.println("Too slow...");
```

  
Bitno je da zapamtite da na ovaj način if uslovni blok može imati samo jednu naredbu. Bilo koja naredba nakon toga neće biti sastavni deo bloka:

```java
intspeed = 11;
if(speed < 10)
    System.out.println("Too slow...");
System.out.println("Too slow...");
```

  
Ovakav kod lako može da navede na zaključak da se zbog neispunjenog uslova neće izvršiti nijedna naredba za ispis poruke. Naime, deluje kao da su obe naredbe za ispis deo if uslovnog bloka. Ipak, tako nešto nije slučaj, pa će se druga naredba svakako izvršiti, s obzirom na to da je ona zapravo izvan if bloka.  
  

### if...else naredba

U ovom trenutku se može postaviti jedno pitanje:

==*Šta ukoliko je potrebno izvršiti određeni blok koda kada if uslov nije zadovoljen**?*==

Odgovor na ovo pitanje krije se u upotrebi ključne reči else, pa tako naredba if postaje naredba if...else.

if...else je ==naredba za kontrolu toka koja omogućava definisanje logike koja će se izvršiti  ukoliko je uslov ispunjen==, ali i logike koja će se izvršiti ukoliko uslov nije ispunjen. Sintaksa if...else naredbe je sledeća:

```java
if(condition) {
    statement_1;
} else{
     statement_2;
}
```

  
U zagradama nakon ključne reči ==if navodi se uslov (condition). U slučaju ispunjenja ovakvog uslova, izvršava se prva izjava (statement\_1), a u protivnom druga (statement\_2).==

Sve ovo ilustrovano je slikom 11.5.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_05.png)

Slika 11.5. if…else naredba  
  

Sa slike 11.5. se može videti da u ovoj situaciji postoje dva bloka koda: *if code* i *else code*. U zavisnosti od ispunjenja uslova, izvršava se jedan od ova dva bloka koda. Bitno je razumeti da će jedan blok koda morati da se izvrši. Koji će to blok biti – zavisi od ishoda uslova.

Primer upotrebe if...else naredbe:

```java
if(1== 1) {
    System.out.println("true");
} else{
    System.out.println("false");
}
```

  
U primeru je definisan uslov 1==1. Potpuno je jasno da će uslov biti ispunjen, te se stoga izvršava if blok, a na izlazu ispisuje:

True  

| **Napomena**  Veoma česta greška koja se javlja prilikom kreiranja uslovnih blokova je korišćenje operatora dodeljivanja (=) umesto operatora poređenja (==). Naravno, integrisano razvojno okruženje kao što je IntelliJ IDEA nikada neće dozvoliti tako nešto (slika 11.6).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_06.png)  *Slika 11.6. Pogrešno korišćenje operatora dodele umesto operatora poređenja      *  Na slici 11.6. se vidi da IntelliJ IDEA jasno stavlja do znanja da je došlo do greške, prikazom poruke da je očekivani tip boolean. Takođe, IntelliJ IDEA obezbeđuje i opciju koja automatski ispravlja našu grešku (*Replace '* *\=* *' with '=='*). |
| --- |

Ukoliko se uslov iz prethodnog primera promeni, menja se i tok izvršavanja našeg Java programa.

```java
if(10== 13) {
    System.out.println("true");
} else{
    System.out.println("false");
}
```

  
Sada se na izlazu dobija:

false

S obzirom na to da se ispituje jednakost brojeva 10 i 13, logički izraz rezultuje stvaranjem vrednosti false. Vrednost false čini da se aktivira else uslovni blok.

==Jedna if...else naredba može imati samo jedan if i samo jedan else blok. Uslov se uvek definiše samo na if bloku.==

### if...else if...else naredba

U prethodnim redovima je prikazano da if...else naredba može imati samo jedan uslov i to na if bloku. Ukoliko je on ispunjen, izvršava se if, a u protivnom else blok. Sada se postavlja novo pitanje:

==*Šta se dešava ukoliko je potrebno definisati dodatne blokove koda sa sopstvenim uslovima?*==

Odgovor na ovo pitanje krije se u ==upotrebi ključnih reči else if.==

else if omogućava da se prilikom kreiranja if...else naredbe definišu dodatni uslovi, pa tako ==naredba if...else postaje if...else if...else naredba==.

Sintaksa ovakve naredbe je sledeća:

```java
if(condition_1) {
    statement_1;
} elseif(condition_2) {
    statement_2;
} elseif(condition_n) {
    statement_n;
} else{
    statement_last;
}
```

  
==U ovom primeru, pored if i else blokova, postoje i dva else if bloka==. Ukoliko je prvi uslov (condition\_1) ispunjen, izvršiće se izjava statement\_1. Ukoliko je uslov condition\_2 ispunjen, izvršiće se izjava statement\_2. Ukoliko je uslov condition\_n ispunjen, izvršiće se naredba statement\_n. Na kraju, ukoliko nijedan uslov nije ispunjen, izvršiće se izjava statement\_last. Bitno je razumeti da broj else if blokova može biti proizvoljan. U primeru ih ima dva, dok je moguće imati bilo koji broj takvih blokova (jedan, dva, tri, četiri...).

Struktura jedne if...else if...else naredbe prikazana je slikom 11.7.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_07.png)

Slika 11.7. if…else if…else naredba  
  

Tok izvršavanja koda sa slike 11.7 je sledeći:

- izvršavanje koda dolazi do prvog uslova (condition1);
- ==ukoliko je uslov condition1 ispunjen, izvršava se block1== i nakon toga se izlazi iz if…else if…else konstrukcije;
- ==ukoliko prvi uslov (condition1) nije ispunjen, ispituje se tačnost drugog== uslova (condition2);
- ukoliko je uslov condition2 ispunjen, izvršava se block2;
- ukoliko nijedan od uslova nije ispunjen, izvršava se else blok koda.

Primer korišćenja if…else if…else naredbe je sledeći:

```java
intspeed = 50;
if(speed < 10) {
    System.out.println("Too slow...");
} elseif(speed <= 80) {
    System.out.println("Regular speed.");
} elseif(speed < 100) {
    System.out.println("Too fast!");
} else{
    System.out.println("Incorrect value");
}
```

  
Nakon izvršavanja prikazanog koda, na izlazu se dobija:

Regular speed.

U narednim redovima biće objašnjen postupak koji je doveo do ispisa ovakve vrednosti na izlazu. Prvom naredbom deklariše se i inicijalizuje promenljiva speed sa vrednošću 50. if…else if…else naredba poseduje tri uslova. Ukoliko je vrednost promenljive speed manja od 10, izvršava se prvi blok koda. Pošto to nije slučaj, ispituje se istinitost drugog uslova. Drugi uslov je istinit ukoliko je vrednost promenljive speed manja ili jednaka broju 80. Ovaj uslov je ispunjen, jer je 50 manje od 80, pa izvršavanje programa ulazi u prvi else if blok i ispisuje se poruka Regular speed.

Bitno je razumeti još jednu veoma bitnu osobinu prikazane konstrukcije. Drugi else if blok poseduje sledeći uslov: speed < 100. Ukoliko se analizira ovakav uslov, može se zaključiti da je i on ispunjen, jer je 50 manje od 100. Ipak, unutar naredbe if…else if…else izvršava se uvek samo jedan blok koda, i to prvi čiji uslov se pokaže kao istinit.

### Ternarni operator

O ternarnom operatoru već je bilo reči u lekciji o operatorima. Tada je rečeno da je ternarni operator veoma koristan u ==situacijama kada je potrebno ostvariti kontrolu toka. Da budemo precizniji, korišćenjem ternarnog operatora moguće je promenljivoj dodeliti vrednost na osnovu nekog uslova:==

```java
String message = (age < 18) ? "You can't enter": "Welcome";
```

  
Struktura ternarnog operatora definisanog u prikazanoj naredbi ilustrovana je slikom 11.8.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_11_08.png)*

*Slika 11.8. Ternarni operator  
  
*

S obzirom na to da je ternarni operator već obrađen, njegov način funkcionisanja je jasan. Uslov je age < 18, a potencijalne vrednosti koje bi mogle da budu dodeljene promenljivoj message su You can’t enter i Welcome. Ukoliko je vrednost promenljive age manja od 18, message dobija vrednost You can’t enter. Ukoliko je vrednost promenljive age 18 ili više, message dobija vrednost Welcome.

==Ternarni operator se uvek može transformisati u if...else naredbu==. Tako se logika sa slike 11.8. može transformisati na sledeći način:

```html
String message = "";
int age = 19;
 
if (age < 18) {
    message = "You can't enter";
} else {
    message = "Welcome";
}
System.out.println(message);
```

  
Rezultat prikazanog primera biće ispis vrednosti Welcome, zato što je vrednost promenljive age veća od 18.

Koji uslovni blok u if konstrukciji se koristi za navođenje logike koja će se izvršiti u slučaju da nijedan od definisanih uslova nije zadovoljen?

  

### Vežbe

**Vežba 1**

Potrebno je prepraviti sledeći kod da bi bio ispravno napisan:

```java
intx = 10;
inty = 12;
 
if(x = y)
{
    
}
elseif(x == 0);
{
    
}     
else(x)
{
    
}
```

**  
Objašnjenje:**

- unutar if uslova treba da stoji operator poređenja, a ne operator dodele;
- nakon else if uslova, karakter tačka i zapeta je višak;
- else nikada ne sme da sadrži uslov.

**Vežba 2**

Napraviti program za obavljanje osnovnih računskih operacija. Program treba da poseduje tri promenljive: dve za čuvanje numeričkih vrednosti, dok treća promenljiva treba da služi za čuvanje karaktera koji će predstavljati aritmetičku operaciju koju je potrebno obaviti nad operandima.

### Rešenja

**Vežba 1**

```java
intx = 10;
inty = 12;
 
if(x == y)
{
    
}
elseif(x == 0)
{
    
}
else
{
    
}
```

**  
Vežba 2**

```java
charop = '*';
doublea = 5;
doubleb = 3;
 
if(op == '+') {
    System.out.println(a + b);
}
elseif(op == '-') {
    System.out.println(a - b);
}
elseif(op == '/') {
    System.out.println(a / b);
}
elseif(op == '*') {
    System.out.println(a * b);
}
else{
    System.out.println("Incorrect operation");
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_11.thb) JCPR1\_11.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_11.Mp4")

Kako Vam mogu pomoći?