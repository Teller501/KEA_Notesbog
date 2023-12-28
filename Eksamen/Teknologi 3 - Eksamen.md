# Spørgsmål 1
1. **Formålet med at bruge CI/CD (Continuous Integration/Continuous Delivery):**
   - **Integration:** CI sikrer løbende integration af kodeændringer fra forskellige udviklere i et hovedrepository. Dette reducerer integrationsproblemer og forbedrer softwarekvaliteten.
   - **Automatisering:** CI/CD automatiserer bygge- og testprocesser, hvilket øger effektiviteten og minimerer menneskelige fejl.
   - **Hurtig feedback:** CI/CD giver hurtig feedback på kodeændringer gennem automatiserede tests, hvilket hjælper med at identificere og rette fejl tidligt i udviklingsprocessen.
   - **Hurtigere levering:** CD muliggør hurtigere levering af nye funktioner og opdateringer til slutbrugere, hvilket forbedrer konkurrenceevnen og kundetilfredsheden.

2. **Hvad er en virtuel computer?**
   - En virtuel computer (VM) er en softwarebaseret simulering af en fysisk computer. Den kører et operativsystem og applikationer, som om den var en reel, fysisk maskine.
   - VM'er giver mulighed for at køre flere operativsystemer på én fysisk hardwarehost, hvilket optimerer ressourceanvendelsen.

3. **Hvad er en Cloud instance?**
   - En Cloud instance er en virtuel server i skyen, som bruges til at køre applikationer og services.
   - Den leveres og styres gennem en skyudbyder som AWS, Azure, eller Google Cloud, hvilket giver fleksibilitet og skalerbarhed.

4. **Hvad er en Azure App Service?**
   - Azure App Service er en cloud-baseret hosting service fra Microsoft, designet til at lette udvikling, implementering og drift af webapplikationer.
   - Den understøtter flere sprog og rammer, herunder .NET, .NET Core, Java, Ruby, Node.js, PHP og Python, og tilbyder funktioner som autoskalerbarhed, integrerede sikkerhedsfunktioner og nem integration med andre Azure-tjenester.

5. **Hvad er GitHub Actions?**
   - GitHub Actions er en CI/CD platform integreret i GitHub, som automatiserer softwareudviklings-workflows direkte fra GitHub repositories.
   - Den tillader automatisering af processer som at bygge, teste og deploye applikationer baseret på git-begivenheder som push eller pull requests.

