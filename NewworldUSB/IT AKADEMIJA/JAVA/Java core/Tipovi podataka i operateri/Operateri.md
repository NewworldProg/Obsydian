---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=534997ee6090c46fdc29860655676b49_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434677"
author:
published:
created: 2025-04-29
description:
tags:
  - "clippings"
---
Jedinica 10 od 22

## Operatori

Do sada smo naučili kako da u Java programu korišćenjem promenljivih definišemo vrednosti različitih tipova i da takve vrednosti prikažemo na izlazu. Ipak, osnovna namena svakog kompjuterskog programa jeste da na neki način izmeni podatke koji se koriste tokom izvršavanja programa. Takva operacija se drugačije naziva obrada podataka, a osnovni mehanizmi obrade podataka zasnivaju se na upotrebi operatora. Stoga će lekcija pred vama u potpunosti biti posvećena pojmu operatora, što će nam na kraju omogućiti da kreiramo znatno upotrebljivije Java programe.  
  

### Šta su operatori?

Operatori su posebni leksički elementi jezika, koji omogućavaju izvršavanje operacija nad vrednostima. Iako to možda niste znali, unutar primera iz prethodnih lekcija intenzivno je korišćen jedan operator:

```java
intx = 10;
```

  
Ovo je primer deklaracije i inicijalizacije jedne promenljive. Za obavljanje inicijalizacije koristi se karakter jednako (=). Reč je o operatoru dodeljivanja. Operator dodeljivanja, kao što i samo ime sugeriše, vrši dodeljivanje vrednosti promenljivoj.  
  

### Koji operatori postoje u Java jeziku?

Java jezik poznaje nekoliko vrsta operatora:

- aritmetički operatori;
- operatori dodeljivanja;
- operatori poređenja;
- logički operatori.

U nastavku ove lekcije detaljno ćemo se upoznati sa svakom upravo navedenom grupom operatora.  
  

### Aritmetički operatori

Aritmetički operatori su oni koji izvršavaju aritmetičke operacije nad vrednostima. Tabela 10.1 prikazuje aritmetičke operatore jezika Java.

| **Operator** | **Značenje** |
| --- | --- |
| + | sabiranje |
| \- | oduzimanje |
| \* | množenje |
| / | deljenje |
| % | modulo (ostatak deljanja) |

*  
Tabela 10.1. Aritmetički operatori u jeziku Java  
  
*

**Sabiranje, oduzimanje, množenje i deljenje**

Četiri operatora standardnih aritmetičkih operacija, baš kao i u matematici, obavljaju sabiranje, oduzimanje, množenje i deljenje. Primer njihovog korišćenja može da izgleda ovako:

```java
intx = 10;
inty = 5;
 
System.out.println(x + y);
System.out.println(x - y);
System.out.println(x * y);
System.out.println(x / y);
```

  
U primeru je prvo obavljeno deklarisanje i inicijalizovanje dve celobrojne promenljive sa vrednostima 10 i 5. Zatim su nad njima upotrebljeni aritmetički operatori za sabiranje, oduzimanje, množenje i deljenje. Kod proizvodi sledeći izlaz:

15  
5  
50  
2

  
Prilikom izvođenja aritmetičkih operacija, treba voditi računa o redosledu njihovog izvršavanja. Aritmetičke operacije u Javi imaju isti prioritet izvršavanja kao i u matematici. Množenje i deljenje imaju prednost nad sabiranjem i oduzimanjem. Redosled izvršavanja operacija može da se promeni upotrebom zagrada.

**Modulo (ostatak)**

Operator % koristi se za dobijanje celobrojnog ostataka pri deljenju dva broja:

```java
intmodulo = 10% 3;    
System.out.println(modulo);
```

  
Ovakav kod proizvodi sledeći rezultat:

1

Do ovakvog rezultata došlo se na sledeći način: najveći ceo broj koji se može dobiti deljenjem broja 10 brojem 3 jeste broj 3; 3 puta 3 je 9, što znači da do vrednosti 10 ostaje 1; 1 je ostatak, što je i rezultat koji se dobija od prikazanog koda.

Evo još nekih primera upotrebe ovog operatora:

```java
System.out.println(10% 4); 
System.out.println(10% 6);
```

  
Nakon samih naredbi, pod komentarima možete videti rezultate koji se na ovaj način dobijaju.  
  

### Operatori za uvećavanje i umanjenje vrednosti

Posebna vrsta aritmetičkih operatora u Java jeziku jesu operatori koji se koriste za uvećavanje i umanjenje vrednosti. Njih karakteriše upotreba nad samo jednim [operandom](https://www.link-elearning.com/linkdl/opisPojma.php?id=160446 "operandom"), te se stoga često drugačije nazivaju unarni operatori. Operatori za uvećavanje i umanjivanje prikazani su tabelom 10.2.

| **Operator** | **Značenje** |
| --- | --- |
| ++ | operator uvećanja (vrši uvećanje za jedan) |
| \-- | operator umanjenja (vrši umanjenje za jedan) |

*  
Tabela 10.2. Operatori za uvećanje i umanjenje  
  
*

Primer korišćenja operatora uvećavanja može da izgleda ovako:

```java
intx = 10;
x++;
```

  
Nakon izvršenja prikazanog koda, promenljiva x će imati vrednost 11.

Operator za uvećavanje je ekvivalent korišćenju aritmetičkog operatora sabiranja, na sledeći način:

```java
intx = 10;
x = x + 1;
```

  
Operatori za uvećavanje i umanjivanje mogu se postavljati nakon, ali i ispred vrednosti, odnosno operanda. Tako nešto posebno je značajno kada se operatori uvećanja i umanjenja koriste unutar naredbe za dodeljivanje vrednosti. Evo pogledajte o čemu je reč:

```java
intx = 10;
inty = x++;
```

  
Možda očekujete da će promenljiva y da dobije vrednost 11 (10+1), ali tako nešto neće biti slučaj. Promenljiva y će nakon izvršavanja prikazanog koda imati vrednost 10. Jednostavno, operator dodeljivanja ima prioritet, pa se dodeljivanje obavlja pre uvećavanja. Ukoliko želimo da se prvo obavi uvećanje, pa tek onda i dodela, potrebno je napisati sledeće:

```java
intx = 10;
inty = ++x;
```

  
Operator uvećavanja sada je premešten pre promenljive čija vrednost se uvećava. Tako će uvećavanje biti obavljeno pre dodele i na kraju će promenljiva y imati vrednost 11.

### Operatori dodeljivanja

Operatorima dodeljivanja obavlja se dodeljivanje neke vrednosti promenljivoj. Osnovni operator dodeljivanja jeste karakter jednako (=). Ipak, Java poznaje i nekoliko drugih operatora ovog tipa, koji predstavljaju zapravo kombinaciju operatora dodeljivanja i aritmetičkih operatora (tabela 10.3).

| **Operator** | **Opis** | **Primer** | **Značenje** |
| --- | --- | --- | --- |
| \= | dodeljuje vrednost sa desne strane promenljivoj sa leve | x = y | x = y |
| += | uvećava vrednost promenljive x za vrednost y i novodobijenu vrednost dodeljuje promenljivoj x | x += y | x = x + y |
| \-= | umanjuje vrednost promenljive x za vrednost y i novodobijenu vrednost dodeljuje promenljivoj x | x -= y | x = x - y |
| \*= | množi vrednost promenljive x sa vrednošću y i novodobijenu vrednost dodeljuje promenljivoj x | x \*= y | x = x \* y |
| /= | deli vrednost promenljive x sa vrednošću y i novodobijenu vrednost dodeljuje promenljivoj x | x /= y | x = x / y |
| %= | računa ostatak deljanja vrednosti x vrednošću y i dobijeni rezultat dodeljuje promenljivoj x | x %= y | x = x % y |

  
*Tabela 10.3. Operatori dodeljivanja  
  
*

Kao što je već rečeno, osnovni operator dodeljivanja jeste karakter jednako (=), sa čijom upotrebom smo se do sada već više puta susretali:

```java
inta = 10;
String myString = "Hello World";
intz = 3;
```

  
Ovo su sve primeri korišćenja operatora dodeljivanja za obavljanje inicijalizacije promenljivih.

U tabeli 10.3. možete da vidite da se standardni operator dodeljivanja može kombinovati sa aritmetičkim operatorima i da se na taj način mogu dobiti zanimljivi efekti. Evo jednog primera kombinovanja operatora sabiranja i operatora dodele:

```java
intx = 10;
x += 5;
System.out.println(x);
```

  
U primeru je prvo deklarisana i inicijalizovana promenljive x, sa vrednošću 10. U drugoj naredbi je vrednost promenljive x uvećana za 5 i tako dobijena nova vrednost dodeljena je promenljivoj x. Na kraju, kod na izlazu proizvodi sledeći efekat:

15

Upravo dobijeni efekat je mogao da bude postignut i na sledeći način:

```java
intx = 10;
x = x + 5;
System.out.println(x);
```

  
Sada možete da vidite jasno raščlanjene sve korake koji su u prethodnom primeru bili sakriveni upotrebom operatora za objedinjeno sabiranje i dodeljivanje. Po identičnom principu funkcionišu i ostali operatori koji predstavljaju kombinaciju neke aritmetičke operacije i dodeljivanja.

### Operatori poređenja

Java poseduje nekoliko operatora koje je moguće koristiti za poređenje dve ili više vrednosti. Poređenjem dolazi do stvaranja nove vrednosti, koja ukazuje na rezultat poređenja. Takva vrednost je logičkog tipa (boolean), što je jedan od prostih Java tipova, obrađen u prethodnim lekcijama.

Operatori poređenja koriste se u logičkim izjavama kako bi utvrdili istinitost nekog izraza. Tabela 10.4. prikazuje operatore poređenja Java jezika.

| **Operator** | **Značenje** |
| --- | --- |
| \== | jednako je |
| != | nije jednako |
| < | manje od |
| \> | veće od |
| \>= | veće ili jednako od |
| <= | manje ili jednako od |

*  
Tabela 10.4. Operatori poređenja*  
  

Osnovni primer korišćenja operatora poređenja biće prikazan nad sledećim promenljivama:

```java
intvalue1 = 1;
intvalue2 = 2;
```

  
Ovo su dve celobrojne promenljive (int tipa) sa vrednostima 1 i 2. Ukoliko bismo želeli da ispitamo njihovu jednakost, dovoljno bi bilo napisati nešto ovako:

```java
System.out.println(value1 == value2);
```

  
U ovakvoj situaciji, na izlazu se dobija sledeći ispis:

false

Vrednosti 1 i 2 nisu jednake, te se zbog toga kao rezultat ovakvog poređenja dobija vrednost false. Već je rečeno da korišćenje operatora poređenja kao svoj rezultat ima stvaranje nove boolean vrednosti. To praktično znači da je prikazani primer samo skraćeni oblik ovakvog koda:

```java
intvalue1 = 1;
intvalue2 = 2;
 
booleanisEqual = value1 == value2;
 
System.out.println(isEqual);
```

  
U primer je sada uključena još jedna promenljiva, unutar koja je smeštena vrednost koja se dobija poređenjem korišćenjem operatora jednakosti.

| **\= i ==**  Pazite da ne pomešate operatore **\=** i **\==**. Prvi operator je operator dodele, dok je drugi operator – operator poređenja. Greška uzrokovana pogrešnom upotrebom ova dva operatora može drastično izmeniti tok programa. Zato je veoma važno da do nje ne dođe. |
| --- |

Po identičnom principu se mogu koristiti i ostali operatori poređenja:

```java
System.out.println(value1 != value2);
```

  
Ovo je sada primer u kome se ispituje nejednakost, pa se na izlazu dobija:

true

Vrednosti 1 i 2 nisu jednake, pa otuda vrednost true (istinito). Izraz bi mogao da se pročita ovako: *Da li su vrednosti promenljivih value1 i value2 različite*? Odgovor je, naravno, potvrdan, pa otuda i kao rezultat vrednost true.

Upotreba operatora < i > poznata je iz matematike:

```java
System.out.println(value1 < value2);
System.out.println(value1 > value2);
```

  
Ovakav kod proizvodi sledeći efekat:

true  
false

  
Vrednost promenljive value1 jeste manja od vrednosti promenljive value2, pa je otuda prva vrednost **true**, a druga **false**.

Pored operatora veće i manje, u Javi, baš kao i u matematici, postoje operatori veće-jednako i manje-jednako:

```java
intvalue1 = 2;
intvalue2 = 2;
 
System.out.println(value1 <= value2);
System.out.println(value1 >= value2);
```

  
Na izlazu se dobijaju sledeći rezultati:

true  
true  
  

### Logički operatori

Logički operatori se koriste kako bi utvrdili logičku povezanost između promenljivih, odnosno vrednosti. Najčešće se koriste u kombinaciji sa upravo prikazanim operatorima poređenja.

Logičkim operatorima se mogu kreirati različiti složeni logički izrazi, koji kao svoju finalnu vrednost uvek moraju imati true ili false. Tabela 10.5. prikazuje logičke operatore.

| **Operator** | **Opis** | **Primer** | **Rezultat** |
| --- | --- | --- | --- |
| && | AND | (6 < 11 && 5 > 1)   (6 < 5 && 5 > 1) | true   false |
| \|\| | OR | (6 < 5 \|\| 5 > 1) | true |
| ! | NOT | !(6==6) | false |

  
*Tabela 10.5. Logički operatori u jeziku Java  
  
*

Analizom primera upotrebe logičkih operatora može se mnogo toga zaključiti. Operator AND zahteva ispunjenje svih navedenih uslova kako bi proizveo vrednost true. U protivnom, proizvodi vrednost false. Tabela 10.6. ilustruje različite situacije upotrebe logičkog operatora AND.

| **Izraz** | **Rezultat** |
| --- | --- |
| true && true | true |
| false && true | false |
| true && false | false |
| false && false | false |

  
*Tabela 10.6. Logički operator AND  
  
*

Sa druge strane, operator OR zahteva ispunjenje samo jednog od uslova kako bi kao svoju finalnu vrednost proizveo true (tabela 10.7).

| **Izraz** | **Rezultat** |
| --- | --- |
| true \|\| true | true |
| false \|\| true | true |
| true \|\| false | true |
| false \|\| false | false |

  
*Tabela 10.7. Logički operator OR  
  
*

Na kraju, operator NOT je operator negacije, koji true vrednost pretvara u false, a false u true, što je ilustrovano tabelom 10.8.

| **Izraz** | **Rezultat** |
| --- | --- |
| !true | false |
| !false | true |

  
*Tabela 10.8. Logički operator NOT  
  
*

| **Napomena**  Logički operatori posebno važnu upotrebnu vrednost imaju prilikom formiranja uslova za kontrolu toka izvršavanja koda. Kontrola toka izvršavanja programa biće predmet jedne od narednih lekcija. |
| --- |

Evo jednog primera upotrebe logičkih operatora:

```java
intvalue1 = 1;
intvalue2 = 2;
 
System.out.println((value1 == 1) && (value2 == 2));
System.out.println((value1 == 1) || (value2 == 2));
```

  
Deklarisane su dve promenljive i obavljena je njihova inicijalizacija vrednostima 1 i 2. Zatim su formulisana dva logička izraza. Rezultat je sledeći:

true  
true

  
Naravno, svaki od zasebnih uslova proizvešće vrednost true (pošto je 1=1 i 2=2), pa će i celokupni izrazi imati vrednosti true.

Ukoliko bismo sada malo izmenili same izraze, situacija bi se promenila. To možemo videti na sledećem primeru:

```java
System.out.println((value1 == 1) && (value2 == 3));
System.out.println((value1 == 1) || (value2 == 3));
```

  
Rezultat izvršavanja koda sada će biti ovakav:

false  
true

  
Jedna true i jedna false vrednost u kombinaciji sa operatorom AND (&&) proizvode konačnu false vrednost, dok u kombinaciji sa OR operatorom (||) daju vrednost true.

**Negacija**

U jeziku Java postoji i logički operator sa nazivom NOT. Reč je o operatoru koji se drugačije naziva operator negacije, a dobija se korišćenjem karaktera uzvičnik. NOT je ujedno i unarni operator, zato što za svoje funkcionisanje zahteva samo jedan operand.

Evo kako izgleda upotreba operatora NOT:

```java
booleansuccess = false;
System.out.println(success);
System.out.println(!success);
```

  
Nakon izvršenja koda, na izlazu se dobija:

false  
true

  
U prvoj naredbi deklarisana je i inicijalizovana promenljiva tipa boolean sa nazivom success.

Drugom naredbom na izlazu se ispisuje vrednost promenljive, dok se trećom naredbom takođe ispisuje vrednost promenljive, ali se pre ispisa obavlja negacija vrednosti korišćenjem operatora **NOT**. Iz tog razloga, na izlazu se dobija true. Zato što vrednost true pretvara u false, a false u true, NOT se veoma često naziva i operator invertovanja.

### Ternarni operator

Ternarni operator je obavezni operator svakog popularnijeg jezika. Ni Java nije izuzetak. Ovaj operator je nešto teži za razumevanje, ali je u osnovi veoma jednostavan i posebno koristan kada se jednom ovlada njegovom sintaksom.

Ternarni operator se koristi za dodelu vrednosti promenljivoj, ali na osnovu nekog predefinisanog uslova. Sintaksa ternarnog operatora je sledeća:

```java
myVariable = (condition) ? value1 : value2;
```

  
Napisano prostim jezikom, značenje navedene sintakse bi bilo: *ukoliko je* condition *ispunjen, promenjivoj* myVariable *dodeli* value1*, a u protivnom* value2*.*

Ternarni operator se gradi korišćenjem karaktera ? i:. Karakter upitnik (?) razdvaja uslov od mogućih vrednosti, a karakter dve tačke (:) razdvaja ponuđene vrednosti.

Primer upotrebe ternarnog operatora je sledeći:

```java
intage = 15;
  String message = (age < 18) ? "You can’t enter": "Welcome";
  System.out.println(message);
```

  
Ukoliko je vrednost promenljive age manja od 18, promenljiva message dobija vrednost *You can’t enter*. U protivnom, promenljiva message dobija vrednost *Welcome*.

### Nadovezivanje stringova

Nešto ranije prikazani aritmetički operator za sabiranje (+) u jeziku Java ima još jednu funkciju. Ova funkcija se ogleda u mogućnosti [nadovezivanja](https://www.link-elearning.com/linkdl/opisPojma.php?id=160457 "nadovezivanja") tekstualnih vrednosti ili konkatenacije stringova. Pogledajte primer:

```java
String s1 = "String";
String s2 = "Value";   
System.out.println(s1 + s2);
```

  
U primeru su definisane dve tekstualne vrednosti, a zatim su ove vrednosti sabrane kao da se radi o brojevima. Na izlazu se dobija:

StringValue

  
Konkatenacija je mogla da se izvede i na druge načine, a da se dobije isti izlaz:

```java
String s1 = "String";    
System.out.println(s1 + "Value");
```

  
Ili:

```java
System.out.println("String"+ "Value");
```

  
Može se zaključiti da u kombinaciji sa String vrednostima operator sabiranja obavlja dodavanje jedne tekstualne vrednosti drugoj, čime se dobija nova tekstualna vrednost.

Sada, u okviru radnog okruženja, možete testirati i operator konkatenacije String -ova.

Koji operator se koristi za proveru nejednakosti u programskom jeziku Java?

  

### Vežbe

**Vežba 1**

Potrebno je napraviti program koji sabira dva broja predstavljena kroz dve promenljive. Prvi broj predstavljen je promenljivom x, koja ima vrednost 1, dok druga promenljiva y ima vrednost 2. Potrebno je dodeliti rezultat sabiranja ove dve promenljive promenljivoj z. Rezultat je potrebno ispisati na izlazu.

**Vežba 2**

Potrebno je napraviti program koji izračunava površinu kruga sa poluprečnikom 5. Rezultat je potrebno ispisati na izlazu.

### Rešenja:

**Vežba 1**

```java
public classTest   {
    public static void main(String[] args)  {
 
    intx =1;
    inty =2;
 
    intz =x +y;
    System.out.println(z);
 
    }
}
```

**  
Vežba 2**

```java
publicclassTest   {
    publicstaticvoidmain(String[] args)  {
 
        doublePI = 3.14;
        doubler = 5;
 
        doublep = (r * r) * PI;
        System.out.println(p);
 
            }
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_10_01.thb) JCPR1\_10\_01.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_10_01.Mp4")

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_10_02.thb) JCPR1\_10\_02.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_10_02.Mp4")

Kako Vam mogu pomoći?