---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=a44d8e4e2e36b6d78c12ee341dfa7bd1_ita_23&c=modul&IDIstorijaKurs=151079&IDJedinica=1434694"
author:
published:
created: 2025-05-21
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 5 od 22

## Refleksija

==Osnova programskog jezika Java== jesu objekti, klase i interfejsi. Konkretne i ==apstraktne klase i interfejsi omogućavaju stvaranje referentnih tipova== koji su potrebni programima koje kreiramo. ==Objekti nastaju na osnovu klasa i predstavljaju instance tipa== koji je definisan klasama i interfejsima na čijoj osnovi su takvi objekti nastali. Tokom izvršavanja programa (*runtime*) imamo mogućnost da ==instanciramo klase i koristimo svojstva i metode koje su definisane unutar objekata i klasa.== Ipak, sve ==do sada, ni na koji način nismo bili u mogućnosti da izmenimo strukturu kreiranih tipova== tokom izvršavanja programa.

Osobine tipova se definišu pisanjem koda. Kada se završi pisanje koda i pokrene program, do sada nismo bili u mogućnosti da dođemo do informacija o tipovima niti da utičemo na njihove osobine. Ipak, ==programski jezik Java poseduje skup funkcionalnosti koje omogućavaju da se tako nešto obavi==. Takav skup funkcionalnosti se naziva refleksija i to je pojam kome će biti posvećena lekcija pred vama.  
  

### Šta je refleksija?

Refleksija je skup funkcionalnosti koji postoji unutar Java platforme i ==omogućava da se u toku izvršavanja programa manipuliše arhitekturom tipova==. Ovakva definicija može zvučati komplikovano, ali je zapravo reč o sasvim jednostavnom konceptu. Refleksija u Javi ==omogućava da se tokom izvršavanja programa ispita struktura klasa i interfejsa i njihovih članova== – polja, konstruktora i metoda. Sve to na kraju omogućava da se napiše kod koji će tokom izvršavanja programa da rukuje tipovima, svojstvima i metodama čija imena i osobine nisu unapred poznati (slika 5.1).

