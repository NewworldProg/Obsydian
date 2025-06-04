---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=9bba66416f3a05087051cca8261ca45e_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434683"
author:
published:
created: 2025-05-05
description:
tags:
  - "clippings"
---
Jedinica 16 od 22

## Svojstva i metode

Prethodne lekcije donele su priču o klasama, objektima i paketima. Tako ste imali prilike da naučite kako se takvi, veoma značajni elementi Java jezika kreiraju i koriste. U uvodnoj lekciji ovog modula predstavljeni su i osnovni klasni članovi, odnosno elementi od kojih su klase sačinjene. Reč je o svojstvima i metodama. U ovoj lekciji će priča o svojstvima i metodama biti dodatno proširena, pa ćete tako imati prilike da upoznate i brojne druge aspekte njihovog korišćenja. Sve to će nam na kraju omogućiti da u potpunosti razumemo kod koji smo u procesu kreiranja svog prvog Java programa napisali još na samom početku ovog kursa:

```java
publicclassMyFirstProgram {
    publicstaticvoidmain(String[] args) {
 
    }
}
```

  
Ovo je kod kojim se obavlja kreiranje klase sa main metodom – ulaznom tačkom svakog Java programa. Klase i metode su pojmovi koji su obrađeni u prethodnoj lekciji, ali u prikazanom kodu postoje neke ključne reči koje su za nas još uvek nepoznanica. To su reči public i static. Za početak ćemo se upoznati sa značenjem ovih reči.  
  

### Modifikatori pristupa

Java jezik poseduje funkcionalnost za kontrolu dostupnosti klasa i njihovih članova. Korišćenjem takve funkcionalnosti možemo da kontrolišemo pristup klasama i njihovim članovima, odnosno da odredimo iz kojih delova našeg programa će njima moći da se pristupi. Takva funkcionalnost se drugačije naziva kontrola pristupa; realizuje se upotrebom posebnih ključnih reči koje se nazivaju modifikatori pristupa.

U Java jeziku postoje četiri modifikatora pristupa:

**private**

Ovo je modifikator pristupa koji označava da će članovi deklarisani ovom ključnom rečju biti vidljivi samo u okviru klase u kojoj se nalaze. Dobija se korišćenjem ključne reči private i moguće ga je koristiti samo nad klasnim članovima.

**package-private**

Modifikator pristupa koji označava da svi drugi elementi istog paketa imaju pristup klasi ili članu klase sa ovakvim modifikatorom. Ovaj modifikator pristupa predstavlja podrazumevani modifikator i jedini je koji ne poseduje ključnu reč. Stoga se dobija kada se ključna reč izostavi.

**protected**

Modifikator pristupa koji ukazuje na to da se članovima može pristupiti iz same klase gde su definisani i iz [izvedenih klasa](https://www.link-elearning.com/linkdl/opisPojma.php?id=160485 "izvedenih klasa"). Ovaj modifikator se može koristiti samo nad klasnim članovima, a dobija se upotrebom ključne reči protected.

**public**

Modifikator pristupa kojim se kreiraju javno dostupne klase i njeni članovi. Takve klase i članovi su dostupni iz svih delova jednog Java programa. Dobija se korišćenjem ključne reči public.

U tabeli 16.1. je dat sažet uporedni prikaz svih pomenutih modifikatora pristupa.

| **Ključna reč** | **Klasa** | **Paket** | **Izvedene klase** | **Svi** |
| --- | --- | --- | --- | --- |
| public | da | da | da | da |
| protected | da | da | da | ne |
|  | da | da | ne | ne |
| private | da | ne | ne | ne |

*  
Tabela 16.1. Osobine modifikatora pristupa u Javi  
  
*

Sada je jasno da ključna reč public prilikom definisanja klase i main metode u kodu našeg prvog Java programa označava da će takvi elementi našeg programa biti javno dostupni. main metoda, kao ulazna tačka programa, mora biti javno dostupna. U protivnom dolazi do greške:

```java
privatestaticvoidmain(String[] args) {
}
```

  
main metodu smo sada učinili privatnom i prilikom prevođenja programa sa ovakvom metodom se dobija poruka:

Error: Main method not found in class MyFirstProgram, please define the main method as:  
public static void main(String\[\] args)  
or a JavaFX application class must extend javafx.application.Application

  
Modifikatore pristupa možemo još bolje razumeti na primeru prve Java klase koju smo u prethodnoj lekciji samostalno kreirali:

```java
classCar {
 
    String make;
    String model;
 
    Car() {
 
    }
 
    Car(String make, String model) {
        this.make = make;
        this.model = model;
    }
 
    voidstartEngine() {
        System.out.println("Engine started...");
    }
}
```

  
Unutar naše klase Car, ni na jednom elementu nema ključne reči koja definiše modifikator pristupa. To praktično znači da sama klasa i svi njeni članovi poseduju podrazumevani modifikator pristupa – *package-private*. Pogledajte šta bi se dogodilo kada bismo, na primer, metodu za startovanje motora učinili privatnom:

```java
privatevoidstartEngine() {
        System.out.println("Engine started...");
}
```

  
Metoda startEngine() je sada privatna i izvan klase se uopšte i ne može pozvati (slika 16.1).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_01.png)*

