# Miniprojekt

- **Fag:** Tværfaglig
- **Oprettet:** March 25, 2023 10:49 AM
- **Type:** Opgave

# Opgavebeskrivelse

[Miniprojekt forår2023.docx](Miniprojekt%200a519d2f04d8476fa49a563700748a85/Miniprojekt_forr2023.docx)

# Forberedelse

## **Krav 1: Implementering af Continuous Integration og Continuous Delivery (CI/CD)**

**Continuous Integration (CI):** Dette henviser til praksis med automatisk at bygge og teste din kode, hver gang der foretages ændringer i den. Dette sikrer, at koden forbliver funktionel, og at eventuelle problemer opfanges tidligt i udviklingsprocessen. For at implementere dette krav skal du oprette en GitHub Actions-arbejdsgang, der udløses af Pull Requests eller nye commits til hoved/mastergrenen. Arbejdsgangen skal indeholde trin til at opbygge og teste koden, f.eks. ved at køre enhedstests eller integrationstests.

**Continuous Delivery (CD):** Dette henviser til praksis med automatisk at distribuere din kode til et produktionsmiljø, når den har bestået alle tests. Dette sikrer, at alle ændringer, der foretages i koden, hurtigt bliver gjort tilgængelige for brugerne. For at implementere dette krav skal du oprette en GitHub Actions-arbejdsgang, der distribuerer koden til et cloud-miljø (f.eks. en Docker-container eller en PaaS), når den har bestået alle test.

## **Krav 2: Dokumenter dit projekt i dit GitHub repository**

Dette krav involverer at skabe dokumentation for dit projekt og inkludere det i dit GitHub repository. Konkret skal du inkludere:

### En README.md fil, der fokuserer på onboarding af brugere og forklarer, hvordan man bruger din applikation.

En god README-fil er vigtig for ethvert softwareprojekt, da den giver et overblik over projektet, hvordan det installeres og bruges, og andre relevante oplysninger. Her er en generel struktur, som du kan følge for en god README-fil:

1. **Projektets titel:** En klar og præcis titel for projektet: Projekttitel: En klar og præcis titel for projektet.
2. **Beskrivelse:** En kort beskrivelse af projektet, der omfatter dets formål og funktionalitet.
3. **Kom i gang:** Dette afsnit bør indeholde trinvise instruktioner om, hvordan projektet kan komme i gang. Dette bør omfatte eventuelle nødvendige softwareafhængigheder, installationsinstruktioner og konfigurationsmuligheder.
4. **Anvendelse:** Dette afsnit bør indeholde instruktioner om, hvordan projektet anvendes, herunder eventuelle kommandoer eller funktioner, der kan køres, og hvad de gør.
5. **Licens:** Dette afsnit bør indeholde projektets licens og eventuelle relevante oplysninger om ophavsret.
6. **Kontakt:** Dette afsnit bør indeholde kontaktoplysninger for projektets vedligeholdere, hvis brugerne har spørgsmål eller problemer.

<aside>
💡 Her er nogle yderligere tips til at skrive en god README-fil:

</aside>

**Hold den kortfattet:** Prøv at holde README-filen så kort og præcis som muligt, samtidig med at den indeholder alle de nødvendige oplysninger.

**Brug formatering:** Brug overskrifter, lister og andre formateringsværktøjer for at gøre filen let at læse og navigere i.

**Medtag eksempler:** Hvis det er muligt, skal du medtage eksempler på, hvordan projektet kan bruges, f.eks. kodestumper eller skærmbilleder.

**Hold den opdateret:** Sørg for at opdatere README-filen efterhånden som projektet udvikler sig, så den altid afspejler projektets aktuelle tilstand.

**Links:**
[https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/) - indeholder en detaljeret vejledning i at skrive en god README-fil, herunder en skabelon, som du kan bruge.

### En CONTRIBUTE.md fil, der fokuserer på onboarding af teammedlemmer og forklarer, hvordan man bidrager til dit projekt.

