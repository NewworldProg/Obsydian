---
title: "Link Elearning 3"
source: "https://www.link-elearning.com/linkdl/usersPortal/?pk=84535124027660c60a5c84a1802dad6f_ita_23&c=modul&IDIstorijaKurs=151078&IDJedinica=1434670"
author:
published:
created: 2025-04-24
description:
tags:
  - "clippings"
---
- Ask AI Assistant
- Copy

Jedinica 3 od 22

## ==Rešavanje problema u kompjuterskom programiranju==

U prethodnoj lekciji definisani su osnovni pojmovi koji učestvuju u procesu rešavanja problema prilikom razvoja kompjuterskih programa. **==Problem==** je definisan kao ==prepreka koju je potrebno prevazići ili pitanje na koje je potrebno dati odgovor kako bi se određena situacija razrešila==. ==Svaki problem== može se definisati ==kroz prizmu **ulaza** i očekivanih osobina **izlaza**.== Na primer, ==problem pripreme palačinki== bi kao ==ulaze== imao sve ==sastojke== koji bi se koristili za pripremu ove poslastice. ==Izlaz== bi, naravno, bio gotov proizvod, odnosno ==palačinka==. Problem sabiranja dva broja bi kao ulaze imao sabirke, a kao izlaz proračunati zbir. Koraci koji bi učestvovali u procesu rešavanja ovakvih problema mogli bi se nazvati **procedurom**. Sve ovo je ilustrovano slikom 3.1.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_01.jpg)

*Slika 3.1. Procedura za rešavanje problema  
  
*

Slika 3.1. ==ilustruje apstrahovani pogled na proceduru kojom se rešava neki problem==. Možete da vidite da procedura dobija neke ulazne vrednosti, koje koristi tokom obrade kako bi proizvela rezultat. Na primer, ==u slučaju sabiranja dva broja, ulazni podaci bi bili neki sabirci, dok bi izlaz koji bi procedura proizvodila bio zbir takvih brojeva==. Ulazni podaci procedure za sabiranje dva broja mogli bi na primer biti 2 i 7. U takvoj situaciji procedura za sabiranje proizvela bi izlaz u obliku vrednosti 9. Dalje, ukoliko bi se proceduri za sabiranje dva broja prosledile vrednosti 12 i 20, ona bi proizvela vrednost 32. Ovo su bile samo dve situacije u kojima bi se mogla upotrebiti procedura za sabiranje dva broja. Potpuno je jasno da je broj ovakvih različitih situacija beskonačan.

Svaka jedinstvena situacija u kojoj se neka procedura može upotrebiti naziva se instanca takve procedure. Ono što instance jedne procedure međusobno razlikuje jesu različite vrednosti ulaznih podataka. Tako bi jedna instanca procedure za sabiranje dva broja bila ona koja bi računala zbir brojeva 2 i 7, a druga instanca ona koja bi sabirala brojeve 12 i 20. Dobra procedura je ona koja proizvodi očekivani rezultat za bilo koju instancu njenog korišćenja. Bez obzira na to koji se brojevi iskoriste kao ulaz procedure za sabiranje dva broja, neophodno je da ona proizvede očekivani rezultat, odnosno tačnu vrednost operacije sabiranja. Upravo to je i definicija algoritma – *procedura koja u svakoj situaciji proizvodi očekivani rezultat.  
  
*

### Osnovne tehnike za rešavanje problema prilikom programiranja

U prethodnoj lekciji ilustrovano je rešavanje samo jednog, veoma jednostavnog, problema do koga može doći prilikom kompjuterskog programiranja. ==U lekciji pred vama biće obrađeno još nekoliko različitih situacija, koje su veoma karakteristične za programiranje==.

| **Napomena**  Za opisivanje načina na koji se neki problem može rešiti koriste se algoritmi, koji se mogu artikulisati na različite načine. U prethodnoj lekciji, za predstavljanje algoritama korišćeni su prirodni jezici i dijagrami tokova. U ovoj lekciji, pored ove dve metode ilustrovanja algoritama, biće uveden još jedan, koji se karakteriše najvećom sličnošću sa izvornim kodom nekog konkretnog jezika. Naravno, reč je o pseudokodu*.* |
| --- |

