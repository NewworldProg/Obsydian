---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=54965ca798b7887d6c537c5bf9abe6bc_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434688"
author:
published:
created: 2025-05-10
description:
tags:
  - "clippings"
---
Jedinica 21 od 22

## Softverske greške i izuzeci

Greške su sastavni deo gotovo svakog softverskog proizvoda. Vrlo je teško pronaći složeniji program bez greške koja se u nekim situacijama može ispoljiti. Takođe, tokom razvoja i testiranja softverskih proizvoda vrlo često se detektuje i otkloni veliki broj softverskih grešaka. Sa druge strane, neke greške nikada ne budu detektovane i otklonjene.

Greške mogu prouzrokovati brojne probleme prilikom izvršavanja nekog programa. Simptomi mogu varirati od neočekivanog rezultata izvršavanja, preko korumpiranih podataka, pa sve do potpunog otkaza i nemogućnosti korišćenja kompletnog sistema. Stoga je razumevanje pojma softverskih grešaka i načina za njihovo otklanjanje od presudnog značaja prilikom razvoja softvera.  
  

### Softverske greške

Greška prilikom izvršavanja nekog programa drugačije se naziva **bug**. Naziv dolazi od engleske reči koja u prevodi znači buba. Pojam je popularizovala američka kompjuterska naučnica Grace Hopper, koja je 1947. godine, pokušavajući da otkloni softversku grešku na harvardskom elektromehaničkom kompjuteru, pronašla moljca zaglavljenog u releju.

Softverska greška jeste bilo koji nedostatak ili otkaz u kompjuterskom programu koji proizvodi netačno ili neočekivano ponašanje. Iz ugla modernih programskih jezika, pa samim tim i Java programiranja, softverske greške se mogu podeliti u tri grupe:

- **sintaksne greške** (*syntax errors*) – greške koje nastaju usled nepoštovanja sintaksnih pravila jezika;
- **greške tokom izvršavanja programa** (*runtime errors*) – greške koje kompajler ne detektuje, a koje se mogu ispoljiti tek tokom izvršavanja programa;
- **logičke greške** (*logic errors*) – greške do kojih dolazi tokom izvršavanja programa, ali okruženje ni na koji način ne signalizira njihovo postojanje; stoga je ovo najkompleksniji tip softverskih grešaka.

Lekcija pred vama biće posvećena razumevanju sintaksnih grešaka i grešaka do kojih dolazi tokom izvršavanja programa. Naredna lekcija biće posvećena detekciji i otklanjanu logičkih grešaka.

Koje greške su teže za detektovanje?

  

### Sintaksne greške

Sintaksne greške nastaju usled nepoštovanja sintaksnih pravila jezika koji se koristi. Ovakvu vrstu grešaka je uglavnom najjednostavnije detektovati i otkloniti, pošto je program sa sintaksnom greškom potpuno nefunkcionalan i ne može se prevesti. To praktično znači da prevođenje Java programa sa sintaksnom greškom neće biti moguće. Tokom prevođenja, kompajler detektuje sve sintaksne greške i na jasan način nas obaveštava o njihovom postojanju. Evo jednog takvog primera:

```java
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        System.out.println("Hello World")
 
    }
 
}
```

  
Ovo je primer jednog vrlo jednostavnog Java programa, koji na izlazu ispisuje poruku Hello World. Ipak, prikazani program poseduje jednu sintaksnu grešku, zbog koje ne može da bude preveden. Možete li da je detektujete?

Unutar prikazanog programa, naredba za ispis poruke na izlazu nije završena karakterom za završetak naredbe – tačkom i zapetom. Stoga, prikazani kod nije sintaksno ispravan i prevođenje neće biti moguće. Prilikom prevođenja, od Java kompajlera se dobija sledeća poruka:

C:\\java\_programs\\JavaProgram\\src\\JavaProgram.java:7:42  
java: ';' expected  
  

Evo upravo sada možete da vidite zbog čega se kaže da su sintaksne greške najjednostavnije za detekciju i otklanjanje. Program nije moguće prevesti, pa samim tim ni pokrenuti, a Java kompajler signalizira u čemu je problem. Tako dobijamo poruku da unutar klase JavaProgram postoji sintaksna greška na 42. karakteru 7. linije koda. Takođe, dobija se i dodatna poruka da se na navedenoj poziciji unutar našeg izvornog koda očekuje karakter tačka i zapeta.

