# Indsigtsbibliotek på tværs af produktteams

**Status:** Tidlig problem- og PoC-skitse. Ikke en godkendt dataarkitektur.

## Situation og problem

Flere produktteams arbejder med de samme investeringstemaer og beslægtede initiativer, eksempelvis fastholdelse af favorit- og sportsbrugere gennem øget aktivering. Det skaber kvalitative data fra flere brugerundersøgelser, men indsigterne opleves som bundet til de enkelte teams og bliver ikke nødvendigvis genfundet eller anvendt på tværs af teams og domæner.

## How might we

Hvordan kan vi etablere et setup, hvor data fra kvalitative brugerundersøgelser kan gemmes, findes og anvendes på tværs af teams og domæner?

## Mulige datakilder

- Brugerinterviews
- Surveys
- Etnografiske feltstudier
- Modererede brugertests
- Umodererede brugertests

## Skitseret PoC: brugerinterviews

Den første afprøvning er tænkt med interviewdata.

### 1. Dataindsamling og klargøring

**Formål:** Indsamle data og klargøre den til videre bearbejdning.

**Skitseret flow:**
- Interview optages via Teams eller Sonar.
- Interview downloades i Word-format.
- Personhenførbare oplysninger fjernes ved hjælp af Copilot.

### 2. Dataopbevaring

**Formål:** Centralisere og organisere data, så den kan anvendes igen.

**Skitseret flow:** Kopiere interviewdata ind i en respondentlinje i et centralt datasæt.

### 3. Søgning

**Formål:** Gøre data søgbar via Copilot.

**Skitseret flow:** Aktivere Copilot for Excel og afprøve prompts. De konkrete prompts (X, Y, Z) er endnu ikke defineret.

### Mulige metadata

- Testansvarlig
- Testperson eller respondent-ID
- Dato
- Opsummering
- Tags

## Vigtige afklaringer før brug af rigtige data

Interviewoptagelser og transskriptioner kan indeholde personoplysninger. At fjerne direkte identifikatorer er ikke nødvendigvis det samme som anonymisering; kombinationen af detaljer kan stadig gøre en person genkendelig. Derfor er dette PoC-flow ikke klar til brug med rigtige interviewdata, før håndtering og adgang er afklaret.

- Afklar med relevante privacy-, sikkerheds- og dataansvarlige, hvilke data der må behandles, i hvilke TV 2-godkendte værktøjer og under hvilke aftaler.
- Afklar formål, information/samtykke hvor relevant, dataminimering, adgangsbegrænsning, opbevaringstid og sletning.
- Afklar præcist, hvordan Copilot behandler data i den aktuelle TV 2-konfiguration, og hvem der kan få søgeresultaterne vist.
- Brug respondent-ID frem for navn i det fælles datasæt; opbevar en eventuel identitetsnøgle separat med begrænset adgang.
- Sørg for, at søgninger viser kilde, kontekst og undersøgelsesforhold, så citater ikke løsrives eller fremstilles som repræsentative uden belæg.

## Anbefalet afgrænsning af første afprøvning

Start med at teste genfinding på allerede godkendte, minimerede eller ikke-personhenførbare indsigtskort frem for at gøre fulde råtransskriptioner søgbare. Hvert kort kan som minimum indeholde:

- Stabilt kilde-/respondent-ID og undersøgelsesdato
- Tema, team/domæne og undersøgelsesspørgsmål
- Indsigt eller citat med nødvendig kontekst
- Markering af evidenstype, begrænsninger og usikkerhed
- Link eller reference til den autoriserede kilde
- Ejer og status for opfølgning

Dette tester, om teams faktisk kan genfinde og genbruge viden, før man investerer i et bredere datalager eller AI-søgning over rådata.

## Åbne produktspørgsmål

- Hvilken konkret beslutning eller arbejdssituation skal biblioteket forbedre?
- Hvem er de primære brugere, og hvilke teams/domæner skal have adgang til hvilke data?
- Er det rådata, transskriptioner, kuraterede indsigter eller en kombination, der skal genbruges?
- Hvad skal et nyttigt søgeresultat vise ud over et matchende citat?
- Hvordan skal prompts, tagging og ejerskab vedligeholdes?
- Hvordan måler vi, om indsigter faktisk bliver genbrugt og påvirker beslutninger?

## Centrale trade-offs

- **Genbrug vs. privatliv:** Mere detaljeret kildedata kan give bedre søgning, men øger risikoen ved adgang og behandling.
- **Åben adgang vs. kontekst og ansvar:** Tværgående adgang kan øge genbrug, men kræver klare rettigheder, kildehenvisning og ansvar for fortolkning.
- **Hurtig PoC vs. varig drift:** Excel og Copilot kan være en hurtig test, men ejerskab, adgangsstyring, versionshistorik og sletning skal afklares, før løsningen bliver en vedvarende kilde.