CONTRIBUTE.md-filen er en vigtig del af ethvert open source-projekt, da den giver vejledning til andre udviklere, som ønsker at bidrage til projektet. Her er en generel struktur, som du kan følge for en god CONTRIBUTE.md-fil:

1. **Introduktion:** Dette afsnit bør indeholde en kort introduktion til projektet, og hvorfor bidrag er velkomne.
2. **Forudsætninger:** Dette afsnit bør indeholde en liste over software eller værktøjer, som bidragyderne skal installere for at kunne bidrage til projektet.
3. **Kom i gang:** Dette afsnit bør indeholde trinvise instruktioner om, hvordan man bidrager til projektet, herunder hvordan man opsætter udviklingsmiljøet, hvordan man kloner repositoriet, og hvordan man foretager ændringer i koden.
4. **Retningslinjer:** Dette afsnit bør indeholde retningslinjer for indsendelse af fejlrapporter, anmodninger om funktioner og pull requests. Dette bør omfatte oplysninger om, hvordan pull requests skal formateres, hvordan man skriver tests og andre retningslinjer, der er specifikke for projektet.
5. **Adfærdskodeks:** Dette afsnit bør indeholde projektets adfærdskodeks og alle relevante oplysninger om, hvordan man rapporterer overtrædelser af adfærdskodeksen.
6. **Kontakt:** Dette afsnit bør indeholde kontaktoplysninger til projektets vedligeholdere, hvis bidragyderne har spørgsmål eller problemer.

<aside>
💡 Her er nogle yderligere tips til at skrive en god CONTRIBUTE-fil:

</aside>

**Hold det kortfattet:** Ligesom README-filen skal du forsøge at holde CONTRIBUTE.md-filen så kort og kortfattet som muligt.

**Vær imødekommende:** Brug et venligt og imødekommende sprog for at tilskynde andre udviklere til at bidrage.

**Giv eksempler:** Hvis det er muligt, skal du give eksempler på gode fejlrapporter, anmodninger om funktioner eller pull requests for at hjælpe andre udviklere med at vejlede dem.

**Hold den opdateret:** Sørg for at opdatere CONTRIBUTE.md-filen efterhånden som projektet udvikler sig, så den altid afspejler projektets aktuelle tilstand.

**Links:**

