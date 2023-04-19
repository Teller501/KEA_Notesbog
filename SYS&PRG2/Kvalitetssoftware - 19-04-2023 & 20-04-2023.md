# Kvalitetssoftware - 19-04-2023 & 20-04-2023

* Fag: SYS/PRG 2
* Oprettet: April 18, 2023 12:55 PM
* Type: Forberedelse

# Cookies

Når du besøger en hjemmeside, kan den gemme en lille tekstfil på din computer, kaldet en cookie. Cookies kan indeholde information om dine præferencer og tidligere handlinger på hjemmesiden, såsom sprogvalg, log ind-information og indhold i din indkøbskurv.

Dette kan være praktisk for dig, fordi hjemmesiden kan huske dine indstillinger, når du vender tilbage. Hvis du for eksempel indtaster dit navn og din e-mailadresse på en hjemmeside, kan den gemme disse oplysninger i en cookie, så du ikke behøver at indtaste dem igen næste gang, du besøger siden.

Der er dog også nogle ulemper ved cookies. Nogle cookies kan bruges til at spore din adfærd på tværs af forskellige hjemmesider og samle oplysninger om dig, som kan bruges til at vise dig målrettede annoncer eller til andre formål. Derfor kan det være en god idé at være opmærksom på, hvilke cookies du tillader på din computer.

Husk på, at du altid kan slette cookies fra din computer, hvis du ikke ønsker at gemme oplysningerne.

## Cookie-based Authentication

Cookie-baseret godkendelse bruges ofte, når du logger ind på en hjemmeside. Når du indtaster dine loginoplysninger, gemmer webserveren dine oplysninger i en cookie på din computer. Næste gang du besøger hjemmesiden, kan den bruge denne cookie til at autentificere dig automatisk uden at du behøver at indtaste dine loginoplysninger igen. Dette gør loginprocessen hurtigere og mere bekvem for brugeren.

Det er vigtigt at bemærke, at cookies kan være sårbare over for forskellige former for angreb, såsom cross-site scripting (XSS) og cross-site request forgery (CSRF). Derfor er det vigtigt, at hjemmesider implementerer sikkerhedsforanstaltninger for at beskytte brugerdata og forhindre uautoriseret adgang til brugerkonti.

Cookie-baseret godkendelse bruges ofte, når du logger ind på en hjemmeside, f.eks. din netbank. Når du indtaster dine loginoplysninger, gemmer webserveren dine oplysninger i en cookie på din computer. Næste gang du besøger netbankens hjemmeside, kan den bruge denne cookie til at autentificere dig automatisk uden at du behøver at indtaste dine loginoplysninger igen. Dette gør loginprocessen hurtigere og mere bekvem for brugeren.

Det afhænger af netbankens politik for cookies. Nogle netbanker vil slette login-cookies efter en vis periode med inaktivitet, mens andre vil beholde dem i en længere periode. Det er en god idé at undersøge netbankens cookie-politik for at få mere information om, hvordan de håndterer cookies.

For eksempel kan din netbank have en politik om at slette login-cookies efter 15 minutters inaktivitet på din konto for at beskytte dine oplysninger mod uautoriseret adgang.

## Cookies & Sessions

Både cookies og sessions bruges til at gemme information om en bruger på en hjemmeside. Cookies gemmes på brugerens computer, mens sessions gemmes på serveren.

Når en bruger besøger en hjemmeside, kan hjemmesiden gemme en cookie på brugerens computer med information om brugerens præferencer og adfærd på hjemmesiden. Når brugeren besøger hjemmesiden igen, kan hjemmesiden bruge denne cookie til at tilpasse indholdet og gøre brugeroplevelsen mere personlig.

Sessions bruges typisk til at gemme midlertidige data, såsom loginoplysninger eller indhold i en indkøbskurv. Når en bruger logger ind på en hjemmeside, kan serveren oprette en sessions-id, som gemmes på serveren. Når brugeren navigerer på hjemmesiden, kan hjemmesiden bruge sessions-id'et til at hente og gemme data om brugeren, såsom indhold i indkøbskurven.

Sessions er normalt mere sikre end cookies, fordi de gemmes på serveren i stedet for brugerens computer. Dette betyder også, at sessions normalt udløber efter en vis periode med inaktivitet for at beskytte brugerdata og forhindre uautoriseret adgang til brugerkonti.

I praksis bruger hjemmesider normalt både cookies og sessions til at gemme information om brugere og tilpasse indholdet.

Cookies kan også gemmes på serveren, men de er normalt klient-baserede og gemmes på brugerens computer.

Sessions er normalt server-baseret og gemmes på serveren i modsætning til cookies, som gemmes på brugerens computer.

