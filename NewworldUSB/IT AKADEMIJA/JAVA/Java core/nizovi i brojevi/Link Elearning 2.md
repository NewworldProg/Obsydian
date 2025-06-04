---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=fad91bd38285ec05615170e3a6aa0ed2_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434685"
author:
published:
created: 2025-05-08
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 18 od 22

## Nizovi

U jednoj od prethodnih lekcija naučili smo kako se barata promenljivama. Iako se vrednosti promenljivih mogu menjati, one u jednom trenutku mogu imati samo jednu vrednost. Na primer:

```java
String cars = "Honda";
```

  
Ovo je jedna String promenljiva koja čuva vrednost koja predstavlja jednog proizvođača automobila. Ipak, šta ukoliko bismo unutar promenljive cars poželeli da sačuvano imena još nekih proizvođača automobila? Za obavljanje takvog posla bili bi nam potrebni nizovi. Pojmu nizova biće posvećena lekcija pred vama.  
  

### Šta su nizovi?

Osnovni sastojak gotovo svih programskih jezika su nizovi. Nizovi omogućavaju da se unutar jedne promenljive smesti veći broj vrednosti. Kako biste ovu rečenicu bolje razumeli, evo kako izgleda struktura jednog Java niza (slika 18.1).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_01.png)*

*Slika 18.1. Struktura niza u Java jeziku  
  
*

Plavi kvadrati oslikavaju različite vrednosti koje postoje unutar jednog niza. Može se videti da ih ukupno ima devet. Svaka vrednost unutar niza se drugačija naziva **element niza**. Svaki element niza poseduje svoju poziciju, koja se izražava korišćenjem **indeksa**. Brojanje indeksa nizova započinje od nule, pa tako prvi element niza ima indeks 0, a peti element niza indeks 4.

Unutar jednog Java niza moguće je smeštati podatke istog tipa. Tako se unutar jednog niza može naći skup brojeva, unutar drugog skup tekstualnih podataka, a unutar trećeg niza skup logičkih vrednosti.

U nastavku lekcije naučićemo kako se kreiraju nizovi i kako se rukuje njihovim vrednostima.  
  

### Deklarisanje niza

Kreiranje niza u Java jeziku započinje njegovom deklaracijom. Deklaracija niza je zapravo deklaracija promenljive, preko koje će vrednosti niza biti dostupne u programu. Evo kako može da izgleda deklaracija jednog niza:

```java
int[] array;
```

  
Baš kao i prilikom deklaracije *regularnih* promenljivih, deklaracija niza se sastoji iz dva dela:

- definisanja tipa niza;
- definisanja naziva niza.

U upravo prikazanom primeru tip niza je **int\[\]**, što znači da kreiramo niz celobrojnih vrednosti tipa **int**. Uglaste zagrade predstavljaju specijalne karaktere koji govore da će ova promenljiva moći da prihvati niz vrednosti, a ne samo jednu int vrednost.

Drugi deo ove deklaracije predstavlja naziv niza i on je u našem slučaju array.

Kao i kod promenljivih drugih tipova, deklarisanjem se ne kreira automatski i sam niz. Deklaracija govori kompajleru da će kreirana promenljiva sadržati vrednost niza naznačenog tipa.  
  

### Kreiranje niza

Kreiranje niza obavlja se korišćenjem ključne reči **new**:

