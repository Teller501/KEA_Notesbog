# Method Comparison - 24-08-2023

- **Fag:** Systemudvikling 2
- **Oprettet:** August 24, 2023
- **Type:** Forberedelse

# Materialer
Avison_InformationSystemsDevelopment_Ch_27.pdf

# Noter
* Kapitlet diskuterer forskellige tilgange til udvikling af informationssystemer, herunder traditionelle livscyklusser for systemudvikling, agile metoder og slutbrugerudvikling.
* Det dækker forskellige udviklingsmetoder som vandfald, prototyping, inkrementel, spiral, hurtig applikationsudvikling og ekstrem programmering.
* De relative fordele og ulemper ved disse forskellige metoder vil sandsynligvis blive sammenlignet med hensyn til fleksibilitet, hastighed, brugerinddragelse, projektrisiko og andre faktorer.
* Der er sandsynligvis en diskussion af, hvordan man vælger en passende udviklingsmetode baseret på et bestemt projekts behov og begrænsninger. Faktorer som projektets omfang, tidslinjer, budget, medarbejdernes færdigheder og usikkerhed i kravene er med til at afgøre, hvilken tilgang der er bedst.
* Kapitlet udforsker sandsynligvis tendenser inden for systemudvikling, som bevægelsen mod mere iterative, agile tilgange i modsætning til stive, sekventielle livscyklusser.
* Slutbrugerudviklingsteknikker som regnearksmodeller, desktopdatabaser og ad hoc-forespørgsler er sandsynligvis også dækket som alternativer til traditionel IT-ledet 



## Sammenligningsproblemer
Der er to hovedårsager til at sammenligne metoder til udvikling af informationssystemer:

1. **Akademisk** - For bedre at forstå metodernes natur, funktioner, mål og filosofier med henblik på at klassificere dem og foreslå forbedringer.
2. **Praktisk** - For at vælge den bedste metode eller kombination af metoder til et bestemt projekt, en række projekter eller en organisation.

De akademiske og praktiske grunde er indbyrdes forbundne - akademiske studier bør informere praktiske valg, og praktisk erfaring bør forme akademiske kriterier.

Teksten giver nogle "ideelle kriterier" til vurdering af metoder:
* At have formelle regler, teknikker, værktøjer, dokumentationsstandarder og ressourceestimater
* Dækker hele livscyklussen for systemudvikling
* Forståelse og udnyttelse af informationsressourcer (data og processer)
* At adskille logisk og fysisk design
* Mulighed for tidlig identifikation af ændringer
* Muliggøre kommunikation mellem faser
* Effektiv problemanalyse
* Planlægning, kontrol og evaluering af ydeevne
* Forbedring af produktivitet og kvalitet
* Opretholdelse af systemets synlighed gennem hele udviklingen
* At være let at forstå og undervise i
* Definition af systemgrænser
* Design til forandring
* Effektiv brugerkommunikation
* Enkelhed
* Mulighed for udvidelse og løbende relevans
* Udnyttelse af automatiserede værktøjer
* Overvejelse af brugernes mål og målsætninger
* Tilskyndelse til deltagelse gennem enkelhed
* Matchning af udøvernes færdigheder og erfaring
* Matchning af systemets karakteristika
* Integrering af tekniske og ikke-tekniske aspekter
* Scanning efter muligheder
* At adskille analyse fra design

De tidligere nævnte "ideelle kriterier" for sammenligning af metodologier er subjektive, og ingen enkelt metodologi opfylder dem alle. Andre eksperter har foreslået yderligere bredere kriterier, som at overveje forskningsparadigmet, værdier, kontekst, ændringspotentiale, brugerinddragelse osv.

* NIMSAD-frameworket evaluerer metoder baseret på problemsituationen, problemløseren og problemløsningsprocessen. Den stiller detaljerede spørgsmål om hvert element før, under og efter brug af metoden.
* Nogle hævder, at der ikke findes én "bedste" metode. Valget afhænger af problemet, anvendelsen, organisationen og kulturen. Ved en beredskabstilgang vælges metoden som en del af selve rammen.
* Metoder kan sammenlignes ud fra, hvordan de håndterer forskellige niveauer af usikkerhed eller klasser af problemsituationer. Mere strukturerede problemer kan passe til traditionelle tilgange, mens prototyper eller evolutionære metoder fungerer til uklare situationer.
* Der er praktiske vanskeligheder ved at sammenligne metoder, såsom versionsforskelle, begrænset adgang til dokumentation, afvigelser mellem teori og praksis og terminologisk forvirring.
* Typiske funktionsbaserede sammenligninger er subjektive baseret på, hvem der vælger kriterierne. Leverandører definerer ofte kriterier, der favoriserer deres egen metode.
* En foreslået sammenligningsramme omfatter vurdering af udviklingsdækning, rammer, modeller, værktøjer, teknikker, fokus, roller, nødvendige færdigheder, forandringshåndtering, påstande om fordele og filosofiske antagelser.
* At forstå filosofien bag en metodes tilgang er afgørende, men ikke altid eksplicit. Sammenligninger fortsætter på trods af vanskeligheder, fordi mange metoder hævder at være universelt anvendelige.