6. **Hvad er YAML?**
   - YAML (YAML Ain't Markup Language) er et data-serieliseringsformat, der bruges til konfigurationsfiler og dataudveksling. Det er kendt for sin læsbarhed og brugervenlighed.
   - Ofte bruges YAML til at definere konfigurationsfiler for forskellige udviklings-, automatiserings- og deploymentværktøjer.

7. **YAML vs JSON:**
   - **Læsbarhed:** YAML er generelt mere læsbar og brugervenlig sammenlignet med JSON.
   - **Format:** YAML understøtter kommentarer, mens JSON ikke gør. YAML bruger indrykning til at repræsentere datastrukturer, mens JSON bruger klemmer og citationstegn.
   - **Anvendelse:** JSON bruges ofte til web-API'er på grund af dens kompatibilitet med JavaScript. YAML bruges ofte til konfigurationsfiler og i situationer, hvor menneskelig læsbarhed er vigtig.

8. **Opsætning af CI/CD for automatisk byg, test og deploy ved nye commits:**
   - **Vælg et CI/CD værktøj:** Brug værktøjer som Jenkins, Travis CI, CircleCI eller GitHub Actions.
   - **Konfigurer et Repository:** Opsæt et repository i GitHub, GitLab eller lignende, og integrer det med dit CI/CD værktøj.
   - **Opret en konfigurationsfil:** Skriv en konfigurationsfil (ofte i YAML-format) for at definere bygge-, test- og deployeringsprocesser.
   - **Opsæt Triggere:** Konfigurer CI/CD-værktøjet til at udløse et nyt byg, når der sker et commit til en bestemt gren i repository.
   - **Automatiser Tests:** Implementer automatiserede tests, der skal køres ved hvert byg.
   - **Konfigurer Deployment:** Opsæt automatisk deployment til et test-, staging- eller produktionsmiljø efter et vellykket byg og test.
   - **Overvågning og Feedback:** Overvåg bygge- og deployeringsprocessen og sørg for feedbackmekanismer for hurtigt at identificere og løse eventuelle fejl.

# Spørgsmål 2
1. **Sådan oprettes en ny Cloud Instance:**
   - **Vælg en Cloud Udbyder:** Start med at vælge en cloud udbyder som AWS, Azure, eller Google Cloud.
   - **Opret en Konto:** Opret en konto hos udbyderen, hvis du ikke allerede har en.
   - **Naviger til Instance Management:** Log ind på cloud udbyderens dashboard og find sektionen for at administrere instances (virtuelle servere).
   - **Opret Ny Instance:** Vælg muligheden for at oprette en ny instance. Du vil typisk blive guidet gennem en opsætningsproces, hvor du kan vælge operativsystem, hardware-specifikationer (som CPU, hukommelse) og netværksindstillinger.

2. **Sådan forbinder du til en Cloud Instance:**
   - **Find Instance Information:** På dit cloud dashboard, find den instance, du vil forbinde til, og notér dens offentlige IP-adresse.
   - **Brug SSH (Secure Shell):** Til Linux-baserede systemer bruger du SSH for at oprette en sikker forbindelse. Du vil bruge kommandoen `ssh [brugernavn]@[IP-adresse]`, hvor du indsætter det relevante brugernavn og IP-adresse.

3. **Hvad er en Terminal?**
   - En terminal er et tekstbaseret interface til at interagere med dit operativsystem. Den tillader dig at køre kommandoer, administrere filer, og køre scripts.

4. **Hvad er en Webserver?**
   - En webserver er software (og den maskine den kører på), der håndterer HTTP-anmodninger fra klienter (som webbrowsere) og serverer dem webindhold, såsom HTML-sider, billeder og scripts.

5. **Hvad er en FTP-klient?**
   - En FTP-klient (File Transfer Protocol-klient) er et softwareværktøj, der bruges til at overføre filer mellem din lokale computer og en server på internettet.

6. **Håndtering af netværksadgang til en Cloud Instance:**
   - **Sikkerhedsgrupper:** Konfigurer sikkerhedsgrupper i din cloud instance for at styre, hvilken trafik der er tilladt ind og ud.
   - **VPN og Firewalls:** Brug VPN'er og firewall-regler for at sikre sikker og begrænset adgang.
   - **IP-Adresserestriktioner:** Begræns adgangen til bestemte IP-adresser for at øge sikkerheden.

7. **Demonstration:**
   - **Oprettelse af en ny Cloud Instance:** Følg trinene i punkt 1 for at vælge cloud udbyderen, oprette en konto, navigere til instance management og oprette en ny instance.
   - **Forbindelse til en Cloud Instance via Terminal:** Brug SSH til at oprette forbindelse til din instance. Åbn en terminal på din computer, og skriv `ssh [brugernavn]@[IP-adresse]`, hvor du erstatter med dit brugernavn og IP-adressen på din cloud instance.
   - **Brug FTP til at uploade en fil til Cloud Instance:**
     - **Installér FTP-klient:** Først skal du have en FTP-klient installeret på din computer, som FileZilla.
     - **Forbind til din server:** Åbn FTP-klienten, indtast serverens IP-adresse, dit brugernavn og password.
     - **Upload Fil:** Naviger til den ønskede mappe på serveren, og træk filen fra din computer til serveren for at uploade den.
    
# Spørgsmål 3
1. **Hvad er Docker?**
   - Docker er et værktøj designet til at lette oprettelsen, implementeringen og kørslen af applikationer ved brug af containere. Det gør det muligt at pakke en applikation med alle dens afhængigheder i en container, der kan flyttes fra et udviklingsmiljø til et produktionsmiljø.

2. **Hvad er en Dockerfile?**
   - En Dockerfile er en tekstfil, der indeholder en sekvens af instruktioner og kommandoer til at bygge et Docker image. Den definerer det miljø, din applikation vil køre i, herunder operativsystem, programmer, filer og konfigurationsindstillinger.

3. **Hvad er et Docker Image?**
   - Et Docker Image er en skabelon, der indeholder applikationskoden, biblioteker, værktøjer, afhængigheder og andre filer, der er nødvendige for at køre en applikation. Images bruges til at oprette Docker-containere.

4. **Hvad er en Docker Container?**
   - En Docker Container er en kørende instans af et Docker Image. Den indeholder alt, hvad der er nødvendigt for at køre applikationen, isoleret fra andre processer.

5. **Hvad er Maven?**
   - Maven er et projektstyrings- og forståelsesværktøj, der bruges primært til Java-projekter. Maven hjælper med projektbygning, afhængighedsstyring og andre aspekter af softwareprojektstyring.

6. **Hvad er en .jar-fil?**
   - En .jar-fil (Java ARchive) er en pakkefilformat, der bruges til at distribuere Java-applikationer eller biblioteker, der indeholder Java-klassefiler og tilknyttede metadata og ressourcer.

7. **Styring af porte på en Docker Container:**
   - Når du opretter eller kører en container, kan du bruge flagget `-p` til at definere portmapping mellem værtsmaskinen og containeren. For eksempel, `-p 80:80` vil mappe port 80 på værtsmaskinen til port 80 i containeren.

8. **Docker-kommandoer:**
   - **Byg et image:** `docker build -t [image-navn] .`
   - **Opret en container:** `docker run -d --name [container-navn] [image-navn]`
   - **Stop/start en container:** 
     - Stop: `docker stop [container-navn]`
     - Start: `docker start [container-navn]`
   - **List alle images:** `docker images`
   - **List alle containere:** `docker ps -a` (Tilføj `-a` for at se alle containere, inklusiv de stoppede)
   - **Slet et image:** `docker rmi [image-navn]`
   - **Slet en container:** `docker rm [container-navn]`

# Spørgsmål 4
1. **Hvorfor bruge Docker til at deploye applikationer?**
   - **Isolation:** Docker sikrer, at applikationer kører i et isoleret miljø, hvilket mindsker konflikter mellem forskellige applikationer.
   - **Konsistens:** Docker garanterer, at applikationen kører ens på forskellige miljøer, da den indeholder alle afhængigheder.
   - **Skalerbarhed:** Med Docker er det nemt at skalere applikationer ved at starte flere containere.
   - **Effektivitet:** Containere er lettere og hurtigere at starte end traditionelle virtuelle maskiner.

2. **Alternativer til brug af Docker:**
   - **Traditionelle Virtuelle Maskiner:** Hvor hver VM har sit eget fulde OS.
   - **Manuel Konfiguration:** Opsætning af applikationer direkte på servere uden containerisering.
   - **Andre Container Teknologier:** Som Kubernetes, LXD, eller Podman.

3. **Hvor på internettet kan vi finde forudbyggede Docker Images?**
   - **Docker Hub:** Den mest populære kilde til Docker images, der indeholder et stort udvalg af officielle og community-baserede images.
   - **GitHub Container Registry:** Et sted, hvor brugere og organisationer kan publicere deres containerimages.
   - **Andre registre:** Som Amazon Elastic Container Registry (ECR) og Google Container Registry (GCR).

4. **Hvordan kan du se output fra en kørende container?**
   - Brug kommandoen `docker logs [container-navn]` til at se logs/output fra en kørende container.

5. **Opsætning af en Docker Container til at køre en MySQL server:**
   - **Hent MySQL Image:** Brug `docker pull mysql` for at hente MySQL image fra Docker Hub.
   - **Start Container:** Kør `docker run --name [container-navn] -e MYSQL_ROOT_PASSWORD=[dit-password] -d mysql` for at starte en MySQL server. Du kan også mappe porte og tilføje volumener efter behov.

6. **Terminal (bash) – Ændre filrettigheder:**
   - **Læse og skrive rettigheder:** Brug kommandoen `chmod u+rw [filnavn]` for at give læse- og skriverettigheder til ejeren af filen.
   - **Eksekveringsrettigheder:** Brug `chmod u+x [filnavn]` for at give eksekveringsrettigheder til ejeren af filen.

7. **Sådan eksekveres en fil (f.eks. et script):**
   - Først skal du sikre, at filen har eksekveringsrettigheder (se ovenstående).
   - Eksekver filen ved at skrive `./[filnavn]` i terminalen, hvor `[filnavn]` er navnet på scriptet.

# Spørgsmål 5
1. **Hvad er et computer netværk, bredt set?**
   - Et computer netværk er et system af sammenkoblede computere og enheder, der bruger fælles kommunikationsteknologier til at dele ressourcer, data og information. Netværket kan være lokaliseret (LAN) eller strække sig over store afstande (WAN), og det inkluderer hardware (som routere og switche) og softwarekomponenter.

2. **Rollen for Applikationslaget:**
   - Applikationslaget i OSI-modellen er det øverste lag, der direkte interagerer med softwareapplikationer. Det tilbyder netværkstjenester til applikationerne og håndterer netværkskommunikationsaspekter, som brugeren interagerer med, for eksempel e-mail, filoverførsler og web browsing.

3. **Rollen for Transportlaget:**
   - Transportlaget styrer overførslen af data mellem systemer og sikrer at dataene ankommer korrekt og fejlfrit. Det vigtigste er, at dette lag segmenterer data fra applikationslaget og håndterer fejlkontrol, flowkontrol og dataoverførselsstyring.

4. **Hvad er et Protokol?**
   - En protokol er et sæt regler og standarder, der definerer, hvordan data overføres og kommunikeres over et netværk. Protokoller sikrer, at enheder på tværs af netværket kan kommunikere effektivt og korrekt.

5. **Hvad er en Protokol data enhed (PDU)?**
   - En PDU er den enhed af data, der overføres over et netværkslag. I forskellige lag af OSI-modellen har PDUs forskellige navne, såsom segmenter (Transportlaget) og pakker (Netværkslaget).

6. **Forklaring af følgende protokoller:**
   - **HTTP (Hypertext Transfer Protocol):** Protokollen bruges til at overføre webindhold og er fundamentet for datakommunikation på World Wide Web.
   - **DNS (Domain Name System):** Et system, der omsætter menneskelæsbare domænenavne (som google.com) til IP-adresser, som computere bruger til at identificere hinanden på netværket.
   - **DHCP (Dynamic Host Configuration Protocol):** En netværksprotokol, der automatisk tildeler IP-adresser og andre netværkskonfigurationsparametre til enheder på et netværk, hvilket forenkler processen med at administrere netværksadresser.

7. **Forskellen mellem TCP og UDP:**
   - **TCP (Transmission Control Protocol):** En forbindelsesorienteret protokol, der sikrer pålidelig, ordnet og fejlfri dataoverførsel. Det bruger håndtryk og fejlrettelsesmekanismer.
   - **UDP (User Datagram Protocol):** En enklere, forbindelsesløs protokol, der sender datagrammer uden at garantere levering, rækkefølge eller fejlfri data. Dette gør UDP hurtigere, men mindre pålidelig end TCP.
  
# Spørgsmål 6
1. **Rollen for Netværkslaget (Network Layer):**
   - Netværkslaget (lag 3 i OSI-modellen) har til opgave at flytte data ind og gennem andre netværk. Det pakker data med korrekte netværksadresseoplysninger, vælger passende netværksruter og videresender den pakkede data op ad stakken til transportlaget.

2. **Hvad er en Router?**
   - En router er en netværksenhed, der videresender datagrammer mellem computernetværk. Routere udfører trafikstyringsfunktioner på internettet og er ofte det, der forbinder et lokalt netværk med internettet.

3. **Hvad er en IP-adresse?**
   - En IP-adresse (Internet Protocol adresse) er et numerisk label tildelt hver enhed tilkoblet et computernetværk, der bruger Internet Protocol til kommunikation. En IP-adresse tjener to hovedformål: 1) identifikation af vært eller netværksinterface og 2) lokaliseringsadressering.

