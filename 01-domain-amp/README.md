# 01 – Domæneviden: Audience Management & Permissions (AMP)

Dette bibliotek indeholder fundamentet for at forstå og arbejde i AMP-teamet hos TV 2.

## Kildebelagt teamkontekst
* [AMP context index](./amp-context-index.md): Første overblik over teamretning, domæne, aktuelle OKR'er, prioriteter og researchindsigter med links til Confluence-kilder.

## Foreløbig kerneopgave (repoets arbejdssammenfatning)
AMP (Audience Management & Permissions) arbejder med sikker og brugervenlig adgang til TV 2's digitale økosystem (primært TV 2 Play, tv2.dk og tilknyttede apps). Dette er repoets arbejdssammenfatning, ikke en officiel mission; AMP-teamspace har endnu ikke udfyldt mission og vision.

### Centrale ansvarsområder:
1. **Identitet & Autentificering:**
   * Login, oprettelse af brugere, Single Sign-On (SSO) og social login.
   * Auth0-integration, token-håndtering og sessionslevetid.
2. **Profilhåndtering:**
   * Hovedprofil vs. underprofiler.
   * Børneprofiler, aldersbegrænsninger og forældrekontrol (PIN-kode).
3. **Permissions & Adgangskontrol:**
   * Validering af abonnementer og pakker (f.eks. Basis, Favorit, Favorit + Sport).
   * Håndtering af samtidig streaming (concurrency limits) på tværs af enheder.
4. **Samtykker & Compliance:**
   * Håndtering af marketing-samtykker, databrug, cookies og vilkårsopdateringer.
   * Overholdelse af GDPR og e-privacy lovgivning.

## Mål for onboardingen (t.o.m. dec '26):
* Opnå dyb forståelse for teamets kapabiliteter, roadmap og tekniske arkitektur.
* Etablere klar snitflade mellem UX/design og PM/udvikling.
* Identificere 1-2 tidlige områder, hvor UX kan skabe mærkbar værdi i teamets WoW.
