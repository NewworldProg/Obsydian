<pre> ```mermaid erDiagram 
ZAPOSLENI ||--o{ EVIDENCIJA : has MESEC ||--o{ EVIDENCIJA : covers ZAPOSLENI { int id PK string ime string prezime } 
MESEC { int id PK string naziv } 
EVIDENCIJA { int id PK date datum string status int zaposleni_id FK int mesec_id FK } ``` </pre>
