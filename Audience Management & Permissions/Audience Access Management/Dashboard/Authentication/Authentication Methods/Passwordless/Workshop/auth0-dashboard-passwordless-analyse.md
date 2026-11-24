# Datakilder til passwordless-initiativet

**Status:** Arbejdsnotat, ikke en godkendt måleplan.  
**Gennemgået:** 23. november 2026.

## Formål

Kortlæg, hvad de tilgængelige rapporter kan bidrage med til discovery og senere evaluering af passwordless. I [AMT-3165](https://tv2cms.atlassian.net/browse/AMT-3165) undersøges Auth0 passwordless med engangskoder (OTP) i lyset af både sikkerhed og brugeroplevelse. Opgaven beskriver, at identifier-first kan påvirke flere loginrelaterede flows; bekræft den aktuelle løsning og udrulningsplan med teamet.

## Rapporter

### Auth0 brugere – Power BI

- [Åbn rapporten](https://app.powerbi.com/groups/me/apps/fbcdc5a9-6836-4756-afac-9c1f0675244c/reports/4da9ff80-0c04-4fb7-b7f7-f9dd618d4e81/ReportSectiond545f9091863f28eb422?ctid=ad00f650-cdf1-41b5-8ff1-88b7c9650d3e&experience=power-bi).
- **Kilde ifølge rapporten:** TV 2 DWH.
- **Gennemgåede visninger:** Auth0 brugere og Oprettelsessteder.
- Rapporten viser udvikling i loginbasen, nye logins, nettoudvikling og slettede logins fordelt på maskinelle og manuelle sletninger. Oprettelsesstedsvisningen fordeler loginbasen og nye logins på oprettelsessteder.
- Filtre omfatter dato, alder, køn og oprettelsessted.

#### Spørgsmål rapporten kan belyse

- Hvordan udvikler loginbasen og antallet af nye og slettede logins sig?
- Hvilke oprettelsessteder bidrager med flest nye logins?
- Hvordan ser de viste tal ud, når de filtreres på alder, køn eller oprettelsessted?

#### Relevans for passwordless

- **Prioritering:** Fordelingen på oprettelsessteder kan hjælpe med at vælge signup- og checkoutforløb til videre undersøgelse.
- **Baseline og overvågning:** Nye og slettede logins kan bruges som overordnede signaler om udsving før og efter en ændring.
- **Researchplanlægning:** Filtrene kan inspirere til valg af brugergrupper og indgangspunkter i en test.

Ved gennemgangen var perioden 24. juli–22. november 2026 valgt med alle alders-, køns- og oprettelsesstedsfiltre. Rapporten viste 61.880 nye logins for Partner API og 30.426 for checkout.play.tv2.dk. Det er antal, ikke konverteringsrater.

#### Begrænsninger

- Oprettelsessted er ikke nødvendigvis det sted eller den platform, hvor brugeren senere logger ind. Tallene beskriver derfor ikke alle brugere eller flows, der påvirkes af passwordless.
- De gennemgåede visninger måler ikke loginforsøg, gennemførelse, frafald, OTP-levering eller oplevet friktion. De viser heller ikke, hvorfor en konto slettes.
- Afklar med D&I definitionerne af login, nyt login og sletningstyper, og hvordan datofilteret påvirker de enkelte visualiseringer.
- [AMT-3165](https://tv2cms.atlassian.net/browse/AMT-3165) beskriver et større signup-angreb i perioden. Undersøg konsekvenserne for baseline, før perioder sammenlignes.
- En ændring før og efter lancering dokumenterer ikke i sig selv en effekt af passwordless.

### Auth0 Metrics – Datadog

- [Åbn rapporten](https://app.datadoghq.eu/dashboard/ajq-8b8-3ef/auth0-metrics?fromUser=false&refresh_mode=sliding&from_ts=1795387440858&to_ts=1795391040858&live=true).
- **Status ved gennemgang:** Indholdet kunne ikke læses uden adgang. Indhold og anvendelighed er derfor ikke verificeret.

### Audience Management & Permissions TV Board – Datadog

- [Åbn rapporten](https://app.datadoghq.eu/dashboard/4t6-asg-dza/ccs-am-audience-management-permissions-tv-board?fromUser=false&refresh_mode=sliding&tile_focus=5664284957993449&from_ts=1795376641257&to_ts=1795391041257&live=true).
- **Status ved gennemgang:** Datadog viste en loginside. Indhold og anvendelighed er derfor ikke verificeret.

Datadog-linkene indeholder den tidsindstilling, der blev delt. Kontrollér tidsinterval og filtre, når de åbnes igen.

## Supplerende kontekst fra discovery-board

Kilde: [Q1 2026_Discovery for improved login journeys](https://lucid.app/lucidspark/642a92a1-de44-4646-8293-c61a71a2a520/edit?invitationId=inv_33c2926f-f3ef-4ad0-95f1-d92aff4d71e7&page=0_0). Boardet samler brugerrejser, workshopantagelser, testnoter og mulige løsninger; det er ikke én samlet valideret konklusion.

- **Tidligere signaler:** Boardet angiver historiske tal for login og glemt-adgangskode-flowet, men beskriver også usikkerhed om frafald og behov for yderligere tracking. Bekræft periode, definitioner og datagrundlag, før tallene bruges som baseline.
- **Kvalitativt materiale:** Boardet beskriver et eksplorativt interview og en usability-test med fem interne brugere og indeholder testnoter. Blandt de sammenfattede temaer er mental belastning ved at finde en ny adgangskode og forventningen om tydelig vejledning. Fundene er signaler, ikke repræsentative mål for alle brugere.
- **Hypoteser til genundersøgelse:** Forkert eller utilgængelig e-mail, forsinket eller manglende e-mail, udløbne links og usikkerhed om vejen tilbage til appen kan skabe friktion. Boardet præsenterer flere af disse som antagelser om glemt-adgangskode-flowet; deres udbredelse og relevans for OTP er ikke fastslået.
- **Mulige alternativer:** Boardet nævner passwordless, adgangskode som alternativ og forskellige recovery-muligheder. Det er idéer til afprøvning, ikke dokumentation for en valgt løsning eller for, at én metode altid er mere sikker.

### Spørgsmål til passwordless-discovery

- Kan brugere få adgang igen uden at skulle opfinde en ny adgangskode, og oplever de det som lettere?
- Hvad sker der, hvis OTP-mailen er forsinket, havner i spam, eller brugeren ikke har adgang til mailboksen?
- Kan brugeren gennemføre på tværs af enheder og finde tilbage til den oprindelige app?
- Hvordan balanceres tydelig hjælp og fallback med risikoen for account enumeration og andre sikkerhedshensyn?

## Supplerende måling og research

Power BI-rapporten bør suppleres med en måleplan, der afklarer, om eksisterende datakilder allerede kan levere:

1. **UX:** Andel, der starter og gennemfører signup og login, gennemførelsestid, frafald og behov for hjælp.
2. **OTP:** Levering, brug, fejl, udløbne koder og nye forsøg, opdelt på relevante flows og platforme.
3. **Sikkerhed:** Aftalte indikatorer for misbrug og account enumeration samt falske blokeringer.
4. **Tilgængelighed og privatliv:** Brugertest af bl.a. manglende umiddelbar adgang til e-mail samt afklaring af dataminimering, behandlingsgrundlag og eventuelle samtykkekrav.

Definér tæller, nævner, segmenter og baseline med D&I. Sammenlign gerne med en kontrolvariant, hvis det er teknisk og organisatorisk muligt; bekræft først, hvilke flows der kan udrulles separat.

## Anbefaling

Brug Power BI som kontekst og overvågningssignal, ikke som selvstændig effektmåling. Gennemgå Datadog-rapporterne efter adgang er etableret, og aftal derefter med D&I og AMP, hvilke eksisterende målinger der kan genbruges, og hvilke der mangler.
