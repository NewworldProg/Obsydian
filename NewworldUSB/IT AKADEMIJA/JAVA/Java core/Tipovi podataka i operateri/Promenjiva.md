---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=534997ee6090c46fdc29860655676b49_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434676"
author:
published:
created: 2025-04-29
description:
tags:
  - "clippings"
---
Jedinica 9 od 22

## Promenljive

U prethodnoj lekciji bilo je reči o različitim tipovima podataka koji postoje u Java jeziku. Mogli ste da vidite, na primer, da se u jednom Java programu neka tekstualna vrednost definiše na sledeći način:

```java
String message = "Hello World";
```

  
U prethodnoj lekciji je takođe rečeno da je message identifikator, pomoću koga je ovako definisana vrednost dostupna u kodu koji pišemo. Zapravo, prikazana naredba ilustruje kreiranje jedne promenljive u jeziku Java. Šta su to promenljive, koje su njihove osobine u jeziku Java i kako se kreiraju i koriste – biće ilustrovano u lekciji koja je pred vama.  
  

### Šta su promenljive?

Promenljive su kontejneri u koje se skladište vrednosti. Drugim rečima, nakon što se neka vrednost uskladišti u memoriji, ona biva reprezentovana kroz promenljivu. Jedna promenljiva tokom izvršavanja Java programa može da ima različite vrednosti i upravo se zbog toga ona i naziva promenljiva.

Osnovni oblik u kome se može javiti jedna promenljiva u Java jeziku izgleda ovako:

```java
String message;
```

  
Na osnovu ove naredbe možemo da zaključimo da se promenljiva minimalno sastoji iz:

- tipa podatka koji će promenljiva moći da prihvati (u prikazanom primeru je to tip String, što znači da će promenljiva moći da prihvati podatke tekstualnog tipa);
- identifikatora koji predstavlja naziv promenljive (u primeru je to message).

U ovom trenutku je bitno da primetite da se dve naredbe koje su prikazane u dosadašnjem toku ove lekcije neznatno razlikuju. U prvoj naredbi obavlja se definisanje vrednosti, dok u drugoj naredbi to nije slučaj. U narednim redovima podrobnije ćemo se posvetiti razlikama između dve prikazane naredbe.  
  

### Deklarisanje i inicijalizovanje

Da bi neka promenljiva postojala, mora se kreirati. Proces kreiranja promenljive naziva se **deklarisanje**. Deklaracija je zapravo sledeća naredba:

```java
String message;
```

  
Deklaracija se sastoji iz dva dela. Prvi označava tip podatka koji će promenljiva predstavljati, a drugi predstavlja naziv promenljive.

Proces dodeljivanja vrednosti nekoj promenljivoj drugačije se naziva inicijalizovanje:

```java
message = "Hello World";
```

  
Stoga prva naredba ilustruje deklaraciju, a druga inicijalizaciju:

```java
String message; 
message = "Hello World";
```

  
Nakon samih naredbi dodati su komentari koji ih opisuju. Prvom naredbom se obavlja kreiranje promenljive, odnosno deklaracija, dok se drugom naredbom obavlja postavljanje vrednosti promenljive, odnosno inicijalizacija.

Deklaracija i inicijalizacija se mogu obaviti i objedinjeno, odnosno u jednoj naredbi i to na sledeći način:

```java
String message = "Hello World";
```

  
Ovde, dakle, imamo deklaraciju i inicijalizaciju u jednoj naredbi. Na ovaj način smo razrešili dilemu o razlikama između dve naredbe koje su prikazane na početku ove lekcije.

| **Zašto se promenljive zovu promenljive?**  Promenljive su dobile naziv zbog mogućnosti redefinisanja vrednosti. To praktično znači da je vrednost jedne promenljive u svakom trenutku moguće promeniti:  ```java String message = "Hello World";  message = "This is new message"; ```     Ovo su sada dve naredbe. U prvoj naredbi se obavlja deklaracija i inicijalizacija promenljive sa nazivom message i vrednošću Hello World. U drugoj naredbi se obavlja promena vrednosti promenljive. Stoga nakon druge naredbe promenljiva message ima novu vrednost – This is new message.  Promenu vrednosti jedne promenljive je moguće obaviti proizvoljan broj puta, sve dok se poštuje njen tip. To znači da prilikom promene vrednosti String promenljive njoj nije moguće dodeliti vrednost nekog drugog tipa:  ```java String message = "Hello World"; message = 33; ```     Ovakav kod nije validan, zbog nepodudaranja tipa nove vrednosti i tipa promenljive. |
| --- |

