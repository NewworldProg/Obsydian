---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=7940547b91ee83335cf8abad2bfbaa16_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434689"
author:
published:
created: 2025-05-11
description:
tags:
  - "clippings"
---
Jedinica 22 od 22

## Debug

U prethodnoj lekciji ilustrovana su dva tipa softverskih grešaka do kojih može doći unutar Java programa. Tako ste imali prilike da čitate o sintaksnim i *runtime* greškama i da se upoznate sa njihovom manifestacijom u Java programima. Preostalo je još da se upoznamo sa najkompleksnijim tipom softverskih grešaka. Reč je o greškama koje se nazivaju logičke. U procesu upoznavanja sa logičkim greškama, u lekciji pred vama biće obrađen i jedan veoma važan aspekt programiranja koji se naziva *debug*, odnosno proces detekcije i pronalaženja grešaka.  
  

### Šta su logičke greške?

Logičke greške su najkompleksnija vrsta grešaka do kojih može doći prilikom izvršavanja softvera. Za njih se kaže da su najkompleksnije zato što ih je najteže uočiti. Ova vrsta grešaka nastaje u situacijama u kojima program ne proizvodi očekivani rezultat, a izvršno okruženje ne prijavljuje bilo kakav izuzetak ili neregularnost. Drugim rečima, kod sa logičkom greškom ne obavlja ono što se od njega očekuje. Zbog nepostojanja bilo kakve poruke od izvršnog okruženja, detekcija i uklanjanje logičkih grešaka zahteva pažljivu analizu koda i poznavanje korišćenja nekog od alata za *debug*. Na sreću, sva moderna razvojna okruženja poseduju takve alate, pa ni IntelliJ IDEA nije izuzetak. Stoga će veliki deo ove lekcije biti posvećen korišćenju *debug* alata koji je sastavni deo IntelliJ IDEA okruženja. Ipak, za početak, pogledajmo primer jednog Java programa koji poseduje logičku grešku.  
  

### Referentni primer

Primer na kome će biti razmotren pojam logičkih grešaka izgledaće ovako:

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        intnumberA;
        intnumberB;
 
        Scanner scanner = newScanner(System.in);
 
        System.out.println("Please, enter number A: ");
        numberA = scanner.nextInt();
 
        System.out.println("Please, enter number B: ");
        numberB = scanner.nextInt();
 
 
        if(numberA > numberB) {
            System.out.println("Number "+ numberA + " is greater then "+ numberB);
        } else{
            System.out.println("Number "+ numberB + " is greater then "+ numberA);
        }
 
    }
