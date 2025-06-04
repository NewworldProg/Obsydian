---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=3feac6d5d948d58a62ad2be639016cbd_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434675"
author:
published:
created: 2025-04-25
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 8 od 22

## Tipovi podataka

==Srž svakog programskog jezika jeste mogućnost obrade podataka==. Podaci koji se obrađuju mogu biti ==različitog tipa: brojevi, tekst, [logičke vrednosti](https://www.link-elearning.com/linkdl/opisPojma.php?id=160438 "logičke vrednosti")==... ==U primeru== našeg prvog Java programa iz prethodnih lekcija, definisali smo ==samo jedan podatak==:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        System.out.println("Hello World");
    }
}
```

  
U kodu naše prve Java aplikacije postoji ==tekstualni podatak *Hello World* koji program emituje== kao svoj rezultat. Kako bismo bili u stanju da napišemo i nešto naprednije programe, unutar kojih bi se obavljala i obrada, a ne samo puko ispisivanje podataka, ==neophodno je da se upoznamo sa različitim tipovima== podataka koji postoje u jeziku Java.  
  

### Šta su tipovi podataka?

Tipovi podataka ==omogućavaju da se unutar programa predstave različite vrste vrednosti – karakteri, tekst, razne vrste brojeva, logičke vrednosti==. Sve su to tipovi podataka. Tipovi podataka omogućavaju da se, prilikom definisanja neke vrednosti, J==ava virtuelnoj mašini naglasi kojeg će tipa biti ta vrednost==. Tako nešto ćete najbolje razumeti na jednom primeru:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        String message = "Hello World";
        System.out.println(message);
    }
}
```

  
Prikazani ==primer neznatno modifikuje izvorni kod== našeg prvog Java programa. ==Unutar main== metode ==dodata== je jedna ==nova naredba pre naredbe za ispis poruke.== Nova naredba izgleda ovako:

```java
String message = "Hello World";
```

  
Najjednostavnije rečeno, prikazana naredba je način da se u Java programu predstavi jedna vrednost. ==Naredba započinje jednom rezervisanom rečju jezika – String==. Upotrebom ključne reči String, ==Java== izvršnom ==okruženju== se ==stavlja do znanja da želimo da kreirano novu vrednost String tipa.== Tako i u praksi dolazimo do pojma tipova podataka.

U upravo prikazanoj naredbi, u kojoj se prvi put pojavljuje jedan Java tip, ==postoji još nekoliko značajnih elemenata, koji su ilustrovani slikom 8.1.==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_01.png)

*Slika 8.1. Struktura naredbe za definisanje jedne tekstualne vrednosti*  
  

==String== je ==tip podataka== kojim se u Java jeziku predstavlja tekst; ==message== je ==primer identifikatora== pomoću koga će tekstualna vrednost biti dostupna u nastavku koda. Karakter ==jednako== (=) je primer jednog ==operatora==. Tekst ==*Hello World*== koji se nalazi ispod navodnika je vrednost, ==odnosno== ==literal==. Na kraju, ==kompletna prikazana naredba jeste način na koji se u Java jeziku kreira jedna promenljiva.== Sve su to pojmovi koji će biti obrađeni u modulu koji je pred nama. Počećemo od pojma tipova podataka.  
  

### Tipovi podataka u Javi

Praktično svi programski jezici podrazumevaju ==generalnu podelu== tipova podataka na ==proste (primitivne)== i ==složene== tipove. Takva je situacija i ==kod programskog jezika Java==, gde ==postoje== ==primitivni== tipovi i ==referentni== tipovi; može se čuti i termin *složeni* ili *objektni tip*, a reč je o sinonimima za termin *referentni tip*. Stoga se na kraju može zaključiti da u Javi postoje dve različite grupe tipova:

- ==prosti, odnosno primitivni== tipovi;
- ==složeni, referentni, odnosno objektni== tipovi.

U nastavku ove lekcije, prvo ćemo se upoznati sa različitim primitivnim tipovima koji postoje unutar jezika Java.  
  

### Primitivni tipovi

==Srž== programskog jezika Java sastoji se od ==osam ugrađenih primitivnih tipova==. Oni su predstavljeni tabelom 8.1.

