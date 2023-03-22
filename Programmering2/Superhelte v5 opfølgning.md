# Superhelte v5 opfølgning - 23-03-2023

- **Fag:** Programmering 2
- **Oprettet:** March 22, 2023 3:44 PM
- **Type:** Forberedelse

# Materialer

[Understanding DTO (Data Transfer Object) Pattern in 4 Minutes](https://www.youtube.com/watch?v=MAIkC9KctVw)

[The POST-Redirect-GET pattern](https://www.youtube.com/watch?v=gu50pxTYc3U)

[20 Understanding Java Beans in 90 Seconds](https://www.youtube.com/watch?v=zt9JH2B9qek)

[21 Java Beans - Hands on](https://www.youtube.com/watch?v=MRQVI0afaB4&list=PL6OCFe4JQ2-OZumytwEwshADHUIWRMo44&index=21)

[Spring ultimate basics: What are Spring Beans and what is the Spring Container?](https://www.youtube.com/watch?v=aS9SQITRocc&t=643s)

# Noter

## DTO

DTO står for Data Transfer Object, og det er en designmønster, der bruges til at overføre data mellem forskellige dele af en applikation. Det kan være mellem forskellige lag i en applikation eller mellem forskellige applikationer.

Hvorfor er det brugbart?

DTO'er bruges ofte i situationer, hvor der er behov for at overføre komplekse data mellem forskellige dele af systemet, såsom mellem serveren og klienten i en webapplikation. Ved at bruge DTO'er kan man sikre, at dataene overføres på en ensartet og struktureret måde, selvom de interne datastrukturer i applikationen ændrer sig over tid. Dette gør det lettere at vedligeholde og udvide applikationen.

En anden fordel ved at bruge DTO'er er, at det giver mulighed for at reducere mængden af data, der overføres mellem forskellige dele af systemet. Dette kan øge ydeevnen og reducere belastningen på netværket og serveren.

DTO'er kan også hjælpe med at øge sikkerheden i applikationen. Ved at bruge DTO'er kan man for eksempel undgå at overføre følsomme data mellem forskellige dele af systemet, hvilket kan reducere risikoen for datamisbrug.

I Java kan DTO'er implementeres som en simpel klasse med instansvariabler og getters og setters metoder for at få adgang til variablerne.

## **Post/Redirect/Get Pattern**

Post/Redirect/Get Pattern er en designmønster, der har til formål at håndtere brugerinput og formularer i webapplikationer. Når en bruger sender en formular, kan applikationen behandle og validere input, gemme data i en database eller udføre en anden form for handling. Efter behandlingen af formularindholdet omdirigeres brugeren tilbage til en ny side. Dette sker ved hjælp af en HTTP GET-anmodning.

Formålet med at anvende Post/Redirect/Get Pattern i webapplikationer er at undgå gentagne formularindsendelser. Hvis brugeren opdaterer eller genindlæser siden, kan det ellers resultere i uønskede gentagelser af formularindsendelser. Ved at anvende Post/Redirect/Get Pattern undgår man dette problem.

En anden fordel ved at anvende Post/Redirect/Get Pattern er, at det reducerer mængden af data, der overføres mellem klient og server. Dette skyldes, at formularindholdet blot bliver behandlet og gemt på serveren, og brugeren omdirigeres herefter til en ny side. På den måde er det ikke nødvendigt at overføre samme data flere gange mellem klient og server. Dette kan forbedre ydeevnen og reducere belastningen på netværket og serveren.

I praksis kan Post/Redirect/Get Pattern implementeres ved at anvende en midlertidig omdirigering (HTTP 302-status) til den nye side, som brugeren skal sendes til efter formularbehandlingen på serveren. Denne midlertidige omdirigering kan eksempelvis ske ved hjælp af JavaScript eller server-side kode.

Alt i alt er Post/Redirect/Get Pattern en simpel og effektiv løsning på et problem, der kan opstå i webapplikationer. Ved at anvende dette designmønster, kan man undgå gentagne formularindsendelser og reducere mængden af data, der overføres mellem klient og server.

## Java Bean

Java beans er en populær softwarekomponent i Java-programmeringssproget. De er designet til at være genanvendelige og lette at bruge, og de opfylder bestemte krav og standarder.

- Kravene for en Java bean inkluderer, at klassen skal have en standard constructor uden parametre. Dette betyder, at en instans af klassen kan oprettes uden at skulle angive nogen parameter til konstruktøren.
- Derudover skal variablerne i klassen være private, så de ikke kan tilgås direkte fra andre klasser. I stedet skal der være getters og setters for hver variabel, som giver mulighed for at hente eller ændre værdien af variablen.
- En anden vigtig ting ved Java beans er, at klassen skal implementere Serializable interface. Dette gør det muligt at gemme og overføre objekter af klassen i en binær form.
- Endelig skal en Java bean følge standarden for Java beans navngivning. Dette betyder, at klassenavnet skal begynde med en stor bogstav og være en beskrivelse af, hvad klassen repræsenterer. Navnet på getters og setters skal også følge en bestemt konvention.

Fordelene ved at bruge Java beans inkluderer, at de er lette at bruge og genanvendelige. Fordi de følger en bestemt standard, er de også nemme at læse og forstå, hvilket gør det lettere for andre programmører at arbejde med dem.

### Spring Beans

Spring Beans er fundamentale til Spring Frameworket. De spiller en vigtig rolle i at styre og organisere instanser af klasser og deres afhængigheder i en applikation.

Typisk anvendte Spring Beans inkluderer `Controller`, `Service` og `Repository`, som hver har en specifik rolle i en applikation. `Controller` håndterer input fra brugeren og kalder relevante metoder i `Service` klasserne, som indeholder applikationslogikken. `Repository` klasserne er ansvarlige for at håndtere dataadgang og kommunikation med en database eller andre datakilder.

At definere og konfigurere Spring Beans til at opfylde applikationens behov er vigtigt, og der er flere måder at gøre det på. Det kan gøres ved brug af annoteringer eller XML-konfigurationsfiler. Ved at definere egne Spring Beans kan man tilpasse og skræddersy applikationens funktionalitet og sørge for, at de forskellige dele af applikationen fungerer sammen på en optimal måde.

Spring Boot er en populær Java-baseret framework, som bygger på Spring Frameworket og gør det nemt at oprette og konfigurere Java-applikationer. Spring Boot gør det nemt at komme i gang med at arbejde med Spring Beans, da det giver en række standardindstillinger og konfigurationsmuligheder, der kan bruges til at oprette og konfigurere Spring Beans.

I praksis vil man ofte definere sine egne Spring Beans, som er specifikke for ens applikation. For eksempel kan man definere en `CustomService` klasse som en Spring Bean, hvis man har et specifikt behov for at behandle data på en bestemt måde.

I sidste ende er Spring Beans en vigtig del af Spring Frameworket og er nødvendige for at bygge komplekse, skalerbare og vedligeholdbare Java-applikationer.