Još 1966. godine kompjuterski naučnici [Corrado Böhm](https://www.link-elearning.com/linkdl/opisPojma.php?id=160422 "Corrado Böhm") i [Giuseppe Jacopini](https://www.link-elearning.com/linkdl/opisPojma.php?id=160423 "Giuseppe Jacopini") uvideli su i demonstrirali da se gotovo s==vi kompjuterski algoritmi mogu predstaviti korišćenjem tri osnovne kontrolne strukture:==

1. ==**sekvenca**==
2. ==**selekcija**==
3. **==ponavljanje==  
	  
	**

**![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_02.jpg)**

*Slika 3.2. Tri osnovna načina za rešavanje problema prilikom programiranja  
  
*

Programiranje korišćenjem bilo kojeg programskog jezika ne može se ni zamisliti bez korišćenja ove tri kontrolne strukture. One predstavljaju osnovu svakog programskog jezika, te ćemo stoga u nastavku ove lekcije posebnu pažnju posvetiti logici ovih struktura, analizom nekoliko jednostavnih algoritama.  
  

### Sekvenca

Sekvencijalna struktura je konstrukcija kod koje se ==koraci algoritma izvršavaju jedan za drugim.== Upravo takav je bio i algoritam za sabiranje dva broja, koji je predstavljen u prethodnoj lekciji (slika 3.3).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_03.jpg)

*Slika 3.3. Linijska struktura algoritma  
  
*

Kao što sa slike 3.3. možete videti, jedan korak algoritma vodi drugom (*početak*, *ulaz*, *obrada*, *izlaz*, *završetak*). Pritom, ==svaki korak algoritma se mora izvršiti kako bi se proizveo očekivani rezultat==. Ukoliko se neki korak izostavi, na primer, ukoliko se izostavi ulaz, algoritam neće proizvesti očekivani rezultat. Takođe, nije moguće da se neki korak algoritma sekvencijalne strukture izvrši više od jednog puta.

Sekvencijalnom strukturom algoritma ==mogu se rešiti samo najjednostavniji problemi== prilikom razvoja [softvera](https://www.link-elearning.com/linkdl/opisPojma.php?id=160416 "softvera"). Stoga se prilikom programiranja ovakva struktura sprovođenja koraka programske logike ==veoma retko koristi za rešavanje kompletnog problema==. Mnogo se češće pribegava kombinovanju sekvencijalne (linijske) strukture sa jednim od dva kontrolna toka opisana u nastavku lekcije.  
  

### Selekcija

Selekcija je jedna od struktura izvršavanja programske logike, koja ==omogućava da se određeni koraci uopšte ne izvrše==. Tako selekcija omogućava modelovanje logike koja treba da sadrži neku odluku. Jedan takav primer već je ilustrovan u prethodnoj lekciji. Reč je o primeru algoritma za odlučivanje da li ==prilikom izlaska iz kuće sa sobom poneti kišobran ili ne==. Kada se govori o kompjuterskom programiranju, algoritam koji u sebi sadrži strukturu selekcije može se ilustrovati rešavanjem problema deljenja dva broja. Evo kako bi takav algoritam izgledao (slika 3.4).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_04.jpg)

*Slika 3.4. Algoritam sa strukturom selekcije  
  
*

Prikazani dijagram toka ilustruje algoritam za ==deljenje dva broja.== Algoritam unutar sebe sadrži strukturu selekcije, pa je idealan za upoznavanje sa ovom strukturom koja se koristi prilikom rešavanja programerskih problema. Prikazani algoritam započinje ulazom koji se karakteriše obezbeđivanjem dva broja – deljenika i delioca (x, y).

Odmah nakon ulaza pribegava se realizaciji selekcije. Drugim rečima, ==ispituje se da li je delilac (broj y) jednak nuli==. Verovatno znate da deljenje nulom u matematici nije dozvoljeno, te bi stoga neproveravanje ove vrednosti u nekim situacijama moglo da izazove proizvodnju neadekvatnog izlaza. Već više puta je rečeno da je algoritam procedura za rešavanje nekog problema koja će proizvesti očekivani rezultat, bez obzira na to kakve vrednosti postoje na ulazu. ==Zbog toga je potrebno osigurati adekvatan izlaz i kada korisnik kao vrednost y prosledi 0.==

