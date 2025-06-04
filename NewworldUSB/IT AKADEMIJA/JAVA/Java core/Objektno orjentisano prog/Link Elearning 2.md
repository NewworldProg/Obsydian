---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=7940547b91ee83335cf8abad2bfbaa16_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434684"
author:
published:
created: 2025-05-11
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 17 od 22

## Postulati OOP-a

U prethodnim lekcijama imali ste prilike da se upoznate sa pojmovima klasa i objekata, ali i sa svim pojmovima koji su sa njima povezani. Tako smo naučili šta su to klase, koji su njihovi elementi i kako se kreiraju, a na kraju i kako se na osnovu klasa kreiraju objekti. Ipak, za kompletno razumevanje objektno orijentisanog programiranja neophodno je da ovladamo još nekim veoma važnim principima. Stoga će lekcija pred vama biti posvećena osnovnim postulatima objektno orijentisanog programiranja. Oni su sledeći:

- apstrakcija;
- enkapsulacija;
- nasleđivanje;
- polimorfizam.

### Apstrakcija

Kreiranje objekata koji predstavljaju entitete iz realnog sveta drugačije se naziva modelovanje. Modelovanjem se omogućava rukovanje entitetima u programskom kodu Java programa. Tako modelovanje omogućava da korišćenjem klasa u programskom jeziku Java stvorimo tipove koji su našem programu potrebni, a inicijalno ne postoje unutar same Java platforme:

```java
publicclassCar {
 
    String make;
    String model;
    intweight;
    String color;
 
    staticintnoCarInTheShowroom = 12;
 
    publicCar() {
 
    }
 
    publicCar(String make, String model, intweight, String color) {
        this.make = make;
        this.model = model;
        this.weight = weight;
        this.color = color;
    }
 
    voidstartEngine() {
        System.out.println("The engine of "+ this.make + " "+ this.model + " has been started.");
 
    }
}
```

  
Ovo je primer Car klase za modelovanje automobila. Klasa nam je poznata iz prethodne lekcije, a u ovoj lekciji je ona blago modifikovana, tako da sadrži:

- četiri objektna svojstva – proizvođač, model, težina i boja;
- jedno klasno svojstvo, koje služi za čuvanje ukupnog broja vozila;
- dva konstruktora, pri čemu prvi nema parametara, a drugi prihvata parametre za inicijalizaciju svojstava;
- objektnu metodu startEngine(), koja formira ispis da je motor određenog automobila pokrenut.

Ovakva klasa se može upotrebiti na sledeći način:

```java
Car myCar = newCar("Honda", "Accord", 1590, "black");
myCar.startEngine();
```

Na ovaj način se kreira jedan objekat klase Car i zatim se poziva metoda startEngine:

The engine of Honda Accord has been started.

U upravo prikazanom primeru ste mogli da vidite da se u procesu modelovanja veoma kompleksni pojmovi iz realnog sveta mogu predstavljati znatno jednostavnije, što se često i radi. Tako smo i mi prilikom kreiranja klase automobila modelovali samo nekoliko osobina i ponašanja takvog realnog pojma. Drugim rečima, jedan automobil se, pored proizvođača, modela, težine i boje, može definisati i brojnim drugim osobinama – tip menjača, emisiona klasa, broj brzina, tip pogona itd. Jasno je da smo mi prilikom modelovanja pojma automobila napravili jedan uprošćeni, pojednostavljeni model. Takav proces, kojim se postiže kreiranje jednostavnih modela znatno kompleksnijih entiteta iz realnog sveta, u objektno orijentisanom programiranju se drugačije naziva apstrakcija.

Apstrakcija omogućava da se složeni entiteti iz realnog sveta modeluju baš onako kako mi to želimo – sa nivoom detalja koji odgovara potrebama našeg programa. Takođe, apstrakcija omogućava i da se u potpunosti skriju unutrašnji detalji nekog entiteta. Tako, na primer, ne moramo znati na koji način će biti obavljeno startovanje motora nekog vozila. Na nama je da pozovemo metodu za startovanje, dok je sam način startovanja (korišćenjem tradicionalnog ključa, ključa-kartice, dugmeta za startovanje...) skriven unutar objekta i logike kojom je realizovana metode za startovanje.

