# Flow Stress-Test & State Machine Audit

Brug dette prompt-workflow, når du vil have Copilot til at gå kritisk til et nyt eller eksisterende AMP-flow og identificere blinde vinkler, fejltilstande og edge cases.

---

## Opgave til Copilot
Undersøg det beskrevne eller vedhæftede flow (fra tekst eller Figma-node) med rollen som **Adversarial UX Auditor** i AMP-teamet.

Gennemfør analysen i følgende tre faser:

### 1. Tilstands- og logikmatrix (State Matrix)
Opstil en tabel med alle tænkelige tilstande:
* **Happy path:** Det ideelle flow.
* **Valideringsfejl (Soft errors):** Ugyldigt format, manglende påkrævet felt, svagt kodeord.
* **Tekniske & sessionsfejl (Hard errors):** Timeout på Auth0/backend, session udløbet, netværksafbrydelse midtvejs.
* **Domæne-specifikke edge cases:**
  * Bruger er under 18 år / børneprofil uden rettighed.
  * Maksimalt antal samtidige streams nået (concurrency limit).
  * Brugeren afviser et obligatorisk eller valgfrit samtykke.
  * Brugeren trykker "Tilbage" i browseren/appen på et kritisk tidspunkt.

### 2. Kritiske udfordringer (The Challenger)
Stil mig 3-5 skarpe spørgsmål:
* *"Har du overvejet, hvad der sker for [brugerprofil X] i [situation Y]?"*
* *"Er der risiko for, at [element Z] forvirrer brugeren eller øger frafaldet?"*
* *"Hvad er det tekniske trade-off ved at vælge denne løsning over enklere alternativer?"*

### 3. Anbefalet microcopy & fejlmeddelelser
Foreslå konkrete danske formuleringer til de identificerede fejltilstande med fokus på at være vejledende, transparente og i TV 2's tone-of-voice.