| **IntelliJ IDEA Tip**  **Sintaksne greške**  Kada se za razvoj programa koristi neko od specijalizovanih razvojnih okruženja, kao što je IntelliJ IDEA, veoma su male šanse da ćete pokušati i da pokrenete program koji poseduje sintaksnu grešku. Naime, IntelliJ IDEA poseduje ugrađene mehanizme koji vrše detektovanje sintaksnih grešaka tokom pisanja koda. Tako se u upravo prikazanom primeru unutar editora dobija situacija kao na slici 21.1.  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_01.png)  *Slika 21.1. Primer detektovanja sintaksne greške od strane IntelliJ IDEA okruženja      *  Prilikom kreiranja ozbiljnijih Java programa, neretko se može dogoditi da u izvornom kodu u jednom trenutku postoji veći broj sintaksnih grešaka. Sve one se kumulativno mogu pregledati korišćenjem panela **Problems** (slika 21.2).  [*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_02.png)*](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_02-original.png)  *Slika 21.2. Panel Problems IntelliJ IDEA okruženja      *  Ukoliko se ipak odlučite da korišćenjem IntelliJ IDEA okruženja pokrenete program koji ima sintaksnu grešku, unutar panela *Build* moći ćete da vidite razlog zbog koga kompajliranje programa nije uspelo (slika 21.3).  [*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_03.png)*](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_03-original.png)  *Slika 21.3. Panel Build IntelliJ IDEA okruženja      *  Kako biste lakše mogli da locirate sintaksne greške u kodu korišćenjem njihove pozicije koja se dobija od Java kompajlera, moguće je koristiti podatak o tačnoj poziciji na kojoj se trenutno nalazi kursor unutar editora. Takav podatak u IntelliJ IDEA okruženju je dostupan unutar statusne trake (*status bar*), koja se nalazi u dnu prozora. Na slici 21.3, desno unutar statusne trake možete videti poziciju na kojoj se nalazi kursor (7:42). Ukoliko kod vas nema statusne trake, ona se može aktivirati/deaktivirati opcijom **View-** **\> Appearance-> Status bar**. |
| --- |

### Greške tokom izvršavanja programa

Ukoliko Java program ne poseduje sintaksne greška, njegovo prevođenje i pokretanje se obavlja bez problema. Ipak, to ne znači da tokom izvršavanja programa ne može doći do pojave grešaka. Evo primera jednog Java programa koji poseduje grešku koja će do izražaja doći tek tokom izvršavanja:

```java
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        int[] nums = newint[4];
        nums[7] = 10;
 
    }
 
}
```

  
U prikazanom programu, obavlja se deklarisanje jednog niza sa četiri celobrojne vrednosti. Zatim se u narednoj naredbi postavlja vrednost osmog člana niza (člana sa indeksom 7). S obzirom na to da u Java jeziku nizovi imaju fiksnu veličinu, ovako nešto proizvodi grešku tokom izvršavanja programa. Jednostavno, kompajler ne poseduje ugrađene mehanizme za detektovanje ovakve vrste grešaka. Zbog toga se ovakav kod prevodi i započinje izvršavanje od strane Java virtuelne mašine. Onoga trenutka kada izvršavanje dođe do naredbe za dodelu vrednosti osmom članu niza, JVM na izlazu emituje sledeću poruku:

Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 7 out of bounds for length 4  
at JavaProgram.main(JavaProgram.java:8)  
  

| **IntelliJ IDEA Tip**  **Greške tokom izvršavanja programa**  Kada se koristi IntelliJ IDEA razvojno okruže, interakciju sa Java programom koji se izvršava moguće je vršiti korišćenjem panela **Run** (slika 21.4).  [*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_04.png)*](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_04-original.png)  *Slika 21.4. Run panel Build IntelliJ IDEA okruženja      *  Ovo je panel u kome smo u svim primerima od sada dobijali poruke od naših Java programa. Stoga je panel Run mesto na kome će biti prikazane informacije i o greškama do kojih dolazi tokom izvršavanja Java programa.  Run panel je u svakom trenutku moguće otvoriti odabirom opcije **View -> Tool Windows -> Run.** |
| --- |

