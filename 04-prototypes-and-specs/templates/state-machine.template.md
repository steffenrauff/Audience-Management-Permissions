# State Machine Specifikation: [Flow Navn]

* **Flow:** [Eks. Login & 2FA verifikation]
* **Enhed / Platform:** Web / iOS / Android / Smart TV
* **Figma Reference:** [Link]

---

## 1. Tilstandsoversigt (States)

| Tilstands-ID | Navn | Beskrivelse | UI-elementer der vises |
| :--- | :--- | :--- | :--- |
| `S01_IDLE` | Grundtilstand | Tom formular klar til input | Inputfelter, primær CTA (disabled) |
| `S02_VALIDATING` | Validering i gang | Bruger har trykket på CTA | Spinner på knap, inputs låst |
| `S03_SUCCESS` | Succes | Autentificering godkendt | Redirect eller grøn bekræftelse |
| `S04_SOFT_ERROR` | Brugerfejl | Forkert kodeord / ugyldig e-mail | Inline rød fejlbesked, fokus i felt |
| `S05_RATE_LIMIT` | For mange forsøg | Bruger blokeret midlertidigt | Advarselsbanner med nedtælling |
| `S06_HARD_ERROR` | Systemfejl | Auth0 timeout / netværksfejl | Modal/banner med "Prøv igen"-knap |

---

## 2. Overgange (Transitions)

* **Fra `S01_IDLE`:**
  * Bruger taster gyldige data -> CTA aktiveres.
  * Bruger trykker CTA -> Skift til `S02_VALIDATING`.
* **Fra `S02_VALIDATING`:**
  * Backend svarer 200 OK -> Skift til `S03_SUCCESS`.
  * Backend svarer 401 Unauthorized -> Skift til `S04_SOFT_ERROR`.
  * Backend svarer 429 Too Many Requests -> Skift til `S05_RATE_LIMIT`.
  * Timeout / 500 Server Error -> Skift til `S06_HARD_ERROR`.

---

## 3. Data & Parametre der skal persisteres
* Hvilke felter skal bevares ved fejl, så brugeren slipper for at gentaste? (Eks. e-mail bevares, kodeord ryddes).