Unutar bloka u kom pišemo kod u ovoj lekciji (a to je unutar main metode) može postajati samo jedna promenljiva sa jednim nazivom (slika 9.1).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_09_01.png)

*Slika 9.1. Unutar jednog bloka koda, sve promenljive moraju imati jedinstvene nazive  
  
*

U kodu primera sa slike 9.1. možete videti dve promenljive istog naziva unutar main metode. Razvojno okruženje jasno signalizira postojanje sintaksne greške i obaveštava nas da promenljiva sa nazivom years već postoji unutar bloka.  
  

### Imenovanje promenljivih

Naziv promenljive je ono što se navodi nakon ključne reči kojom se definiše njen tip. Programer ima mogućnost da samostalno definiše naziv promenljive. Ipak, naziv promenljive je zapravo jezički element koji se naziva **identifikator** i o njemu je već bilo reči u lekciji o sintaksi Java jezika. Prilikom imenovanja promenljivih važe sva ona pravila koja su navedena i za formiranje identifikatora:

- naziv promenljive može biti sastavljen iz slova, brojeva i karaktera donja crta i dolar;
- naziv promenljive mora imati makar jedan karakter;
- naziv promenljive ne sme početi brojem;
- naziv promenljive je osetljiv na velika i mala slova, tako da myVar i MyVar nije isto;
- naziv promenljive ne sme sadržati razmake;
- ključne reči se ne mogu koristiti kao naziv promenljive.

Upravo navedene stavke se odnose na pravila kojih se moramo pridržavati kako bi kod koji pišemo bio sintaksno ispravan. Pored neophodnih pravila, prilikom imenovanja promenljivih dobro je pridržavati se i nekih ustaljenih dobrih praksi, koje su formulisane kroz konvencije imenovanja. Jedna od najpopularnijih je *CamelCase* notacija, koja podrazumeva veliko slovo na početku svake reči u promenljivoj, osim eventualno prve:

MyVariable ili myFirstVariable

Kao što možete videti, sve reči od kojih se sastoji naziv promenljive pišu se sastavljeno, sa početnim velikom slovom, s tim što prvo slovo naziva promenljive može biti malo ili veliko.

Praksa je da se promenljive nazivaju intuitivnim imenima. Na primer, sledeći kod predstavlja loše nazvane promenljive:

```java
String i;
intnumber;
floatp1;
doublea;
```

  
Na osnovu naziva ovih promenljivih ni na koji način se ne može zaključiti čemu su one namenjene. Stoga je mnogo bolja praksa imenovanja u sledećem primeru:

```java
String userName;
intusersNumber;
floatbirthYear;
doublefirstOperand;
```

  
Ovo su sada primeri naziva promenljivih koji su slikoviti i intuitivni.

Na kraju, najčešća je praksa da se u okviru jednog programerskog tima, odnosno jedne organizacije, usvoje pravila o imenovanju svih elemenata koda, koja zatim primenjuju svi programeri. Na taj način se olakšava snalaženje u kodu i podiže produktivnost prilikom timskog rada.  
  

### Ispis vrednosti promenljivih

U skupu ugrađenih funkcionalnosti Java jezika nalazi se i nekoliko metoda koje omogućavaju ispis poruka na izlazu:

- println
- print
- printf

Do sada smo se već upoznali sa jednim od načina za ispis vrednosti iz Java programa. Naravno, reč je o metodi **println***.* Evo kako se ona koristi:

```java
intx = 5;
System.out.println(x);
```

  
Na izlazu dobijamo ispisanu vrednost promenljive x, a to je 5. Metoda println ispisuje poruku na izlazu i prelazi u novi red. U ovo se možemo uveriti ukoliko napišemo sledeći kod:

```java
intx = 5;
inty = 10;
System.out.println(x);
System.out.println(y);
```

  
Vrednosti promenljivih će biti ispisane jedna ispod druge:

5  
10

  
Ukoliko je potrebno ispisati vrednosti u istom redu, može se koristiti metoda **print**:

```java
intx = 5;
inty = 10;
System.out.print(x);
System.out.print(y);
```

  
Primer je identičan prethodnom, osim što se upotrebljava metoda print umesto metode println. Ipak, ispis je sada ovakav:

510

Vrednosti su napisane jedna nakon druge, bez razmaka i prelaska u novi red. U tome je razlika između metoda print i println.