4. **Rollen for Datalinklaget (Data Link Layer):**
   - Datalinklaget (lag 2 i OSI-modellen) er ansvarlig for at overføre data mellem tilstødende netværksenheder i et WAN eller på samme LAN-segment. Laget sørger for de funktionelle og proceduremæssige midler til at overføre data mellem netværksenheder og kan muligvis også detektere og korrigere fejl, der opstår i det fysiske lag.

5. **Hvad er et Netværksinterfacekort (NIC)?**
   - Et netværksinterfacekort (NIC) er en hardwarekomponent, der forbinder en computer til et computernetværk. NIC tillader computere at kommunikere over et netværk, enten via kabler eller trådløst.

6. **Hvad er en Switch?**
   - En netværksswitch er en enhed, der forbinder enheder sammen på et computernetværk ved at bruge frame switching til at modtage, behandle og videresende data til den ønskede destination.

7. **Hvad er en MAC-adresse?**
   - En MAC-adresse (Media Access Control adresse) er en unik identifikator tildelt til en netværksinterfacecontroller (NIC) for kommunikation på datalinklaget af et netværkssegment. MAC-adresser bruges som netværksadresse i de fleste IEEE 802 netværksteknologier, inklusiv Ethernet og Wi-Fi.

8. **Hvad er Wireshark?**
   - Wireshark er et netværksprotokolanalyseværktøj, der bruges til at fange og inspicere data, der passerer gennem et netværk. Det giver detaljerede oplysninger om netværkstrafik og protokoller og bruges til fejlfinding og netværksanalyse.