# Database Transactions

En database transaction er en samling af én eller flere databasemodifikationer, der skal udføres som én enhed. En transaktion skal være enten fuldstændig fuldført eller rullet tilbage, hvis der opstår en fejl under udførelsen. Dette sikrer, at databasen forbliver i en konsistent tilstand og undgår ufuldstændige eller inkonsekvente modifikationer. Transaktioner bruges ofte i applikationer, der involverer flere brugere, der samtidig ændrer data i databasen, og hvor det er vigtigt at opretholde dataintegriteten.

En praktisk anvendelse af database-transaktioner kan ses i en webshop-applikation. Når en bruger køber en vare, skal der foretages flere modifikationer i databasen, herunder at trække varens beholdning og at oprette en ny ordre i systemet.

Hvis en fejl opstår under denne proces, f.eks. hvis varebeholdningen ikke er tilstrækkelig eller hvis der er problemer med betalingen, skal transaktionen rulles tilbage for at undgå inkonsekvente data i databasen.

Ved at bruge database-transaktioner kan applikationen sikre, at alle modifikationer udføres som en enhed og enten fuldføres eller rulles tilbage i tilfælde af fejl, hvilket sikrer, at databasen forbliver i en konsistent tilstand.

## ACID

ACID er en forkortelse for fire krav, som en transaktion skal opfylde for at sikre datakonsistens i en database. ACID står for Atomicity, Consistency, Isolation og Durability.

### Atomicity

Atomicity sikrer, at en transaktion udføres som én enhed. Enten udføres alle dele af transaktionen, eller også rulles hele transaktionen tilbage, hvis der opstår en fejl. På den måde sikrer man, at databasen er i en konsistent tilstand.

**Eksempel**: En bankoverførsel er en transaktion, der består af to dele - trækning af beløb fra afsenderens konto og indsættelse af beløbet på modtagerens konto. Hvis en af disse dele fejler, skal hele transaktionen rulles tilbage, således at hverken afsender eller modtager mister penge.

### Consistency

Consistency sikrer, at en transaktion ikke kan efterlade databasen i en inkonsistent tilstand. Hvis en transaktion udfører flere modifikationer af databasen, skal alle disse modifikationer udføres korrekt, eller også skal transaktionen rulles tilbage.

**Eksempel**: En database, der indeholder data om lagerbeholdning og salg, skal opretholde konsistente data, således at varelageret altid svarer til de solgte varer. Hvis en transaktion, der trækker varer fra lageret og registrerer et salg, fejler, skal hele transaktionen rulles tilbage for at undgå inkonsistente lagerdata.

### Isolation

Isolation sikrer, at transaktioner udføres parallelt uden at påvirke hinanden. Hvis flere transaktioner udføres samtidigt, skal de ikke interferere med hinanden, og databasen skal stadig være i en konsistent tilstand.

**Eksempel**: Hvis to brugere forsøger at opdatere samme produkt på en webshop, skal transaktionerne udføres i isolation, så de ikke påvirker hinandens data. Hvis transaktionerne ikke udføres i isolation, kan det føre til inkonsistente lagerdata eller tab af data.

### Durability

Durability sikrer, at transaktioner, der er fuldført, er permanente og ikke kan mistes på grund af systemfejl. Det betyder, at når en transaktion er fuldført, skal dens virkninger være varige og overleve eventuelle systemfejl.

**Eksempel**: Hvis en transaktion, der registrerer et salg, er fuldført, skal salget være permanent og ikke kunne mistes på grund af en systemfejl. Hvis en systemfejl opstår, mens transaktionen er i gang, skal den enten fuldføres eller rulles tilbage for at opretholde databasens konsistens.

## Hvorfor

Database transaktioner er vigtige for et software program, fordi de sikrer databasens dataintegritet og konsistens. En database transaktion er en samling af en eller flere databasemodifikationer, der skal udføres som én enhed. Hvis der opstår en fejl under udførelsen, skal transaktionen rulles tilbage, så databasen forbliver i en konsistent tilstand.

Dette er særligt vigtigt i applikationer, der involverer flere brugere, der samtidig ændrer data i databasen, hvor det er vigtigt at opretholde dataintegriteten og undgå ufuldstændige eller inkonsekvente modifikationer. Ved at bruge database transaktioner kan applikationen sikre, at alle databasemodifikationer udføres som én enhed og enten fuldføres eller rulles tilbage i tilfælde af fejl, hvilket sikrer, at databasen forbliver i en konsistent tilstand.

