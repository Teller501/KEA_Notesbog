# Interfaces - 16-02-2023

- **Fag:** SYS/PRG 2
- **Oprettet:** March 7, 2023 8:50 AM
- **Type:** Forberedelse

# **Interfaces**

- Et Java Interface definerer en samling af metoder og konstanter, som en klasse kan implementere for at opfylde en bestemt kontrakt eller adfærd. Interfacet fungerer som en abstrakt beskrivelse af funktionaliteten, som klassen skal have, og den specificerer, hvordan klassen skal interagere med andre objekter i systemet. Ved at implementere et Java Interface kan man opnå en høj grad af fleksibilitet og genbrugelighed i koden, da forskellige klasser kan implementere det samme interface og dermed opfylde den samme kontrakt.
- Interfaces i Java bruges typisk til at definere en abstrakt kontrakt, som en klasse skal opfylde. Interfaces kan bruges på flere måder i Java, blandt andet:
- **Implementering af multiple arv**: Java tillader ikke multiple arv af klasser, men en klasse kan implementere flere interfaces. Ved at definere interfaces med forskellig funktionalitet kan man opnå en høj grad af fleksibilitet i systemet, samtidig med at man undgår problemet med konfliktende arv.
- **Opdeling af ansvar**: Ved at definere et interface kan man adskille ansvar og funktionalitet fra selve implementeringen. Det kan gøre det lettere at vedligeholde og ændre koden, da man kan ændre implementeringen af en klasse, mens man stadig opfylder den samme kontrakt.
- **Testbarhed**: Ved at designe klasser, der opfylder et bestemt interface, kan man opnå en høj grad af testbarhed i koden. Det er muligt at skrive unit-tests, som tester, om en klasse opfylder kravene i interface, og dermed sikre, at koden fungerer som forventet.
- **Genbrugelighed**: Ved at definere et interface kan man opnå en høj grad af genbrugelighed i koden, da flere forskellige klasser kan implementere det samme interface. Det gør det muligt at dele funktionalitet på tværs af forskellige dele af koden, og kan dermed reducere mængden af duplikeret kode.

# **Interface Segregation Principle**

- Interface Segregation Principle (ISP) er en designregel inden for softwareudvikling, som siger, at man bør opdele et interface i mindre og mere specialiserede interfaces, som kun inkluderer de metoder, som en klasse faktisk har brug for. ISP er en af de fem grundlæggende principper i SOLID-designprincipperne, som er en samling af principper og regler for objektorienteret softwareudvikling.
- ISP er vigtig, fordi det kan hjælpe med at sikre, at en klasse kun afhænger af de metoder og funktioner, som den faktisk har brug for. Hvis et interface er for stor og omfatter for mange metoder, kan det føre til, at en klasse bliver afhængig af funktioner, som den ikke har brug for, og som kan gøre koden mere kompleks og svær at vedligeholde.
- Ved at opdele et interface i mindre og mere specialiserede interfaces, kan man undgå denne afhængighed og sikre, at en klasse kun har adgang til de metoder, som den faktisk har brug for. Det kan også gøre koden mere fleksibel og modulær, da man kan udskifte et interface med en mere specialiseret version, hvis kravene til funktionalitet ændrer sig.
- Et eksempel på ISP kunne være et interface til en printer, som inkluderer en række metoder til at udskrive, kopiere og scanne dokumenter. Hvis en klasse kun har brug for at udskrive dokumenter, bør den ikke være afhængig af de andre metoder i interfacet. I stedet bør man opdele interfacet i mindre og mere specialiserede interfaces, som kun inkluderer de metoder, som en klasse faktisk har brug for.

Her er et eksempel på et Java interface med brug af Interface Segregation Principle:

```java
interface TændSlukInterface {
  void tænd();
  void sluk();
}

interface KørselInterface {
  void kør();
  void bremse();
  void låsDøre();
}

class Bil implements TændSlukInterface, KørselInterface {
  // implementer metoder fra begge interfacene
}

```

I dette tilfælde opdeles bil-interfacet i to mindre interfacene, som hver især inkluderer de metoder, som en klasse faktisk har brug for. Klassen `Bil` implementerer begge interfacene, og kan dermed bruges til både at tænde og slukke bilen samt styre bilen. Hvis en anden klasse kun har brug for at tænde og slukke bilen, kan den i stedet implementere `TændSlukInterface`. Hvis en klasse kun har brug for at styre bilen, kan den i stedet implementere `KørselInterface`. Dette giver en mere fleksibel og modulær arkitektur, hvor klasser kun afhænger af de metoder, som de faktisk har brug for.