```

  
Ovo je Java program koji od korisnika prihvata dva broja. Brojevi koje korisnik unese smeštaju se unutar promenjivih numberA i numberB. Program zatim utvrđuje koji od dva uneta broja je veći i obaveštenje prikazuje korisniku.

Kada ovakav program prevedete i pokrenete, neće se dogoditi ništa neuobičajeno. Možete probati da unesete različite ulazne podatke i program će na izlaz emitovati poruke različitog sadržaja. Ipak, ukoliko se malo bolje udubite u poruke koje se dobijaju od programa, može se uočiti nekonzistentnost. Pogledajte o čemu je reč. U nastavku će biti ilustrovani različiti slučajevi korišćenja prikazanog programa, kako bi se detektovala logička greška.

| **Slučaj 1**  Ulazni podaci: 13, 15  Poruka: Number 15 is greater than 13 |
| --- |

| **Slučaj 2**  Ulazni podaci: 15, 13  Poruka: Number 15 is greater than 13 |
| --- |

| **Slučaj 3**  Ulazni podaci: 5, 5  Poruka: Number 5 is greater than 5 |
| --- |

Analizom navedenih slučajeva korišćenja može se dosta toga zaključiti o unutrašnjem izvršavanju programa. U prvom slučaju, uneti su brojevi 13 i 15. Program obaveštava da je broj 15 veći od broja 13, na osnovu čega se može zaključiti da program uspešno funkcioniše. Drugi slučaj je sličan – ulazni podaci su identični, ali su uneti obrnutim redom. Program emituje identičnu poruku, pa se može zaključiti da i na osnovu *Slučaja 2* program funkcioniše korektno.

*Slučaj 3* pokazuje evidentan nedostatak programa. Uneti brojevi su 5 i 5, a program obaveštava da je broj 5 veći od broja 5.

Na ovom primeru se može videti baš ono što je rečeno na početku ove lekcije. Logičke greške ne proizvode izuzetak, ali čine da program ne emituje očekivani rezultat. I upravo je to ono što se događa u ovom primeru. Program nas obaveštava je broj 5 veći od broja 5, što svakako nije odgovarajući izlaz.

Upravo prikazana logička greška je jedna od jednostavnijih reprezentacija takve vrste grešaka i svakako je mogla da bude detektovana i pažljivijom opservacijom koda. Ipak, ukoliko još uvek ne uviđate u čemu je problem u našem programu, iskoristićemo jedan specijalizovani alat razvojnog okruženja koji će nam pomoći u detekciji logičke greške.  
  

### Debugger

Gotovo svako moderno razvojno okruženje unutar sebe poseduje i specijalizovani alat koji se naziva debugger. Na osnovu ovog naziva možete da naslutite da je reč o alatu koji pomaže u uklanjanju grešaka iz izvornog koda programa. Reč je zapravo o alatu koji omogućava pauziranje i kontrolisanje izvršavanja koda. Kako bi se aktivirao debugger IntelliJ IDEA okruženja, neophodno je program pokrenuti na poseban način, a ne kao što smo to obavljali do sada.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_01.png)*

*Slika 22.1. Opcije za pokretanje programa u debug modu  
  
*

Slika 22.1. ilustruje tri najznačajnija mesta sa kojih je jedan Java program moguće pokrenuti u debugger modu. Pokretanjem programa u debugger modu, razvojno okruženje ulazi u poseban režim, što se može videti na slici 22.2.

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_02.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_02-original.png)

*Slika 22.2. Opcije za osnovnu kontrolu debug moda izvršavanja  
  
*

Na slici 22.2. možete videti program koji se izvršava u debugger režimu. Prvo je potrebno da primetite da se automatski otvara *Debug* prozor okruženja i da se dalja interakcija sa okruženjem obavlja isključivo korišćenjem takvog panela. Unutar njega postoji nekoliko veoma važnih opcija, koje možete videti na slici 22.2:

- **Rerun** – ponovno pokreće program u debug režimu;
- **Resume** – ukoliko je program pauziran, nastavlja izvršavanje koda;
- **Pause** – zaustavlja izvršavanje koda neposredno pre naredbe koja treba da se izvrši sledeća;
- **Stop** – zaustavlja izvršavanje programa i napušta debug režim; okruženje se vraća u stanje u kome je bilo pre pokretanja programa u debug režimu.

Svakako, najznačajnija opcija je ona koja omogućava da se izvršavanje programa pauzira, čime se ulazi u poseban debug režim, koji omogućava da se izvršavanje koda eksplicitno kontroliše.  
  

### Kontrola izvršavanja koda

Nakon što se obavi pauziranje koda, postaje dostupno nekoliko veoma važnih opcija, kojima je moguće kontrolisati izvršavanje programa (slika 22.3).

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_03.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_03-original.png)

*Slika 22.3. Opcije za kontrolu izvršavanja koda nakon pauziranja  
  
*

Na slici 22.3. možete da vidite grupu opcija koje se koriste za kontrolisanje izvršavanja koda nakon što se izvršavanje pauzira. Opcije su obeležene sa *Step Actions*, zato što omogućavaju da se kroz izvorni kod prođe korak po korak (*step*), odnosno naredbu po naredbu.

Značenje ovih opcija ilustrovano je slikom 22.4.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_04.png)*

*Slika 22.4. Opcije za kontrolu izvršavanja koda nakon pauziranja (2)  
  
*

- **Step Over** – prelazi na izvršavanje prve sledeće linije; ipak, ukoliko je sledeća linija poziv neke metode, takva metoda se izvršava u celosti, a izvršavanje se ponovo pauzira na prvoj naredbi nakon poziva metode;
- **Step Into** – prelazi na izvršavanje sledeće linije, ali ukoliko je sledeća linija poziv metode, takva metoda se ne izvršava u celosti, već se izvršavanje pauzira na prvoj naredbi unutar metode;
- **Force Step Into** – omogućava ispitivanje funkcionalnosti koje ne pripadaju direktno našem programu; drugim rečima, naš program može da koristi funkcionalnosti koje se nalaze u nekim drugim kompajliranim bibliotekama; ova opcija omogućava da se uđe u kod takvih funkcionalnosti kao da je reč o onima koje smo samostalno pisali;
- **Step Out** – ukoliko se izvršavanje nalazi unutar metode, izvršava se kompletan ostatak metode, a izvršavanje se pauzira na prvoj naredbi nakon poziva takve metode;
- **Drop Frame** – omogućava da se prilikom izvršavanja koda vratimo unazad, odbacivanjem izvršavanja metode koja se trenutno izvršava; ova opcija omogućava da ponovo ispitamo izvršavanje metode u kojoj smo već bili;
- **Run to Cursor** – izvršava sve naredbe sve dok ne stigne do pozicije na kojoj se unutar editora trenutno nalazi kursor.

Ukoliko se tokom prolaska kroz kod programa nalazimo na naredbi u kojoj se poziva neka metoda i želimo da debuggerom uđemo u njen programski kod, iskoristićemo opciju:

  

### Tačke prekida

Upravo prikazani primer korišćenja IntelliJ IDEA debuggera imao je jednu olakšavajuću okolnost. Naime, jedna od prvih naredbi programa je i ona koja blokira izvršavanje programa sve dok korisnik ne unese neke vrednosti. Stoga smo imali praktično neograničeno vreme na raspolaganju da izvršavanje programa pauziramo i upoznamo se sa svim opcijama za kontrolisanje izvršavanja. Ipak, u programima koji nemaju ovakvih naredbi, odnosno naredbi koje blokiraju izvršavanje programa, pokretanje programa u debug modu ne bi se mnogo razlikovalo od regularnog pokretanja. U to se možete uveriti ukoliko naredbe za preuzimanje podataka od korisnika zamenite direktnom inicijalizacijom promenljivih. Nakon toga, pokrenite program u debug modu i moći ćete da vidite da unutar Debug konzole dobijamo rezultat izvršavanja i da praktično nemamo vremena da stignemo da pauziramo izvršavanje programa.

Kako bi se i u ovakvim situacijama omogućilo pauziranje programa, pribegava se korišćenju tačaka prekida. Tako su tačke prekida još jedan način da se pauzira izvršavanje programa.

Tačka prekida se postavlja jednostavnim klikom na prostor koji se nalazi na levoj strani editora, odnosno između editora i brojeva koji predstavljaju linije koda. Kao potvrda da je tačka prekida uspešno postavljena, dobija se karakteristična crvena oznaka (slika 22.5).

[![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_05.png)](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_22_05-original.png)

*Slika 22.5. Postavljanje tačke prekida  
  
*

Nakon postavljanja tačke prekida u primeru iz ove lekcije, potrebno je program pokrenuti u debug modu, isto kao i u prethodnom primeru. Ipak, ovoga puta će se izvršavanje zaustaviti u definisanoj tački prekida, a mi ćemo izvršavanje dalje moći da kontrolišemo korišćenjem već opisanih komandi.

Korišćenjem upravo prikazanih funkcionalnosti IntelliJ IDEA debuggera veoma lako možemo da utvrdimo u čemu je problem našeg programa. Jednostavno, prilikom pisanja programa nismo predvideli slučaj po kome bi ulazni podaci bili jednaki. S obzirom na to da korisnik ima mogućnost da unese dve identične vrednosti, neophodno je i da program poseduje odgovarajuću logiku za obradu takvih ulaznih podataka. Drugim rečima, program mora za bilo koji unos da proizvede odgovarajući izlaz:

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        intnumberA;
        intnumberB;
 
        Scanner scanner = newScanner(System.in);
 
        System.out.println("Please, enter number A: ");
        numberA = scanner.nextInt();
 
        System.out.println("Please, enter number B: ");
        numberB = scanner.nextInt();
 
        
        if(numberA > numberB) {
            System.out.println("Number "+ numberA + " is greater then "+ numberB);
        } elseif(numberB > numberA) {
            System.out.println("Number "+ numberB + " is greater then "+ numberA);
        } else{
            System.out.println("Numbers are equal.");
 
        }
        
    }
 
}
```

