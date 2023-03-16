# Bin, Bash and the whole Shebang - 06-02-2023

Fag: Teknologi 2
Oprettet: March 7, 2023 9:03 AM
Reviewed: No
Type: Forberedelse

# **What is an Operating System?**

- Operativsystemet er en central del af en computer, da det fungerer som en mellemlægger mellem hardwaren og softwaren. Det styrker computerens ydeevne ved at administrere ressourcerne, såsom CPU, hukommelse og harddisk, på en effektiv måde. Det gør også det muligt for andre programmer at køre på computeren ved at levere en grænseflade mellem hardwaren og softwaren.
- De mest populære operativsystemer er Windows, macOS og Linux. Windows er det mest udbredte operativsystem til personlige computere, mens macOS er specifikt til Apple-computere. Linux er et gratis, **open source** operativsystem, der er meget anvendt til servere og andre typer computere.
- Operativsystemer tilbyder også funktioner som filhåndtering, sikkerhed, multitasking og netværkstjenester. Det er vigtigt at have et opdateret operativsystem for at opretholde en stabil og sikker computerydelse.

# **Terminal on MacOS**

- Terminal-applikationen på en Mac med macOS er ikke Linux. Terminalen er et kommandolinje-interface, der giver adgang til det underliggende **Unix**baserede operativsystem. macOS er baseret på **Unix**, så det har mange af de samme funktioner og evner som Linux. Terminal-applikationen på macOS er dog ikke den samme som en Linux-terminal, og kommandoerne i terminalen kan variere mellem de to operativsystemer.
- Apples distributionsnavn er **Darwin**, og det er ikke en rigtig distro - men det er det samme som en: Det er bygget på samme måde, som om det var en distro.

# **Difference between console, command line (CLI), terminal and Shell**

- **Console**: En console er en specifik type af output-enhed, der ofte bruges til at vise resultaterne af en kommando, der udføres i et operativsystem.
- **Command** Line Interface (CLI): CLI beskrives som en tekstbaseret grænseflade til at interagere med et operativsystem.
- **Terminal**: En terminal er en specifik type af CLI, der bruges til at interagere med et operativsystem. Terminalen tillader en bruger at udføre administrative opgaver ved hjælp af kommandoer.
- **Shell**: En shell beskrives som en program, der fungerer som en mellemstation mellem en bruger og et operativsystem. Det modtager kommandoer fra en bruger og sender dem videre til operativsystemet for udførelse. Shell kan bruges i en terminal eller anden type CLI.

# **Difference between Bash og Zsh**

- Bash (Bourne Again SHell) og Zsh (Z Shell) er begge Unix-baserede shells, men der er nogle afgørende forskelle mellem dem:
- Funktionalitet: Zsh har en række avancerede funktioner, såsom en intelligent kommandofærdighed, automatiske korrektioner og fulde emulering af andre shells. Bash er en mere grundlæggende shell med mindre funktioner.
- Tilpasning: Zsh giver brugerne en bred vifte af tilpasningsmuligheder, såsom muligheden for at ændre prompt-formatet, bruge forskellige temaer og plugins, mens Bash har færre tilpasningsmuligheder.
- Skriptsprog: Bash er et fuldt fungerende scriptsprog, mens Zsh har mindre støtte til scriptsprog.
    
    Så i alt er Bash en grundlæggende shell med mindre funktioner og tilpasningsmuligheder, mens Zsh er en avanceret shell med mange funktioner og tilpasningsmuligheder. Valget mellem Bash og Zsh afhænger af ens personlige præferencer og behov.
    

# **Most common and useful commands to use**

- Ifølge denne artikel er følgende nogle af de mest almindelige og nyttige kommandoer at bruge i en kommandolinje:
- `ls`: List filer og mapper i den aktuelle mappe.
- `cd`: Skift til en anden mappe.
- `pwd`: Vis den aktuelle mappe.
- `mkdir`: Opret en ny mappe.
- `rmdir`: Slet en mappe.
- `touch`: Opret en ny fil.
- `cp`: Kopiér en fil eller mappe.
- `mv`: Flyt eller omdøb en fil eller mappe.
- `rm`: Slet en fil.
- `cat`: Vis indholdet af en fil.
- `less`: Vis indholdet af en fil en side ad gangen.
- `head`: Vis de første linjer af en fil.
- `tail`: Vis de sidste linjer af en fil.
- `grep`: Søg i filer for en bestemt tekststreng.
- `curl` er en kommandolinjeværktøj, der bruges til at hente data fra internettet eller sende data til et websted. Det støtter mange protokoller, herunder HTTP, HTTPS, FTP, FTPS, SCP, SFTP, TFTP, DICT, TELNET, LDAP og SMTP.
- `pushd` d

# **Git commands**

