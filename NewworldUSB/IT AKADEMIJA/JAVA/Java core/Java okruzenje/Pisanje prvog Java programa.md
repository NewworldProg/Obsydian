---
title: "Link Elearning"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=922e2e4b7bf10954b111ef3113959a14_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434672"
author:
published:
created: 2025-04-25
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 5 od 22

## Pisanje prvog Java programa

U prethodnoj lekciji imali ste prilike da saznate šta je to Java i da se upoznate sa koracima za uspostavljanje okruženja za izvršavanje i razvoj Java programa. U ovoj lekciji, priču o Javi ćemo nastaviti tamo gde smo se zaustavili u prethodnoj lekciji. Preduslov za praćenje lekcije jeste uspostavljeno Java okruženje, zato što ćemo u narednim redovima prvi put napisati i pokrenuti jedan Java program. Stoga će ==u lekciji pred vama biti obavljeni sledeći koraci:==

1. pisanje izvornog koda Java programa;
2. kompajliranje izvornog Java koda u bytecode;
3. prevođenje bytecodea u mašinski kod od strane Java virtuelne mašine;
4. pokretanje Java programa.

Obavljanje navedenih koraka biće ilustrovano bez ikakvih pomagala, odnosno direktnim ==korišćenjem različitih alata iz OpenJDK skupa==. U narednoj lekciji, identični koraci će biti obavljeni korišćenjem jednog specijalizovanog programa namenjenog za razvoj Java programa, odnosno korišćenjem jednog razvojnog okruženja.

| **Napomena**  U ovom trenutku je potrebno da znate da Vam za potrebe ovog kursa pokretanje Java programa kroz komandnu liniju operativnog sistema nije neophodno, jer će razvojno okruženje to za Vas automatski uraditi. Takođe, u praksi se Java programi ne prevode kroz terminal, a u ovim lekcijama je to urađeno zbog demonstracije kako Java radi. |
| --- |

### Pisanje Java programa

Java programi nastaju pisanjem Java izvornog koda. Java izvorni kod je tekst koji zadovoljava [sintaksna pravila jezika](https://www.link-elearning.com/linkdl/opisPojma.php?id=160419 "sintaksna pravila jezika"). S obzirom na to da je izvorni kod običan tekst, njega je moguće pisati korišćenjem bilo kog tekst editora. Tako je na ==Windows operativnom sistemu moguće koristiti Notepad, a na macOS-u TextEdit.==

U narednim redovima biće prikazan postupak za pisanje izvornog koda našeg prvog Java programa. Iz prethodne lekcije, poznato je da se izvorni kod Java programa piše unutar fajlova sa ekstenzijom **.java**, te je stoga prvi korak kreiranje takvog fajla, koji ćemo zatim ispuniti izvornim kodom našeg programa.

Savet je da na primarnoj particiji svog hard diska ==kreirate jedan novi folder sa nazivom java\_programs ili nekim drugim proizvoljnim nazivom i da unutar takvog foldera zatim obavite kreiranje novog .java fajla unutar koga će se naći izvorni kod našeg prvog programa.==

| **Kreiranje fajla sa ekstenzijom.java na Windows operativnom sistemu**  Za kreiranje .java fajla na Windows operativnim sistemima dovoljno je odabrati opciju za kreiranje novog tekstualnog (.txt) fajla. Opcija **New -> Text Document** može se naći unutar kontekstnog menija koji se dobija desnim klikom unutar nekog foldera ili Desktopa (slika 5.1).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_01.png)  *Slika 5.1. Opcija za kreiranje novog tekstualnog fajla (Windows)      *  Aktiviranje prikazane opcije stvoriće novi fajl kojem je potrebno postaviti naziv promeniti mu ekstenziju u .java (slika 5.2).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_02.png)  *Slika 5.2. Novi tekstualni fajl sa definisanim nazivom i promenjenom ekstenzijom (Windows)      *  Nakon definisanja naziva fajla i promene ekstenzije u.java, operativni sistem Windows će nas pitati da li smo sigurni da želimo da izvršimo promenu ekstenzije fajla koji smo kreirali (slika 5.3).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_03.png)*  *Slika 5.3. Potvrda promene ekstenzije (Windows)      *  Naravno, potrebno je odgovoriti potvrdno, čime je posao kreiranja .java dokumenta na Windows operativnom sistemu završen.  Kreirani .java fajl je potrebno otvoriti korišćenjem aplikacije Notepad. Da biste kreirani fajl otvorili unutar Notepada, odaberite opciju **Open with** koja se nalazi u kontekstnom meniju koji se dobija desnim klikom na .java fajl (slika 5.4).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_04.png)*  *Slika 5.4. Opcija Open with (Windows)      *  U prozoru koji se zatim otvara, potrebno je pronaći Notepad i odabir potvrditi klikom na OK (slika 5.5).  ![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_05.png)  *Slika 5.5. Odabir programa Notepad za otvaranje.java fajla (Windows)*     Na ovaj način biće otvoren nešto ranije kreirani .java fajl (slika 5.6).  *![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_06.png)*  *Slika 5.6. Prazan.java fajl otvoren u Notepadu* |
| --- |