For yderligere at sikre databasens dataintegritet og konsistens, skal transaktioner opfylde de såkaldte ACID-krav, som står for Atomicity, Consistency, Isolation og Durability. Disse krav sikrer, at databasen altid er i en konsistent tilstand og undgår inkonsekvente data og data-tab i tilfælde af systemfejl.

# Testing

[Testing Level Dynamics: Achieving Confidence From Testing](https://dzone.com/articles/testing-level-dynamics-achieving-confidence-from-t?edition=596292&utm_campaign=&utm_content=How%20does%20SAFe%20differ%20from%20LeSS%3F&utm_medium=email&utm_source=dzone&utm_term=)

Der er to hovedkategorier af test, når det kommer til softwaretestning: *dybde* og *bredde*. Dybde-tests er mere detaljerede og omfattende tests, der normalt udføres manuelt, mens bredde-tests er hurtigere og mere overfladiske tests, der kan udføres automatisk.

Når man vælger at udføre dybde-tests, fokuserer man på at teste et mindre antal funktioner eller aspekter af applikationen meget grundigt. Disse tests er ofte manuelle og kan tage betydelig tid at gennemføre. På den anden side fokuserer man i bredde-tests på at teste så mange funktioner og aspekter som muligt, men på en mere overfladisk måde. Disse tests kan ofte automatiseres og kan udføres meget hurtigt.

Når man vælger at udføre dybde-tests, vælger man normalt at fokusere på de mest kritiske aspekter af applikationen, hvor der er den største risiko for fejl. På den anden side kan bredde-tests udføres på hele applikationen og er derfor velegnede til at fange mindre fejl eller problemer i mindre kritiske områder.

Det er vigtigt at bemærke, at både dybde- og bredde-tests er vigtige og bør anvendes i kombination for at opnå en god testdækning. Dybde-tests kan fange store og kritiske fejl, mens bredde-tests kan fange mindre fejl og sikre, at applikationen fungerer som forventet i forskellige scenarier.

Som en generel regel bør man udføre dybde-tests i starten af en testcyklus, mens man udfører bredde-tests senere i cyklussen. Dette sikrer, at de mest kritiske fejl fanges tidligt, mens mindre kritiske fejl fanges senere.

## Levels of Testing: Speed vs Scope

Når man planlægger en teststrategi, er det vigtigt at overveje både hastighed og omfang af testene. Hastighed refererer til, hvor hurtigt tests kan udføres, mens omfang refererer til, hvor mange tests der kan udføres.

Hvis man har brug for at udføre mange tests i en kort periode, er det vigtigt at vælge tests, der kan udføres hurtigt, selvom det betyder, at man må nøjes med en mindre testdækning. På den anden side, hvis man har mere tid til rådighed, kan man vælge at udføre flere tests, der dækker flere aspekter af applikationen.

Det er vigtigt at finde den rette balance mellem hastighed og omfang af testene, så man kan opnå en god testdækning uden at bruge for meget tid på testning. Det kan også være en god idé at prioritere testene efter deres vigtighed og risiko, så man fokuserer på de mest kritiske tests først.

Der findes fire hovedtyper af softwaretests: unit-tests, integrationstests, systemtests og acceptancetests.

- **Unit-tests** er tests af de mindste dele af koden, såsom individuelle metoder eller funktioner. Disse tests udføres normalt automatisk og er hurtige og billige at udføre. Unit-tests er vigtige for at sikre, at koden fungerer som forventet i mindste detalje.
- **Integrationstests** tester, hvordan forskellige dele af koden fungerer sammen. De kan udføres på forskellige niveauer, f.eks. integration af klasser, komponenter eller systemer. Formålet med integrationstests er at identificere fejl eller uoverensstemmelser i samspillet mellem forskellige dele af koden.
- **Systemtests** er tests af hele systemet, inklusive brugergrænsefladen og alle dets funktioner. Disse tests udføres normalt manuelt og er mere omfattende end unit-tests og integrationstests. Formålet med systemtests er at identificere fejl eller mangler i systemet som helhed.
- **Acceptancetests** er tests, der udføres for at sikre, at systemet opfylder kundens krav og forventninger. Disse tests kan udføres manuelt eller automatisk og er normalt sidste trin i testprocessen, før systemet frigives til kunden. Formålet med acceptancetests er at sikre, at systemet fungerer som forventet og opfylder de krav og forventninger, som kunden har angivet.

Det er vigtigt at udføre alle fire typer tests for at sikre en høj kvalitet af softwaren. Unit-tests og integrationstests kan udføres tidligt i udviklingsprocessen for at identificere fejl eller uoverensstemmelser tidligt og spare tid og ressourcer senere i processen. Systemtests og acceptancetests udføres normalt senere i processen, når systemet er mere stabilt og klar til at blive testet som en helhed.