```java
int[] array = newint[5];
```

  
Ovakvom naredbom kreira se jedan niz celobrojnih vrednosti koji će [alocirati](https://www.link-elearning.com/linkdl/opisPojma.php?id=160488 "alocirati")  memoriju potrebnu za smeštanje pet celobrojnih vrednosti tipa int. Drugim rečima, nakon ove naredbe promenljiva x imaće referencu na niz sa pet elemenata od kojih će svaki predstavljati prostor za jednu celobrojnu vrednost.

| **Nizovi u Javi imaju fiksnu veličinu**  Odmah je potrebno primetiti jednu vrlo važnu osobinu nizova u Java jeziku. Njihova veličina se mora unapred utvrditi, odnosno, prilikom kreiranja je neophodno navesti njihovu veličinu. To je učinjeno i u prikazanoj naredbi, gde broj 5 unutar uglastih zagrada predstavlja broj elemenata koje će niz imati. Nakon kreiranja niza u Java jeziku, veličinu niza **nije** moguće menjati. |
| --- |

| **Nizovi su objekti**  U programskom jeziku Java, nizovi su objekti. To možete videti i na osnovu upotrebe ključne reči new koja se koristi za njihovo kreiranje. U pozadini, za svaki tip niza, Java jezik poseduje odgovarajuću klasu koju koristi prilikom kreiranja niza. |
| --- |

Nakon izvršavanja upravo prikazane naredbe za kreiranje niza, svi njegovi članovi će biti automatski inicijalizovani i imaće podrazumevane vrednosti 0.

Koje zagrade se upotrebljavaju prilikom deklarisanja niza?

  

### Ispis vrednosti niza i klasa Arrays

Kako bismo se uverili da je ovo što smo upravo rekli tačno, odnosno da kreirani niz poseduje pet članova čije vrednosti su trenutno podrazumevane, u narednim redovima ćemo obaviti ispisivanje elemenata niza na izlazu. Za obavljanje takvog posla, iskoristićemo jednu ugrađenu klasu Java platforme. Reč je o klasi Arrays.

Klasa Arrays poseduje skup različitih funkcionalnosti koje su dostupne za manipulaciju nizovima. Jedna od takvih funkcionalnosti jeste i ona koja omogućava da se svi elementi niza objedine unutar jedne String vrednosti:

```java
int[] array = newint[5];
System.out.println(Arrays.toString(array));
```

  
Kao što možete videti, klasa Arrays i njena statička metoda toString omogućavaju nam da dobijemo sve elemente niza, objedinjene u jednu String vrednost, koju možemo da ispišemo na izlazu:

\[0, 0, 0, 0, 0\]

Izlaz koji se dobija potvrđuje ono što je rečeno nešto ranije – niz koji smo kreirali ima pet članova i svaki od njih je inicijalizovan na podrazumevanu vrednost 0.

| **Napomena**  Korišćenje klase Arrays zahteva da se ona prethodno uveze, pa je na početak dokumenta potrebno dodati sledeću naredbu:  ```java importjava.util.Arrays; ``` |
| --- |

### Dodela vrednosti članovima niza

U prethodnim redovima ste mogli da vidite da odmah nakon kreiranja niza njegovi članovi dobijaju podrazumevane vrednosti, koje naravno zavise od njihovog tipa. Kod numeričkih tipova, podrazumevane vrednosti su 0 ili 0.0, kod logičkih false, a kod referentnih tipova null.

Da bismo samostalno definisali vrednosti članova niza, neophodno je uraditi nešto ovako:

array\[0\] = 23;

Na ovaj način je obavljeno postavljanje vrednosti prvog elementa niza. Već je rečeno da se elementi nizova numerišu korišćenjem indeksa, a u prikazanoj naredbi je iskorišćen upravo indeks kako bi se pristupilo elementu niza. S obzirom na to da je unutar uglastih zagrada navedena vrednost 0, obavlja se pristup prvom elementu niza.

Nakon ovakve naredbe možemo da proverimo da li je vrednost prvog elementa našeg niza zaista promenjena:

```java
int[] array = newint[5];
array[0] = 23;
System.out.println(Arrays.toString(array));
```

  
Kod će proizvesti ovakav efekat:

\[23, 0, 0, 0, 0\]

Na osnovu dobijenog ispisa, možemo da vidimo da je vrednost prvog člana niza uistinu promenjena.

Članovi niza se ponašaju kao i bilo koje druge promenljive, pa je tako njihovu vrednost moguće menjati proizvoljan broj puta, koristiti unutar izraza, obrađivati operatorima i slično.  
  

### Čitanje vrednosti elemenata niza

Na identičan način je moguće obaviti i čitanje vrednosti pojedinačnih elemenata niza. Opet je potrebno iskoristiti naziv niza i u uglastim zagradama navesti indeks elementa čiju vrednost želimo da dobijemo:

```java
int[] array = newint[5];
array[0] = 23;
System.out.println(array[0]);
```

  
U ovom primeru, na izlazu se ne ispisuju svi elementi niza, već samo onaj koji ima indeks 0. Drugim rečima, na izlazu se dobija vrednost prvog člana niza:

23  
  

### Objedinjena deklaracija i inicijalizacija

Niz je u Javi moguće deklarisati i inicijalizovati u jednoj naredbi, ukoliko unapred znamo vrednosti njegovih elemenata:

```java
int[] array = newint[]{3, 5, 2, 6, 1, 6};
```

  
Odmah nakon kreiranja niza, sada su navedene vitičaste zagrade i unutar njih vrednosti elemenata niza.

Prilikom objedinjene deklaracije i inicijalizacije, moguće je otići i korak dalje i potpuno izostaviti logiku za kreiranje novog objekta:

```java
int[] array = {3, 5, 2, 6, 1, 6};
```

  
U programskom jeziku Java, ovo je najkompaktniji način za kreiranje nizova, pod uslovom da unapred znamo elemente koje je niz potrebno da ima.  
  

### Nizovi u Javi prihvataju elemente samo jednog tipa

Niz može da prihvati isključivo vrednosti istog tipa. To znači da nije moguće napraviti niz celobrojnih vrednosti u kome će se naći i vrednost sa pokretnim zarezom (double ili float).

```java
intintegerArray[] = {3, 6.5, 2, 6, 1, 6};
```

  
Pokušaj inicijalizacije niza ovakvim vrednostima stvoriće efekat kao na slici 18.2.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_02.png)*