Pojam apstrakcije može se razumeti i na primeru metoda koje nam Java platforma izlaže na korišćenje. Jedna od takvih metoda je i metoda println, koju smo intenzivno koristili u gotovo svim prethodnim lekcijama. Apstrakcija omogućava da se ova metoda koristi za ispis teksta, bez potrebe za poznavanjem načina na koji je takva metoda realizovana. Tako apstrakcija, naposletku, smanjuje ponavljanje koda, jer nas oslobađa potrebe za ponovnim pisanjem funkcionalnosti koje su već realizovane.  
  

### Enkapsulacija

Objekat predstavlja zaokruženu celinu, zato što u potpunosti opisuje jedan pojam iz realnog sveta. Unutar objekata objedinjuju se informacije i funkcionalnosti koje se tiču entiteta koji se modeluje. Objedinjavanje takvih informacija i funkcionalnosti drugačije se naziva enkapsulacija.

Enkapsulacija se najbolje može razumeti na već prikazanim primerima kreiranja objekata automobila. Jedan automobil, modelovan korišćenjem Java objekta, ilustrativno se može prikazati kao na slici 17.1.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_17_01.png)*

*Slika 17.1. Enkapsulacija  
  
*

Slika 17.1. dočarava pojam enkapsulacije na primeru jednog Java objekta. Na slici 17.1. nije slučajno prikazana prava kapsula – svojstva i metode objedinjuju se unutar objekta baš kao i različiti sastojci unutar jedne farmaceutske kapsule. Enkapsulacijom se različita svojstva i metode jednog objekta prezentuju kao celina, kojom se rukuje korišćenjem naziva promenljive koja čuva referencu na objekat.

Veoma bitan scenario kojim se u Java jeziku postiže enkapsulacija, jesu modifikatori pristupa o kojima je već bilo reči. Naime, korišćenjem modifikatora pristupa, mi imamo mogućnost da veoma precizno definišemo kako se objektima i članovima naših klasa može rukovati. Drugim rečima, korišćenjem modifikatora pristupa imamo mogućnost da kontrolišemo vidljivost određenih objektnih članova i da na taj način postignemo još bolji efekat enkapsulacije.

Enkapsulacija se veoma često demonstrira na primeru objektnih svojstava, tako što se ona kreiraju kao privatna polja. Kako bi moglo da im se pristupi i izvan klase u kojoj su definisana, pribegava se definisanju specijalnih metoda koje se koriste za upis i čitanje vrednosti privatnih svojstava. Takve metode su poznate pod nazivom **get i set metode**. Evo kako to izgleda na praktičnom primeru:

```java
publicclassCar {
 
    privateintweight;
 
    publicintgetWeight() {
        returnweight;
    }
 
    publicvoidsetWeight(intweight) {
        this.weight = weight;
 
    }
  
}
```

  
Ovo je isečak klase Car, unutar koje je svojstvo weight privatno, pa mu se ne može pristupiti izvan klase. Kako bi njegovom vrednošću moglo da se rukuje, kreirane su dve metode – getWeight i setWeight. Unutar tela ovih metoda obavlja se čitanje i upisivanje vrednosti privatnog weight polja, upravo tim redosledom.

Ipak, sada se možete zapitati zbog čega bismo nešto ovako radili, kada u slučaju postojanja javnog weight polja njime možemo direktno da rukujemo. Ovakav pristup se čini kao uvođenje dodatnog koda bez pravog razloga. Ipak, tako je samo na prvi pogled.

Postojanje *get i set metoda* omogućava kontrolisanu interakciju sa privatnim poljem weight. To praktično znači da na ovaj način možemo da definišemo neku posebnu logiku koja će se aktivirati prilikom čitanja i upisivanja vrednosti ovog svojstva. Na primer, nešto ovako:

```java
publicvoidsetWeight(intweight) {
 
        if(weight < 0) {
            this.weight = 0;
        } elseif(weight > 3000) {
            this.weight = 3000;
        } else{
            this.weight = weight;
        }
 
}
```

  
Ovo je metoda za postavljanje vrednosti weight svojstva. Možete da vidite da unutar ovakve metode, pored osnovne logike postavljanja vrednosti, postoji i kod koji proverava prosleđenu vrednost. Ukoliko je ona manja od nule, svojstvo dobija vrednost 0, a ukoliko je prosleđena vrednost veća od 3000, svojstvo dobija vrednost 3000. Drugim rečima, definisana logika ne dozvoljava da svojstvo weight ima vrednost izvan opsega 0–3000.

Korišćenje get i set metoda može da učini da neko ko koristi objekte naše klase, a nema pristup izvornom kodu, ne može ni da zna da li neko svojstvo postoji ili ne. Evo jednog takvog primera:

```java
publicclassCar {
 
    privateString make;
    privateString model;
 
    publicvoidsetMake(String make) {
        this.make = make;
    }
 
    publicvoidsetModel(String model) {
        this.model = model;
    }
 
    publicString getName() {
        returnmake + " "+ model;
    }
 
}
```

  
Primer opet podrazumeva isečak klase Car, sa akcentom na make i model svojstva, koja su privatna. Za postavljanje njihovih vrednosti postoji po jedna set metoda. Ipak, direktno čitanje vrednosti ovih svojstava izvan klase nije moguće, s obzirom na to da nisu napravljene pojedinačne get metode. Umesto njih, u klasi postoji jedna *get metoda* – getName. Reč je o metodi koja isporučuje kompletno ime automobila, koje je sačinjeno iz proizvođača i modela. Ovaj primer ilustruje dve bitne osobine:

- get i set metode omogućavaju da se naprave polja koje se mogu samo čitati ili samo upisivati;
- get i set metode omogućavaju da se javna vrednost formira na osnovu više privatnih vrednosti (u prikazanom primeru, korisnik klase ne može ni da zna da u klasi ne postoji polje name).

### Nasleđivanje

Naredna, veoma značajna osobina objektno orijentisanog programiranja o kojoj će biti reči jeste nasleđivanje. Nasleđivanje omogućava kreiranje klasa koje osobine i ponašanja nasleđuju od neke druge klase (slika 17.2).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_17_02.png)*

*Slika 17.2. Nasleđivanje  
  
*

Slika 17.2. ilustruje jedan primer nasleđivanja u objektno orijentisanom svetu. Klase Convertible i Pickup nasleđuju osnovni skup svojstava i ponašanja od klase Car. Unutar klase Car objedinjene su osnovne karakteristike koje poseduju svi automobili. Klase Convertible i Pickup nasleđuju takav skup osnovnih osobina, ali pored njih poseduju i određene osobine koje su karakteristične samo za njih. Kako sve ovo izgleda u praksi, biće ilustrovano u narednim redovima. Za početak, pogledajmo kako će izgledati klasa Car:

```java
publicclassCar {
 
    privateString make;
    privateString model;
    privateintweight;
    privateString color;
 
    publicString getName() {
        returnmake + " "+ model;
    }
 
    publicString getMake() {
        returnmake;
    }
 
    publicvoidsetMake(String make) {
        this.make = make;
    }
 
    publicString getModel() {
        returnmodel;
    }
 
    publicvoidsetModel(String model) {
        this.model = model;
    }
 
    publicintgetWeight() {
        returnweight;
    }
 
    publicvoidsetWeight(intweight) {
 
        if(weight < 0) {
            this.weight = 0;
        } elseif(weight > 3000) {
            this.weight = 3000;
        } else{
            this.weight = weight;
        }
 }
 
    publicString getColor() {
        returncolor;
    }
 
    publicvoidsetColor(String color) {
        this.color = color;
    }
 
    staticintnoCarInTheShowroom = 12;
 
    publicCar() {
 
    }
 
    publicCar(String make, String model, intweight, String color) {
        this.make = make;
        this.model = model;
        this.weight = weight;
        this.color = color;
    }
 
    String getInfo() {
        return"Make: "+ this.make + "\n"+
                "Model: "+ this.model + "\n"+
                "Weight: "+ this.weight + "\n"+
                "Color: "+ this.color;
    }
 
}
```

  
Novina u prikazanoj klasi je metoda getInfo, koja je postavljena umesto metode startEngine. Reč je o metodi koja koristi vrednosti privatnih svojstava kako bi formirala ispis koji sadrži informacije o vozilu. Ona može da se upotrebi na sledeći način:

```java
Car myCar = newCar("Honda", "Accord", 1590, "black");
System.out.println(myCar.getInfo());
```

Na ovaj način se na izlazu dobija kumulativni prikaz osobina automobila:

Make: Honda  
Model: Accord  
Weight: 1590  
Color: black  
  

Pređimo sada na prvi primer nasleđivanja. U nastavku ćemo kreirati klasu Convertible za predstavljanje posebne vrste automobila – kabrioleta:

```java
publicclassConvertible extendsCar {
 
                 
 
}
```

  
Ključna reč kojom se obavlja nasleđivanje između klasa u Java jeziku jeste **extends**. Ova ključna reč navodi se između naziva klase koja se nasleđuje i nasleđene klase. Sledeći korak jeste definisanje klasnih članova naše nove klase. Klasa Convertible imaće sve članove koje ima i klasa Car, uz dodatak jednog svojstva koje će čuvati vrednost koja oslikava tip krova kabrioleta. S obzirom na to da smo obavili nasleđivanje, ne moramo da sve one članove iz klase Car ponovo kreiramo unutar klase Convertible, već je potrebno da kreiramo isključivo članove koji se razlikuju:

```java
publicclassConvertible extendsCar {
 
    String roofType;
 
}
```

  
Kao što je rečeno, osobenost klase Convertible jeste svojstvo za čuvanje tipa krova, te smo unutar nje deklarisali samo njega.

Sledeći korak je da definišemo konstruktor:

```java
publicclassConvertible extendsCar {
 
    String roofType;
 
    publicConvertible(String make, String model, intweight, String color, String roofType) {
        super(make, model, weight, color);
        this.roofType = roofType;
    }
 
}
```

  
Konstruktor Convertible klase prihvata sve parametre kao i onaj iz klase Car, uz dodatak parametra koji je karakterističan za nju. Unutar konstruktora koristi se jedna posebna ključna reč – **super**. To je ključna reč koja omogućava da se obavi pozivanje konstruktora ili pristupanje svojstvima i metodama roditeljske klase. Ključa reč super najčešće se koristi za pozivanje konstruktora roditeljske klase, što je učinjeno i u primeru. Prilikom takvog poziva se prosleđuju parametri koje prihvata konstruktor roditeljske klase. Tako će roditeljska klasa da obavi njihovu obradu, a nama samo preostaje da inicijalizujemo svojstvo roofType, što je u primeru i učinjeno.

Klasa Convertible kreirana u prethodnim redovima nasledila je sve osobine klase Car. Stoga je sada moguće napisati ovako nešto:

```java
Convertible convertible1 = newConvertible("Honda", "S2000", 1274, "silver", "Vinyl, soft-top");
System.out.println(convertible1.getName());
```

Kreiramo jedan objekat Convertible tipa i pozivamo metodu getName, koja je definisana u roditeljskoj klasi. Da sve funkcioniše bez problema, možemo se uveriti na osnovu ispisa koji se dobija:

Honda S2000  

| **Pravila pr** **ilikom nasleđivanja u Javi**  Prilikom nasleđivanja postoji par pravila koja treba da budu ispoštovana i od kojih zavisi tretman nasleđenih elemenata. Prvo pravilo glasi da klasa koja nasleđuje može imati samo jednu roditeljsku klasu.  Drugo pravilo se odnosi na modifikatore pristupa. Naime, direktno se nasleđuju samo *public*, *protected* i *package-private* klasni članovi. Klasnim članovima koji su obeleženi private modifikatorima pristupa ne može se direktno pristupiti iz klasa koje nasleđuju. Kako bi im se pristupilo, takvi elementi moraju imati protected modifikator ili odgovarajuće get i set javne metode. |
| --- |