## Framework for sammenligning af metoder
Det er svært og subjektivt at sammenligne metoder, men det er nyttigt, når man skal vælge og forbedre dem. Den foreslåede ramme har 7 elementer:

1. Filosofi - Principper, som metoden er baseret på:
* Paradigme - Videnskab vs. systemtænkning
* Målsætninger
* Domæne
* Anvendelser
2. Model - Konceptuelle modeller, diagrammer osv.
3. Teknikker og
4.   værktøjer
5. Omfang - aspekter af udviklingsprocessen, der dækkes
6. Output - producerede dokumenter, specifikationer, modeller osv.
* Praksis - Brug af metoden i den virkelige verden baseret på:
* Baggrund
* Brugerbase
* Deltagere
7. Produkt - Systemer udviklet ved hjælp af metoden

### 1. Filosofi - Paradigme
* En metodes filosofi er afgørende, men ofte implicit. To vigtige paradigmer er naturvidenskab (reduktionistisk, gentagelig) og systemtænkning (holistisk, emergente egenskaber).
* Ontologi og epistemologi er nyttige til at analysere filosofi. Ontologi relaterer til tingenes essens, epistemologi til grundlaget for viden.
* Objektivist vs. subjektivist og realisme vs. nominalisme er eksempler på spektre. Metodologier gør antagelser her.
* Teknikker indeholder også filosofi, men kan potentielt bruges imod deres "naturlige" antagelser. Men de skubber stadig i bestemte retninger.
* Sammenligning af metodologier på disse linjer kan hjælpe med at matche udviklerens overbevisninger og problemsituation med metodologiens antagelser.

### 1. Filosofi - Mål
* En metodes mål er en vigtig ledetråd til dens filosofi. Nogle metoder sigter udelukkende mod at udvikle et computeriseret informationssystem. Andre har bredere mål som at afgøre, om der overhovedet er brug for et informationssystem.
* Metoder, der kun fokuserer på "computeriserbare" aspekter, sætter en kunstig grænse i forhold til forretningslogikken. Løsningen på et problem ligger måske ikke kun i det, der kan automatiseres.
* Ofte er der brug for en grundig analyse og redesign af hele problemområdet, ikke bare computerisering. At beslutte, at et IT-system er løsningen først, kan være at "sætte vognen foran hesten".
* Det er vigtigt at overveje, om en metode kan føre til ikke-IT- eller organisatoriske løsninger. Hvis svaret er definitivt "nej", så adresserer metoden et andet problem end et, hvor svaret er "ja".
* Mange udbredte kommercielle metoder ser ud til at svare "nej" til at tillade ikke-IT-løsninger. I modsætning hertil vil de fleste akademiske metoder sandsynligvis svare "ja". En undtagelse er business process reengineering-metoder, der fokuserer på generelle forbedringer af forretningsprocesser, ikke kun IT.

### 1. Filosofi - Domæne
* Tidlige metoder fokuserede på at løse specifikke, snævre problemer. At løse flere problemer isoleret kan føre til et miskmask af forskellige systemer.
* Selv velkoordinerede løsninger på indbyrdes forbundne problemer er måske ikke det samme som summen af individuelle løsninger.
* Nogle nyere metoder tager et bredere perspektiv og løser ikke kun umiddelbare problemer.
* Argumentet er, at for at løse individuelle problemer korrekt, skal hele organisationen og strategien for informationssystemer først analyseres top-down.
* Det sikrer, at informationssystemerne grundlæggende understøtter de strategiske forretningskrav, ikke kun isolerede problemer.

### 1. Filosofi - Anvendelser
* Nogle metoder er designet til specifikke typer af problemer, miljøer eller organisationer.
* Andre hævder at være generelle og anvendelige på tværs af forskellige kontekster.
* En metodes tilsigtede anvendelighed, uanset om den er snæver eller bred, giver indsigt i dens filosofiske antagelser og egnethed.

### 2. Model
* Modellen repræsenterer metodens syn på verden og indfanger essensen af problemet eller designet.
* Modeller fungerer som kommunikation, kortlægning til implementering og giver indsigt.
* Fire modeltyper:
1. Verbal
2. Matematisk
3. Ikonisk/billedlig/skematisk
4. Simulering
* Metoder til informationssystemer bruger hovedsageligt ikoniske/billedlige modeller til kommunikation mellem brugere og analytikere.
* Modeller har til formål at indfange den nødvendige information på det rigtige tidspunkt for at udvikle systemet.

### 3/4. Teknikker og værktøjer

### 5. Omfang
* Omfanget angiver, hvilke faser af systemudviklingens livscyklus metoden dækker.
* Detaljeringsgraden på hvert trin er også nyttig at analysere.
* Selvom nogle metoder ikke følger en livscyklus, er det stadig nyttigt at undersøge omfanget i forhold til livscyklusens faser.

