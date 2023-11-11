![[Software Plan 3 of 3.pdf]]
# Formålet med software estimering

Formålet med estimering er at få et realistisk overblik over tidsforbrug, ressourcer og omkostninger før projektstart. Danner grundlag for planlægning, prioritering og risikovurdering.

# Teknikker til estimering

## Analog estimering

Estimer ud fra lignende projekter vha. erfaringsdatabase. Simpel, men kræver solidt erfaringsgrundlag.

## Procesbaseret
- Nedbryd processen i aktiviteter
- Estimér hver aktivitet baseret på historik
- Summér estimater

Estimér ved at nedbryde processen i aktiviteter og estimere hver aktivitet:

Effort = Σ Effort(activitet i)

Aktivitetsestimater baseres på historiske data.

## Problembaseret
- Nedbryd scope i funktioner
- Estimér hver funktion i f.eks. LOC, FP eller objekter
- Anvend produktivitetsdata

Nedbryd scope i funktioner og estimér hver:

Effort = Σ Volume(funktion i) / Produktivitet

Fx ved at estimere LOC, FP eller objekter for hver funktion.

## Use case point
- Vurder kompleksitet af use cases og aktører
- Justér med tekniske og miljøfaktorer
- Omregn til tidsestimat

UCP = (UUCW + UAW) * TCF * ECF

UCP omregnes til effort vha. historisk produktivitet.

## Agil
- Nedbryd user stories i tasks
- Anvend erfaring til estimering
- Summér estimater for sprint

Estimer opgaveestimationer eller user story volumen.

Effort(sprint) = Σ Effort(user story i)

# Software size estimering

Størrelse estimeres ud fra funktioner, use cases, klasser, processer, LOC, FP, etc.

# Usikkerhed og risici

Tag højde for usikkerhed med intervalestimater eller sandsynlighedsfordelinger.

Overvej projektrisici som truer estimaterne.

# Afstemning af estimater

Lav estimater med flere teknikker. Afstem ved at vægte eller analysere forskelle.

# Opsummering

Nøglen er korrekt skøn af software size og produktivitet samt bredt erfaringsgrundlag. Kvantificer usikkerhed og tag højde for risici.


# Opgave
![[Function Point - Tutorial.docx]]

a) Jeg udfylder estimeringstabellen:

Complexity Weighting

---

Element Low Average High Total

Inputs 10 x 2 = 20 0 x 3 + 0 x 4 = 0 20

Outputs 0 x 3 20 x 6 = 120 0 x 9 = 0 120

Inquiries 0 x 2 10 x 4 = 40 0 x 6 = 0 40

Files 0 x 5 0 x 8 = 0 30 x 12 = 360 360

Interface 0 x 5 0 x 10 = 0 50 x 15 = 750 750

TOTAL = 1290 Function Points

Total Function Points = 1290

Med 5 function points per person-month og 6 personer:

Total Person Months = 1290/5 = 258

Project duration = 258/6 = 43 months

---

b) Med 20 personer:

Total Person Months = 258 Project Duration = 258/20 = 13 months

---

c) For 6 måneder med x antal personer:

258 person-months / 6 months = 43 people

Så der skal 43 personer til for at fuldføre projektet på 6 måneder.