| **Zabrana** **nasleđivanja**  U programskom jeziku Java moguće je i onemogućiti da se neka klasa nasledi. Sve što je potrebno uraditi, jeste postaviti ključnu reč final u deklaraciju klase:  ```java publicfinalclassCar {              } ```     Sada je definisano da se klasa Car neće moći naslediti, pa u ovakvoj situaciji kod koji smo do sada pisali u ovoj lekciji neće funkcionisati. |
| --- |

### Polimorfizam

Prilikom realizovanja nasleđivanja u objektno orijentisanom programiranju, veoma često dolazi do potrebe za redefinisanjem nekih nasleđenih ponašanja. Tako roditeljski objekat može definisati neku funkcionalnost koja ne zadovoljava u potpunosti njegove naslednike. Ipak, naslednici imaju mogućnost da nasleđeno ponašanje prilagode, dopune ili u potpunosti izmene. Na taj način se stvaraju različite verzije jednog istog ponašanja, odnosno verzije koje odgovaraju svakom pojedinačnom tipu objekta. Takva osobina objektno orijentisanog programiranja drugačije se naziva polimorfizam, odnosno višestruko značenje jednog istog pojma.

Upravo opisanu situaciju imamo u prethodnom primeru. Pogledajte o čemu je reč:

```php
Convertible convertible1 = newConvertible("Honda", "S2000", 1274, "silver", "Vinyl, soft-top");
 
System.out.println(convertible1.getInfo());
```

  
U prikazanom primeru kreiran je jedan objekat tipa Convertible. Zatim je nad njim pozvana metoda getInfo koja je definisana unutar roditeljske klase. Evo kako izgleda ispis:

Make: Honda  
Model: S2000  
Weight: 1274  
Color: silver  
  

Ukoliko analizirate dobijeni ispis, moći ćete da zaključite da u njemu nedostaje informacija o tipu krova. Ovo je potpuno očekivano, pošto se metoda getInfo nalazi u roditeljskoj klasi, a roditeljska klasa uopšte ne poseduje polje za čuvanje informacije o tipu krova. Da bi se ovakav problem prevazišao, neophodno je i unutar klase Convertible definisati metodu getInfo. Takav postupak se u objektno orijentisanom programiranju naziva redefinisanje metoda (**overriding**):

```java
publicclassConvertible extendsCar {
 
    String roofType;
 
    publicConvertible(String make, String model, intweight, String color, String roofType) {
        super(make, model, weight, color);
        this.roofType = roofType;
    }
 
    @Override
    String getInfo() {
        return"Make: "+ this.getMake() + "\n"+
                "Model: "+ this.getModel() + "\n"+
                "Weight: "+ this.getWeight() + "\n"+
                "Color: "+ this.getColor() + "\n"+
                "Roof type: "+ this.roofType;
    }
 
}
```

  
Sada i unutar klase Convertible postoji metoda getInfo. Ona obavlja isto što i metoda iz roditeljske klase, uz dodatak ispisa informacije o tipu krova. Kako bi se naznačilo da je reč o redefinisanoj metodi, odnosno kako bi se naglasilo da metoda sa istim nazivom postoji i unutar roditeljske klase, pre potpisa metode postavljena je oznaka **@Override**.

S obzirom na to da je najveći deo upravo prikazane metode identičan onom u roditeljskoj klasi, dobro bi bilo kada bismo na neki način mogli da iskoristimo logiku koja je već definisana unutar roditeljske klase. Tako nešto zapravo i možemo da uradimo i to korišćenjem jedne ključne reči sa kojom smo se već susretali. U pitanju je ključna reč super. Ona će nam omogućiti da pristupimo getInfo metodi iz roditeljske klase:

```java
@Override
    String getInfo() {
 
        returnsuper.getInfo() + "\n"+
                "Roof type: "+ this.roofType; 
    }
```

  
Ključna reč super omogućava pristup objektu roditeljske klase. Nju smo iskoristili kako bismo pozvali metodu getInfo iz Car klase. Od nje dobijamo informacije o proizvođaču, modelu, težini i boji, pa na kraju na takve informacije dodajemo još samo podatak o tipu krova. Ovakav pristup je, kao što možete videti, znatno kompaktniji i predstavlja vrhunac redefinisanja metoda.

