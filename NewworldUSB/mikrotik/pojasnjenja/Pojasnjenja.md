# Dynamic Public IP


## 🔄 **Šta znači “Dynamic Public IP”?**

To znači da tvoj MikroTik **automatski dobija javnu IP adresu** od tvog internet provajdera (ISP-a) — **bez da ti ručno podešavaš IP, DNS, gateway itd.**

---

## 📡 Kako to funkcioniše?

1. **Povežeš MikroTik na internet** (najčešće preko `ether1`, WAN port).
    
2. **Na tom portu uključiš DHCP klijenta**.
    
3. **MikroTik zatraži IP adresu od ISP-a**, i dobije sve što mu treba:
    
    - Javni IP (npr. 203.0.113.10),
        
    - DNS servere (npr. 8.8.8.8),
        
    - Default route (put do interneta),
        
    - NTP server (vreme).
        

---

## ✅ **Zašto je ovo korisno?**

- **Ne moraš ništa da kucaš ručno.**
    
- **Radi out-of-the-box** sa većinom internet provajdera.
    
- Ako ti ISP povremeno menja javnu IP adresu (što je često), MikroTik će to **automatski osvežiti**.
    

---

## 🛠️ Kako to izgleda u MikroTik (CLI primer):

Ako je `ether1` tvoj WAN port:

bash

CopyEdit

`/ip dhcp-client add interface=ether1 disabled=no`

U **Winbox-u**:

1. Idi na **IP > DHCP Client**.
    
2. Klikni **Add (+)**.
    
3. Izaberi interfejs (npr. `ether1`).
    
4. Očekuj da dobiješ IP adresu nakon par sekundi.
    

---

## 📌 VAŽNO:

Ovo se koristi **samo na strani prema internetu (WAN)** — **ne na LAN strani!**

- Na LAN strani ti _daješ_ IP adresu korisnicima (preko DHCP servera).
    
- Na WAN strani ti _dobijaš_ IP adresu od ISP-a (preko DHCP klijenta).
    

---

## 📡 DHCP klijent može dobiti:

### 1. ✅ **IP adresa**

- Javna IP adresa koju ti ISP dodeljuje.
    
- Primer: `203.0.113.57`
    

---

### 2. 🌐 **DNS serveri** (Domain Name System)

- Koriste se za prevod sa **domena u IP adrese**.
    
- Na primer, `google.com` ➝ `142.250.186.206`
    
- ISP može ti dodeliti svoje DNS servere, ili globalne kao:
    
    - `8.8.8.8` (Google DNS)
        
    - `1.1.1.1` (Cloudflare)
        

---

### 3. 🕓 **NTP serveri** (Network Time Protocol)

- Koriste se da tvoj MikroTik (i svi uređaji u mreži) imaju **tačno vreme**.
    
- Bitno za:
    
    - Logove
        
    - VPN protokole
        
    - Sertifikate i bezbednost
        
- Primer NTP servera: `time.google.com`, `pool.ntp.org`
    

---

### 4. 🚦 **Default route (Gateway / Default Gateway)**

- To je **put ka internetu**.
    
- DHCP klijent dobije info: „Za sve destinacije koje ne znaš — šalji kroz ovaj gateway.“
    
- Na primer: `0.0.0.0/0 via 203.0.113.1`
    

---

### Bonus: 🛑 **Možda, ali retko — WINS server**

- Windows-centrisani sistem za ime računara u lokalnoj mreži.
    
- Danas se vrlo retko koristi, ali može biti deo DHCP lease-a.
    

---

## 🧠 Zaključak:

Kad MikroTik dobije IP preko DHCP-a, dobija zapravo **čitav paket informacija**, koji uključuje:

|Parametar|Svrha|
|---|---|
|IP adresa|Tvoja javna adresa|
|DNS serveri|Za prevod domena|
|NTP serveri|Za sinhronizaciju vremena|
|Default route|Za izlazak na internet|

Sve ovo omogućava da MikroTik **radi bez dodatnog ručnog podešavanja**.

Ako želiš da vidiš šta tačno tvoj MikroTik dobija, mogu ti pokazati kako da to proveriš u **Winbox-u ili kroz CLI** komandu.