*![](https://www.link-elearning.com/linkdl/coursefiles/1520/ADJAVA1_05_01.png)*

*Slika 5.1. Java refleksija  
  
*

Refleksija je veoma ==korisna kada je podatke iz jednog oblika potrebno pretvoriti u neki drugi.== Na primer, veoma čest oblik za predstavljanje podataka jeste format koji se zove ==[JSON](https://www.link-elearning.com/linkdl/opisPojma.php?id=160748 "JSON"). Takav format se veoma često koristi za razmenu podataka između više aplikacija ili aplikativnih celina==. Naime, unutar programa, ==podaci postoje u objektnom obliku.== ==Kako bi se prosledili== nekoj drugoj aplikaciji preko mreže, ==pribegava se njihovom transformisanju u JSON oblik.== U obavljanju takvog posla, refleksija može biti i više nego korisna, pošto omogućava da se detektuju sva svojstva objekata koje je potrebno pretvoriti u neki drugi oblik.

Refleksija se može ==koristiti i za kreiranje univerzalne funkcionalnosti za čuvanje i izmenu podataka u nekoj [bazi podataka](https://www.link-elearning.com/linkdl/opisPojma.php?id=160749 "bazi podataka")==. Naime, podaci se u bazama čuvaju u tabelama sa redovima i kolonama, pa se refleksija može koristiti za kreiranje funkcionalnosti koja će automatski, na osnovu naziva svojstava, da generiše nazive kolona. ==Refleksija se može koristiti i za postizanje konverzije podataka u suprotnom smeru== – na osnovu naziva kolona unutar kojih se nalaze ==podaci koji su pročitani iz baze podataka, može se napisati funkcionalnost koja automatski poziva odgovarajuću *get* ili *set* metodu.==

Da bismo u toku izvršavanja aplikacije mogli da dobavimo neke informacije kao što su tip određenog objekta, spisak polja određene klase i slično, potrebno je koristiti:

  

### Šta sve omogućava refleksija?

Već je rečeno da refleksija u Javi omogućava da se dinamički, odnosno tokom izvršavanja programa ispitaju osobine tipova i modifikuju njihovi članovi. ==Najznačajniji poslovi koji se mogu obaviti korišćenjem refleksije su:==

- ==rukovanje klasama i kreiranje novih objekata;==
- ==rukovanje poljima;==
- ==rukovanje konstruktorima;==
- ==rukovanje metodama i njihovo pozivanje.==

==U nastavku će upravo nabrojane intervencije biti ilustrovane na primeru klase Product==, sa kojom smo se već susretali:

```java
public class Product {
 
    private String brand;
    private String model;
    private double price;
 
 
    public String getBrand() {
        returnbrand;
    }
 
    public void setBrand(String brand) {
        this.brand = brand;
    }
 
    public String getModel() {
        returnmodel;
    }
 
    public void setModel(String model) {
        this.model = model;
    }
 
    public double getPrice() {
        returnprice;
    }
 
    public void setPrice(doubleprice) {
        this.price = price;
    }
 
    public Product() {
 
    }
 
    public Product(String brand, String model) {
        this.brand = brand;
        this.model = model;
    }
 
    public Product(String brand, String model, double price) {
        this.brand = brand;
        this.model = model;
        this.price = price;
    }
 
 
    @Override
    public String toString() {
        return"Brand='"+ brand + '\''+
                ", Model='"+ model + '\''+
                ", Price="+ price;
    }
}
```

### Rukovanje klasama

==Prvi korak== u iskorišćavanju mogućnosti refleksije u Javi jeste ==dolazak do reference na objekat koji se u svetu refleksije koristi da predstavi klase i interfejse==. ==Reč je o klasi Class==. Do objekta ove klase može se doći na sledeće načine:

- ==korišćenjem== odrednice ==class==;
- korišćenjem ==metode== ==getClass();==
- korišćenjem ==metode== ==forName()==.

==Ukoliko poznajemo naziv tipa čije osobine želimo da ispitamo, moguće je iskoristiti odrednicu class:==

```java
Class productClass = Product.class;
```

  
Ovo je ==najjednostavniji način kako bi se došlo do objekta koji u svetu refleksije predstavlja neku klasu==. D==o objekta klase Class došli smo korišćenjem odrednice class,== koja je iskorišćena nad nazivom tipa. Naime, Java virtuelna mašina automatski kreira objekte koji reprezentuju sve tipove koji postoje tokom izvršavanja programa. Na nama je samo da im pristupimo, baš kao u primeru.

Upravo ==prikazani pristup moguće je koristiti kada znamo naziv nekog tipa==. ==Ukoliko naziv nekog tipa ne znamo==, ali posedujemo njegov objekat, moguće je upotrebiti ==sledeći pristup:==

```java
Product product1 = newProduct("Logitech", "F710", 129.99);
Class productClass = product1.getClass();
```

  
Sada je ==prvo kreiran objekat klase Product==, a zatim je ==nad tako kreiranim== objektom upotrebljena ==metoda getClass()==, ==kako bi se došlo do objekta klase== Class.

Do objekta klase Class ==moguće je doći na još jedan način,== koji podrazumeva ==definisanje naziva klase u tekstualnom oblik==u:

```java
Class productClass = Class.forName("Product");
```

  
==Za dobijanje objekta klase Class== ==iskorišćena je njena statička metoda== ==forName().== Inače, klasa ==Class ne poseduje javno dostupan konstruktor i nije je moguće naslediti.== ==Metodi forName() prosleđuje se pun kvalifikovan naziv klase== (*fully-qualified class name*). U prikazanom primeru, klasa ==Product se nalazi unutar podrazumevanog paketa, te je stoga dovoljno navesti samo naziv klase.== Ukoliko je potrebno dobiti referencu na neku ==klasu koja se ne nalazi u podrazumevanom paketu, navode se i nazivi svih paketa unutar kojih se klasa nalazi:==

```java
Class stringClass = Class.forName("java.lang.String");
```

  
==Nakon dolaska do reference na objekat klase Class, moguće je dobiti neke osnovne informacije o klasi==. Metode za dobijanje nekih najznačajnijih informacija prikazane su tabelom 5.1.

| **Metoda** | **Opis** |
| --- | --- |
| getName() | vraća pun naziv klase, uključujući i nazive svih paketa u kojima se klasa nalazi |
| getSimpleName() | vraća uprošćen naziv klase, odnosno naziv bez paketa |
| getModifiers() | vraća numeričku vrednost koja određuje modifikatore koji su upotrebljeni prilikom deklarisanja klase |
| getPackage() | vraća objekat tipa Package koji predstavlja paket unutar koga se klasa nalazi |
| getSuperclass() | vraća objekat klase Class koji predstavlja roditeljsku klas |

  
*Tabela 5.1. Metode za dobijanje informacije o Java tipovima*

  
Upravo prikazane metode se mogu upotrebiti na sledeći način:

```java
Class stringClass = String.class;
String className = stringClass.getName();
String simpleClassName = stringClass.getSimpleName();
intmodifiers = stringClass.getModifiers();
Package classPackage = stringClass.getPackage();
Class superclass = stringClass.getSuperclass();
System.out.println(className);
System.out.println(simpleClassName);
System.out.println("Is private: "+ Modifier.isPrivate(modifiers));
System.out.println("Is public: "+ Modifier.isPublic(modifiers));
System.out.println("Is final: "+ Modifier.isFinal(modifiers));
System.out.println(classPackage.getName());
System.out.println(superclass.getName());
```

  
  

Prikazanim kodom obavljeno je ispitivanje ugrađene klase String. Na izlazu se dobija sledeći ispis:

java.lang.String  
String  
Is private: false  
Is public: true  
Is final: true  
java.lang  
java.lang.Object

  
Korišćenje svih prikazanih metoda vrlo je jednostavno. Jedina metoda za koju je potrebno dodatno pojašnjenje jeste metoda getModifiers(). Ona vraća vrednost int tipa, koja nije namenjena za krajnje korišćenje. Naime, tako dobijenu vrednost je neophodno proslediti nekoj od metoda klase Modifier, kako bi se utvrdilo njeno finalno značenje. Stoga su u primeru upotrebljene metode isPrivate(), isPublic() i isFinal() kako bi se utvrdilo da li je klasa String privatna, javna ili finalna, respektivno.  
  

### Rukovanje konstruktorima

Nakon dobijanja reference na objekat klase Class, kojim se neki tip predstavlja u svetu refleksije, moguće je doći do svih članova koji postoje unutar neke klase. Za početak će biti prikazano kako se mogu dobiti informacije o konstruktorima:

```java
Class productClass = Product.class;
 
Constructor[] constructors = productClass.getConstructors();
 
for(Constructor constructor :
                constructors) {
 
            System.out.println(constructor.getParameterCount());
        }
```

  
Kod ilustruje kompletan primer za dobijanje reference na konstruktore naše Product klase. Bitno je da primetite da se u svetu refleksije konstruktor predstavlja klasom Constructor. Referenca na sve konstruktore jedne klase dobija se pozivanjem metode getConstructors(). U primeru je, nakon dobijanja reference na sve konstruktore, obavljen prolazak kroz niz konstruktora i na izlazu je ispisan broj parametara koji svaki konstruktor poseduje. S obzirom na to da naša klasa Product poseduje tri konstruktora, na izlazu će biti ispisano sledeće:

2  
0  
3

  
Na sličan način je moguće dobiti i razne druge informacije o konstruktorima neke klase. Da bismo, na primer, dobili tipove ulaznih parametara konstruktora, dovoljno je napisati:

```java
Class productClass = Product.class;
 
Constructor[] constructors = productClass.getConstructors();
 
for(Constructor constructor :
        constructors) {
System.out.println(Arrays.toString(constructor.getParameterTypes()));
}
```

  
Na ovaj način se na izlazu dobija sledeće:

\[class java.lang.String, class java.lang.String\]

\[class java.lang.String, class java.lang.String, double\]

\[\]  

  
  

### Instanciranje klasa korišćenjem refleksije

Constructor klasa koju smo koristili u prethodnim redovima može se iskoristiti i za instanciranje neke klase koja sa ispituje korišćenjem refleksije:

```java
Class productClass = Product.class;
 
try{
    Constructor constructor = productClass.getConstructor(String.class, String.class, double.class);
    Product product = (Product) constructor.newInstance("Logitech", "F710", 129.99);
    System.out.println(product);
    } catch(NoSuchMethodException | IllegalAccessException | InstantiationException | InvocationTargetException e) {
    e.printStackTrace();
    }
```

  
U prikazanom primeru, prvo se dolazi do objekta klase Class kao i do sada. Takvim objektom se predstavlja klasa Product. Zatim je unutar try bloka napisan kod kojim se dolazi do reference na konstruktor sa tri parametra. Tako u prikazanom primeru možete videti još jedan način za dolazak do reference na konstruktore klase, ovoga puta pojedinačno, na osnovu tipova ulaznih parametara. Za dolazak do reference na konkretan konstruktor koristi se metoda getConstructor(), kojoj se prosleđuju reference na objekte kojima se predstavljaju tipovi ulaznih parametara.

Instanciranje neke klase korišćenjem refleksije obavlja se pozivanjem metode newInstance() nad referencom koja pokazuje na jedan konstruktor. Pri tom se metodi newInstance() prosleđuju vrednosti ulaznih parametara.

Metode getConstructor() i newInstance() mogu da proizvedu nekoliko različitih izuzetaka, ukoliko traženi konstruktor ne postoji ili kada se ne proslede parametri odgovarajućeg tipa. Upravo zbog toga je u primeru kompletan kod smešten unutar try bloka, dok se u catch bloku obrađuje nekoliko izuzetaka različitih tipova.

### Rukovanje poljima

Pristup poljima jedne klase moguće je obaviti korišćenjem metode getDeclaredFields(), baš kao u primeru koji sledi:

```java
Class productClass = Product.class;
Field[] fields =  productClass.getDeclaredFields();
for(Field field : fields) {
    System.out.println(field.getName());
}
```

  
  

Metoda getDeclaredFields() omogućava dobijanje reference na sva polja koja se nalaze unutar neke klase, bez obzira na identifikator pristupa koji postoji na polju. Stoga prikazani kod u našem primeru proizvodi sledeći ispis:

brand  
model  
price

  
Kada je potrebno dobiti referencu samo na polja koja su javna, moguće je koristiti metodu getFields(). U našem primeru, ona će kao svoju povratnu vrednost emitovati prazan niz, s obzirom na to da unutar klase Product ne postoje polja koja nisu javna.

Ukoliko želimo da dobijemo samo jedno polje iz neke klase, moguće je iskoristiti metodu getField(), kojoj je potrebno proslediti naziv polja:

```java
try{
    Field field1 = productClass.getField("brand");
} catch(NoSuchFieldException e) {
    e.printStackTrace();
}
```

  
S obzirom na to da se može dogoditi da traženo polje ne postoji, metodu getField() je uvek neophodno pozivati unutar try bloka, baš kao u primeru.

Sve upravo prikazane metode emituju jedan ili više objekata tipa Field. Drugim rečima, Field je klasa kojom se reprezentuju polja klase.

### Čitanje i promena vrednosti svojstava

Kada se dođe do reference na neko od svojstava klase, korišćenjem refleksije je moguće čitati ili menjati njihove vrednosti. Sledeći primer će ilustrovati pristup za čitanje naziva svojstava i njihovih imena iz jednog objekta:

```java
Product product1 = newProduct("Logitech", "F710", 129.99);
 
Class productClass = Product.class;
 
Field[] fields =  productClass.getDeclaredFields();
 
for(Field field : fields) {
    try{
        field.setAccessible(true);
        System.out.println(field.getName() + ": "+ field.get(product1));
    } catch(IllegalAccessException e) {
    e.printStackTrace();
    }
}
```

  
Primer ilustruje pristup za čitanje svih svojstava jednog objekta, uključujući njihove nazive i vrednosti. U primeru smo prvo došli do referenci na sva svojstva unutar klase Product, a zatim je unutar jedne for petlje obavljen ispis naziva svojstava i njihovih vrednosti unutar objekta čija je referenca smeštena unutar promenljive product1. Kao rezultat se na kraju dobija:

brand: Logitech  
model: F710  
price: 129.99

  
Iz primera se može zaključiti da se čitanje vrednosti nekog svojstva korišćenjem refleksije obavlja korišćenjem metode get(), koja se poziva nad objektom Field klase. Njoj se prosleđuje referenca na konkretan objekat čije vrednosti svojstava želimo da pročitamo.

Metoda get() klase Field omogućava čitanje vrednosti samo onih svojstava kojima je iz tekućeg konteksta moguće pristupiti. Upravo zbog toga je u primeru pre korišćenja metode get() iskorišćena još jedna metoda – setAccessible(). Kada se ovoj metodi prosledi vrednost true, omogućava se pristup čak i privatnim poljima, kojima se inače ne može pristupiti.

Za izmenu vrednosti svojstava nekog objekta koristi se metoda set(). Evo kako može izgledati jedan primer postavljanja vrednosti svojstava korišćenjem refleksije:

```java
Product product1 = newProduct();
 
Class productClass = Product.class;
 
Field[] fields = productClass.getDeclaredFields();
 
for(Field field : fields) {
 
    field.setAccessible(true);
 
    if(field.getType() == String.class) {
        if(field.getName().equals("brand")) {
            field.set(product1, "Logitech");
        } elseif(field.getName().equals("model")) {
            field.set(product1, "F710");
        }
     } elseif(field.getType() == double.class) {
            field.set(product1, 129.99);
     }
}
 
System.out.println(product1);
```

  
Na početku primera obavlja se kreiranje jednog Product objekta, korišćenjem konstruktora bez parametara. Na taj način se dobija objekat koji ima podrazumevane vrednosti svojstava koja nisu eksplicitno postavljena. Zatim se, kao i u prethodnim primerima, prolazi kroz niz svojstava klase Product. Kroz niz dobijenih svojstava se prolazi jednom for petljom. Svakom svojstvu se omogućava pristup pozivanjem metode setAccessible(), kojoj se prosleđuje vrednost true. Nakon toga je napravljena jedna uslovna konstrukcija u kojoj se prvo utvrđuje tip svojstva. Ukoliko je svojstvo tipa String, proverava se njegov naziv, zato što klasa Product poseduje dva String svojstva.

| **Napomena**  Upravo prikazani primer podrazumeva da je main() metoda obeležena throws IllegalAccessException oznakom, kako bi se izbeglo definisanje blokova za obradu eventualnih izuzetaka i primer učinio jednostavnijim. |
| --- |

### Rukovanje metodama

U svetu refleksije, metode se predstavljaju korišćenjem klase Method. Evo kako se može doći do svih metoda koje se nalaze unutar naše klase Product:

```java
Class productClass = Product.class;
Method[] methods = productClass.getMethods();
for(Method method : methods) {
    System.out.println(method.getName());
}
```

  
  

Prikazanim kodom dolazi se do svih metoda klase Product, korišćenjem metode getMethods(). Zatim se unutar jedne for petlje ispisuje naziv svake metode. Ispis koji se dobija nakon izvršavanja prikazanog koda je sledeći:

toString  
getModel  
setPrice  
getBrand  
getPrice  
setModel  
setBrand  
wait  
wait  
wait  
equals  
hashCode  
getClass  
notify  
notifyAll

  
U ovom trenutku se možete zapitati odakle ovoliki broj metoda unutar naše klase Product. Ukoliko se sećate priče o nasleđivanju, neće biti teško da zaključite odakle dolazi određeni broj metoda čiji su nazivi ispisani. Tako su npr. wait(), equals(), hashCode(), getClass(), notify() i notifyAll() metode koje je klasa Product nasledila iz klase Object. Preostale metode su one koje su deklarisane direktno unutar klase Product.

Ukoliko je potrebno doći samo do metoda koje su deklarisane unutar Product klase, umesto metode getMethods() koristi se metoda getDeclaredMethods():

```java
Class productClass = Product.class;
 
Method[] methods = productClass.getDeclaredMethods();
    for(Method method : methods) {
        System.out.println(method.getName());
}
```

  
Primer je identičan prethodnom. Jedina razlika je u upotrebi metode getDeclaredMethods(). Stoga se na izlazu dobijaju samo metode klase Product:

toString  
getBrand  
setBrand  
setModel  
getModel  
setPrice  
getPrice

  
Referenca na pojedinačnu metodu se može dobiti na sledeći način:

Method method = productClass.getMethod("toString");

Na ovaj način se dobija referenca na metodu po nazivu – toString(). Metoda toString() je bez parametara, a ukoliko je potrebno dobiti referencu koja prihvata neki ulazni parametar, koristi se sledeći pristup:

Method method = productClass.getMethod("setBrand", String.class);  

### Pozivanje metoda

Kada se dobije referenca na neku metodu, refleksija omogućava da se takva metoda i pozove. Prvo će biti prikazano kako se poziva metoda toString(), odnosno metoda bez ulaznih parametara:

```java
Product product1 = newProduct("Logitech", "F710", 129.99);
 
Class productClass = Product.class;
Method method = productClass.getMethod("toString");
String returnValue = (String) method.invoke(product1);
 
System.out.println(returnValue);
```

  
U primeru je prvo obavljeno kreiranje novog objekta Product klase. Takav objekat u nastavku služi kako bi se nad njim obavio poziv metode korišćenjem refleksije. Prvo se dolazi do reference na metodu sa nazivom toString(), a zatim se korišćenjem metode invoke() takva metoda i poziva. Prilikom pozivanja njoj se prosleđuje objekat, s obzirom ne to da je metoda toString() objektni član. Povratna vrednost metode toString() hvata se unutar jedne String promenljive i na kraju ispisuje i na izlazu.

| **Napomena**  Metode getMethod() i invoke() mogu da stvore nekoliko različitih izuzetaka - NoSuchMethodException, SecurityException, InvocationTargetException, IllegalAccessException. Njih je neophodno obraditi korišćenjem try i catch blokova ili unutar potpisa metode dodati throws oznaku i nakon nje spomenute izuzetke. |
| --- |

Pozivanje metode koja poseduje ulazni parametar može da izgleda ovako:

```java
Product product1 = newProduct("Logitech", "F710", 129.99);
 
Class productClass = Product.class;
Method method = productClass.getMethod("setBrand", String.class);
method.invoke(product1, "HP");
 
System.out.println(product1);
```

  
Primer je vrlo sličan prethodnom. Unutar njega dolazi se do reference na metodu setBrand(). To je jedna od *set* metoda, odnosno metoda za postavljanje vrednosti privatnih polja. Upravo zbog toga, ona prihvata jedan ulazni parametar String tipa. To je i razlog zbog koga se metodi invoke() ovoga puta, pored reference na objekat, prosleđuje i vrednost ulaznog parametra. Da je na ovaj način vrednost svojstva make zaista i promenjena, dokazuje poslednja naredba u primeru, koja na izlaz ispisuje sledeće:

Brand='HP', Model='F710', Price=129.99  

### Vežba

Data je sledeća klasa:

```java
publicclassMyClass {
 
    publicvoidsayHelloWorld(){
        System.out.println("Hello World");
    }
 
    publicvoidsayHello(String name){
        System.out.println("Hello "+ name);
    }
}
```

  
Potrebno je napisati kod koji će korišćenjem refleksije da ispita osobine klase MyClass. Metode unutar klase MyClass je potrebno pozvati i ispisati njihove povratne vrednost.

**Rešenje**

```java
importjava.lang.reflect.InvocationTargetException;
importjava.lang.reflect.Method;
importjava.lang.reflect.Parameter;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) throwsInvocationTargetException, IllegalAccessException, ClassNotFoundException {
 
        Class c = Class.forName("MyClass");
        MyClass mc = newMyClass();
 
        String stringArgument = "John";
 
        Method[] methods = c.getDeclaredMethods();
 
        for(Method method : methods) {
            System.out.println("Invoking of method: "+ method.getName());
 
            if(method.getParameterCount() > 0) {
                Parameter[] param = method.getParameters();
                if(param.length == 1) {
                    if(param[0].getType() == String.class) {
                        method.invoke(mc, stringArgument);
                    }
                }
            } else{
                method.invoke(mc);
            }
        }
    }
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Advanced_Java_Programming/multimedijaFinal/ADJAVA1_05.thb) ADJAVA1\_05.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "ADJAVA1_05.Mp4")

Kako Vam mogu pomoći?