| **Overloading**  Još jedan pojam u Javi koji oslikava klasičan primer polimorfizma jeste *overloading*. Sa ovim pojmom smo se već sreli u jednoj od prethodnih lekcija, kada je bilo reči o definisanju konstruktora. Naime, *overloading* se ogleda u mogućnosti da u okviru jedne iste klase postoji veći broj metoda istog imena, ali različitih ulaznih i izlaznih parametara. Prilikom poziva metode, u zavisnosti od prosleđenih parametara, poziva se odgovarajuća metoda. I u primeru iz ove lekcije postoji *overloading*. Reč je o klasi Car, u kojoj postoje dva konstruktora. Oni, naravno, imaju iste nazive, a različite ulazne parametre, što je primer overloadinga. |
| --- |

Postojanje više metoda sa istim nazivom, ali različitim parametrima naziva se:

  

### Vežbe

**Vežba 1**

Potrebno je napraviti jednu klasu Shape*,* koja bi sadržala neke podatke o geometrijskom obliku: poziciju (x, y) i boju. Potrebno je napraviti tri klase koje nasleđuju ovu klasu – jednu za krug, jednu za kvadrat i jednu za pravougaonik.

Svaka treba da sadrži metodu za izračunavanje površine, kao i sopstvene atribute koji su neophodni za ovo izračunavanje (stranice za pravougaonik i kvadrat i poluprečnik za krug). Krug, takođe, treba da poseduje i konstantu PI.

Sve vrednosti mogu biti celobrojne (ne računajući PI i boju).

**Rešenje**

*Shape.java*

```java
publicclassShape {
 
    publicString color;
    publicintx, y;
}
```

*  
Rectangle.java*

```java
publicclassRectangle extendsShape {
 
    publicdoublea, b;
 
    publicdoublearea()
    {
        returna * b;
    }
}
```

*  
Square.java*

```java
publicclassSquare extendsShape {
 
    publicdoublea;
 
    publicdoublearea()
    {
        returna * a;
    }
}
```

*  
Circle.java*

```java
publicclassCircle extendsShape {
 
    publicfinaldoublePI = 3.14;
    publicdoubler;
 
    publicdoublearea()
    {
   returnr * r * PI;
   }
}
```

  
*Main.java*

```java
publicclassMain {
 
    publicstaticvoidmain(String[] args) {
 
        Circle c = newCircle();
        c.x = 100;
        c.y = 200;
        c.color = "red";
        c.r = 12;
        System.out.println(c.area());     
   }
}
```

  
**Vežba 2**

Nаpisаti klаsu Animal. Svаku životinju kаrаkteriše njenа vrstа. Iz klаse Animal izvesti klаsu Dog. Zа psа je poznato njegovo ime i rаsа. Ako se prilikom kreirаnjа psа ne nаvede njegovа rаsа, postаviti je nа *dachshund*.

**Rešenje**

*Animal.java*

```java
publicclassAnimal {
 
    privateString type;
 
    publicAnimal(String type)
    {
        this.type = type;
    }
 
    @Override
    publicString toString()
    {
        return"This is "+ type;
    }
 
}
```

*  
Dog.java*

```java
publicclassDog extendsAnimal
{
    privateString name, breed;
 
    publicDog(String name)
    {
        super("dog");
        this.name = name;
        breed = "dachshund";
    }
 
    publicDog(String name, String breed)
    {
        super("dog");
        this.name = name;
        this.breed = breed;
    }
 
    @Override
    publicString toString()
    {
        returnsuper.toString() + " "+ name + ", "+ breed + ".";
    }
 
}
```

*  
Glavna klasa:*

```java
publicclassTest
{
    publicstaticvoidmain(String[] args)
    {
        Dog dog = newDog("Max", "labrador");
        Dog famousDog = newDog("Betoven");
 
        System.out.println(dog);
        System.out.println(famousDog);
    }
 
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_17_01.thb) JCPR1\_17\_01.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_17_01.Mp4")

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_17_02.thb) JCPR1\_17\_02.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_17_02.Mp4")

Kako Vam mogu pomoći?