*Slika 16.1. Privatnoj metodi se ne može pristupiti izvan klase  
  
*

Razvojno okruženje IntelliJ IDEA jasno signalizira da metoda startEngine() ima privatni modifikator pristupa. Stoga ovakav kod poseduje grešku zbog koje neće biti moguće njegovo prevođenje.

| **Modifikatori pristupa klasa**  Kao što ste nešto ranije mogli da pročitate, direktno nad klasama se mogu definisati samo dva modifikatora pristupa: *public* i *package-private*. Nad klasnim članovima se mogu primeniti i svi ostali modifikatori. |
| --- |

Kojim modifikatorom pristupa se omogućava da element bude vidljiv samo u okviru sopstvene klase i izvedenih klasa?

  

### Statički elementi klasa

Ulazna tačka Java programa, odnosno main metoda poseduje još jednu ključnu reč koja je za nas nepoznanica:

```java
publicstaticvoidmain(String[] args) {
 
}
```

  
To je ključna reč **static** koju možete videti u potpisu main metode. Korišćenje ključne reči static govori da određeni element klase pripada isključivo klasi, a ne nekom pojedinačnom objektu koji se korišćenjem takve klase kreira. To na kraju omogućava da se statičkom elementu može pristupiti bez prethodnog instanciranja klase.

Metoda main po jezičkoj specifikaciji mora biti statička, kako bi virtuelna mašina prilikom pokretanja aplikacije mogla da je pozove bez prethodnog kreiranja objekta klase u kojoj se main metoda nalazi.

I mi smo u prethodnoj lekciji kreirali jednu metodu koja je idealni kandidat da postane statička. Reč je o metodi klase Car, koja je namenjena za pretvaranje snage motora iz kilovata u konjske snage:

```java
doublekwToHp(intkw){
    returnkw / 0.745699872;
}
```

  
S obzirom na to da svaki automobil mora imati motor, metoda za računanje jačine motora u konjskim snagama karakteristična je za sve automobile. Stoga bi bilo dobro kada bismo takvu metodu mogli da koristimo bez prethodnog instanciranja. Tako nešto se može postići njenim pretvaranjem u statičku metodu:

```java
staticdoublekwToHp(intkw){
    returnkw / 0.745699872;
}
```

  
Ovakva metoda sada se može pozvati na sledeći način:

```java
doublehpPower = Car.kwToHp(150);
```

Bitno je primetiti da se u prikazanoj naredbi metoda kwToHp direktno poziva nad klasom i da prethodno nije izvršeno njeno isntanciranje. Na primeru metode za pretvaranje kilovata u konjske snage, ovo je potpuno logičan izbor, zato što ovakva funkcionalnost nije vezana ni za jedan konkretan automobil.

Po identičnom principu, mogu se kreirati i statička polja:

```java
classCar {
    String make;
    String model;
    staticintnoCarInTheShowroom = 16;
}
```

  
Klasa Car sada poseduje još jedno svojstvo (polje) tipa int, sa nazivom noCarInTheShowroom. Njegova vrednost je direktno unutar klase inicijalizovana na 16. Ovo svojstvo možete da doživite kao način da se u programu vodi evidencija o ukupnom broju vozila koja se nalaze u nekom auto-salonu. Svakako to nije informacija koja je vezana za neku konkretnu instancu klase Car, pa je upravo zbog toga ovo polje i proglašeno statičkim, definisanjem ključne reči static ispred njegovog tipa.

Ovakvom polju se sada može pristupiti na sledeći način:

```java
System.out.println(Car.noCarInTheShowroom);
```

  
Ovakva naredba će na izlazu da ispiše vrednost 16.

Zanimljivo je da se statičkim elementima klase može pristupiti i nad objektima:

```java
Car myCar = newCar();
System.out.println(myCar.noCarInTheShowroom);
```

  
Rezultat će biti identičan kao i u prethodnom primeru. Ipak, pristup statičkim članovima klase preko njihovih instanci predstavlja lošu programersku praksu. Ovde smo to uradili kako bismo ilustrovali jednu veoma važnu osobinu statičkih svojstava:

```java
Car myCar = newCar();
Car myCar2 = newCar();
 
myCar.noCarInTheShowroom = 20;
System.out.println(myCar2.noCarInTheShowroom);
```

  
U primeru je prvo obavljeno kreiranje dva objekta klase Car. Zatim je nad promenljivom koja referencira prvi objekat obavljen pristup statičkom polju noCarInTheShowroom i njegova vrednost je promenjena na 20. Na kraju je obavljen ispis vrednosti statičkog polja noCarInTheShowroom i na izlazu se dobija:

20

Iz ovoga se može zaključiti da, iako izgleda kao da noCarInTheShowroom pripada pojedinačnim objektima, to zapravo nije tako. Kao što je već rečeno, statička polja pripadaju klasi, a ne pojedinačnim instancama.

### Konstante

Logičan nastavak priče o statičkim poljima jeste definisanje pojma konstanti. Konstante su polja čije se vrednosti nakon inicijalizacije ne mogu menjati. Konstanta se može kreirati na sledeći način:

```java
publicstaticfinaldoublePI = 3.14;
```

  
Prikazanom naredbom definiše se jedna konstanta. Konstanta je zapravo matematička vrednost PI. Bitno je da primetite da se u Javi konstante kreiraju kombinacijom ključnih reči static i final. Značenje ključne reči static smo već obradili, dok ključna reč **final** osigurava da se vrednost ovakvog polja neće moći menjati (slika 16.2).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_02.png)*

*Slika 16.2. Promena vrednosti final svojstva nije moguća  
  
*

Na slici 16.2. možete videti da pokušaj promene vrednosti konstante PI dovodi do greške.

Konstante se po konvenciji imenuju velikim slovima, baš kao što je to obavljeno u prethodnom primeru (PI). Ukoliko se naziv konstante sastoji iz više reči, pojedinačne reči se odvajaju donjom crtom:

```java
publicstaticfinalString APPLICATION_PATH = "c:/myApplication/";
```

### Tipovi promenljivih u zavisnosti od mesta deklaracije

S obzirom na to da smo se u dosadašnjem toku lekcije upoznali sa klasama i metodama, možemo da razmotrimo sva ona mesta na kojima se mogu pojaviti promenljive u jednom Java programu. Kao referentni primer, poslužiće nam kod prikazan slikom 16.3.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_03.png)*

*Slika 16.3. Različite vrste promenljivih  
  
*

Slika 16.3 prikazuje kod naše Car klase. Klasa poseduje tri svojstva, dva konstruktora i jednu metodu. Na primeru ovakvog koda, možemo konstatovati da promenljive u Javi mogu imati nekoliko različitih uloga, na osnovu kojih se može reći da postoje sledeće vrste promenljivih:

- objektne promenljive (svojstva);
- klasne (statičke) promenljive;
- lokalne promenljive;
- parametarske promenljive.

Sve ove promenljive postoje unutar koda na slici 16.3, na kojoj su adekvatno obeležene.