Iz prethodne lekcije je poznato da se korišćenjem dijagrama tokova, selekcija, odnosno grananje, predstavlja korišćenjem simbola romboidnog oblika (slika 3.5).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_05.jpg)

*Slika 3.5. Način na koji se korišćenjem dijagrama toka modeluje selekcija  
  
*

Unutar romboidnog simbola, koji predstavlja selekciju (slika 3.5), postavlja se uslov, odnosno pitanje na koje je potrebno odgovoriti. U primeru prikazanog dijagrama, simbol za selekciju sadrži tekst y=0. Ovakav tekst se jednostavnim rečima može pročitati: *Da li je y jednako 0?*

==Svaka struktura selekcije poseduje tačno jedan ulaz i tačno dva izlaza==. To znači da svaka selekcija u kompjuterskim algoritmima mora evoluirati u jedan od dva odgovora (tačno/netačno, da/ne, 0/1 i slično). U prikazanom primeru dve izlazne grane su imenovane korišćenjem engleskih reči *true* (tačno) i *false* (netačno). Svaka selekcija u kompjuterskom programiranju okončava se odabirom samo jednog toka kretanja. Jednostavnim rečima, to bi moglo da glasi ovako: ==*Broj y biće ili jednak nuli ili neće biti jednak nuli. Zadovoljenje oba uslova za istu vrednost nije moguće*.==

==Ukoliko je broj y jednak nuli, algoritam nastavlja svoj tok kroz desnu granu koja vodi do izlaza, koji je u takvoj situaciji u obliku tekstualne poruke error.==

==Ukoliko broj y ima vrednost različitu od nule, sledeći korak algoritma jeste obrada, odnosno računanje količnika, deljenjem== broja x brojem y. Nakon završetka obrade, emituje se izračunata vrednost z kao finalni rezultat algoritma.

| **Napomena**  Da je kojim slučajem algoritam za deljenje dva broja realizovan bez upotrebe strukture za selekciju, odnosno bez provere vrednosti delioca, ozbiljno bi bila narušena jedna od osnovnih osobina algoritama, a to je tačnost izlaza za bilo koju vrednost ulaza. |
| --- |

### Ponavljanje

U prethodnom poglavlju, koje se bavilo korišćenjem selekcije u cilju rešavanja problema prilikom programiranja, mogli ste da vidite prvi primer algoritma koji nije pratio striktnu linijsku formu. Struktura selekcije je omogućila odabir jednog od dva puta kojim je bilo moguće nastaviti tok algoritma. ==Selekcija nije jedina struktura koja omogućava da se odstupi od striktnog linearnog izvršavanja algoritma. Tako nešto omogućava i struktura ponavljanja.==

Struktura ponavljanja o==mogućava da se određeni koraci algoritma, samim tim, i kompjuterskog programa izvrše više puta,== sve dok za tim ima potrebe. ==Idealni primer== situacije koja bi zahtevala jedan takav scenario bio bi kompjuterski program čiji bi cilj bio ==ispisivanje prvih n celih pozitivnih brojeva==. Kažemo, prvih n brojeva, s obzirom na to da bi korisniku takvog programa bilo omogućeno da odluči koliko prvih celih pozitivnih brojeva je potrebno da program ispiše. Ispisivanje bi počinjalo od broja 1.

Prirodnim jezikom, ovakav algoritam bismo mogli da definišemo na sledeći način:

1. ==*preuzmi od korisnika celobrojni pozitivan broj* *n*==
2. *==ispisuj brojeve počevši od broja jedan sve dok je broj koji se ispisuje manji ili jednak broju n.==  
	  
	*

Opisani koraci za rešavanje definisanog problema predstavljaju veoma ogoljen algoritam, sačinjen samo od najosnovnijih koraka. Tako je proceduru rešavanja ovog problema moguće dodatno produbiti:

1. ==*preuzmi od korisnika celobrojnu pozitivnu vrednost* *n*==
2. ==*definiši broj* *i* *sa vrednošću 0*==
3. ==*uvećaj* *i* *za jedan*==
4. ==*prikaži vrednost*==
5. ==*proveri da li je i manje od* *n**; ukoliko jeste, vrati se na korak 3; ukoliko nije, završi.==  
	  
	*

Upravo opisan algoritam formulisan prirodnim jezikom, korišćenjem dijagrama toka može se predstaviti kao na slici 3.6.

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_06.jpg)*

*Slika 3.6. Algoritam programa za ispis prvih n celih pozitivnih brojeva*  
  

Dijagram toka ilustrovan slikom 3.6. predstavlja algoritam za ispisivanje prvih n celih pozitivnih brojeva. Ovakav algoritam sadrži strukturu ponavljanja. Ona je realizovana simbolima prikazanim slikom 3.7.

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_07.jpg)

Slika 3.7. Struktura ponavljanja ilustrovana dijagramom toka  
  

Struktura ponavljanja gotovo uvek se realizuje korišćenjem nekog uslova. U prikazanom primeru taj uslov je sledeći:

```java
i<n
```

  
Isečak algoritma koji je ilustrovan slikom 3.7. jednostavnim rečima se može pročitati ovako: *Sve dok je vrednost* ***i*** *manja od vrednosti* ***n****, uvećavaj* ***i*** *za 1 i prikazuj njegovu vrednost. Kada* ***i*** *postane veće ili jednako* ***n****, nastavi dalje.*

Sada je jasno zbog čega se prikazana struktura naziva struktura ponavljanja. Jednostavno, u zavisnosti od okolnosti, odnosno od konkretnih vrednosti, nekoliko koraka algoritma ponoviće se određeni broj puta.

| **Prolazak kroz algoritam**  *Da biste prikazani algoritam što bolje razumeli, u nastavku će biti prikazana kompletna procedura prolaska kroz njegove korake, za neke proizvoljne ulazne vrednosti. Na primer, pretpostavimo da je korisnik kao broj* *n* *uneo vrednost 5. Tada bi svi koraci prolaska kroz algoritam bili sledeći:*  1. *n = 5* 2. *i = 0* 3. *i = 0 +1, odnosno **i = 1*** 4. ***prikaži vrednost 1*** 5. *da li je i manje od n, odnosno **da li je 1 manje od 5**; s obzirom na to da jeste, nastavi sa uvećavanjem i prikazivanjem vrednosti i* 6. *i = 1 + 1, odnosno **i = 2*** 7. ***prikaži vrednost 2*** 8. *da li je i manje od n, odnosno **da li je 2 manje od 5**; s obzirom na to da jeste, nastavi sa uvećavanjem i prikazivanjem vrednosti i* 9. *i = 2 + 1, odnosno **i = 3*** 10. ***prikaži vrednost 3*** 11. *da li je i manje od n, odnosno **da li je 3 manje od 5**; s obzirom na to da jeste, nastavi sa uvećavanjem i prikazivanjem vrednosti i* 12. *i = 3 + 1, odnosno **i = 4*** 13. ***prikaži vrednost 4*** 14. *da li je i manje od n, odnosno **da li je 4 manje od 5**; s obzirom na to da jeste, nastavi sa uvećavanjem i prikazivanjem vrednosti i* 15. *i = 4 + 1, odnosno **i = 5*** 16. ***prikaži vrednost 5*** 17. *da li je i manje od n, odnosno **da li je 5 manje od 5**; s obzirom na to da nije, završi algoritam.   	   	*  *Ilustrovani koraci predstavljaju kompletan tok algoritma za situaciju kada korisnik kao ulaznu vrednost* *n* *postavi broj 5. Odmah možete da primetite da je broj koraka prilikom prolaska kroz algoritam značajno veći nego broj koraka koji su ilustrovani dijagramom. Takođe, broj koraka algoritma direktno zavisi od vrednosti koju korisnik prosledi. Da je, na primer, korisnik prosledio vrednosti 100, prolazak kroz algoritam bi se sastojao iz mnogo većeg broja koraka. Ovakva osobina prikazanog algoritma postoji upravo zbog strukture ponavljanja koja je inkorporirana u ovakav algoritam.* |
| --- |