Evo još jednog primera koji može da proizvede grešku tokom izvršavanja programa:

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        intnumberA;
        intnumberB;
        doublenumberC;
 
        Scanner scanner = newScanner(System.in);
 
        System.out.println("Please, enter number A: ");
        numberA = scanner.nextInt();
 
        System.out.println("Please, enter number B: ");
        numberB = scanner.nextInt();
 
        numberC = numberA / numberB;
 
        System.out.println("Result: "+ numberC);
 
    }
 
}
```

  
Ovo je sada znatno realniji primer, koji podrazumeva ulazne podatke koji nisu unapred poznati. Drugim rečima, ulazni podaci (dva broja) preuzimaju se od korisnika, korišćenjem klase objekta Scanner. Zatim se prvi broj deli drugim i dobijeni rezultat se emituje na izlaz. Na prvi pogled, ne može se uočiti problem, a ni razvojno okruženje ni kompajler ne detektuju bilo kakav problem. I zaista, vrlo je moguće da ćete ovakav program upotrebiti dosta puta i da on neće proizvesti nikakvu grešku (slika 21.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_05.png)

*Slika 21.5. Primer toka izvršavanja programa za deljenje dva broja  
  
*

Ovo je jedan primer upotrebe našeg programa, sa ulaznim vrednostima 100 i 50. Kao što vidite, sve prolazi bez problema. Ipak, pogledajte i sledeći primer (slika 21.6).

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_06.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_06-original.png)

*Slika 21.6. Primer greške prilikom izvršavanja programa za deljenje dva broja  
  
*

Programu su sada prosleđeni nešto drugačiji ulazni parametri (100 i 0) i na slici 21.6. možemo da vidimo da dolazi do greške prilikom njegovog izvršavanja. Poruka koja se dobija od izvršnog okruženja je vrlo jasna: *deljenje nulom nije dozvoljeno*. Ovo je klasičan primer greške do koje može doći prilikom izvršavanja programa.

| **Greške prilikom izvršavanja programa čine da program odmah završi svoje izvršavanje**  Veoma bitna osobina grešaka do kojih dolazi tokom izvršavanja programa je da one čine da program momentalno zaustavlja svoje izvršavanje. Drugim rečima, dolazi do otkaza programa. To znači da će sve one naredbe koje se nalaze nakon naredbe sa greškom ostati neizvršene. U ovu konstataciju se veoma lako možemo uveriti. Dovoljno je da postavimo jednu naredbu za ispis jednostavne poruke odmah nakon naredbe koja može da proizvede grešku:  ```java numberC = numberA / numberB; System.out.println("Hello World"); ```     Prilikom pojave greške, moći ćete da vidite da se naredba za ispis poruke *Hello World* uopšte neće izvršiti. |
| --- |

### Pojam izuzetka

Pojava greške tokom izvršavanja Java programa propraćena je stvaranjem jednog veoma bitnog pojma. Reč je o pojmu izuzetka (*exception*). Drugim rečima, prilikom pojave greške tokom izvršavanja programa, Java izvršno okruženje kreira jedan objekat koji se naziva izuzetak i koji se koristi da reprezentuje grešku do koje je došlo.

Izuzetke smo mi već imali prilike da vidimo u prethodna dva primera. Poruke koje smo dobijali bile su zapravo poruke objekata izuzetka, a klase koje su korišćene za njihovo kreiranje takođe su bile ispisane u porukama koje smo dobijali. Tako je u primeru pristupa nepostojećem članu niza između ostalog bilo ispisano:

Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException

Ovo praktično znači da je u programu došlo do greške i da je tom prilikom kreiran objekat izuzetka na osnovu klase java.lang.ArrayIndexOutOfBoundsException.

Prilikom pojave greške u programu za deljenje dva broja, dobijali smo, između ostalog, sledeću poruku:

Exception in thread "main" java.lang.ArithmeticException

Ovo znači da je prilikom pokušaja deljenja nulom došlo do greške koja je reprezentovana objektom izuzetka koji je kreiran na osnovu klase java.lang.ArithmeticException.

S obzirom na to da su izuzeci reprezentacija grešaka do kojih dolazi tokom izvršavanja programa, Java platforma poseduje veliki broj ugrađenih klasa koje se koriste za predstavljanje različitih vrsta grešaka do kojih može doći prilikom izvršavanja programa (slika 21.7).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_07.png)*

*Slika 21.7. Ugrađene klase izuzetaka  
  
*

### Zbog čega su nam potrebni izuzeci?

Već je rečeno da su izuzeci objekti koje kreira okruženje kako bi moglo da artikuliše greške do kojih dolazi tokom izvršavanja programa. Ipak, osim poruke izuzetka, koja nam govori do kakve greške je došlo tokom izvršavanja programa, mi se još uvek nismo upoznali sa najznačajnijom osobinom izuzetaka. Reč je o mogućnosti njihove obrade.

Obrada izuzetaka podrazumeva adekvatno rukovanje objektima izuzetaka, čime se sprečava prekid izvršavanja Java programa. Proces obrade izuzetaka podrazumeva korišćenje tri specijalne naredbe Java jezika:

- try
- catch
- finally

Svaka od tri upravo prikazane naredbe poseduje svoje specifično zaduženje. Ipak, prikazane naredbe se nikada ne koriste samostalno, već se pribegava njihovom kombinovanju, pa se tako dobijaju:

- try..catch
- try..catch...finally

U nastavku će biti obrađene upravo navedene naredbe za obradu izuzetaka.  
  

### try...catch

Naredba try...catch sačinjena je iz pojedinačnih naredbi try i catch. Svaka od ovih naredbi ujedno je i zaseban blok koda. Tako naredba try...catch ima sledeći oblik:

```java
try{
          
}
catch(Exception err) {
           
}
```

  
Unutar bloka koji se definiše try naredbom navodi se kod koji može da proizvede izuzetak. Ukoliko tokom izvršavanja koda unutar try bloka dođe do izuzetka, aktivira se blok koda definisan catch naredbom.

Uvidom u sintaksu try...catch naredbe, može se videti da catch blok prihvata jedan parametar koji je u primeru imenovan kao err. Ovo je promenljiva koja se od strane izvršnog okruženja popunjava objektom izuzetka kada dođe do pojave greške. Naziv err je proizvoljan i može se menjati.

Evo kako se try...catch može upotrebiti na nešto ranije prikazanom primeru inicijalizacije nepostojećeg člana niza:

```java
int[] nums = newint[4];
 
