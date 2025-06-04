## onus: Serial Number Logging Tip

Now that you’ve confirmed the disk is:

- ✅ Detected
    
- ✅ Serial Number is known MARTUDM - HDD S.M.A.R.T. Viewer 2.00
    
- ✅ Wiped (confirmed in KillDisk)
    

You can create a log like:

yaml

CopyEdit

`Serial: 123456789012 Model: Maxtor 6Y080L0 Status: ✅ WIPED - UNALLOCATED (Confirmed via KillDisk) Date: 2024-04-02`

---

Want me to generate a printable log sheet or .txt template for tracking multiple drives like this? Just say the word. 🔐💾

### 🔍 Šta znači kad BIOS kaže:

- **SATA 1: ATAPI iHAS122**
    
- **SATA 2, 3, 4...: Not Detected**
    

---

### ✅ SATA 1: ATAPI iHAS122

- To je **DVD/CD čitač/pisač** (Lite-On iHAS122 je poznat model optičkog drajva).
    
- BIOS **ga vidi**, što znači da:
    
    - Napajanje i SATA konekcija rade
        
    - BIOS ga uspešno detektuje
        

---

### ❌ Ostali SATA portovi: "Not Detected"

- To znači da **ništa nije povezano** ili da **BIOS ne može da prepozna uređaj**.
    
- Najčešće se odnosi na **HDD ili SSD** koji **nije detektovan**.
    

---

### 📋 Mogući razlozi zašto hard disk nije prepoznat:

1. **Nema napajanja** do HDD/SSD-a
    
2. **SATA kabl** nije dobro povezan ili je neispravan
    
3. **SATA port** na ploči je pokvaren
    
4. Disk je **pokvaren** ili ne funkcioniše
    
5. U BIOS-u je isključen određeni SATA port
    
6. Ponekad BIOS traži "Auto Detect" – pa nije pokrenuo automatsko otkrivanje
    
7. Ako je NVMe SSD – ne prikazuje se kao SATA uopšte
    

---

### 🛠️ Šta možeš da probaš:

- Proveri da li se **disk okreće** (kod HDD-a možeš čuti vibraciju)
    
- Proveri SATA i naponski kabl, izvuci i ponovo priključi
    
- Probaj drugi SATA port na ploči
    
- Probaj drugi kabl (ako imaš rezervni)
    
- Udji u BIOS i vidi da li postoji "Detect Drives" opcija
    
- Ako je noviji SSD/NVMe – proveri pod "PCIe" ili "M.2" sekcijom u BIOS-u
    

---

Ako hoćeš, mogu te voditi korak po korak kroz dijagnostiku, samo mi reci koji je model diska i matične ploče (ili laptop ako je laptop).