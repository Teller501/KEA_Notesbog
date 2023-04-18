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