try{
         nums[7] = 10;
} catch(Exception exc) {
         System.out.println("There is an error.");
}
```

  
Naredba koja je proizvodila grešku, pa samim tim i izuzetak, sada je smeštena unutar try bloka. Unutar catch bloka je definisan kod koji će se aktivirati ukoliko do izuzetka dođe. Na kraju, efekat programa će biti ovakav:

There is an error.

Na izlazu dobijamo poruku da je došlo do greške prilikom izvršavanja programa. Ipak, što je najznačajnije, program ne prekida svoje izvršavanje kada dođe do izuzetka. U to se vrlo lako možemo uveriti:

```html
int[] nums = new int[4];
 
try {
    nums[7] = 10;
} catch (Exception exc) {
    System.out.println("There is an error.");
}
 
System.out.println("Hello World");
```

  
Nakon postojećeg koda, dodali smo još jednu naredbu za ispis poruke na izlaz:

There is an error.  
Hello World  
  

Iako u programu dolazi do pojave greške, on bez problema nastavlja svoje izvršavanje, sve do kraja. Ovo je najznačajnija osobina obrade izuzetaka.

### Čitanje informacija izuzetka

U prikazanom primeru, obavljena je najosnovnija obrada izuzetka, koja je sprečila zaustavljanje programa. Ipak, obrada izuzetaka omogućava mnogo više, pa je tako moguće doći do različitih informacija o samom izuzetku:

```java
int[] nums = newint[4];
 
try{
        nums[7] = 10;
} catch(Exception exc) {
        System.out.println("Exception class: "+ exc.getClass());
        System.out.println("Exception message: "+ exc.getMessage());
}
```

  
Sada smo, umesto jednostavne poruke koju smo samostalno formirali, zapravo prvi put iskoristili objekat izuzetka kako bismo kroz njega došli do nekih informacija o grešci. Na izlazu smo ispisali naziv klase i poruku izuzetka:

Exception class: class java.lang.ArrayIndexOutOfBoundsException  
Exception message: Index 7 out of bounds for length 4  
  

### Različiti tipovi izuzetaka

U upravo prikazanom primeru, prvi put smo iskoristili objekat izuzetka koji se našem programu isporučuje kao promenljiva koja postoji unutar catch bloka. Ipak, bitno je da primetite da je ta promenljiva trenutno tipa Exception. Nešto ranije ste mogli da vidite da je Exception jedna od osnovnih klasa svih izuzetaka. To na kraju znači da je njome moguće predstaviti veliki broj različitih izuzetaka do kojih može doći prilikom izvršavanja Java programa. Ipak, kada tačno znamo do kog izuzetka može doći prilikom izvršavanja neke funkcionalnosti, moguće je definisati i specijalizovani tip izuzetka:

```java
try{
        nums[7] = 10;
} catch(ArrayIndexOutOfBoundsException exc) {
        System.out.println("Exception class: "+ exc.getClass());
        System.out.println("Exception message: "+ exc.getMessage());
}
```

  
Tip promenljive koja predstavlja izuzetak sada je promenjen na ArrayIndexOutOfBoundsException, što je specijalizovani tip izuzetka koji i dobijamo u upravo prikazanom primeru. Stoga će efekat biti identičan kao u prethodnom primeru.

Prilikom samostalnog definisanja tipa izuzetka, potrebno je voditi računa. Naime, ukoliko navedemo specijalizovani tip izuzetka, a prilikom izvršavanja programa dođe do emitovanja izuzetka nekog drugog tipa, izuzetak neće biti obrađen:

```java
int[] nums = newint[4];
 