**Objektne promenljive** ili, kako se često nazivaju, instance jesu one promenljive koje predstavljaju svojstva instance neke klase. Ovo su promenljive koje se pojavljuju samo u kontekstu objekta i nije moguće pristupiti im bez prethodnog instanciranja klase. U prikazanom primeru, to su svojstva make i model (ali ne i ulazni parametri konstruktora make i model; oni su nešto drugo):

```java
Car.make = "Honda";
```

  
Ovakva naredba proizvodi grešku, zato što se svojstvu make ne može pristupiti bez objekta.

**Klasne (statičke) promenljive** postoje samo u domenu klase, što znači da nije potrebno obaviti instanciranje kako bi im se pristupilo. U primeru sa slike 16.3, klasna promenljiva je noCarInTheShowroom:

```java
Car.noCarInTheShowroom = 20;
```

**  
Lokalne promenljive** su one koje su deklarisane u okviru nekog bloka koda. U našem primeru, takva je promenljiva result unutar metode kwToHp. Reč je o promenljivama koje postoje samo u okviru metode u kojoj su definisane, pa se upravo zbog toga i zovu lokalne. To praktično znači da njima nije moguće pristupiti izvan metode u kojoj se nalaze. Evo jednog takvog primera (slika 16.4).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_04.png)

*Slika 16.4. Lokalnim promenljivama se ne može pristupiti izvan metode u kojoj su deklarisane  
  
*

Primer podrazumeva jednu klasu sa dve metode. Jedna je osnovna main metoda, a druga metoda sa nazivom testMethod unutar koje je deklarisana jedna lokalna promenljiva. Unutar main metode se pokušava pristupiti promenljivoj myVariable – što, naravno, rezultuje neuspehom.

Pojam lokalnih promenljivih nije ograničen na metode. Drugim rečima, lokalne promenljive mogu da postoje i unutar drugih vrsta blokova sa kojima smo se već susretali. Reč je o uslovnim blokovima i blokovima petlji. Promenljive deklarisane unutar takvih blokova takođe su lokalne:

```java
if(true) {
     String myValue = "Hello World";
}
System.out.println(myValue);
```

  
Ovde možemo da vidimo jednu promenljivu (myValue) koja je deklarisana unutar uslovnog if bloka. Uslov je formulisan tako da će se njegov kod uvek izvršiti. Ipak, i pored toga, pokušaj ispisa vrednosti promenljive myValue izvan bloka u kome je ona deklarisana stvara grešku:

java: cannot find symbol  
symbol: variable myValue

**  
Parametarske promenljive** su zapravo jedna vrsta lokalnih promenljivih, ali promenljivih koje omogućavaju da metode dobiju ulazne ili emituju izlazne vrednosti. U primeru sa slike 16.3, takve promenljive su make i model, kao ulazni parametri konstruktora, i kw kao ulazni parametar metode kwToHp. Bitno je da razumete da će takve promenljive prilikom pozivanja metode biti popunjene prosleđenim vrednostima i da se od tog trenutka one ponašaju kao upravo ilustrovane lokalne promenljive:

```java
staticdoublekwToHp(intkw) {
 
        kw = 10;
 
        doubleresult = kw / 0.745699872;
        returnresult;
}
```

  
Evo sada smo obavili i pristup takvoj lokalnoj promenljivoj i čak izvršili i promenu njene vrednosti. U ovakvoj situaciji, šta god da se ovoj metodi prosledi kao ulazni parametar, ona će kao vrednost kilovata uvek koristiti broj 10:

```java
System.out.println(Car.kwToHp(150));
```

  
Da su parametarske promenljive zaista lokalne promenljive, najlakše je uvideti na primeru ilustrovanom slikom 16.5.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_05.png)

*Slika 16.5. Ulazni parametri su zapravo lokalne promenljive unutar svoje metode  
  
*

Unutar metode se pokušava deklarisati lokalna promenljiva sa nazivom kw, odnosno promenljiva identičnog naziva kao i ulazni parametar. Dobija se jasna poruka: da u okviru bloka već postoji promenljiva sa tim imenom, pri čemu se misli na ulazni parametar.

### Primitivni/referentni parametri