Još jedan način za ispis poruka na izlazu jeste korišćenje metode **printf**. Metoda printf omogućava kombinovanje predefinisanog teksta i vrednosti promenljivih i koristi se na sledeći način:

```java
intx = 5;
System.out.printf("The value of variable x is %d", x);
```

  
Izvršavanjem ovakvog koda, dobija se sledeći ispis:

The value of variable x is 5

Evo kako je dobijen ovakav ispis. U okviru tekstualnog ispisa (koji se nalazi pod znacima navoda), bitno je da primetite sekvencu karaktera **%d**. U okviru finalnog ispisa, ova sekvenca karaktera je zamenjena vrednošću promenljive x. To je upravo i svrha ovakvog načina prikaza promenljivih na izlazu. Sekvenca karaktera %d označava da će na njenom mestu u okviru ispisa stajati celobrojna vrednost promenljive, koja je navedena nakon navodnika.

Identičan pristup je moguće koristiti i za ispis većeg broja promenljivih:

```java
intx = 5;
doubley = 12.1313467445;
System.out.printf("The value of variable x is %d%nThe value of variable y is %.4f", x, y);
```

  
Ovoga puta se na izlazu dobija sledeći ispis:

The value of variable x is 5  
The value of variable y is 12.1313  
  

Na izlazu se dobijaju dve linije ispisa, koje potiču iz jedne naredbe za ispis. Naredbom se zapravo ispisuju vrednosti dve promenljive. Prva je tipa int, a druga tipa double. Za dobijanje prikazanog ispisa, unutar String vrednosti postavljeno je nekoliko specijalnih sekvenci karaktera:

- %d – označava mesto na kome je potrebno umetnuti celobrojnu vrednost neke promenljive;
- %n – označava prelazak u novi red, baš kao i sekvenca karaktera **\\n**;
- %.4f – označava mesto na kome je potrebno da se pojavi broj sa decimalnim delom;.4 označava da je broj potrebno zaokružiti na četiri decimale.

| **Gde se nalaze metode za ispis vrednosti?**  U prethodnim redovima podrobnije smo se upoznali sa tri ugrađene funkcionalnosti Java jezika za ispis poruka unutar konzole/terminala. Za takve funkcionalnosti se kaže da su ugrađene, s obzirom na to da su one sastavni deo samog jezika, odnosno Java izvršnog okruženja. Sve one se nalaze unutar klase PrintStream koja objedinjuje funkcionalnosti za ispis podataka. Ova klasa sastavni je deo ugrađene klase System. |
| --- |

### Konverzija vrednosti

Nešto ranije ste imali prilike da vidite da je vrednost jedne promenljive moguće menjati proizvoljan broj puta, sve dok se ostaje u okvirima tipa koji je definisan. U narednim redovima, moći ćete da vidite da pravilo striktnog poštovanja tipa nije u potpunosti isključivo i da je u nekim situacijama vrednost promenljive jednog tipa moguće dodeljivati promenljivoj koja je drugog tipa. Java virtuelna mašina u takvim situacijama samostalno obavlja konverziju tipova. Kako biste lakše razumeli o čemu je reč, analiziraćemo sledeću situaciju:

```java
intx = 10;
doubley = x;
System.out.println(y);
```

  
U prikazanom primeru, prvo je deklarisana i inicijalizovana jedna promenljiva tipa int. Njena vrednost je postavljena na 10. Zatim je deklarisana još jedna promenljiva (y) i njoj je dodeljena vrednost promenljive x. Iako su vrednosti različitih tipova, JVM u pozadini za nas obavlja konverziju. Upravo zbog toga se ovakva vrsta konverzije naziva **implicitna konverzija**.

**Implicitnu konverziju** je moguće obaviti isključivo između kompatibilnih tipova, odnosno kada se promenljivoj čiji je tip šireg opsega dodaje vrednost promenljive čiji je tip užeg opsega. U prikazanom primeru je upravo to i obavljeno. Tip int u memoriji zauzima 4 bajta, a tip double 8 bajtova. Upravo zbog toga, JVM može da pretvori vrednost int tipa u tip double bez ikakvih gubitaka. Obrnuti slučajevi implicitne konverzije nisu mogući:

```java
doublex = 10.5;
inty = x;
```

  
Ovakva situacija će da proizvede sintaksnu grešku, zato što pokušavamo da dodelimo vrednost double tipa promenljivoj koja je tipa int. Vrednosti tipa double zauzimaju duplo veću količinu memorije, pa JVM podrazumevano ovakvu vrstu konverzije ne dozvoljava. Ipak, i nju je moguće obaviti, ali je to neophodno naglasiti. Tako dolazimo i do druge vrste konverzije koja postoji u Javi. Reč je o eksplicitnoj konverziji.

**Eksplicitna konverzija** se obezbeđuje navođenjem tipa u koji želimo da izvršimo konverziju. Tip se navodi u zagradama ispred naziva promenljive čiji tip vrednosti konvertujemo:

```java
doublex = 10.5;
inty = (int)x;
```

  
Sada je ispred naziva promenljive x, unutar zagrada, postavljen tip int. Na taj način se postiže eksplicitna konverzija. Eksplicitna konverzija se često drugačija naziva kastovanje.

S obzirom na to da se u prikazanom primeru konvertuje vrednost koja u memoriji zauzima 8 bajtova (double) u vrednost koja u memoriji zauzima 4 bajta (int), očekivano je da dolazi do gubitka određenih informacija. U to se lako možemo uveriti ispisom vrednosti promenljive y, koja je sledeća:

10

Deo iza decimalne tačke je izgubljen, pa se ovakva vrsta konverzije često naziva i konverzija sa gubicima (*lossy conversion*).

Upravo prikazane konverzije je moguće obavljati samo između kompatibilnih vrednosti. Tako, na primer, nije moguće konvertovati boolean u double:

```java
booleanx = true;
doubley = (double) x;
```

  
Ovakav kod proizvodi grešku. Jednostavno, konverziju tipa boolean nije moguće izvršiti ni eksplicitno ni implicitno.

Kako se naziva konverzija manjeg primitivnog podatka u veći, koju JVM obavlja automatski?

  

### Promenljive bez eksplicitno definisanog tipa

U programskom jeziku Java moguće je obaviti kreiranje promenljive bez eksplicitnog definisanja njenog tipa. Za obavljanje takvog posla, umesto konkretnog tipa, koristi se posebna rezervisana reč – **var**.

```java
var name = "Ben";
```

  
Ovo je primer deklaracije i inicijalizacije jedne promenljive bez eksplicitno definisanog tipa. U ovakvim situacijama, kompajleru se prepušta da samostalno utvrdi kojeg tipa je definisana vrednost. Upravo zbog toga se var može koristiti samo prilikom objedinjene deklaracije i inicijalizacije. Drugim rečima, ovako nešto ne bi bilo validno:

```java
var name;
```

  
S obzirom na to da je var upotrebljen prilikom deklaracije, ovakva naredba nije validna, što jasno signalizira i razvojno okruženje (slika 9.2).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_09_02.png)

*Slika 9.2. var se ne može koristiti u naredbama bez inicijalizacije  
  
*

S obzirom na to da se Java kompajler oslanja na vrednost kako bi pogodio tip promenljive, upotreba reči var u naredbama bez inicijalizacije nije moguća.

Upotreba reči var posebno je korisna prilikom baratanja složenim tipovima podataka, kada može značajno da pojednostavi i ubrza proces pisanja izvornog koda.

| **Napomena**  Reč var zapravo nije ključna reč u jeziku Java, već samo rezervisan naziv tipa podatka. Stoga je reč var moguće koristiti i kao identifikator za imenovanje promenljivih. |
| --- |

Sada, u okviru radnog okruženja, možete testirati i upotrebu ključne reči var prilikom deklaracije i inicijalizacije promenljivih.  
  

### Vežbe

**Vežba 1**

Nazive promenljivih treba izmeniti tako da budu sintaksno ispravni i u skladu sa konvencijama:

```java
String 1stUserName;
intbdt; 
floato1;
```

**  
Vežba 2**

Potrebno je deklarisati dve promenljive: jednu promenljivu tipa double sa vrednošću 15,757 i jednu celobrojnu promenljivu tipa int. Potrebno je izvršiti konverziju promenljive sa pokretnim zarezom u celobrojnu vrednost.

### Rešenja

**Vežba 1**

```java
String firstUserName;
intbirthDate;  //date of birthday
 
floatoperand1; //first operand
```

  
ili

```java
floatfirstOperand; //first operand
```

**  
Vežba 2**

```java
public classMain {
    public static void main(String[] args) {
 
        double x =15.757;
        inty =(int) x;
        System.out.println(y);
       
    }
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_09.thb) JCPR1\_09.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_09.Mp4")

Kako Vam mogu pomoći?