Prikazani algoritam, koji je i ilustrovan dijagramom na slici 3.6, sadrži još jednu spornu tačku. Ona se tiče vrednosti koju korisnik može da prosledi. Na osnovu definisanih koraka algoritma, može se konstatovati da se podrazumeva da će korisnik uvek uneti pozitivnu celobrojnu vrednost. Naravno, prilikom konstrukcije algoritama nije dobro bilo šta prepustiti slučaju, pa je potrebno predvideti i situaciju u kojoj će korisnik slučajno ili namerno uneti neku vrednost koja predstavlja neispravan ulaz. ==Ispravnim ulazom smatra se bilo koja celobrojna pozitivna vrednost. Da bismo regulisali i ovaj scenario, algoritam će biti modifikovan još jednom:==

1. ==*preuzmi od korisnika broj* *n*==
2. ==*proveri da li je korisnik uneo celobrojnu vrednost veću od nule; ukoliko jeste, nastavi dalje; ukoliko nije, prikaži grešku*==
3. ==*definiši broj* *i* *sa vrednošću 0*==
4. ==*uvećaj* *i* *za jedan*==
5. ==*ispiši vrednost broja* *i*==
6. ==*proveri da li je i manje od* *n**; ukoliko jeste, nastavi dalje; ukoliko nije, završi.==  
	  
	*

Kako biste bolje vizuelizovali opisani algoritam, on će biti predstavljen korišćenjem dijagrama toka (slika 3.8).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_08.jpg)

*Slika 3.8. Algoritam za prikaz prvih n celih pozitivnih brojeva  
  
*

Prikazani dijagram toka gotovo je identičan onom prikazanom na slici 3.6. Razlika je samo u postojanju dodatne strukture selekcije, kojom se vrši provera vrednosti koju je korisnik uneo. Ukoliko je korisnik uneo vrednost koja je manja ili jednaka nuli, emituje se greška i završava se algoritam. Ukoliko vrednost koju je korisnik uneo nije ni manja, a ni jednaka nuli, to znači da je veća od nule, pa se u tom slučaju nastavlja sa već prikazanom logikom za prikazivanje uzastopnih brojeva. Tako ==algoritam prikazan slikom 3.8. u sebi objedinjuje i linijsku i cikličnu i razgranatu strukturu.==

Algoritam poseduje linijsku strukturu ukoliko se neki njegovi koraci mogu izvršiti više od jednom.

  

### Pseudokod

Više puta u prethodnim lekcijama spomenut je pojam pseudokod. Pseudokod je ==još jedan od načina na koji je moguće artikulisati algoritme==, i to korišćenjem izjava napisanih prirodnim jezikom, koje mogu sadržati određene reči engleskog jezika. Pseudokod je oblik za izražavanje algoritama, koji je najbliži pisanju izvornog koda nekog programskog jezika, te smo stoga upoznavanje s njim ostavili za sam kraj ovoga uvodnog modula. Tako pseudokod omogućava da se najviše približimo postupku pisanja izvornog koda, ali bez potrebe da razmišljamo o sintaksnim pravilima konkretnog jezika. Jednostavno, svi programski jezici poseduju svoj skup pravila za pisanje koda, koja se drugačije nazivaju **sintaksa**. Algoritam napisan korišćenjem pseudokoda je univerzalan, tako da je njega sa lakoćom moguće implementirati korišćenjem bilo kog programskog jezika.

Pseudokod ==poseduje veliki broj elemenata koji se mogu koristiti prilikom njegovog dizajna==. Tu se prevashodno misli na različite reči engleskog jezika koje predstavljaju različite akcije koje se obavljaju tokom izvršavanja logike algoritma. Neke od najznačajnijih takvih reči ilustrovane su tabelom 3.1.