Nakon kreiranja .java fajla, možemo preći na pisanje našeg prvog Java programa. Njegov izvorni kod će izgledati ovako:

```java
publicclassMyFirstProgram
{
    publicstaticvoidmain(String[] args)
    {
        System.out.println("Hello World");
    }
}
```

  
Ovo je izvorni kod jednog jednostavnog Java programa, koji ==na izlazu ispisuje poruku *Hello World*==. S obzirom na to da se još nismo bavili sintaksnim pravilima za pisanje Java koda, sve ono što je upravo napisano za nas je u ovom trenutku potpuna nepoznanica. ==Upravo prikazani izvorni kod našeg prvog Java programa u potpunosti ćemo biti u stanju da razumemo tek nakon 10-ak narednih lekcija== ovoga kursa. Stoga se sada nećemo posebno baviti značenjem upotrebljenih reči, već ćemo samo načelno pokušati da razumemo ono što je napisano.

Java izvorni kod je posebno formulisan tekst koji nakon prevođenja u mašinski kod može da uputi određene instrukcije kompjuteru. Na primeru našeg prvog programa, takva instrukcija jeste ispis *Hello World* poruke.

U ovom trenutku lako je ==uočiti i to da se izvorni kod Java programa sastoji iz određenih reči engleskog jezika, koje za kompajler imaju posebno značenje==. Pored takvih specijalnih reči, za formiranje Java izvornog koda koriste se i brojni specijalni karakteri, ali i tekst koji možemo samostalno da formulišemo. Takav tekst na primeru našeg programa je *Hello World*.

| **Napomena**  Kompletan izvorni kod našeg prvog programa grupisan je u nešto što se u Java jeziku naziva *klasa*. Svaki Java kod postoji isključivo unutar neke klase. Drugim rečima, nijedan Java kod ne može postojati izvan klase. U ovom trenutku je posebno važno da primetite da je klasa u našem primeru imenovana isto kao i fajl unutar koga se nalazi izvorni kod našeg prvog Java programa – *MyFirstProgram*. Ova činjenica je posebno značajna za obavljanje narednog koraka – kompajliranja. |
| --- |

Izvorni kod našeg prvog Java programa postaće vam mnogo jasniji u narednim lekcijama, a sada ćemo se posvetiti operacijama koje će nam omogućiti da upravo napisani prvi Java program pokrenemo.

Izvorni kod Java programa piše se unutar fajlova sa ekstenzijom:

  

### Kompajliranje Java izvornog koda

==Prvi korak u procesu oživljavanja našeg prvog Java programa jeste njegovo kompajliranje==. Iz prethodne lekcije znamo da se takav proces obavlja ==korišćenjem Java kompajlera i da se tom prilikom dobija bytecode==.