*Slika 18.2. Niz tipa int ne može imati vrednost tipa double  
  
*

Razvojno okruženje jasno markira vrednost drugog člana niza, koja ima tip double i obaveštava nas da svi članovi moraju biti tipa int.

Ipak, u Java jeziku postoji način da se i ovako nešto prevaziđe:

```java
Object[] myArray = {3, 6.5, 2, 6, 1, 6};
```

  
Napravljena je samo jedna mala intervencija na već prikazanoj naredbi i greške više nema. Naime, tip članova niza je iz int promenjen u Object. Object je u Javi osnovni tip, odnosno tip na kome se baziraju svi ostali tipovi, pa je ovako nešto potpuno legitimno. Drugim rečima, s obzirom na to da je osnova svih tipova, Object se može koristiti za predstavljanje bilo kojih vrednosti u Javi. Tako možemo da odemo i korak dalje, pa da napišemo ovako nešto:

```java
Object[] myArray = {3, 6.5, 2, 6, 1, 6, "Hello"};
```

  
Sada je na kraj niza postavljen još jedan element koji je tipa String. To praktično znači da u ovom trenutku naš niz poseduje vrednosti tri različita tipa. Zapravo, ukoliko želimo da budemo u potpunosti precizni, svi elementi upravo prikazanog niza imaju isti tip – Object. Pre nego što se upišu u niz, vrednosti koje vidite su različitog tipa. Ali, prilikom upisivanja u niz, okruženje obavlja njihovo prevođenje u Object tip, tako da unutar niza svi članovi poseduju identičan tip. Prilikom čitanja vrednosti iz niza, obavlja se obrnut postupak, odnosno, vrednosti iz Object tipa konvertuju se nazad u svoj izvorni tip. Takve konverzije se drugačije nazivaju *boxing* i *unboxing* i obavljaju se automatski od strane Java okruženja.  
  

### Utvrđivanje dužine niza

Dužina niza se veoma lako može dobiti svojstvom **length**:

```java
int[] array = {3, 5, 2, 6, 1, 6};
System.out.println(array.length);
```

  
Prikazani kod proizvodi rezultat: 6. To znači da niz array poseduje šest članova.

| **Indeks i broj elemenata**  Potrebno je obratiti pažnju na to da indeks niza nije isto što i broj elemenata niza, što često ume da zbuni. U ovom slučaju, broj elemenata niza (length) je šest, iako je poslednji indeks niza zapravo 5, a sve zbog računanja indeksa nizova od nule. |
| --- |

U upravo prikazanom primeru možete videti još jedan detalj koji potvrđuje da su nizovi u Javi objekti. Naime, nad promenljivom koja čuva referencu na niz pristupa se svojstvu length, što nesumnjivo potvrđuje da je reč o objektu. Prosti tipovi ne mogu imati svojstva.  
  

### Prolazak kroz niz

Kada se govori o nizovima u programiranju, veoma često se može čuti fraza *prolazak kroz niz*. Reč je zapravo o operaciji koja podrazumeva sukcesivno čitanje svakog elementa pojedinačno, i to uglavnom redom.

Prolazak kroz niz se najčešće obavlja kada je potrebno:

- sprovesti određene intervencije nad svakim od elemenata niza;
- pojedinačno ispisati svaki od elemenata jednog niza.

Osnovni pristup za postizanje prolaska kroz niz jeste upotreba for petlje, koja je obrađena u jednom od prethodnih modula. Evo kako može izgledati primer prolaska kroz niz korišćenjem for petlje:

```java
int[] array = {3, 5, 2, 6, 1, 6};
for(inti = 0; i < array.length; i++) {
    System.out.println(array[i]);
}
```

  
U prikazanom primeru, for petlja je iskorišćena za ispis vrednosti svakog elementa niza, pa se na izlazu dobija ovakav ispis:

3  
5  
2  
6  
1  
6  
  

Pored for petlje, Java jezik poseduje još jednu petlju, koja je specijalno namenjena za prolazak kroz nizove. Reč je o petlji koja se naziva *unapređeni for* (*enhanced for*):

```java
int[] array = {3, 5, 2, 6, 1, 6};
 
for(intvalue : array) {
      System.out.println(value);
}
```

*  
Unapređeni for* poseduje sintaksu ilustrovanu slikom 18.3.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_03.png)*

*Slika 18.3. Sintaksa unapređene for petlje  
  
*

S obzirom na to da je specijalno namenjen za prolazak kroz nizove, *unapređeni for* ne poseduje delove za deklarisanje brojača, definisanje uslova i naredbu koja se izvršava nakon svake iteracije. Umesto takvih delova koji karakterišu standardnu for petlju, *unapređeni for* unutar zagrada poseduje samo dva dela:

- deklaraciju promenljive koja će u svakoj iteraciji da dobija vrednost narednog elementa niza (u primeru je to int value); naziv promenljive je moguće samostalno definisati, dok tip zavisi od tipa elemenata niza;
- referencu na niz (u primeru je to array, što je naziv promenljive koja čuva referencu na niz kroz koji je potrebno proći).

Dva upravo opisana segmenta unapređene for petlje odvajaju se karakterom dve tačke.

*Unapređeni for* se često drugačije naziva i **for each**.

U nastavku ove lekcije biće prikazane još tri veoma značajne operacije koje se mogu sprovoditi nad nizovima:

- kopiranje
- sortiranje
- pretraga

Sve ove operacije je moguće sprovesti ručno, prolaskom kroz niz korišćenjem petlji i sprovođenjem odgovarajuće logike u zavisnosti od namene. Ipak, navedene operacije je moguće sprovoditi i upotrebom ugrađenih funkcionalnosti Java platforme, što će biti ilustrovano u nastavku.  
  

### Kopiranje niza

Već je rečeno da nakon kreiranja niza njegovu veličinu nije moguće menjati. To praktično znači da nizu nakon kreiranja nije moguće dodeliti nove članove. Ukoliko se takva potreba ipak javi, rešenje može da predstavlja kreiranje novog niza koji bi imao sve elemente starog i nekoliko novih elemenata koje želimo da dodamo. Upravo jedan takav primer će biti prikazan u nastavku. U primeru će biti obavljeno spajanje dva niza u jedan nov niz:

```java
int[] array = {3, 5, 2, 6, 1, 6};
int[] array1 = {12, 13, 14};
int[] destArray = newint[array.length + array1.length];
System.arraycopy(array, 0, destArray, 0, array.length);
System.arraycopy(array1, 0, destArray, array.length, array1.length);
System.out.println("Array length is: "+ destArray.length);
System.out.println("Elements are: ");
System.out.println(Arrays.toString(destArray));
```

  
Primer započinje deklaracijom i inicijalizacijom dva niza – array i array1. Zatim se obavlja kreiranje još jednog, trećeg niza (destArray), čija se veličina postavlja na zbir prva dva niza. Reč je o nizu unutar koga će biti objedinjeni svi elementi prva dva niza, pa se upravo zbog toga njegova dužina postavlja na zbir prva dva niza.

Kako bi se novi niz (destArray) popunio vrednostima koje se nalaze u prva dva niza, koristi se jedna ugrađena metoda Java platforme – arraycopy.