| **Tip podatka** | **Značenje**                           | **Veličina u bajtovima** | **Opseg vrednosti**                              |
| --------------- | -------------------------------------- | ------------------------ | ------------------------------------------------ |
| byte            | 8-bitna celobrojna vrednost            | 1 bajt                   | Od -128 do 127                                   |
| short           | celobrojna vrednost smanjenog opsega   | 2 bajta                  | od -32768 do 32767                               |
| int             | celobrojna vrednost standardnog opsega | 4 bajta                  | od -2147483648 do 2147483647                     |
| long            | celobrojna vrednost proširenog opsega  | 8 bajtova                | od -9223372036854775808L do 9223372036854775807L |
| float           | decimalna vrednost                     | 4 bajta                  | ±3.40282347 E+38F                                |
| double          | decimalna vrednost, duple preciznosti  | 8 bajtova                | ±1.79769313486231570 E+308                       |
| char            | karakter                               | 2 bajta                  | 0–65535                                          |
| boolean         | logička vrednost tačno ili netačno     | 1 bit                    | true ili false (0 ili 1)                         |

*  
Tabela 8.1. Primitivni tipovi Java jezika*

U tabeli 8.1. prikazani su svi primitivni tipovi jezika Java. Kolona *Tip podatka* oslikava naziv tipa, ali i ključnu reč jezika koja se koristi za dobijanje konkretnog tipa prilikom pisanja programskog koda. U tabeli 8.1. je takođe prikazan i prostor koji podaci različitih tipova zauzimaju u kompjuterskoj memoriji, kao i opsezi vrednosti koje oni mogu imati.

| **Bit i bajt i opsezi prostih tipova**  Svaki podatak zauzima određeni prostor unutar kompjuterske memorije. Memorijski prostor koji podaci zauzimaju u memoriji izražava se korišćenjem jedinice bit. **Bit** je najmanja jedinica za predstavljanje digitalnih podataka. Jedan bit može imati samo dve vrednosti – 0 ili 1. U tabeli 8.1. možete videti da boolean tip podatka u memoriji zauzima samo jedan bit, i upravo zbog toga podaci takvog tipa mogu imati samo dve vrednosti.  Ostali prosti tipovi u Javi zauzimaju veću količinu memorije, a sve u zavisnosti od njihovog opsega. Tako tip byte u kompjuterskoj memoriji zauzima 1 bajt. Bajt je jedinica koja predstavlja 8 bita. S obzirom na to da se sastoji od 8 bita, opseg ovog tipa podataka se računa vrlo lako: 2 <sup>8</sup> = 256 (dva na osmi jednako je 256). S obzirom na to da se tipom byte može predstaviti 256 različitih vrednosti, njegov opseg je od -128 do 127, što na kraju daje 256 jedinstvenih vrednosti. Po identičnom principu se računaju i opsezi ostalih prostih tipova u Javi. |
| --- |

Ukoliko malo bolje analizirate opise prostih Java tipova iz tabele 8.1, moći ćete da zaključite da u Javi ==postoji nekoliko tipova za predstavljanje brojeva i po jedan za predstavljanje karaktera i logičkih vrednosti.== Može se, zapravo, reći da u Javi postoje tri osnovne grupe primitivnih tipova:

- ==celobrojni tipovi – byte, short, int, long;==
- ==tipovi za predstavljanje brojeva sa decimalom – float, double;==
- ==tip za predstavljanje karaktera – char;==
- ==logički tip - boolean.==

Ovim redosledom ćemo i nastaviti upoznavanje sa prostim tipovima Java jezika.  
  

### Celobrojni tipovi

Java definiše ==četiri vrste celobrojnih podataka==: ==byte, short, int i long.==

==Najčešće korišćeni tip podataka== u Javi je ==**int**==, zato što njegov opseg u većini slučajeva zadovoljava potrebe predstavljanja celobrojnih vrednosti. Stoga je, kako bi se u Java programu definisala jedna celobrojna vrednost, moguće napisati sledeće:

```java
intx = 10;
```

**  
Gde pisati kod iz ove lekcije?**