Kada smo već kod ulaznih parametara metoda, dobro je poznavati još jednu njihovu osobinu koja je veoma važna. Naime, u programskom jeziku Java, metodama se mogu prosleđivati primitivne vrednosti, ali i parametri složenih tipova, odnosno objekti.

Pogledajmo šta se dešava kada se metodi prosleđuje parametar primitivnog tipa:

```java
publicclassTestClass {
    publicstaticvoidmain(String[] args) {
        intx = 5;
        System.out.println("This is initial value: "+ x);
        passMethod(x);
        System.out.println("This is the value after the completion of the method: "+ x);
    }
    publicstaticvoidpassMethod(intx) {
        x = 10;
        System.out.println("This is the value from method: "+ x);
    }
}
```

  
U prikazanom kodu definisana je jedna klasa sa nazivom TestClass. Ona sadrži standardnu main metodu za pokretanje programa i još jednu metodu sa nazivom passMethod*,* koja će poslužiti kao metoda na kojoj ćemo obavljati ogled. Ova metoda prihvata jedan ulazni parametar tipa int*,* postavlja njegovu vrednost na 10 i na kraju na izlazu ispisuje vrednost promenljive x.

U okviru main metode deklarisana je promenljiva x i njoj je dodeljena vrednost 5.

| **Lokalne promenljive istog naziva**  Obratite pažnju na to da unutar obe metode (main i passMethod) postoje promenljive identičnog naziva (x). Ovako nešto je potpuno legitimno, s obzirom na to da je reč o lokalnim promenljivama, koje postoje samo unutar bloka u kome su deklarisane. Stoga je svaka od ovih promenljivih potpuno nezavisna i one ne utiču jedna na drugu. |
| --- |

Unutar main metode zatim je obavljen poziv metode passMethod i njoj je prosleđena vrednost lokalne promenljive x. Pre i posle poziva metode, dodate su naredbe za ispis vrednosti lokalne promenljive x. Na kraju izvršavanja programa, na izlazu se dobija sledeće:

This is initial value: 5  
This is the value from method: 10  
This is the value after the completion of the method: 5  
  

Možemo da se uverimo da metoda nije izvršila promenu vrednosti promenljive x. Razlog je vrlo jednostavan. Primitivne promenljive se prosleđuju po vrednosti, odnosno, metode dobijaju samo kopije vrednosti promenljivih. Na taj način, promenljive izvan metoda ostaju nepromenjene.

Referentni tipovi podataka se u Javi takođe prosleđuju po vrednosti. U Javi ne postoji nešto što se naziva prosleđivanje po referenci. Kada se metodi prosledi neki objekat, njoj se, u suštini, prosleđuje pokazivač na objekat, odnosno vrednost memorijske lokacije objekta. Ipak, vrednosti polja jednog objekta se mogu izmeniti u okviru metode ukoliko imaju modifikator pristupa koji to omogućava. To će ilustrovati naredni primer, u kome ćemo koristiti jedan referentni tip koji ćemo samostalno kreirati:

```java
publicclassReferenceType {
    publicintx = 5;
}
```

  
Kao što vidite, reč je o klasi ReferenceType unutar koje se nalazi samo jedno polje sa imenom x i vrednošću 5. Logika unutar glavne klase će izgledati ovako:

```java
publicclassMyFirstProgram {
    staticReferenceType rt = newReferenceType();
    publicstaticvoidmain(String[] args) {
        System.out.println("This is initial value: "+ rt.x);
        passMethod(rt);
        System.out.println("This is the value after the completion of the method: "+ rt.x);
    }
    publicstaticvoidpassMethod(ReferenceType rt) {
        rt.x = 10;
        System.out.println("This is the value from method: "+ rt.x);
    }
}
```

Primer je praktično identičan prethodnom, s tim što je sada korišćena promenljiva x koja se nalazi unutar objekta klase ReferenceType. Efekat će sada biti ovakav:

This is initial value: 5  
This is the value from method: 10  
This is the value after the completion of the method: 10  
  

Na osnovu ispisa sada je lako zaključiti da se unutar metode passMethod zaista dogodila promena vrednosti svojstva prosleđenog objekta. U tome je razlika između prostih i referentnih vrednosti kao ulaznih parametara metoda.  
  