| **Metoda arraycopy**  arraycopy je statička metoda klase System, koja se može koristiti za kopiranje vrednosti iz jednog niza u neki drugi. Reč je o metodi koja poseduje ovakav potpis:  ```java publicstaticvoidarraycopy(Object src, intsrcPos, Object dest, intdestPos, intlength) ```     Metoda arraycopy prihvata pet parametara:  - Object src – izvorišni niz; - int srcPos – početni indeks izvorišnog niza; - Object dest – odredišni niz; - int destPos – početni indeks u odredišnom nizu, gde će početi smeštanje elemenata iz izvorišnog niza; - int length – broj članova koji će biti kopirani. |
| --- |

U prikazanom kodu, metoda arraycopy koristi se dva puta, odnosno po jednom za kopiranje svakog od početnih nizova u odredišni destArray niz. Na kraju se može reći da se na ovaj način obavlja neka vrsta sabiranja, odnosno nadovezivanja nizova.

### Sortiranje niza

Sortiranje je još jedna od veoma čestih operacija koje se sprovode nad nizovima. U nastavku će biti prikazan primer sortiranja sledećeg niza:

```java
int[] array = {3, 5, 2, 6, 1, 6};
```

  
Sortiranje ovog niza može se obaviti na sledeći način:

```java
int[] array = {3, 5, 2, 6, 1, 6};
Arrays.sort(array);
System.out.println(Arrays.toString(array));
```

  
Nakon izvršavanja prikazanog koda, na izlazu se dobija:

\[1, 2, 3, 5, 6, 6\]  
  

Za obavljanje sortiranja u prikazanom primeru se koristi metoda sort ugrađene klase Arrays.

### Pretraga niza

U okviru ugrađene klase Arrays postoji i metoda za pretragu nizova. Reč je o metodi koja pretražuje određeni niz u potrazi za definisanim elementom. Evo kako izgleda primer pretrage niza:

```java
int[] a = {5, 1, 3, 4, 2};
Arrays.sort(a);
 
System.out.println(Arrays.binarySearch(a, 2));
System.out.println(Arrays.binarySearch(a, 10));
```

  
Prvo je bitno da primetite da se nakon deklaracije i inicijalizacije niza obavlja njegovo sortiranje, korišćenjem već prikazane metode sort. Jednostavno, metoda za pretragu koja je iskorišćena u nastavku zahteva da niz bude sortiran pre nego što se obavi pretraga. Za obavljanje pretrage, u prikazanom primeru se koristi metoda binarySearch.

| **Metoda binarySearch**  Metoda binarySearch nalazi se unutar klase Arrays. Reč je o statičkoj metodi, koja poseduje sledeći potpis:  ```java publicstaticintbinarySearch(int[] a, intkey) ```     Metoda binarySearch prihvata dva parametra:  - prvi parametar se odnosi na niz koji je potrebno pretražiti; nije neophodno da to bude niz čiji su članovi int tipa – metoda binarySearch može da pretraži nizove bilo kog tipa; - drugi parametar predstavlja ključ pretrage, odnosno vrednost koju je potrebno potražiti unutar niza.  Ukoliko metoda binarySearch unutar niza pronađe traženu vrednost, kao svoj rezultat ona isporučuje poziciju (indeks) na kojoj se nalazi tražena vrednost. Ukoliko vrednost ne postoji unutar niza, isporučuje se negativna vrednost. Takva povratna vrednost se dobija kada se dužina niza, uvećana za jedan, pretvori u negativan broj. |
| --- |

Nakon upoznavanja sintakse metode binarySearch, moći ćemo da razumemo povratne vrednosti koje dobijamo:

1  
\-6  
  

Vrednost 1 znači da prva tražena vrednost (2) postoji unutar niza i da ima indeks 1. Vrednost \-6 znači da druga tražena vrednost (10) ne postoji unutar niza. Na izlazu se dobija -6 zato što je 6 dužina koju bi niz imao da unutar njega postoji i traženi element. Pretvaranjem takvog broja u negativni broj, dobija se \-6.

### Višedimenzionalni nizovi

Nizovi u Java jeziku nisu ograničeni samo na proste tipove, već je unutar njih moguće smestiti i referentne, odnosno složene vrednosti. To sve na kraju znači da je unutar jednog niza moguće smestiti više drugih nizova. U takvoj situaciji se dobijaju nizovi sa više dimenzija (slika 18.4).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_04.png)*

*Slika 18.4. Višedimenzionalni niz  
  
*

