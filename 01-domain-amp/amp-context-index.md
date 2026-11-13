# AMP context index

**Status:** Første, kildebelagte overblik – ikke en komplet kortlægning.  
**Confluence tjekket:** 13. november 2026. Confluence er kilden; brug links og tjek seneste version, før indhold bruges til beslutninger.

## Teamretning

AMP's teamspace [Audience Management & Permissions](https://tv2cms.atlassian.net/wiki/spaces/AM/overview) er stadig en Confluence-skabelon: felterne for mission, vision, teammål og vigtige sider er placeholders. Jeg har derfor ikke fundet en aktuel, eksplicit teammission dér.

Den mest aktuelle dokumenterede retning er i stedet **OKR for cyklus 4, 2026** (2. november 2026–1. februar 2027). Det er en operationel retning for cyklussen, ikke nødvendigvis en langsigtet strategi.

## Domæne og applikationer

De officielle applikationsbeskrivelser findes primært i recovery-planer. De beskriver systemansvar, men udgør ikke alene en fuldstændig produkt- eller UX-domænemodel.

- **Audience Access Management (AAM):** Auth0 håndterer kundevendt login og brugeroprettelse for TV 2 Play og TV 2 Free samt authentication/authorization mellem systemer. [Kilde](https://tv2cms.atlassian.net/wiki/spaces/AM/pages/4953145347/Audience+Access+Management), senest opdateret 28. maj 2026.
- **Audience Identity Management (AIM):** Masterdata om brugere samt interaktion med brugerdata, kontorelaterede e-mails og videreformidling af ændringer til interne systemer. [Kilde](https://tv2cms.atlassian.net/wiki/spaces/AM/pages/4948066674/Audience+Identity+Management), senest opdateret 22. maj 2026.
- **Audience Identity Consent Management / Terms and Permissions (TaPs):** Indsamler, lagrer og behandler vilkår og kommercielle tilladelser, herunder registrering af accepterede vilkår og tilladelser, som downstream services kan bruge. [Kilde](https://tv2cms.atlassian.net/wiki/spaces/AM/pages/5012946952/Audience+Identity+Consent+Management), senest opdateret 8. juli 2026.

## Fremtidige AMP-kapabiliteter

Følgende kapabiliteter er oplyst som områder, AMP ejer og driver fremadrettet. Listen er tilføjet på baggrund af teamkontekst og er ikke verificeret mod en Confluence-kilde.

- Login Interface (storskærme)
- Konto- og brugeradministration (Mit TV 2)
- Profil Interface
- Terms & Permissions Interface
- Husstandsadministration
- Administration af præferencer
- CMP (Cookie frontend)
- Push-notifikationer
- Authentication Platform (backend)
- Brugeridentiteter (backend)
- Distribution af 1. parts brugerdata
- Single Customer View

## UX-relevans og mulige undersøgelsesspor

Nedenstående er Steffens foreløbige vurdering af, hvor UX-research kan bidrage på tværs af kapabiliteterne. Relevansniveauerne gengiver farvekodningen i oplægget; undersøgelsessporene er idéer, ikke validerede brugerbehov.

| Kapabilitet | UX-relevans | Mulige undersøgelsesspor |
|---|---|---|
| Login Interface (storskærme) | Grøn | Login-friktion, QR-flow, pairing-flow, fejlforståelse, recovery-flow og first-time setup |
| Konto- og brugeradministration (Mit TV 2) | Grøn | Hvad forsøger brugerne at opnå? Hvad er svært at finde? Forståelse af abonnement, konto, data og indstillinger |
| Profil Interface | Grøn | Forståelse af profiler, børneprofiler, husholdningsbrug og profilskift |
| Terms & Permissions Interface | Grøn | Forståelse af samtykker, GDPR, privatliv, informationsarkitektur og tillid |
| Husstandsadministration | Grøn | Mental model omkring husstand, antal brugere, begrænsninger og fejlscenarier |
| Administration af præferencer | Gul | Hvilke præferencer giver værdi? Hvad forventer brugerne at kunne styre? |
| CMP (Cookie frontend) | Gul | Cookieforståelse, samtykke-flow, tillid og compliance versus brugeroplevelse |
| Push-notifikationer | Gul | Forståelse af notifikationer, relevans og styring |
| Authentication Platform (backend) | Rød | Primært indirekte research gennem frontend-effekter |
| Brugeridentiteter (backend) | Rød | Mest indirekte research |
| Distribution af 1. parts brugerdata | Rød | Meget begrænset direkte brugerflade |
| Single Customer View | Rød | Mere konceptuelt og organisatorisk end brugerrettet |

Kilde: Steffens UX-overblik delt 13. november 2026. Farverne viser en foreløbig vurdering af UX-relevans, ikke prioritering eller beslutning om researchindsats.

## OKR'er – cyklus 4, 2026

Kilde: [OKR - cyklus 4, 2026](https://tv2cms.atlassian.net/wiki/spaces/AM/pages/6737854651/OKR+-+cyklus+4+2026), senest opdateret 30. oktober 2026.

1. **Enhedsbaseret samtykke:** Lancere samtykke til målrettet markedsføring og reklame på alle 17 platforme inden udgangen af 2026 og opnå en høj samtykkerate.
2. **Kontobeskyttelse:** Afsøge tre Auth0-sikkerhedstiltag, der balancerer sikkerhed og brugeroplevelse, og implementere mindst ét.
3. **Omkostningsbevidsthed / FinOps:** Isolere og migrere E-mail Service til egen LeanIX-applikation og egne AWS-konti som led i migration til applikations-scoped konti.
4. **Lambda-migrering:** Migrere 30 af 53 Lambda-funktioner fra Serverless Framework til Go for at reducere sikkerhedsrisici og fremtidige omkostninger.

Siden angiver ikke en aktuel status for disse key results. Kontrollér derfor status direkte i Confluence, før der konkluderes på fremdrift.

## Aktuelle prioriteter

Den seneste fundne sprintplan er [NAPKIN sprint 2 i cyklus 4](https://tv2cms.atlassian.net/wiki/spaces/AM/pages/6809452857/NAPKIN+sprint+2+i+cyklus+4+2026), opdateret 13. november 2026. Den gælder sprinten frem til 27. november og er et øjebliksbillede – ikke et roadmap.

**P1 i sprintplanen:**
- Support til OneTrust.
- Ny end-to-end-testrunde på Play og Free i uge 47.
- Opsætning af automatiske rapporter i OneTrust.

**Discovery/refinement nævnt i planen:**
- Onboarding på ny incidentproces.
- Tagging af applikationer i AWS.
- Rækkefølge og onboarding af services fra PDL.
- Afklaring af Auth0 Security-tiltag.
- Refinement af migrationen af E-mail Service til egen AWS-konto.

Sprintplanen indeholder åbne spørgsmål og blandede prioritetsnoter. Brug den til at finde aktuelle emner, men bekræft prioriteringen hos teamet/PM.

## Researchindsigter

### Direkte relevant for AMP: login og MFA

- **Juni 2025, intern test med 10 TV 2-medarbejdere:** Deltagerne oplevede selve MFA-flowet som forholdsvis let, men der var friktion omkring uventet logout, at opdage at man var logget ud, at finde/indtaste engangskoden og at familien var afhængig af kontoejerens e-mail. Der blev også efterspurgt tydeligere adgang til QR-login på TV. **Begrænsning:** Interne medarbejdere er ikke repræsentative for kunder. [Test og findings](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/5364350998/Intern+test+af+MFA+2+faktor+godkendelse+i+fbm+login+-+juni+25).
- **September 2025, kvalitativ modereret test med tre ældre deltagere:** MFA-siden blev forvekslet med login-siden; engangskodefeltets visuelle tilstand og tastaturet, der skjulte forklarende tekst, bidrog til forvirring. **Begrænsning:** Meget lille kvalitativ test; fundene er signaler til videre undersøgelse, ikke mål for udbredelse. [Test og findings](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/5394300960/Brugertest+af+MFA+i+fbm+login+-+sep+25).

Disse fund er relevante i lyset af C4-OKR'et om kontobeskyttelse, men de er fra 2025. De bør ikke antages at beskrive den nuværende MFA-oplevelse uden at tjekke nyere tests og produktændringer.

### Nært beslægtet, men ikke AMP-ejet: partneraktivering

- **Mayflower / Apple TV og Disney+, 2026:** Samlet research peger på en forventning om en mere integreret oplevelse med ét app-/login-flow, mens separate apps og logins skaber mismatch. Brugere var også usikre på pakkens værdi og indhold, eksisterende partnerabonnementer og aktiveringsforløbet. Kildesiden samler flere metoder og Kundecenter-viden; den er ikke en isoleret effektmåling. [Key findings](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/6333169701/Mayflower+-+Apple+TV+og+Disney).
- **Preely-test af aktiveringsmails, juni 2026, 33 gennemførte besvarelser:** 22 af 33 forstod, at Disney+-indhold ses i Disney+-appen. De øvrige svar fordelte sig på forventning om begge apps (5), usikkerhed (3) eller forventning om TV 2 Play alene (3). Mail 2 og 3 blev foretrukket omtrent lige ofte; tydelighed, overblik og balance mellem korthed og nødvendig information var centrale. **Begrænsning:** Umoderret prototypetest; ikke dokumentation for faktisk aktivering i drift. [Test og findings](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/6375669857/Preely+test+af+aktiveringsmails+for+Apple+TV+og+Disney).

### Hvor flere indsigter findes

- [Audience Interactions – researchoversigt](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/5810094098/1.+Audience+Interactions) er et aktivitetskatalog med studier på tværs af Play og Mit TV 2. Kataloget er en indgang til undersøgelser, ikke i sig selv en syntese af fund.
- [UX ResearchOps](https://tv2cms.atlassian.net/wiki/spaces/URR/pages/5801771041/UX+ResearchOps) beskriver fælles metodeapparat, processer og værktøjer. Flere enkeltstudier linker videre til SharePoint, Preely, GetWhy eller andre kilder.

## Huller og brug af indekset

- Der er ikke fundet én samlet, aktuel AMP-mission/vision eller en komplet domænebeskrivelse i AMP-teamspace.
- Research er fordelt på ResearchOps-oversigter og enkeltstudier; de fundne eksempler dækker ikke alle AMP-emner eller platforme.
- Før en beslutning: åbn kilden, tjek dato og status, og skeln mellem kundetest, intern test, usability-test og drifts-/QA-test.
- Brug dette indeks som startpunkt. Ved konkrete spørgsmål bør de relevante Confluence-sider hentes igen, så nyere beslutninger og ændringer ikke overses.