==Java kompajler je zapravo fajl koji nosi naziv **javac**==. U prethodnoj lekciji je navedena naredba za proveru dostupnosti javac alata:

javac -version  

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_07a.jpg)

*Slika 5.7. Komanda za ispis verzije Java kompajlera  
  
*

Poruka javac 17 znači da je Java kompajler operativan i spreman za korišćenje.

Pre nego što pokrenemo kompajliranje izvornog koda, neophodno je da se pozicioniramo unutar foldera u kome se nalazi .java fajl. S obzirom na to da je Command Prompt uglavnom pozicioniran unutar system32 foldera, za pozicioniranje unutar nešto ranije kreiranog java\_programs foldera dovoljno je aktivirati sledeće komande:

cd..  
cd..  
cd java\_programs

  
Nakon pozicioniranja unutar foldera sa izvornim kodom, ==kompajliranje se obavlja na sledeći način:==

==javac MyFirstProgram.java==

Prikazana komanda se sastoji iz dva dela:

- javac je naziv fajla koji predstavlja Java kompajler;
- MyFirstProgram.java je naziv fajla sa izvornim kodom.

Ukoliko proces kompajliranja prođe bez ikakve poruke, baš kao na slici 5.8, možemo konstatovati da je prevođenje uspešno obavljeno.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_08.png)

*Slika 5.8. Uspešno obavljeno kompajliranje Java izvornog koda  
  
*

==Uspešno okončanje kompajliranja podrazumeva kreiranje još jednog fajla unutar foldera sa izvornim kodom (slika 5.9).==

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_09.png)

*Slika 5.9. Komanda za ispis verzije Java kompajlera  
  
*

Kompajliranjem se dobija fajl sa ekstenzijom ==.class. Reč je o fajlu sa bytecodeom.==  
  

### Pokretanje Java programa

==Nakon kompajliranja== i dobijanja bytecodea, moguće je pokrenuti naš prvi Java program. Pokretanje je moguće obaviti upućivanjem bytecodea na prevođenje od strane Java virtuelne mašine, na sledeći način:

java MyFirstProgram

Prikazana komanda sastoji se iz dva dela:

- java – alat koji se koristi za prevođenje i pokretanje Java programa;
- MyFirstProgram – naziv programa koji je potrebno pokrenuti.

Rezultat pokretanja našeg prvog Java programa jeste ispis poruke *Hello World*. To možete videti na slici 5.10.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR1_05_10.png)

*Slika 5.10. Efekat pokretanja našeg prvog Java programa  
  
*

==Na ovaj način obavljeno je izvršavanje bytecodea== od strane Java virtuelne mašine i ovde smo prvi put mogli da vidimo efekat Java koda koji smo samostalno napisali. Izvršavanje Java programa sastoji se zapravo iz prevođenja bytecodea u mašinski kod, koji se zatim izvršava od strane hardvera kompjutera.

| **Napomena**  MyFirstProgram unutar komande za pokretanje programa odnosi se na naziv klase unutar koje je definisan Java program. Nešto ranije je rečeno da naziv klase mora biti isti kao naziv fajla sa izvornim kodom.  Prikazana komanda za pokretanje Java programa skraćeni je oblik komande u kojoj se navodi i putanja na kojoj se nalazi klasa:  java -cp. MyFirstProgram  Ovakva komanda za pokretanje Java programa proširena je delom za definisanje putanje na kojoj se nalazi klasa. Tako je \-cp zapravo skraćenica za \-classpath. Korišćenjem karaktera tačka (.) definiše se trenutna putanja, odnosno putanja na kojoj se nalazimo prilikom upućivanja ovakve komande. S obzirom na to da smo prilikom upućivanja ovakve komande pozicionirani unutar foldera sa .class fajlom, definisanje putanje do klase se može izostaviti. |
| --- |

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_05.thb) JCPR1\_05.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_05.Mp4")

Kako Vam mogu pomoći?