- `git init`: Initialiser et nyt Git-repository.
- `git clone`: Klon et eksisterende Git-repository.
- `git status`: Vis status for det aktuelle Git-repository.
- `git add`: Tilføj filer til det næste commit.
- `git commit`: Committet ændringer til det aktuelle Git-repository.
- `git push`: Send de lokale commits til et remote repository.
- `git pull`: Træk ændringer fra et remote repository til det lokale repository.
- `git branch`: Behandle Git-branches.
- `git checkout`: Skift mellem branches eller tagge.
- `git merge`: Flet to branches sammen.
- `git log`: Vis historikken for commits i det aktuelle Git-repository.
- `git show`: Vis information om et bestemt commit.
- `git diff`: Vis forskelle mellem to versioner af en fil.
- `git stash`: Gem ændringerne lokalt i Git-repositoryet uden at committe dem.
- `git reset`: Nulstil en fil til en tidligere version.
- `git revert`: Omgør en tidligere commit.

# **POSIX**

- Artiklen beskriver POSIX (Portable Operating System Interface) som en samling af standarder, der definerer et programmelinterface til Unix-lignende operativsystemer. POSIX gør det muligt for softwareudviklere at skrive programmer, der kan køre på en række forskellige operativsystemer, herunder Linux og macOS, uden at skulle tilpasse deres kode til den enkelte platform.
- Richard Stallman, grundlægger af Free Software Foundation, forklarer, at POSIX standarderne gør det muligt for softwareudviklere at fokusere på det faktiske program, frem for at bekymre sig om, hvordan det kører på en given platform. Stallman fremhæver også, at POSIX er en af de ting, der gør det muligt for Linux og andre Unix-lignende operativsystemer at fungere så effektivt og stabilt.
- Artiklen slutter med at fremhæve, at POSIX er et vigtigt element i den åbne kildes softwarebølge og har spillet en central rolle i at gøre det muligt for softwareudviklere at opbygge avancerede og pålidelige systemer på en lang række platforme.

# **Wikipedia 'Linux'**

- Linux er et frit og open-source operativsystem, der er baseret på Unix. Det blev først frigivet i 1991 af Linus Torvalds og har siden været udviklet og vedligeholdt af et samarbejde af frivillige udviklere over hele verden.
- Linux er blevet bredt anvendt på mange platforme, herunder supercomputere, servere, mobiltelefoner, smart-tv'er og i den Internet of Things (IoT). Det bruges også ofte som det primære operativsystem i webhostingmiljøer og for at køre virtualiseringssoftware.
- Linux er kendt for sin skalerbare arkitektur, robuste sikkerhedsmodeller og store samling af open-source software, herunder en række gratis programmer til kontor, grafik, webudvikling, databasehåndtering og meget mere.
- Der findes mange varianter af Linux, kaldet distributions eller "distros", hver med deres egne unikke funktioner og målgrupper. De mest populære distributions inkluderer Ubuntu, Fedora, Debian og CentOS.
- I det hele taget har Linux været en stor succes i it-branchen og har været en drivkraft bag mange af de teknologier, vi tager for givet i dag, såsom internettet, cloud computing og big data-analyse.

### **History of Unix-like operating systems**

- 
    
    ![Unix-like operating systems through history: [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Unix_timeline.en.svg/1280px-Unix_timeline.en.svg.png)
    
    Unix-like operating systems through history: [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)
    

### **Layers within Linux**

![Layers within Linux: [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)](Bin,%20Bash%20and%20the%20whole%20Shebang%20-%2006-02-2023%20ace84920491a4af8a6d517d4d47f5ea6/Untitled.png)

Layers within Linux: [https://en.wikipedia.org/wiki/Linux](https://en.wikipedia.org/wiki/Linux)

# **Linux kernel**

- Artiklen beskriver Linux-kernen som det centrale stykke software i Linux-operativsystemet. Det fungerer som en liaison mellem hardwaren og de øvrige programmer, der kører på systemet. Linux-kernen administrerer systemressourcer såsom hukommelse, processorkraft og input-output-enheder og sørger for, at de er tilgængelige for de andre programmer, der kører på systemet.
- Linux-kernen er open-source software, hvilket betyder, at den er frit tilgængelig og kan ændres og tilpasses af udviklere over hele verden. På grund af dette har Linux-kernen gennemgået mange forbedringer og tilføjelser gennem årene, hvilket har gjort det til et af de mest pålidelige og skalerbare operativsystemer.
- Artiklen slutter med at fremhæve, at Linux-kernen er blevet brugt som grundlag for mange andre operativsystemer, herunder Android, og er et af de mest succesrige open-source projekter nogensinde.
    
    *kilde:* [https://www.redhat.com/en/topics/linux/what-is-the-linux-kernel](https://www.redhat.com/en/topics/linux/what-is-the-linux-kernel)