| **Jezička konstrukcija** | **Značenje**                                                                                                                                                                                                                 | **Primer**                                                                                                                            |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **GET**                  | Preuzimanje informacija od korisnika.                                                                                                                                                                                        | GET number                                                                                                                            |
| **COMPUTE**              | Obavljanje računanja, odnosno sprovođenje različitih aritmetičkih operacija; prilikom obavljanja aritmetičkih operacija, moguće je koristiti sve standardne aritmetičke operatore (+, -, \*, /, =, ()).                      | COMPUTE z   z = a+b                                                                                                                   |
| **ASSIGN**               | Dodeljivanje vrednosti nekoj promenljivoj.                                                                                                                                                                                   | ASSIGN 10 to x                                                                                                                        |
| **INCREMENT**            | Uvećavanje vrednosti promenljive.                                                                                                                                                                                            | INCREMENT counter                                                                                                                     |
| **DISPLAY, PRINT**       | Prikaz informacija korisniku.                                                                                                                                                                                                | DISPLAY x   PRINT x                                                                                                                   |
| **STORE**                | Čuvanje neke vrednosti koja će se koristiti u narednim koracima algoritma.                                                                                                                                                   | STORE x                                                                                                                               |
| **IF** **–** **THEN**    | Konstrukcija za modelovanje selekcije.                                                                                                                                                                                       | IF answer is yes THEN   DISPLAY "Get an umbrella"                                                                                     |
| **IF – ELSE IF - ELSE**  | Konstrukcija za realizaciju višestruke selekcije.                                                                                                                                                                            | IF age < 18   DISPLAY "Too young to drive"   ELSE IF age = 18   DISPLAY "Better clear the road"   ELSE   DISPLAY "You’re getting old" |
| **WHILE**                | Konstrukcija za realizaciju ponavljanja; sve dok je uslov ispunjen, izvršava se određena logika.                                                                                                                             | WHILE x <= 10   COMPUTE 2x + x + 5   STORE answer   PRINT answer   INCREMENT x                                                        |
| **DO – WHILE**           | Konstrukcija za realizaciju ponavljanja sa post uslovom; za razliku od prethodne konstrukcije, kod ove se prvo izvršava logika pa se tek onda vrši provera uslova; na taj način se osigurava makar jedno izvršavanje logike. | DO   COMPUTE 2x + x + 5   STORE answer   PRINT answer   INCREMENT x   WHILE x <= 10                                                   |

  
*Tabela 3.1. Jezički element pseudokoda  
  
*

==U nastavku lekcije neki od algoritama koji su već realizovani korišćenjem dijagrama tokova biće predstavljeni korišćenjem pseudokoda.== Prvo će biti prikazan algoritam za sabiranje dva broja (slika 3.9).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_09.jpg)*

*Slika 3.9. Algoritam za sabiranje dva broja, predstavljen dijagramom toka (levo) i pseudokodom (desno)  
  
*

Algoritam za sabiranje dva broja sada je prikazan na dva različita načina, korišćenjem dijagrama toka (leva polovina slike 3.9) i korišćenjem pseudokoda (desna strana slike). Bez obzira na to da li tumačili dijagram toka ili pseudokod, algoritam ćete pročitati na isti način: *preuzmi vrednosti x i y; izračunaj z tako što ćeš sabrati x i y; prikaži vrednost z*.

Prilikom konstrukcije algoritma u obliku pseudokoda korišćene su tri reči engleskog jezika koje su specifične za pseudokod ==(GET, COMPUTE, DISPLAY). Njihovo značenje je identično onom koje imaju u engleskom jeziku.==

Iz prikazanog pseudokoda možete da primetite da je linija sa kodom z = x+y uvučena u odnosu na druge linije. Ovo je veoma česta praksa prilikom pisanja pseudokoda, ali i prilikom pisanja koda realnih, stvarnih programskih jezika. Uvlačenjem se definiše pripadnost određenom bloku koda. Na primer, u prikazanom primeru uvlačenjem je rečeno da linija z = x+y pripada akciji izračunavanja (COMPUTE).

Pogledajmo sada kako bismo pseudokodom predstavili algoritam za deljenje dva broja (slika 3.10).

*![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_10.jpg)*

*Slika 3.10. Algoritam za deljenje dva broja, predstavljen dijagramom toka (levo) i pseudokodom (desno)  
  
*

