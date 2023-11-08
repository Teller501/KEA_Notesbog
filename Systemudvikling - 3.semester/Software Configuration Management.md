# Hvad er software configuration management

Software configuration management (SCM) er en vigtig disciplin indenfor softwareudvikling, som handler om at styre ændringer der sker i et softwareprojekt. SCM involverer en række aktiviteter og værktøjer til at identificere, organisere og kontrollere ændringer i softwarekomponenter og arbejdsprodukter.

## Formålet med SCM

Det overordnede formål med SCM er at maksimere produktiviteten og minimere fejl i et softwareprojekt. Ved at have systematiske og veldefinerede procedurer for ændringsstyring, kan man undgå kaos og forvirring når softwaren løbende videreudvikles. SCM er en integreret del af kvalitetsstyringen i et softwareprojekt.

## SCM vs. software support

SCM adskiller sig fra almindelig software support ved at det starter allerede når softwareprojektet startes, og ikke først når softwaren er udviklet. SCM tracker og styrer ændringer gennem hele softwareprojektets levetid.

# Baselines

Et centralt begreb i SCM er baselines. En baseline er en godkendt version af en softwarekomponent eller et softwareprodukt.

## Ændringer til baselines

Når først en baseline er etableret, så kan der kun laves ændringer til den gennem formelle ændringsstyringsprocedurer. Dette sikrer at ændringer analyseres og godkendes før de implementeres.

## Tekniske reviews

Når alle dele af en baseline er blevet revideret og godkendt, så kan den frigives. Herefter kan der kun laves ændringer til baseline efter tekniske reviews og godkendelse.

# Software Configuration Items (SCIs)

De individuelle arbejdsprodukter og softwarekomponenter der er under SCM kaldes Software Configuration Items (SCIs).

## Organisering af SCIs

SCIs organiseres i configuration objekter som kan katalogiseres i et projekt repository med et fælles navn. Et configuration object har attributter og relationer til andre objekter.

## Udtræk fra repository

Hvis en udvikler vil lave en ændring til en baseline SCI, så tjekkes den ud fra repository til udviklerens private workspace. Her kan den så ændres hvis SCM procedurer følges.

# SCM Repository

SCM repository'et er kernen i SCM. Det gemmer alle SCIs og udbyder services til versionsstyring, ændringssporing, kravssporing, konfigurationsstyring og audit trails. Repository'et håndterer dataintegritet, deling og integration af data.

## Integration med værktøjer

SCM repository'et integrerer med softwareudviklingsværktøjer og er central for softwareprocessen. Det kan håndhæve ensartet struktur og format på arbejdsprodukter.

## Meta-model

Repository'et bygger på en meta-model som definerer hvordan data lagres, tilgås og sikres. Meta-modellen muliggør udvidelse af systemet.

# Nøglefunktioner i SCM

Nogle nøglefunktioner SCM-systemet skal understøtte:

- Versionsstyring
- Sporing af afhængigheder og ændringer
- Kravssporing
- Konfigurationsstyring
- Audit trails

Derudover integration med værktøjer til Continuous Integration og issues tracking.

# Ændringsstyringsprocessen

Ændringsstyringsprocessen definerer opgaver til at:

- Identificere alle SCIs
- Styre ændringer til SCIs
- Muliggøre konstruktion af forskellige versioner
- Opretholde kvalitet over tid

Processen består af opgaver som:

- Identifikation
- Versionsstyring
- Ændringsstyring
- Konfigurationsrevision
- Statusrapportering

# Opsummering

SCM giver styr på ændringer i et softwareprojekt gennem systematisk identifikation, kontrol, sporing og rapportering af alle arbejdsprodukter. Dette er afgørende for at opretholde kvalitet og integrtitet af softwaren gennem hele dens levetid.

# Opgave
**Q1: What are the 4 elements that exist when an effective SCM system is implemented? Discuss each briefly.**

Answer:
- Component elements - Tools and file management for managing SCIs
- Process elements - Procedures and tasks for change management
- Construction elements - Tools to automate software construction
- Human elements - Tools and processes for the software team

**Q2: What are the 5 definitions of SCM tasks?**

Answer:
- Identification
- Version control
- Change control
- Configuration auditing
- Status reporting

**Q3: What is the final task and purpose when a change is approved by the CCA?**

Answer:
En Engineering Change Order (ECO) genereres for at beskrive og godkende ændringen.

**Q4: What is the definition of a Baseline?**

Answer:
En baseline er en version af software eller en specifikation, der er blevet formelt gennemgået og aftalt, og som derefter kun kan ændres gennem formelle procedurer.

**Q5: What the 4 primary objectives to software change management process?**

Answer:
- Identify configuration items
- Manage changes
- Facilitate version construction
- Ensure quality

**Q6: Describe what Impact Management is?**

Answer:
Impact management identificerer og vurderer ændringers indvirkning på andre dele af softwaren og udviklingsteamet. Det hjælper med at kontrollere de afledte effekter af ændringer.

**Q7: What are the 6 General contents in a repository?**

Answer:
Versioning, dependency tracking, requirements tracing, configuration management, audit trails, and storage for text/graphics/video/audio.

**Q8: What are the 4 fundamental sources of change?**

Answer:
New requirements, new stakeholder needs, reorganization/growth, and budget/schedule constraints.

**Q9: What the advantages of using Continuous Integration?**

Answer:
Accelerated feedback, increased quality, reduced risk, and improved reporting/metrics.

**Q10: What are SCIs?**

Answer:
Software Configuration Items - de enkelte dele af arbejdsprodukter under konfigurationsstyring.

**Q11: Who are involved in a typical CM operational scenario, and what are their goals?**

Answer:
Projektlederen, konfigurationslederen, softwareingeniørerne og kunden er involveret. Deres mål er rettidig udvikling, ændringskontrol, effektivt arbejde og kvalitetssikring.

**Q12: Who makes the final decision on the status and priority of the change?**

Answer:
The change control authority (CCA).

**Q13: What is required to make a new baseline?**

Answer:
Review, correction, and approval of all parts of the software.

**Q14: How do you ensure that the change has been properly implemented?**

Answer:
Via technical reviews and configuration audits.

**Q15: What contains a system model in a Version Control System?**

Answer:
A component hierarchy, build order, construction rules, and verification rules.

**Q16: Why is the first law of system engineering true? Provide specific examples for each of the four fundamental reasons for change.**

Answer:
Loven er sand, fordi ændringer er uundgåelige i softwaresystemer af årsager som nye krav, omorganisering, nye interessenters behov og ressourcebegrænsninger.

**Q17: Describe the value of continuous integration tools to agile software developers.**

Answer:
CI-værktøjer giver agile udviklere mulighed for ofte at integrere og teste kodeændringer. Det giver hurtigere feedback, reducerer risikoen og forbedrer kvaliteten.