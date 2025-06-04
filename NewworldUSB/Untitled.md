## 📑 **Tabela najčešćih file potpisa**

| 🧾 Format     | 🧩 HEX Signature                         | 🔤 Tekstualni prikaz u Notepad++ | 📁 Pravi tip             |
| ------------- | ---------------------------------------- | -------------------------------- | ------------------------ |
| ZIP           | `50 4B 03 04`                            | `PK`                           | `.zip`, `.docx`, `.xlsx` |
| RAR (v5)      | `52 61 72 21 1A 07 01`                   | `Rar!....`                       | `.rar`                   |
| PDF           | `25 50 44 46`                            | `%PDF`                           | `.pdf`                   |
| EXE (Windows) | `4D 5A`                                  | `MZ`                             | `.exe`                   |
| ELF (Linux)   | `7F 45 4C 46`                            | `.ELF`                           | izvršni fajl             |
| PNG           | `89 50 4E 47`                            | `.PNG`                           | `.png`                   |
| JPG           | `FF D8 FF`                               | n/a                              | `.jpg`                   |
| GIF           | `47 49 46 38`                            | `GIF8`                           | `.gif`                   |
| OGG           | `4F 67 67 53`                            | `OggS`                           | `.ogg`, `.oga`           |
| MP3           | `FF FB` (ili `49 44 33` ako ima ID3 tag) | n/a                              | `.mp3`                   |
| DOCX (Word)   | `PK` + `/word/` u strukturi            | kao ZIP                          | `.docx`                  |
| XLSX (Excel)  | `PK` + `/xl/` u strukturi              | kao ZIP                          | `.xlsx`                  |