try{
         nums[7] = 10;
} catch(ArithmeticException exc) {
         System.out.println("Exception class: "+ exc.getClass());
         System.out.println("Exception message: "+ exc.getMessage());
}
```

  
U ovom primeru, obrađujemo izuzetak tipa ArithmeticException. Međutim, u programu dolazi do pojave izuzetka drugog tipa, pa je efekat kao da obrada izuzetka nije ni definisana.

Prilikom obrade izuzetaka, moguće je definisati i veći broj tipova izuzetaka koji će biti obrađeni:

```java
try{
         nums[7] = 10;
} catch(ArithmeticException | ArrayIndexOutOfBoundsException exc) {
         System.out.println("Exception class: "+ exc.getClass());
         System.out.println("Exception message: "+ exc.getMessage());
}
```

  
Sada su prilikom kreiranja catch bloka definisana dva tipa izuzetaka koji će moći da budu obrađeni. Klase izuzetaka se razdvajaju karakterom uspravna crta.

### try...catch...finally

Pored try i catch naredbi, nešto ranije je spomenuta još jedna naredba koja se može koristiti u postupku obrade izuzetaka. Reč je o naredbi finally:

```java
try{
            block of code to try
}
catch(Exception err) {
             block of code to handle errors
}
finally{
              block of code to always execute
            }