9. **Eksempel på brug af Wireshark til at analysere en HTTP-anmodning:**
   - For at analysere en HTTP-anmodning med Wireshark, skal du først starte Wireshark og vælge det netværksinterface, hvor trafikken skal fanges. Når du har startet fangst, skal du besøge en webside for at generere HTTP-trafik. I Wireshark kan du derefter filtrere visningen til kun at vise HTTP-trafik og analysere detaljerne i HTTP-anmodninger og -svar.

# Spørgsmål 7
1. **Etablering af sikker forbindelse via HTTPS:**
   - Klienten initierer en sikker sideanmodning ved at bruge HTTPS.
   - Serveren svarer med sit offentlige nøgle og et digitalt certifikat.
   - Klienten validerer serverens certifikat ved hjælp af en certifikatautoritet (CA) for at sikre, at serveren er troværdig.
   - Når serveren er valideret, opretter klienten en session-nøgle, som er krypteret med serverens offentlige nøgle.
   - Serveren dekrypterer session-nøglen med sin private nøgle.
   - Herefter kommunikerer klient og server ved hjælp af den aftalte session-nøgle til at kryptere al dataoverførsel, hvilket sikrer en sikker kommunikation.

2. **Forskellen mellem self-signed certifikat og CA-signed certifikat:**
   - Et **self-signed certifikat** er et certifikat, der er underskrevet af den samme enhed, hvis identitet det certificerer. Dette er ikke tillid til af browsere og brugere, fordi enhver kan lave et sådant certifikat og hævde at være enhver.
   - Et **CA-signed certifikat** er et certifikat, der er underskrevet og valideret af en betroet certifikatautoritet. Dette tilføjer et lag af tillid, da CA'er kun udsteder certifikater efter at have gennemført nogle former for validering af anmoderens identitet.

3. **Java Spring projekt - aktivering af HTTPS:**
   - For at aktivere HTTPS i en Spring Boot-applikation, skal du tilføje nogle egenskaber i `application.properties` filen, såsom:
     ```
     server.port=443
     server.ssl.key-store=stien/til/keystore.jks
     server.ssl.key-store-password=dinKeystorePassword
     server.ssl.keyAlias=dinKeyAlias
     ```
   - Her refererer `key-store` til stien til din Java KeyStore fil, som indeholder serverens SSL certifikat.

4. **Java-klasse nødvendig for at aktivere HTTPS i et Java Spring projekt:**
   - I mange tilfælde vil konfigurationen ovenfor være nok til at aktivere HTTPS. Spring Boot konfigurerer automatisk HTTPS, hvis det finder de nødvendige SSL egenskaber i `application.properties`.
   - For mere avanceret konfiguration, kan du tilføje en konfigurationsklasse, der udvider `WebSecurityConfigurerAdapter` og overskriver metoden `configure(HttpSecurity http)`, for at tilpasse sikkerhedsindstillingerne.