Već više puta je rečeno da svaki ==Java program zahteva postojanje main metode==. Ova metoda se mora naći unutar neke klase, pa je tako ==postojanje jedne klase i main metode apsolutni minimum== koda koji moramo imati kako bismo mogli da dobijemo neki efekat. Prilikom pokretanja programa od strane Java virtuelne mašine, aktivira se kod koji se nalazi unutar main metode, pa će upravo to biti mesto unutar koga ćemo i mi pisati kod u ovoj lekciji:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
        intx = 10;
        System.out.println(x);
    }
}
```

  
==Unutar main metode postavljena je naredba za definisanje celobrojne vrednosti==, ali i ==naredba za== ispis ==takve== vrednosti. Stoga, kada se program pokrene, na izlazu se dobija vrednost 10. U nastavku će biti korišćena ovakva struktura koda, a radi bolje preglednosti biće prikazivane samo naredbe za definisanje podataka.

Nešto ranije, u tabeli 8.1, mogli ste da vidite da je najveći broj koji je moguće predstaviti korišćenjem int tipa 2147483647. ==Evo šta se događa ukoliko se kao int tip pokuša definisati vrednost koja je veća od upravo navedene== (slika 8.2).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_02.png)

*Slika 8.2. Primer probijanja opsega tipa int  
  
*

Na slici 8.2. možete videti da razvojno okruženje jasno signalizira da u kodu postoji sintaksna greška i da je definisani broj isuviše veliki kako bi bio definisan kao int tip. Rešenje se ogleda u korišćenju celobrojnog tipa proširenog opsega. ==Takav tip se u Javi zove **long**:==

```java
longx = 2147483648L;
```

  
==Sada je tip podatka promenjen u long==, što omogućava definisanje celobrojnih vrednosti znatno šireg opsega. Takođe, i s==amu vrednost je bilo potrebno modifikovati i na njen kraj dodati veliko slovo L==. Nakon takvih izmena, naš kod više ne sadrži sintaksu grešku.

==Po identičnom principu funkcionišu i byte i short celobrojni tipovi.== Razlika je samo u opsegu vrednosti koje se mogu definisati. Vrednosti u opsegu od -128 do 127 moguće je predstavljati tipom **byte**:

```java
bytex = 10;
```

  
==Kada je potrebno predstaviti vrednost veću od 127, ali manju od 32767, može se koristiti tip **short**:==

```java
shortx = 322;
```

  
==Tipovi byte i short koriste se kada ušteda memorije== igra važnu ulogu i kada znamo da celobrojne vrednosti neće biti veće od opsega ovih tipova. ==U realnim okolnostim==a, prilikom razvoja modernog softvera za web, desktop ili pametne telefone, ==upotreba byte i short tipova je vrlo retka, pa su najkorišćeniji tipovi int i long.==

Bez obzira na celobrojni tip koji se koristi, ==vrednost je moguće definisati u nekoliko različitih oblika:==

- ==dekadni (decimalni);==
- ==[oktalni](https://www.link-elearning.com/linkdl/opisPojma.php?id=160440 "oktalni");==
- ==[heksadecimalni](https://www.link-elearning.com/linkdl/opisPojma.php?id=160441 "heksadecimalni");==
- ==binarni==

==Dekadni==, odnosno decimalni oblik je ==podrazumevan==. ==Ostali oblici se definišu korišćenjem specifičnih prefiksa koji se dodaju na vrednosti:==

```java
intdecVal = 26;
intoctVal = 032;       
inthexVal = 0x1a;      
intbinVal = 0b11010;
```

  
Kod ilustruje definisanje četiri pojedinačne celobrojne vrednosti korišćenjem različitih oblika, i to po redosledu definisanja: dekadni, oktalni, heksadecimalni i binarni. Svakim oblikom se zapravo definiše identična vrednost (26), a ==u komentarima koji su definisani u nastavku naredbi možete videti matematiku koja se koristi za pretvaranje konkretne vrednosti u dekadni oblik==.  
  

### Decimalni tipovi

==Do sada smo se bavili predstavljanjem celih brojeva== u Java jeziku. Podjednako je značajna i ==mogućnost predstavljanja brojeva koji nisu celi,== već poseduju i određenu vrednost nakon decimalne tačke. Takvi tipovi se veoma često nazivaju i ==tipovi sa pomičnim (pokretnim) zarezom (*floating point*) ili jednostavno decimalni tipovi.== U Java jeziku postoje dva takva tipa: ==float i double==. Razlika je samo u preciznosti, odnosno opsegu, pri čemu ==double obezbeđuje duplo veći opseg==, što možete videti i unutar tabele 8.1.

Kako bi se, na primer, u Java programu predstavila ==konstanta Pi, neophodno je iskoristiti jedan== od dva upravo spomenuta tipa:

```java
doublePI = 3.14;
```

  
Kao što možete videti, vrednost PI je definisana korišćenjem double tipa. Tip double se podrazumevano koristi za definisanje vrednosti koje poseduju decimalu. Šta to praktično znači – možete videti na slici 8.3.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_03.png)

*Slika 8.3. U Java jeziku, definisanje float vrednosti se mora naglasiti  
  
*

U primeru sa slike 8.3, ==double tip je promenjen u float==. ==Razvojno okruženje odmah prijavljuje grešku==, odnosno da definisani tip i vrednost nisu kompatibilni. O čemu je reč? Pa baš kao i kod nešto ranije spomenutog long tipa, ==na float vrednost je neophodno dodati veliko slovo **F**, kako bi prevodilac znao da želimo da koristimo tip duplo manje preciznosti:==

```java
floatPI = 3.14F;
```

### Karakteri

==Kada je u Java programu potrebno predstaviti neki karakter==, koristi se primitivni ==tip **char**==. Evo kako može izgledati definisanje karaktera koji predstavlja veliko slovo X:

```java
charsomeChar = 'X';
```

  
Bitno je da odmah primetite da se prilikom definisanja vrednosti karaktera ==koriste apostrofi==, odnosno da se karakter postavlja između jednostrukih navodnika.

U tabeli 8.1 možete videti da char tip u Javi zauzima 16 bita (2 bajta), te da je njegov ==opseg vrednosti od 0 do 65535. Opseg vas može zbuniti.== Naime, govorimo o tipu za predstavljanje karaktera, a spominjemo opseg numeričkih vrednosti. ==O čemu je zapravo reč==?

==Karakteri se u pozadini predstavljaju korišćenjem celobrojnih numeričkih vrednosti [Unicode](https://www.link-elearning.com/linkdl/opisPojma.php?id=160466 "Unicode") s==eta karaktera. Da je to stvarno tako, možete se uveriti na sledeći način:

```java
charsomeChar = 78;
```

  
Za vrednost je sada postavljen broj 78. Svakako to nije karakter, ali je ovako nešto u Javi potpuno legitimno. Na ovaj način se, naime, dobija karakter koji ima kod 78 ==u Unicode setu karaktera. Reč je o karakteru N.==

Naravno, karakteri se gotovo uvek definišu direktno, odnosno između jednostrukih navodnika, u svom izvornom obliku. Definisanje karaktera korišćenjem celobrojnih kodova može biti korisno kada je potrebno dobiti neki specifičan karakter, koji se ne može direktno otkucati na tastaturi:

```java
charsomeChar = 169;
```

  
==Na ovaj način dobija se sledeći karakter:==

```java
©
```

| **Napomena**  Tip char koristi se isključivo za predstavljanje pojedinačnih karaktera. To praktično znači da nije moguće postaviti više od jednog karaktera ispod jednostrukih navodnika prilikom definisanja char vrednosti (slika 8.4).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_04.png)  *Slika 8.4. Vrednosti char tipa mogu imati samo jedan karakter      *  Definisanje većeg broja karaktera prilikom korišćenja char tipa proizvodi sintaksnu grešku, što jasno markira i IntelliJ IDEA razvojno okruženje. |
| --- |

### Logički tip – boolean

U osnovi svakog programskog jezika jeste i logički tip podataka, koji omogućava definisanje podataka koji mogu imati d==va oblika: tačno/netačno, uključeno/isključeno, 0/1==... Reč je o tipu koji se u Java jeziku naziva boolean.

Tip boolean u memoriji zauzima 1 bit, što praktično znači da može imati samo dve vrednosti:  0 i 1. U programskom jeziku Java se ove dve vrednosti predstavljaju vrednostima **true** ili **false** (tačno ili netačno):

```java
booleanisTrue = true;
```

  
Ili:

```java
booleanisTrue = false;
```

  
Logički tip podataka se ==najčešće koristi za postizanje kontrole toka== izvršavanja programa. To je za nas u ovom trenutku nepoznanica, pa ćemo upoznavanje sa boolean tipom nastaviti u jednoj od narednih lekcija.

### Složeni (referentni) tipovi

==U dosadašnjem toku== ove lekcije ==bilo je reči o prostim tipovima.== Pored prostih tipova, u jeziku Java ==postoji i složeni tipovi.== Složeni tipovi podataka su naziv dobili na osnovu osobine koja im omogućava da ==unutar sebe mogu da objedine veći broj vrednosti,== ali ==i operacija,== odnosno ponašanja.

Složeni tipovi podataka u ovom trenutku značajno prevazilaze naše poznavanje Java jezika. Kako bismo se na pravi način upoznali sa složenim tipovima podataka, neophodno je da obradimo pojmove klasa i objekata. Tim pojmovima biće posvećen naredni modul ovog kursa. Ipak, sa ==nekoliko složenih, odnosno referentnih tipova== možemo se upoznati i sada. Oni će biti predstavljeni ==u nastavku== ove lekcije.  
  

### Tekstualni podaci

U programskom jeziku Java, za rukovanje tekstualnim vrednostima koristi se ==tip **String**.== Stoga, kada je potrebno definisati neki tekst, pribegava se sledećem:

```java
String myWord = "Hi!";
```

  
Ovo je način da se u Java jeziku definiše tekstualni podatak. Potrebno je obratiti pažnju na sledeće:

- ključna reč ==String== ima ==veliko početno slovo;== veliko slovo ==izdvaja ovaj tip od skupa primitivnih tipova koji se pišu malim slovom==; naime, String je složeni tip, ali se može kreirati kao i primitivni tipovi; zbog toga se String veoma često naziva specijalnim tipom;
- vrednosti tipa String ==pišu se između klasičnih, dvostrukih navodnika==, ==za razliku od char== tipa, čije se vrednosti smeštaju između ==jednostrukih navodnika==.

Kao što možete videti, upotreba String tipa se ni po čemu ne razlikuje od korišćenja prostih tipova prikazanih ranije u ovoj lekciji. Mi ćemo i ==u nastavku koristiti String kao da je reč o prostom tipu, a kada se bolje upoznamo sa pojmom složenih tipova, iskoristićemo i sve blagodeti koje String poseduje kao složeni tip podatka.==

**Specijalni karakteri unutar Stringa**

Upravo ste mogli da vidite da se tekstualni podaci u Java jeziku smeštaju ispod navodnika==. Pogledajte šta bi se dogodilo kada bismo želeli da unutar teksta uvrstimo navodnik (slika 8.5).==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_05.png)

*Slika 8.5. Direktno korišćenje navodnika unutar tekstualne vrednosti proizvodi sintaksnu grešku  
  
*

Slika 8.5. ilustruje primer u kome želimo da definišemo tekstualnu vrednost: This is quotation mark - ". Unutar teksta koji želimo da definišemo nalazi se i karakter navodnik. S obzirom na to da je u jeziku njegova namena specijalna, odnosno da se koristi za oivičavanje String vrednosti, dobija se sintaksna greška. Jednostavno, kompajler neće moći da zna gde su granice String vrednosti. Kako bi se rešio ovakav problem, pribegava se upotrebi karaktera obrnuta kosa crta (*backslash*):

```java
String message = "This is quotation mark - \"";
```

  
Ispred karaktera navodnik sada je postavljen karakter *backslash*, čime se dobija sintaksno ispravan kod. Jednostavno, karakter *backslash* signalizira kompajleru da je unutar tekstualne vrednosti potrebno da se pojavi navodnik.

Ovo nije jedina situacija u kojoj se karakter *backslash* koristi ispred određenih karaktera prilikom definisanja String vrednosti. Korišćenje karaktera *backslash* čini da u nekim situacijama karakter koji sledi dobije posebno značenje i da ga kompajler tretira drugačije. Takve situacije predstavljene su tabelom 8.2.

| **Escape sekvenca** | **Opis** |
| --- | --- |
| \\t | tab razmak |
| \\b | backspace |
| \\n | novi red |
| \\r | povratak na početak linije |
| \\' | jednostruki navodnik |
| \\" | dvostruki navodnik |
| \\\\ | kosa crta |

*  
Tabela 8.2. Escape sekvence karaktera*

Karakter *backslash* zajedno sa karakterom koji sledi često se drugačija naziva *escape sekvenca*. U nastavku će biti prikazani primeri korišćenja takvih sekvenci iz tabele 8.2:

```html
System.out.println("Hello\tWorld");
System.out.println("HelloWorld\b\b\b\b\b");
System.out.println("Hello\nWorld");
System.out.println("Hello\rWorld");
System.out.println("\'HelloWorld\'");
System.out.println("\"HelloWorld\"");
System.out.println("This is backslash - \\");
```

  
Ovakav kod će na izlazu da proizvede ispise kao na slici 8.6.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_06.png)*

*Slika 8.6. Efekat escape sekvenci  
  
*

Pojedinačni ispisi koji se postižu upravo navedenim naredbama su na slici 8.6 razdvojeni horizontalnim linijama, kako biste jasnije mogli da razumete efekat upotrebljenih specijalnih karaktera.

### Omotači primitivnih tipova

U programskom jeziku Java, za svaki od 8 primitivnih tipova postoji po jedan složeni referentni tip. Takvi tipovi dodatno proširuju mogućnosti prostih tipova, njihovim kombinovanjem sa određenim funkcionalnostima. Zato što se sastoje iz odgovarajućeg prostog tipa i skupa pripadajućih funkcionalnosti, ovi tipovi se veoma često nazivaju i omotači prostih tipova.

Tabela 8.3. prikazuje složene tipove koji u Javi predstavljaju omotače primitivnih tipova.

| **Primitivni tip** | **Referentni tip** |
| --- | --- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| boolean | Boolean |
| char | Character |

*  
Tabela 8.3. Primitivni tipovi i njihovi pripadajući referentni tipovi, odnosno omotači  
  
*

Iz tabele 8.3. opet možete videti nepisano pravilo koje je spomenuto ranije: nazivi složenih tipova započinju velikim slovom.

Na primeru omotača primitivnih tipova na najbolji način ćemo moći da se upoznamo sa razlikama između prostih i složenih tipova u Javi. Jedna celobrojna numerička vrednost se korišćenjem upravo prikazanih složenih tipova unutar programa može predstaviti na sledeći način:

```java
Integer x = 5;
```

  
Na prvi pogled, razlika između int i Integer tipova je samo u ključnoj reči. Ipak, već više puta je rečeno da složeni tipovi nisu ograničeni isključivo na vrednost, već da pored vrednosti mogu da poseduju i različita ponašanja. U to se možemo uveriti korišćenjem razvojnog okruženja, na način ilustrovan slikom 8.7.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_08_07.png)

*Slika 8.7. Ponašanja koja su dostupna nad vrednošću složenog tipa  
  
*

U primeru sa slike 8.7, nakon identifikatora x je postavljen karakter tačka, čime je razvojno okruženje odmah prikazalo spisak svih funkcionalnosti (ponašanja) dostupnih nad ovako definisanom vrednošću. Korišćenjem ovakvih ugrađenih funkcionalnosti sada, na primer, možemo da obavimo poređenje dva broja:

```java
Integer x = 5;
System.out.println(x.equals(6));
```

  
Ovakvim primerom obavlja se poređenje vrednosti 5 i 6. S obzirom na to da vrednosti nisu iste, na izlazu se dobija ispis false, što je jedna od dve logičke vrednosti predstavljene nešto ranije u ovom kursu. Poređenje se obavlja korišćenjem funkcionalnosti equals, koja je ugrađena u složeni tip Integer. Takva i slične funkcionalnosti koje se mogu koristiti nad vrednostima su ono što izdvaja složene, odnosno referentne tipove od prostih, odnosno primitivnih tipova.

| **Napomena**  O omotačima prostih tipova biće još reči u lekcijama koje slede. Za sada je bitno da znate da je omotače prostih tipova preporučljivo koristiti samo onda kada za tim stvarno ima potrebe, odnosno onda kada je neophodno koristiti neku od ugrađenih funkcionalnosti koje ovi tipovi imaju. U svim ostalim situacijama, najbolje je koristiti proste tipove, jer oni obezbeđuju neuporedivo bolje performanse. |
| --- |

### Vežbe

**Vežba 1  
**  
U jednom Java programu potrebno je definisati vrednosti koje predstavljaju broj godina i ime i prezime jednog radnika. Broj godina je 47, a ime i prezime John Lord.  
  

**Vežba 2**

U jednom Java programu je potrebno definisati celobrojnu vrednost 130, korišćenjem memorijski najefikasnijeg pristupa.  
  

### Rešenja

**Vežba 1**

```java
intyears = 47;
    String name = "John Lord";
```

**  
Vežba 2**

S obzirom na to da zahtev podrazumeva memorijski najefikasnije rešenje, potrebno je iskoristiti tip sa najmanjim opsegom u koji se uklapa vrednost 130. Tip byte ne dolazi u obzir, zato što prihvata vrednosti do 127. Stoga je rešenje problema prvi naredni tip sa širim opsegom:

```java
shortmyValue = 130;
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_08.thb) JCPR1\_08.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_08.Mp4")

Kako Vam mogu pomoći?