[https://opensource.guide/how-to-contribute/](https://opensource.guide/how-to-contribute/) - indeholder en detaljeret vejledning i, hvordan du bidrager til open source-projekter, herunder hvordan du finder projekter, hvordan du opretter udviklingsmiljøet, og hvordan du bidrager.

[https://brainhub.eu/blog/open-source-documentation-tips](https://brainhub.eu/blog/open-source-documentation-tips) - indeholder generelle tips om at skrive open source-dokumentation, herunder CONTRIBUTE.md-filer.

### En ER-model af database-designet, som er en konceptuel model af, hvordan din database er struktureret.

You can create Entity-Relationship (ER) diagrams using Mermaid syntax in Markdown files. Here's how you can do it:

1. Først skal du have Mermaid-biblioteket installeret. Du kan enten installere det lokalt på din computer eller bruge et CDN-link i din Markdown-fil. Du kan finde installationsvejledninger på Mermaid-webstedet: **[https://mermaid-js.github.io/mermaid/#/installation](https://mermaid-js.github.io/mermaid/#/installation)**
2. I din Markdown-fil opretter du en kodeblok og indstiller sproget til "mermaid". Du kan bruge følgende syntaks til at oprette et ER-diagram:
    
    ```mermaid
    erDiagram
       CUSTOMER ||--o{ ORDER : places
       ORDER ||--|{ LINE-ITEM : contains
       PRODUCT }|--|{ LINE-ITEM : comprises
       CUSTOMER }|--|{ DELIVERY-ADDRESS : uses
    ```
    
3. Du kan tilpasse diagrammet yderligere ved at bruge forskellige Mermaid-syntakselementer. Her er et eksempel på et mere komplekst ER-diagram:
    
    ```mermaid
    erDiagram
       CUSTOMER {
          int customer_id
          string name
          string email
          date created_at
          date updated_at
       }
       ORDER {
          int order_id
          int customer_id
          date order_date
          date shipped_date
          string status
          date created_at
          date updated_at
       }
       LINE-ITEM {
          int line_item_id
          int order_id
          int product_id
          int quantity
          float price
          date created_at
          date updated_at
       }
       PRODUCT {
          int product_id
          string name
          string description
          float price
          date created_at
          date updated_at
       }
    
       CUSTOMER ||--o{ ORDER : places
       ORDER ||--|{ LINE-ITEM : contains
       PRODUCT }|--|{ LINE-ITEM : comprises
       CUSTOMER }|--|{ DELIVERY-ADDRESS : uses
    ```
    

**Links:**

[https://mermaid.js.org/syntax/entityRelationshipDiagram.html](https://mermaid.js.org/syntax/entityRelationshipDiagram.html) - Dokumentation

[https://coda.io/@leandro-zubrezki/diagrams-and-visualizations-using-mermaid/entity-relationship-7](https://coda.io/@leandro-zubrezki/diagrams-and-visualizations-using-mermaid/entity-relationship-7)

### En klassediagram som endelig dokumentation af programdesignet. Dette diagram bør ikke være autogenereret og ulæseligt, men på et detaljeniveau, hvor andre programmører faktisk vil være i stand til at bruge det til at få et overblik over systemet.

1. **Brug et program:** Visual Paradigm, Diagrams.net
2. **Hold det enkelt:** Det er vigtigt at medtage alle relevante klasser og relationer i dit diagram, men du må ikke overvælde læserne med for mange oplysninger. Fokuser på de vigtigste klasser og relationer, og udelad alle dem, der ikke er vigtige for at forstå strukturen i dit program.
3. **Brug klare og præcise labels:** De labels, du bruger til hver klasse og relation, skal være klare og præcise. Undgå at bruge teknisk jargon, som måske ikke er kendt af alle læsere. Brug beskrivende betegnelser, der formidler formålet med hver klasse og relation.
4. **Grupper klasser sammen:** Hvis du har flere klasser, der er relateret til hinanden, skal du gruppere dem sammen i dit diagram. Dette vil hjælpe læserne med at forstå relationerne mellem klasserne lettere.
5. Brug UML
6. **Giv yderligere kontekst:** Du kan også give yderligere kontekst i din dokumentation, selv om klassediagrammet skal give et overblik på højt niveau over klassestrukturen og relationerne. Du kan f.eks. give en kort forklaring på hver klasse og dens formål eller beskrive, hvordan klasserne arbejder sammen for at udføre specifikke opgaver.

## Krav 3: Feasibility Study

Kravet om et feasibility studie indebærer at man undersøger, om ens projekt er muligt at gennemføre. I denne sammenhæng skal du lave et slide deck (diasshow), som skal præsenteres mundtligt i virksomhedsfaget. Her er nogle trin, der kan hjælpe dig med at gennemføre et feasibility studie:

1. **Definer problemet:** Start med at definere det problem, som dit projekt forsøger at løse.
2. **Identificer målgruppen:** Identificer hvem dit projekt henvender sig til, og hvad deres behov og ønsker er.
3. **Identificer konkurrenterne:** Identificer konkurrenter og vurder deres styrker og svagheder.
4. **Foretag en SWOT-analyse:** Analyser dine egne styrker, svagheder, muligheder og trusler (SWOT) for at vurdere, om dit projekt er realistisk.
5. **Identificer ressourcer og krav:** Identificer de ressourcer, du har brug for, og de krav, du skal opfylde, for at gennemføre projektet.
6. **Foretag en risikovurdering:** Identificer potentielle risici og udvikl en plan for at håndtere dem.

Husk, at et feasibility studie ikke garanterere success, men det hjælper med at identificere potentielle problemer og risici, og giver dig mulighed for at tage skridt til at minimere dem.