Na slici 3.10. se može videti pseudokod kojim se predstavlja algoritam za deljenje dva broja. Prikazani pseudokod sadrži i deo kojim se modeluje selekcija, odnosno grananje. To je postignuto korišćenjem konstrukcije ==IF-ELSE.== Kod je veoma intuitivan, pa se jednostavno može pročitati: *pribavi vrednosti x i y; **ukoliko (IF)** je* *y* *jednako 0, **onda (THEN)** prikaži poruku* *GREŠKA**, **u protivnom (ELSE)** izračunaj* *z* *tako što ćeš podeliti* *x* *sa* *y* *i prikaži dobijenu vrednost.*

Prilikom formiranja pseudokoda za deljenje dva broja opet se pribegava uvlačenju određenih linija. Linija sa naredbom ==DISPLAY== je uvučena u odnosu na liniju iznad i time je definisana pripadnost linije za prikaz poruke IF bloku. Takođe, i linije za računanje vrednosti z i njen prikaz uvučene su u odnosu na ELSE blok i time je ilustrovana njihova pripadnost ELSE bloku.

Za kraj, pogledaćemo na koji način se i poslednji obrađeni algoritam, za štampanje prvih n celih brojeva, može predstaviti korišćenjem pseudokoda (slika 3.11).

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_11.jpg)

*Slika 3.11. Algoritam za prikaz prvih n celih brojeva većih od nule, predstavlje* n dijagramom toka (levo) i pseudokodom (desno)  
  

Prilikom formiranja pseudokoda sa slike 3.11. modelovana je konstrukcija za predstavljanje ponavljanja. To je postignuto korišćenjem ključnih reči DO i WHILE, što je samo jedan od načina da se korišćenjem pseudokoda modeluje ponavljanje. U tabeli 3.1. navedeni su još neki načini na koje je korišćenjem pseudokoda moguće modelovati ponavljanje.

Ključnom rečju ==DO== definiše se logika koju je potrebno ponavljati sve dok je uslov definisan ključnom rečju WHILE ispunjen. Logika ponavljanja definiše se između ključnih reči ==DO i WHILE==, a na slici se može videti kao dve linije koje su uvučene u odnosu na ključnu reč DO.

Cilj prethodnih nekoliko primera jednostavnih algoritama za rešavanje problema prilikom razvoja softvera jeste da vas pripreme za izazove koji su pred vama, te da vam olakšaju razvijanje programerske logike i upoznavanje sa sintaksom programskih jezika koje ćete učiti u nastavku. Takođe, znanja u vezi sa kreiranjem algoritama koristiće vam sve dok se budete bavili poslom pisanja kompjuterskih programa. Pred vama su sada nova tema i novi izazovi - upoznavanje sintakse programskih jezika višeg nivoa.  
  

### Vežba

**Problem:** Potrebno je naći najveći od 3 uneta broja.

**Rešenje:**

![](https://www.link-elearning.com/linkdl/coursefiles/1519/JCPR_03_12.png)

*Slika 3.12. Dijagram toka  
  
*

**Objašnjenje rešenja:**

Na početku se obavlja učitavanje svih vrednosti (a*,* b i c) i uzima se da je vrednost a najveća (max = a). Zatim se proverava da li je vrednost b veća od trenutne maksimalne vrednosti. Ukoliko jeste, b postaje novi maksimum. Ukoliko nije, prelazi se na sledeću proveru. Proverava se da li je c veće od trenutnog maksimuma. Ukoliko jeste c postaje novi maksimum. Ukoliko nije maksimum je neka od prethodnih vrednosti, pa sa obavlja emitovanje max vrednosti. Na kraju programa, unutar max vrednosti biće upisana maksimalna od tri ulazne vrednosti.

Na samom početku max može biti bilo koja od 3 ulazne vrednosti (ne mora to da bude baš a, može i b ili c). Postupak određivanja maksimalne vrednosti je identičan u svakom slučaju i upoređivanja se mogu vršiti bilo kojim redosledom.

### Multimedija

 [![](https://multimedia.dizajn-akademija.com/sr//Core_Java_Programming/multimedijaFinal/JCPR1_03.thb) JCPR1\_03.Mp4](https://www.link-elearning.com/linkdl/usersPortal/ "JCPR1_03.Mp4")

Kako Vam mogu pomoći?