# **Inversion of Control**

- Inversion of Control (IoC) er et designmønster inden for softwareudvikling, som handler om at vende kontrollen i et program om. Traditionelt set vil en klasse have kontrol over, hvordan dens afhængigheder bliver instantieret og brugt, men med IoC mønsteret overlades denne kontrol til en container eller framework.
- Det grundlæggende princip bag IoC er, at en klasse ikke bør have direkte kendskab til, hvordan dens afhængigheder er blevet instantieret eller implementeret. I stedet bør den kun have adgang til en abstraktion eller grænseflade, som dens afhængigheder implementerer, og så lade en container eller framework sørge for at instantiere og konfigurere afhængighederne korrekt.
- Dette kan føre til en mere modulær og fleksibel arkitektur, da klasser kan være mere uafhængige af deres afhængigheder, og afhængigheder kan nemmere udskiftes og opdateres uden at påvirke hele systemet. IoC gør også det nemmere at teste koden, da man kan erstatte de rigtige implementeringer af afhængigheder med mock-objekter eller stubs.
- IoC kan implementeres på forskellige måder, men en af de mest populære metoder er at bruge en Dependency Injection (DI) container. En DI-container tager ansvar for at instantiere og konfigurere alle klassernes afhængigheder, og injicere dem ind i klasserne, når de skal bruges. Dette kan reducere koden for at instansiere og konfigurere afhængighederne, og gøre koden mere modulær og fleksibel.

# **Dependency Injection**

- Dependency Injection (DI) er et designmønster i softwareudvikling, som bruges til at implementere Inversion of Control (IoC) principperne og hjælpe med at opnå løs kobling mellem klasser og deres afhængigheder. DI handler om at eksternt tilføre afhængigheder til en klasse i stedet for at lade klassen selv instantiere eller håndtere deres egne afhængigheder.
- I DI, vil en klasse normalt have nogle afhængigheder, som den har brug for at kunne fungere korrekt. I stedet for at lade klassen selv instantiere og håndtere disse afhængigheder, så bliver de eksternt injiceret ind i klassen gennem dens konstruktør, metode parametre eller en særlig "injektions-container". På denne måde kan afhængighederne udskiftes eller konfigureres på en mere fleksibel måde, og koden bliver mindre afhængig af specifikke implementeringer af afhængighederne.
- DI kan også hjælpe med at gøre koden mere testbar, da man kan mocke eller stubbe afhængighederne, når man tester klassen. På denne måde kan man fokusere på at teste klassens specifikke funktionalitet, uden at bekymre sig om dens afhængigheder.
- DI kan implementeres på forskellige måder, og der er mange DI-containere og biblioteker, som kan hjælpe med at implementere DI i forskellige sprog og miljøer. Nogle af de mest almindelige DI-mønstre inkluderer Constructor Injection, Property Injection, og Method Injection.

Her er et eksempel på Dependency Injection i Java:

```
public class KundeService {
    private final KundeRepository kundeRepository;

    public KundeService(KundeRepository kundeRepository) {
        this.kundeRepository = kundeRepository;
    }

    public void opretKunde(Kunde kunde) {
        kundeRepository.opretKunde(kunde);
    }
}

public interface KundeRepository {
    void opretKunde(Kunde kunde);
}

public class JpaKundeRepository implements KundeRepository {
    @Override
    public void opretKunde(Kunde kunde) {
        // Opret kunde i database
    }
}

```

I dette eksempel er der en klasse `KundeService`, som afhænger af en implementering af interfacet `KundeRepository`. I stedet for at `KundeService` selv instantiere og håndtere sin egen instans af `KundeRepository`, så bliver den eksternt injiceret i dens konstruktør. Dette gør det muligt at udskifte eller konfigurere implementeringen af `KundeRepository` på en fleksibel måde. I dette tilfælde er `JpaKundeRepository` en implementering af `KundeRepository`, som opretter kunder i en database ved hjælp af Java Persistence API (JPA).

```
KundeRepository kundeRepository = new JpaKundeRepository();
KundeService kundeService = new KundeService(kundeRepository);
kundeService.opretKunde(new Kunde("John", "Doe"));

```

I dette eksempel instantieres `JpaKundeRepository` og injiceres i `KundeService` gennem dens konstruktør. Derefter kan `KundeService` bruge `KundeRepository`-instansen til at oprette en ny kunde i databasen. Hvis man senere ønsker at skifte til en anden implementering af `KundeRepository`, kan man blot oprette en ny instans og injicere den i `KundeService` i stedet.