Na slici 18.4. je prikazana struktura jednog višedimenzionalnog niza sa četiri elementa. Pri tome je svaki od elemenata zaseban niz (svi oni su predstavljeni plavom bojom). Tako se, na primer, može reći da je prvi element niza, na poziciji 0, zapravo još jedan niz. S obzirom na to da su i sami elementi nizovi, i oni poseduju svoje indekse (slika 18.5).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_05.png)*

*Slika 18.5. Višedimenzionalni niz (2)  
  
*

Sada su pored indeksa glavnog niza prikazani i indeksi pojedinačnih elemenata. Na taj način, četvrti element drugog elementa glavnog niza jednoznačno je određen indeksima \[1, 3\].

Ovakvi višedimenzionalni nizovi sačinjeni su iz dve dimenzije, pa se zbog toga drugačije nazivaju dvodimenzionalni nizovi. Ipak, višedimenzionalni nizovi mogu imati proizvoljan broj dimenzija (dve, tri, četiri...).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_18_06.png)*

*Slika 18.6. Trodimenzionalni niz  
  
*

Na slici 18.6. prikazan je jedan višedimenzionalni niz sa tri dimenzije. On ima tri elementa (0, 1 i 2), od kojih je svaki po jedan dvodimenzionalni niz.

Kreiranje višedimenzionalnih nizova veoma je lako i ne zahteva korišćenje bilo kakve specijalne sintakse. U nastavku će biti prikazano nekoliko takvih primera:

```java
int[][] matrix
        = {
         {1, 2, 3, 4},
         {5, 6, 7, 8},
         {9, 10, 11, 12}
         };
```

  
Ovo je primer jednog dvodimenzionalnog niza. Kako bi Java izvršno okruženje znalo da je reč o nizu sa dve dimenzije, nakon tipa niza, postavljaju se dva para uglastih zagrada – **\[\]\[\]**.

Kako bi se pristupilo elementu jednog ovakvog niza, koristi se sledeći pristup:

```java
System.out.println(matrix[0][0]);
```

  
Rezultat ovakve naredbe će biti vrednost 1, pošto je u zagradama navedeno da želimo da pristupimo prvom elementu prvog podniza (\[0\]\[0\]).

Ukoliko bismo želeli da pristupimo trećem elementu drugog podniza, dovoljno bi bilo napisati:

```java
System.out.println(matrix[1][2]);
```

| **Odvojena deklaracija i inicijalizacija višedimenzionalnih nizova**  U upravo prikazanom primeru, niz je odmah inicijalizovan vrednostima, koje su navedene unutar vitičastih zagrada. Višedimenzionalni niz se može kreirati i bez inicijalizacije:  ```java int[][] arr = newint[3][4];         arr[0][0] = 1;         arr[0][1] = 2;         arr[1][0] = 3;         arr[1][1] = 4;         System.out.println(arr[0][1]); ``` |
| --- |

Kao što je nešto ranije rečeno, višedimenzionalni nizovi nisu ograničeni na dve dimenzije. To znači da je vrlo lako moguće uvesti novu dimenziju:

```java
int[][][] matrix =
                {
                        {
                                {1, 2, 3, 4},
                                {5, 6, 7, 8},
                                {9, 10, 11, 12},
                                {13, 14, 15, 16}
                        },
                        {
                                {17, 18, 19, 20},
                                {21, 22, 23, 24},
                                {25, 26, 27, 28},
                                {29, 30, 31, 32}
                        }
                };
```

  
Ovo je sada niz sa tri dimenzije, koji ima dva člana. To su zapravo dva dvodimenzionalna niza. Svaki dvodimenzionalni niz poseduje po četiri pojedinačna jednodimenzionalna niza.

Na kraju, prilikom kreiranja višedimenzionalnih nizova, broj dimenzija se ne mora zaustaviti na tri. Moguće je napraviti i nizove sa četiri i više dimenzija. Ipak, ovakvi nizovi su teški za razumevanje, a njihova upotreba retka.  
  

### Vežbe

**  
Vežba 1**

Potrebno je napraviti program koji će utvrđivati da li definisana vrednost postoji u nekom nizu. Program je potrebno napisati bez upotrebe metode binarySearch koja je ilustrovana u ovoj lekciji. Niz koji je potrebno pretražiti izgleda ovako:

int\[\] array = {1, 5, 33, 563, 0, 2, 23, 9, 9, 11, 987, 23, 934, 999, 43};

