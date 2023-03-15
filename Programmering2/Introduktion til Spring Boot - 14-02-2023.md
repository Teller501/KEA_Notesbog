# Introduktion til Spring Boot - 14-02-2023

- **Fag:** Programmering 2
- **Oprettet:** March 7, 2023 11:53 AM
- **Type:** Forberedelse

# Materialer

# Intro til Spring Boot

Spring Boot Framework er et open source Java-baseret framework, der gør det nemt at oprette og køre standalone, produktionsklare Spring-baserede applikationer med minimal konfiguration. Det er bygget på toppen af det populære Spring Framework, og bruger konvention over konfiguration, som gør det muligt for udviklere hurtigt at starte med at skrive kode uden at skulle bekymre sig om grundlæggende konfiguration.

Spring Boot leverer en række funktioner og værktøjer, der hjælper med at øge produktiviteten og reducere kompleksiteten ved udvikling af Spring-baserede applikationer. Nogle af de funktioner, der følger med Spring Boot, omfatter automatiske konfigurationer, indlejret serverunderstøttelse, tomme starter-projekter og integrerede testværktøjer.

I modsætning til traditionelle Spring-baserede applikationer, der kræver en masse XML-konfiguration og boilerplate-kode, kan Spring Boot-baserede applikationer oprettes og køres med minimal konfiguration og uden behov for en separat webserver. Alt dette gør Spring Boot til et populært valg for både små og store applikationer, og gør det muligt for udviklere at fokusere på selve koden og funktionaliteten i stedet for at skulle bruge tid på konfiguration og opsætning.

# Pakkestruktur

Pakkestrukturen beskriver en typisk opdeling af ansvarsområder i en Spring Boot-applikation med web.

- **controllers** - denne pakke indeholder klasser, der fungerer som controllers i en Model-View-Controller (MVC) arkitektur. Disse klasser håndterer forespørgsler fra klienter og returnerer data til visning eller videre behandling.
- **repositories** - denne pakke indeholder interfaces og implementeringer af dataadgangslag. Repositories bruges til at udføre CRUD-operationer (Create, Read, Update, Delete) på data i en database eller andre typer af datakilder.
- **models** - denne pakke indeholder klasser, der repræsenterer dataobjekter i applikationen. Disse klasser bruges til at overføre data mellem de forskellige lag i applikationen og til at gemme data i en database.
- **services** - denne pakke indeholder klasser, der indeholder applikationslogikken. Disse klasser bruges til at udføre komplekse operationer, der involverer flere dataobjekter eller kald til andre systemer.
- **dto** - denne pakke indeholder klasser, der repræsenterer dataobjekter, der er specifikt designet til at blive overført over et netværk eller mellem forskellige systemer. Disse klasser bruges typisk til at reducere mængden af data, der skal overføres, eller til at skjule kompleksiteten af de underliggende dataobjekter.
