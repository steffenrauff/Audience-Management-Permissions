# Jira Spec & Acceptkriterie Generator (AMT Bridge)

Brug dette prompt-workflow, når du har et færdigt design i Figma eller en flow-specifikation, som skal overleveres præcist til udviklerne i Jira-projekt `AMT`.

---

## Opgave til Copilot
Konverter det angivne designflow/specifikation til en formel Jira-beskrivelse med **Given/When/Then** acceptkriterier og tekniske tilstande.

### Output-format:

#### 1. Baggrund & Formål
* Kort resumé af brugerrejsen og hvorfor vi laver ændringen.
* Link til Figma-frame/prototype.

#### 2. Acceptkriterier (Given / When / Then)
* **AC 1 (Happy path):**
  * *Given* en bruger er logget ind med gyldig session...
  * *When* brugeren klikker [knap]...
  * *Then* opdateres [tilstand], og brugeren ser [bekræftelse].
* **AC 2 (Fejlhåndtering / validering):**
  * *Given* brugeren indtaster...
  * *When* ...
  * *Then* ...
* **AC 3 (Edge cases & permissions):**
  * Håndtering af udløbet token, manglende rettigheder, afvist samtykke.

#### 3. Data- og tilstandskrav
* Relevante datafelter (f.eks. `dataLayer.permissions.*`, Auth0 metadata, profil-ID).
* Påkrævede API-kald eller redirects.

#### 4. Tekstnøgler / Microcopy
* Nøjagtig ordlyd på overskrifter, hjælpetekster, knapper og fejlbeskeder.