### Vežba

U ovoj lekciji je rečeno da je potrebno da program bude u stanju da proizvede adekvatan izlaz za bilo koji unos. Ipak, ukoliko se programu iz ovog primera proslede neki podaci koji nisu broj, dolazi do pojave izuzetka. Korišćenjem pristupa iz prethodne lekcije, modifikovati program tako da izrečena činjenica bude u potpunosti istinita.

**  
Rešenje**

```java
importjava.util.Scanner;
 
publicclassJavaProgram {
 
    publicstaticvoidmain(String[] args) {
 
        intnumberA = 0;
        intnumberB = 0;
 
        Scanner scanner = newScanner(System.in);
 
        try{
 
            System.out.println("Please, enter number A: ");
            numberA = scanner.nextInt();
 
            System.out.println("Please, enter number B: ");
            numberB = scanner.nextInt();
        } catch(Exception exc) {
            System.out.println("There is an error");
            return;
        }
       
        if(numberA > numberB) {
            System.out.println("Number "+ numberA + " is greater then "+ numberB);
        } elseif(numberB > numberA) {
            System.out.println("Number "+ numberB + " is greater then "+ numberA);
        } else{
            System.out.println("Numbers are equal.");
 
        }
 
    }
 
}
```

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_22.thb) JCPR1\_22.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_22.Mp4")

Kako Vam mogu pomoći?