### 6. Output
* Outputs er de leverancer, der produceres på hvert trin, især den endelige leverance.
* Outputs kan variere fra en analysespecifikation til en fuldt fungerende systemimplementering

### 6. Output - Praksis
* Praksis omfatter:
1. Baggrund - kommerciel eller akademisk oprindelse
2. Brugerbase - antal og typer af brugere
3. Deltagere - kan brugerne gøre det, eller er der brug for professionelle? Færdighedsniveauer?
4. Vurdering af vanskeligheder, problemer, succeser, fiaskoer gennem brugererfaringer
5. Grad af skræddersyning og fortolkning i praksis
6. Forskelle mellem praksis og teori

### 7. Produkt
* Produktet er det, som køberne af metoden rent faktisk får.
* Produktet kan omfatte software, dokumentation, træning, hjælpetjenester, rådgivning osv.
* En analyse af produktet giver indsigt i den fulde pakke, man får, når man anvender metoden.

## Sammenligning
Sammenligningen bruger rammerne filosofi, model, teknikker, omfang, output, praksis og produkt.

**Filosofi:**

* Paradigme - SSM og ETHICS er systemorienterede, de andre er videnskabelige/reduktionistiske paradigmer.
* Målsætninger - SSM, ETHICS, ISAC og DSDM har bredere målsætninger end blot IT-systemer. De andre fokuserer på computerstyrede systemer.
* Domæne - IE, PI og SSM beskæftiger sig med organisatorisk planlægning og strategi. De andre starter med et defineret problem, der skal løses.
* Mål - De fleste hævder, at de kan anvendes til generelle formål, men har antagelser om organisationsstørrelse, applikationer osv.

**Model:**

* SSM, Soft Systems Methodology, bruger Rich Pictures, Root Definitions, CATWOE og Conceptual Models.
* ETHICS bruger modeller som organisationsmodellen og den menneskelige aktivitetsmodel.
* Mange bruger dataflowdiagrammer - STRADIS, YSM, SSADM, ISAC. Andre bruger forskellige procesmodeller som JSD's strukturdiagrammer.
* SSM bruger Rich Pictures, ETHICS bruger socio-tekniske modeller. OOA/RUP integrerer proces og data.

**Teknikker og værktøjer:**

* Hver metodologi indeholder forskellige teknikker og værktøjer, som allerede er diskuteret.
* Nogle metodologier som STRADIS og SSADM er defineret i form af teknikker. Andre som ISAC er ikke afhængige af specifikke teknikker.
* Det er vigtigt at identificere grundlæggende metodologier adskilt fra aktuelle teknikker. Det påvirker udvidelsesmulighederne.
* Værktøjer spænder fra valgfrie til fuldt integrerede som i IE og RUP. Graden af leverandør-lock-in varierer.

**Omfang:**

* Varierer med hensyn til livscyklusdækning og detaljeringsniveau. SSM følger ikke en livscyklusmodel.
* Kortlagt til livscyklusfaser, men metodologier som SSM følger ikke livscyklusser. De fleste fokuserer på analyse/design.
* Stor variation i dækningen af faser som gennemførlighed, implementering, vedligeholdelse osv.

**Output:**

* Spænder fra analysespecifikationer til fuldt fungerende systemer.
* Varierer med hensyn til de leverancer, der produceres, og niveauet af specifikationsdetaljer. Relateret til, hvor meget der er mandat til.

**Praksis:**

* Baggrund, brugergrundlag, behov for færdigheder og forskelle mellem teori og praksis varierer.
* Baggrunden varierer fra akademisk som SSM til kommerciel som SSADM. Meget tyder på, at kommercielle metoder bruges mindre end påstået.
* Deltagerne spænder fra tekniske specialister til inkludering af forretningsbrugere som i ETHICS. Behovet for færdigheder varierer.

**Produkt:**

* Dokumentation, software, træning og inkluderede tjenester varierer også.
* Spænder fra bøger til multimedier på nettet. Kan kræve konsulenter, uddannelse, certificering osv.

## Opsamling
* Der er to hovedårsager til at sammenligne metodologier:
1. Akademisk - For bedre at forstå deres natur, funktioner, mål, filosofier osv.
2. Praktisk - for at vælge passende metoder til projekter eller organisationer.
* NIMSAD-rammen har 3 elementer: problemsituationen, problemløseren og problemløsningsprocessen (selve metoden).
* Den foreslåede sammenligningsramme har 7 elementer:
1. Filosofi - paradigme, mål, domæne, målapplikationer
2. Modeller
3. Teknikker og værktøjer
4. Omfang
5. Output
6. Praksis - baggrund, brugerbase, deltagere, færdigheder
7. Produkt - hvad du rent faktisk får
* Sammenligning af metoder ved hjælp af denne ramme giver indsigt i deres forskelle og antagelser.
* Værdien ligger ofte mere i den øgede forståelse end i de specifikke resultater.
* Hvis man f.eks. sammenligner omfang, viser det sig, at metoder adresserer stadier som gennemførlighed, implementering osv. på meget forskellige måder.
