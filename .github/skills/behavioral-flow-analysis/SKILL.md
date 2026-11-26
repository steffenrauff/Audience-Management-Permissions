---
name: behavioral-flow-analysis
description: Analyze observed user behavior in a product flow using analytics, event data, funnels, or supplied dashboards. Use when investigating completion, drop-off, repeated steps, flow duration, or differences across products and platforms, including login, signup, and account recovery. Distinguish observed behavior from hypotheses and connect findings to research questions and product decisions.
---

# Behavioral flow analysis

Undersøg, hvad brugere gør i et flow, og hvad teamet bør undersøge eller beslutte. Analytics kan vise **hvad** der sker, men forklarer ikke i sig selv **hvorfor**.

## 1. Afgræns flowet

- Beskriv beslutningen eller spørgsmålet, analysen skal kvalificere, samt periode, produkt og målgruppe.
- Definér startpunkt, ønsket outcome og centrale steps. Skeln mellem antaget flow og dokumenteret tracking.
- Afklar, om outcome er en teknisk hændelse eller faktisk adgang til den ønskede aktivitet. Spørg brugeren, hvis en væsentlig afgrænsning ikke kan udledes.

## 2. Definér målingen

- Vælg relevante spørgsmål: completion og frafald, tilbagevenden til tidligere steps, gentagne forsøg, tid gennem flowet samt forskelle på produkt, platform eller segment.
- Angiv tæller, nævner, analyseenhed (fx events, sessioner eller brugere), tidsvindue og regler for rækkefølge og gentagelser. Definér, hvad der tæller som completion og frafald.
- Undersøg, om tracking dækker alle steps og relevante platforme. Vær særligt opmærksom på sessioner, der krydser browser, app, e-mail eller TV. Antag ikke, at de kan forbindes.
- Sammenlign både antal og andele, når data tillader det. Kontrollér stikprøvestørrelser, manglende værdier og sammenlignelige definitioner.

## 3. Indhent data

- Brug autoriserede, tilgængelige kilder, fx Adobe Analytics, relevante dashboards, eksporter eller brugerens materiale. Find relevante events, page views og funnel- eller completion-målinger, og kontrollér kilde, periode og filtre.
- Oplys, hvis adgang, tracking eller dimensioner mangler. Bed om adgang eller de nødvendige data; opfind ikke tal, events, dimensioner eller en tilgængelig MCP-forbindelse.
- Behandl API-kald og fejlkoder som tekniske observationer: De er ikke automatisk unikke brugere, afbrudte brugerrejser eller dokumenterede brugerproblemer. Overfør ikke en fordeling fra én måling til en anden uden dokumenteret sammenhæng.
- Brug aggregerede data og godkendte identifikatorer; undgå personoplysninger og uautoriseret sammenkobling på tværs af kilder.

## 4. Analysér og fortolk

For hvert væsentligt fund, adskil:

1. **Observation:** Hvad viser data konkret? Angiv kilde, periode, måling og nævner.
2. **Mønster:** Hvilke forskelle eller gentagelser kan faktisk understøttes af data?
3. **Mulig forklaring:** Hvilke alternative hypoteser, inklusive tracking- eller tekniske forhold, kan forklare mønstret?
4. **Researchspørgsmål:** Hvad skal undersøges kvalitativt eller med yderligere data?

Korrelation med completion er ikke bevis for årsag. Vurdér selektion og om forskellen kan skyldes forskellige brugergrupper eller mangelfuld tracking. Et fald mellem to events er ikke nødvendigvis frafald, hvis næste step ikke måles eller sker på en anden enhed.

Eksempel: Et målt fald på 42 % mellem to definerede events er en observation. At brugerne ikke forstår det næste step er en hypotese, som kræver anden evidens.

## 5. Lever resultatet

Tilpas længden til opgaven, men medtag:

- **Flow og målegrundlag:** start, outcome, steps, kilde, periode og afgrænsninger.
- **Observationer og mønstre:** antal og andele med definitioner, hvor de findes.
- **Mulige forklaringer og researchspørgsmål:** markeret som hypoteser, ikke fund.
- **Datamangler og næste skridt:** hvad kan besvares nu, og hvad kræver mere tracking, D&I eller brugerresearch?
- **Betydning og anbefaling:** hvilken beslutning kan data understøtte, og hvilke trade-offs mellem brugeroplevelse, sikkerhed og jura er relevante?

Hvis brugeren ønsker en board-egnet spørgeliste frem for en fuld analyse, brug de ønskede overskrifter og opfind ikke observationer for at udfylde dem.
