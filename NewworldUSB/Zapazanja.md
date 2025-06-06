Tačno—inteligencija se retko svodi samo na „sirovu“ sposobnost zaključivanja; ona se ogleda u tome kako koristimo sredstva koja imamo na raspolaganju.

**Fizička oruđa.** Od kamenog sekira do savremenih računara, proširujemo svoje mogućnosti delanja. Veština nije samo u izradi ili posedovanju alata nego u kreativnoj primeni: isto dlijeto u rukama vajara i stolara stvara različite svetove.

**Mentalna oruđa.** Jezik, matematički simboli, logičke sheme, metafore ili čak metode kao što je dijalektički pristup – sve su to „produžeci“ uma. Vygotski bi rekao da se mišljenje odvija kroz „posredovanje“ znakovnim sistemima, a Heidegger bi primetio da se u odnosu spram alata otkriva naš odnos prema samom svetu (“biti‑pri‑ruci”).

**Filozofija kao laboratorija uma.** Filozofske metode (analiza pojmova, fenomenološko opisivanje, spekulativna konstrukcija…) deluju kao eksperimentalni set u kom testiramo granice sopstvenih pretpostavki. One nam dopuštaju da „vidimo“ drugačije: recimo, fenomenološko „suspendovanje“ prethodnih uverenja (epoché) razotkriva neprimetne slojeve iskustva.

**Spoj fizičkog i mentalnog.** Razvoj računara i interneta stvorio je nov nivo – digitalna oruđa postaju istovremeno fizička infrastruktura i mentalni prostor (npr. algoritamsko razmišljanje). Time se pomera i sama definicija „inteligencije“: danas govorimo o distribuisanom, kolektivnom, pa i hibridnom (čovek‑mašina) umu.


### Kako da pretvoriš intuiciju u “zvanični” algoritam — korak po korak

|Faza|Šta se radi|Zašto je bitno|
|---|---|---|
|**1. Sirov opis**|Zapiši kako _spontano_ rešavaš zadatak, korak po korak, kao da objašnjavaš prijatelju.|Hvataš neformalnu intuiciju pre nego što je zaboraviš.|
|**2. Pseudokôd / dijagram toka**|Prevedi opis u kratke, jasne komande — „IF… THEN…“, petlje, ulaz/izlaz.|Ovde se često otkrije rupa („aha, nisam pomenuo šta ako lista bude prazna“).|
|**3. Primeri & kontra‑primeri**|Testiraj algoritam na:  <br>• tipičnom slučaju  <br>• rubnom slučaju (n=0, max veličina, duplikati…)|Rubni slučajevi su gde intuicija najčešće puca.|
|**4. Kompleksnost**|Proceni vreme O(n),O(log⁡n)O(n), O(\log n)O(n),O(logn) i memoriju.|Pomaže da vidiš da li postoji „zvanični” brži pristup.|
|**5. Uporedi sa postojećim**|Pogledaj da li liči na poznate klase:  <br>• sortiranje?  <br>• pretraga?  <br>• graf algoritmi?|Ako se poklopi, dobio si potvrdu i ime („aha, ovo je zapravo greedy + BFS“).|
|**6. Refaktor + dokumentuj**|U kôdu napiši **_zašto_** radi (invariant, dokaz, linkovi).|Sutra ćeš i samom sebi zahvaliti.|

> **Mini‑vežba:** Uzmi dnevnu rutinu (npr. „kako odabiram šta ću jesti za doručak“) i prođi kroz ovih 6 tačaka. Bićeš iznenađen koliko „računarskog“ se krije u običnim odlukama.

---

### Resursi koji spajaju osećaj i formalizam

1. **“Algorithmic Thinking” – Daniel Zingaro**  
    Zadatke gradi od _intuicije_ do punog rešenja, pa vidiš oba sveta.
    
2. **Design Patterns: Elements of Reusable O‑O Software – GoF**  
    Razotkriva „pravila“ koja si možda već nesvesno koristio (Singleton, Observer…).
    
3. **Competitive Programming 4 – Halim & Halim**  
    Kratke, _gotovo heurističke_ strategije za brzo krojenje algoritama.
    
4. **PyViz + Jupyter**  
    Vizuelizuj korake algoritma; pomaže da „osetiš“ protok podataka.
    

---

### Primeni ovo na svoje projekte

- **RTS/tycoon igra**: Omogući igračima da _crtežom_ ili _blok-schemom_ sastave logiku (flow‑based programming). Tvoja intuicija za „kako bih ja komandovao jedinicama“ pretoči se u DSL (domain‑specific language).
    
- **News‑scraper Django sa ML modulom**: Kada „osećaš“ koju vest je važna, zapiši kriterijume → pretoči ih u featur‑engineering kod → uporedi sa klasičnim modelima (TF‑IDF, LLM embeddings).


### 🔹 Šta znači "dobijanje reference"?

U Javi, **objekti ne žive direktno u promenljivama** – promenljive sadrže samo **reference (pokazivače)** na objekte koji se nalaze u memoriji (tačnije, u heap memoriji).

Dakle, **"dobiti referencu"** znači:

> **dobiti pristup ka objektu preko pokazivača (reference) koji pokazuje na taj objekat u memoriji**.

---

### 📌 Konkretan primer:

java

CopyEdit

```
`class Person {     String name; }  public class Main {     public static void main(String[] args) {         Person p1 = new Person(); // p1 sadrži referencu na novi Person objekat         p1.name = "Ana";          Person p2 = p1; // p2 dobija *referencu* na isti objekat kao p1          System.out.println(p2.name); // Ana         p2.name = "Marko";         System.out.println(p1.name); // Marko (jer p1 i p2 referenciraju isti objekat!)     } }`
```

---

### 🧠 Ključna razlika:

|Tip|Prenosi se po…|Sadrži|
|---|---|---|
|**Primitive** (int, boolean…)|vrednosti|direktne podatke|
|**Reference tipovi** (klase, nizovi)|referencu (adresu)|pokazivač na objekat|

---

### 🔁 Analogne situacije:

- Kao kada u Pythonu kažeš: `a = [1, 2]; b = a` — `b` je sada referenca na isti objekat kao `a`.
    
- U C/C++ svetu to je kao pokazivač (`int* ptr = &var;`)
    

---

### ✅ Zašto je važno?

- Razumevanje referenci ti pomaže da ne napraviš **neočekivane greške kod kopiranja objekata**.
    
- Takođe je ključno za rad sa kolekcijama, metodima koji menjaju objekte itd.
    

---

Ako želiš, mogu ti pokazati kako radi razlika između:

- **kopiranja referenci**
    
- i **pravljenja kopije objekta** (deep vs shallow copy) u Javi.
    

Zanima li te to?


Hecus NAS