**  
Vežba 2**

Potrebno je napraviti program koji sabira dve matrice. Prva matrica ima vrednost:

1 2 3  
5 6 7  
9 0 1  
  

Druga matrica ima vrednost:

4 1 6  
2 3 5  
7 4 3  
  

Ipak, rešenje je moguće i značajno optimizovati i to korišćenjem petlji, pa se veliki broj naredbi za sabiranje može zameniti sledećom logikom:

```html
int[][] matrix1 = {{1, 2, 3}, {5, 6, 7}, {9, 0, 1}};
int[][] matrix2 = {{4, 1, 6}, {2, 3, 5}, {7, 4, 3}};
int[][] matrix3 = new int[3][3];
 
 
for (int i = 0; i < matrix1.length; i++) {
    for (int j = 0; j < matrix2.length; j++) {
        matrix3[i][j] = matrix1[i][j] + matrix2[i][j];
    }
}
```

**  
Vežba 3**

Dat je niz brojeva:

```java
int[] arr = {1,2,3,4,5,6,7,8,9,10};
```

  
Potrebno je izlistati dati niz putem while petlje.

**  
Vežba 4**

Modifikovati kod iz prethodnog zadatka tako da se izvrši korišćenjem do-while petlje.  
  

### Rešenja

**Vežba 1**

```java
publicclassJavaProgram {
    publicstaticvoidmain(String[] args) {
 
        int[] array = {1, 5, 33, 563, 0, 2, 23, 9, 9, 11, 987, 23, 934, 999, 43};
 
        System.out.println(searchArray(array, 12));
        System.out.println(searchArray(array, 999));
 
    }
 
    privatestaticbooleansearchArray(int[] array, intkey) {
 
        for(intvalue : array) {
            if(value == key)
                returntrue;
        }
 
        returnfalse;
    }
}
```

  
**Vežba 2**

Matrice se sabiraju tako što se svaki član jedne matrice sabira sa članom druge matrice na istoj poziciji.

Znači:

1 + 4 2 + 1 3 + 6

5 + 2 6 + 3 7 + 5

9 + 7 0 + 4 1 + 3

  
Kada se ovaj princip implementira u Javi, izgleda ovako:

```java
int[][] matrix1 = { {1,2, 3} , {5, 6, 7} , {9, 0, 1} };
int[][] matrix2 = { {4, 1, 6}, {2, 3, 5}, {7, 4, 3} };
int[][] matrix3 = newint[3][3];
 
matrix3[0][0] = matrix1[0][0] + matrix2[0][0];
matrix3[0][1] = matrix1[0][1] + matrix2[0][1];
matrix3[0][2] = matrix1[0][2] + matrix2[0][2];
matrix3[1][0] = matrix1[1][0] + matrix2[1][0];
matrix3[1][1] = matrix1[1][1] + matrix2[1][1];
matrix3[1][2] = matrix1[1][2] + matrix2[1][2];
matrix3[2][0] = matrix1[1][0] + matrix2[2][0];
matrix3[2][1] = matrix1[1][1] + matrix2[2][1];
matrix3[2][2] = matrix1[1][2] + matrix2[2][2];
```

  
Ipak, rešenje je moguće i značajno optimizovati i to korišćenjem petlji, pa se veliki broj naredbi za sabiranje može zameniti sledećom logikom:

```java
int[][] matrix1 = {{1, 2, 3}, {5, 6, 7}, {9, 0, 1}};
int[][] matrix2 = {{4, 1, 6}, {2, 3, 5}, {7, 4, 3}};
int[][] matrix3 = newint[3][3];
 
 
for(inti = 0; i < matrix1.length; i++) {
    for(intj = 0; j < matrix2.length; j++) {
        matrix3[i][j] = matrix1[i][j] + matrix2[i][j];
    }
}
```

**  
Vežba 3**

```java
int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
 
intx = 0;
while(x < arr.length) {
    System.out.println(arr[x]);
    x++;
}
```

**  
Vežba 4**

```java
int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
 
intx = 0;
do{
    System.out.println(arr[x]);
    x++;
} while(x < arr.length);
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_18_01.thb) JCPR1\_18\_01.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_18_01.Mp4")

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_18_02.thb) JCPR1\_18\_02.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_18_02.Mp4")

Kako Vam mogu pomoći?