### Podrazumevane vrednosti polja

Već više puta do sada ste mogli da vidite da je promenljivu moguće deklarisati bez inicijalizacije, odnosno bez dodeljivanja početne vrednosti. Vrlo je bitno znati šta će se u takvim situacijama dogoditi sa takvim promenljivama, odnosno da li one poseduju neku podrazumevanu vrednost ili ne.

Prilikom rada sa lokalnim promenljivama (promenljive unutar metoda), situacija je vrlo jasna. Sve promenljive moraju biti inicijalizovane ili dolazi do pojave greške (slika 16.6).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_06.png)

*Slika 16.6. Lokalne promenljive moraju biti inicijalizovane  
  
*

Promenljiva sa nazivom value nije inicijalizovana i prilikom pokušaja da joj se pristupi dolazi do pojave greške.

Ipak, drugačija je situacija sa promenljivama koje se deklarišu unutar klase, bilo da je reč o klasnim ili o objektnim promenljivama:

```java
publicclassTestClass {
    intvariableA;
    String variableB;
    booleanvariableC;
    charvariableD;
}
```

  
Ovo je klasa sa četiri polja, odnosno četiri promenljive koje su deklarisane, ali nisu inicijalizovane. Pogledajte sada šta se dešava ukoliko napravimo jedan objekat na osnovu ove klase:

```java
TestClass myObj = newTestClass();
 
System.out.println(myObj.variableA);
System.out.println(myObj.variableB);
System.out.println(myObj.variableC);
System.out.println(myObj.variableD);
```

  
Rezultat koji se dobija ovakvim kodom ilustrovan je slikom 16.7.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_16_07.png)

*Slika 16.7. Podrazumevane vrednosti nekih Java tipova  
  
*

Sada u okviru radnog okruženja možete provežbati primer iz ovog odeljka sa klasom TestClass i njene četiri promenljive koje nemaju definisane inicijalne vrednosti. Takođe, možete dodati neinicijalizovane promenljive još nekog tipa, recimo, double ili float.

Na osnovu ovakvog izlaza, može se zaključiti da objektne promenljive, odnosno svojstva, dobijaju određene podrazumevane vrednosti kada ih ne inicijalizujemo eksplicitno. Podrazumevana vrednost se razlikuje u zavisnosti od tipa promenljive:

- numeričke promenljive dobijaju podrazumevanu vrednost 0 ili 0 u zavisnosti od tipa;
- promenljive tipa String kao podrazumevanu vrednost dobijaju null;
- promenljive tipa boolean imaju podrazumevanu vrednost false;
- promenljive tipa char imaju podrazumevanu vrednost karaktera koji u [Unicode](https://www.link-elearning.com/linkdl/opisPojma.php?id=160466 "Unicode") setu karaktera ima kod \\u000; reč je o karakteru koji se zove *null character*.

| **Šta je to null?**  Upravo ste mogli da vidite da je podrazumeva vrednost String promenljivih null. To je zapravo rezervisana vrednost koju mogu imati objektne promenljive. Ona predstavlja referencu koja ne pokazuje ni na jedan objekat. Tako null predstavlja neku vrstu pandana vrednosti 0, koja se može dodeliti prostim tipovima, s tim što se null može koristiti samo nad objektima.  O stacku i heapu već je bilo reči u jednoj od prethodnih lekcija, tako da znamo da se referentni tipovi smeštaju na heap, dok se na stacku nalazi samo pokazivač, odnosno memorijska lokacija objekta. Kada neki objekat ima vrednost null (odnosno nema vrednost), to znači da kreirana objektna promenljiva ne pokazuje ni na jednu memorijsku lokaciju.  Pošto je moguće razdvojiti kreiranje i instanciranje jednog objekta, u periodu između ove dve operacije vrednost deklarisane promenljive biće null. |
| --- |

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_16_01.thb) JCPR1\_16\_01.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_16_01.Mp4")

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_16_02.thb) JCPR1\_16\_02.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_16_02.Mp4")

Kako Vam mogu pomoći?