```

  
Kod definisan finally blokom uvek se izvršava, bez obzira na to da li je došlo do greške ili ne:

```java
try{
    nums[7] = 10;
} catch(Exception exc) {
    System.out.println("Exception class: "+ exc.getClass());
    System.out.println("Exception message: "+ exc.getMessage());
} finally{
    System.out.println("Code to always execute.");
}
```

  

  
Primer sada podrazumeva i jedan blok više. Reč je o bloku finally. Unutar njega se nalazi kod koji će se uvek izvršiti, bez obzira na to da li dolazi do greške.  
  

### Samostalno emitovanje izuzetaka

Da sada smo videli nekoliko primera obrade izuzetaka koje Java okruženje automatski kreira prilikom pojave greške tokom izvršavanja Java programa. Ipak, moguće je i samostalno vršiti njihovo emitovanje i to korišćenjem naredbe throw. Sintaksa ove naredbe je:

throw expression;  

Naredba throw formira se korišćenjem ključne reči throw, nakon koje se navodi objekat izuzetka koji je potrebno emitovati. Evo kako može da izgleda jedna metoda koja emituje izuzetak:

```java
staticvoiderrorMethod() {
    Exception exc = newException("There is an error");
    throwexc;
}
```

  
Unutar tela metode errorMethod obavlja se kreiranje jednog objekta tipa Exception. Konstruktoru klase Exception prosleđuje se tekst greške. Ovakav izuzetak se zatim emituje korišćenjem naredbe throw. Ipak, kako bi ovakav primer bio u potpunosti funkcionalan, neophodno je obaviti još jednu intervenciju nad našom metodom errorMethod. Naime, sve metode koje emituju izuzetke moraju biti obeležene korišćenjem specijalne ključne reči **throws**:

```java
staticvoiderrorMethod() throwsException {
    Exception exc = newException();
    throwexc;
}
```

  
Ovo je sada potpuno validna i sintaksno ispravna metoda koja emituje izuzetak iz svog tela. S obzirom na to da iz svog tela emituje izuzetak, ona se sada ne može pozvati bez koda za obradu izuzetka:

```java
try{
        errorMethod();
} catch(Exception e) {
        System.out.println(e.getMessage());
}
```

  
S obzirom na to da proizvodi izuzetak, metodu errorMethod je neophodno pozvati unutar try bloka. Nakon emitovanja izuzetka, on biva uhvaćen od strane catch bloka. Do poruke izuzetka koju smo nešto ranije kreirali dolazi se korišćenjem metode getMessage, pa se na izlazu dobija:

There is an error  

| **Proveravani i neproveravani izuzeci**  U dosadašnjem toku lekcije spominjali smo samo klasu Exception, kao jednu od korenih klasa svih ostalih klasa izuzetaka u Java jeziku. Ipak, pored ove klase postoji jedan još generalniji tip izuzetaka. Reč je o klasi Throwable.  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_21_08.png)  *Slika 21.8. Osnovne ugrađene klase izuzetaka*       Klasa Throwable osnovna je klasa svih ostalih klasa izuzetaka. Kao što vidite, nju direktno nasleđuju dve klase:  - Error - Exception  Klasa Error koristi se za reprezentaciju ozbiljnih problema tokom izvršavanja programa. Stoga nije predviđeno da izuzeci koji nasleđuju ovu klasu budu obrađeni, jer se smatra da sistem ne može da nastavi svoj rad nakon pojave takve vrste greške. Neke od najpoznatijih klasa kojima se predstavljaju takve ozbiljne greške u sistemu su OutOfMemoryError, StackOverflowError, InternalError...  Klasa Exception, kao što ste mogli da vidite u dosadašnjem toku ove lekcije, koristi se za predstavljanje grešaka koje ne ugrožavaju izvršavanje programa, pa je stoga predviđeno da budu obrađene od strane programera, kako bi program mogao da nastavi svoje izvršavanje.  Izuzeci tipa Error drugačije se nazivaju neproveravani, a izuzeci tip Exception proveravani izuzeci.  Na kraju, sve ovo znači da bi se nasleđivanjem klase Error stvorio jedan izuzetak koga ne bi bilo potrebe eksplicitno obrađivati korišćenjem try...catch blokova. |
| --- |

### Samostalno kreiranje klasa izuzetaka

Prethodni primer ilustrovao je samostalno emitovanje izuzetka koji je kreiran na osnovu osnovne ugrađene klase Exception. U realnim okolnostima najčešće se pribegava samostalnom kreiranju klasa izuzetaka. Evo kako može izgledati jedna klasa izuzetka koji mi samostalno kreiramo:

```java
publicclassOutOfRangeException extendsException {
 
    @Override
    publicString getMessage() {
        return"The number is out of range!";
    }
 
}
```

  
Klasa koju smo kreirali ima naziv OutOfRangeException. Ona nasleđuje osnovnu klasu proveravanih izuzetaka – Exception. Takođe, unutar klase OutOfRangeException obavili smo redefinisanje metode getMessage koja se nalazi unutar roditeljske klase. Na ovaj način smo definisali poruku koja će moći da se dobije kada se nad objektom izuzetka pozove metoda getMessage.

Ovako kreiran izuzetak sada se može upotrebiti na sledeći način:

```java
staticvoidcalculate(intnum) throwsOutOfRangeException {
 
        if(num > 100|| num < 0) {
            thrownewOutOfRangeException();
        }
        
}
```

  
Izuzetak koji smo samostalno kreirali upotrebili smo unutar metode calculate. To je metoda koja prihvata jedan celobrojni parametar i koja na osnovu takvog parametra treba da obavi određenu kalkulaciju. Ipak, zamislite da za potrebe kalkulacije prosleđena vrednost treba da bude u opsegu od 0 do 100. Upravo zbog toga je unutar metode dodata logika za proveru opsega vrednosti. Ukoliko vrednost nije u spomenutom opsegu, obavlja se emitovanje izuzetka koji smo upravo kreirali. Logika metode calculate je izostavljena kako bi metoda bila što jednostavnija i kako bismo se mogli usredsrediti na logiku za emitovanje izuzetka.

Na kraju, ovakva metoda se može pozvati na sledeći način:

```java
try{
    calculate(150);
} catch(OutOfRangeException e) {
    System.out.println(e.getMessage());
}
```

  
S obzirom na to da je prosleđena vrednost izvan definisanog opsega, na izlazu se dobija:

The number is out of range!  

Ovo je poruka koju smo nešto ranije samostalno definisali unutar metode getMessage naše klase OutOfRangeException.  
  

### Vežbe

**  
Vežba 1**

Primer iz ove lekcije koji je ilustrovao deljenje dva broja potrebno je modifikovati tako da se unutar koda obrade eventualne greške do kojih može doći (deljenje nulom).

**  
Vežba 2**

Kod prikazan u nastavku je potrebno obezbediti tako da ne prijavljuje grešku.

```html
public class Main
{
    static int calculate(int a, int b, String op)
    {
        if(op.equals("+"))
            return a + b;
        if(op.equals("-"))
            return a - b;
        if(op.equals("/"))
            return a / b;
        if(op.equals("*"))
            return a * b
        return 0;
    }
 
    public static void main(String[] args)
    {
        int x = calculate(5, 0, "/");
        System.out.println(x);
    }
 
}
```

**Vežba 3**

Data je sledeća klasa User:

```java
publicclassUser
{
    publicintid;
    publicString firstName;
    publicString lastName;
    publicString email;
 
    publicUser(intid, String firstName, String lastName, String email)
    {       
        this.id = id; 
        this.firstName = firstName;
        this.lastName = lastName;
        this.email = email;
    }
 
}
```

  
Potrebno je kreirati klasne izuzetke za nepravilan unos ID-ja, imena, prezimena i e-maila.

Potrebno je implementirati sistem provere u konstruktor klase User tako da, ukoliko je id veći od 100, bude emitovan InvalidIdException i da, ako su firstName, lastName i email polja prazna, bude emitovan InvalidFirstNameException, InvalidLastNameException ili InvalidEmailException.  
  

### Rešenja

**Vežba 1**

```java
intnumberA;
intnumberB;
doublenumberC = 0;
 
Scanner scanner = newScanner(System.in);
 
System.out.println("Please, enter number A: ");
numberA = scanner.nextInt();
 
System.out.println("Please, enter number B: ");
numberB = scanner.nextInt();
 
try{
    numberC = numberA / numberB;
 
} catch(Exception exc) {
    System.out.println(exc.getMessage());
}
 
 
System.out.println("Result: "+ numberC);
```

**  
Vežba 2**

```java
publicclassJavaProgram {
 
    staticintcalculate(inta, intb, String op) {
 
        if(op.equals("+"))
            returna + b;
 
        if(op.equals("-"))
            returna - b;
 
        if(op.equals("/"))
            returna / b;
 
        if(op.equals("*"))
            returna * b;
 
        return0;
    }
 
    publicstaticvoidmain(String[] args) {
 
        intx = 0;
 
        try{
            x = calculate(5, 0, "/");
            System.out.println(x);
 
        } catch(ArithmeticException ex) {
            System.out.println("There is an error.");
        }
    }
 
}
```

**  
Vežba 3**

```java
classInvalidEmailException extendsException {
}
 
classInvalidFirstNameException extendsException {
}
 
classInvalidIdException extendsException {
}
 
classInvalidLastNameException extendsException {
}
 
classUser {
 
    publicintid;
    publicString firstName;
    publicString lastName;
    publicString email;
 
    publicUser(intid, String firstName, String lastName, String email) throwsInvalidIdException, InvalidFirstNameException, InvalidLastNameException, InvalidEmailException {
 
        if(id > 100)
            thrownewInvalidIdException();
        else
            this.id = id;
 
        if(firstName.equals(""))
            thrownewInvalidFirstNameException();
        else
            this.firstName = firstName;
 
        if(lastName.equals(""))
            thrownewInvalidLastNameException();
        else
            this.lastName = lastName;
 
        if(email.equals(""))
            thrownewInvalidEmailException();
        else
            this.email = email;
    }
}
 
publicclassJavaProgram {
    publicstaticvoidmain(String[] args) {
 
        try{
            User u = newUser(10, "Ben", "Lord", "ben.lord@mail.mm");
 
        } catch(InvalidIdException ex) {
            System.out.println("Invalid ID");
 
        } catch(InvalidFirstNameException ex) {
            System.out.println("Invalid name");
 
        } catch(InvalidLastNameException ex) {
            System.out.println("Invalid surname");
 
        } catch(InvalidEmailException ex) {
            System.out.println("Invalid e-mail");
        }
    }
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_21.thb) JCPR1\_21.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_21.Mp4")

Kako Vam mogu pomoći?