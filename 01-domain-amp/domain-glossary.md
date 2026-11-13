# AMP Begrebsordbog (Domain Glossary)

Fælles terminologi og tekniske begreber, som anvendes i Audience Management & Permissions hos TV 2.

| Begreb | Beskrivelse | Relevans for UX / Design |
| :--- | :--- | :--- |
| **Auth0** | Den centrale Identity-as-a-Service platform, som TV 2 benytter til login og autentificering. | Sætter tekniske rammer for login-skærme, passwordless login, 2FA og sessionslevetid. |
| **AMT** | Jira-projektkoden for Audience Management & Permission udviklingsteamet (`https://tv2cms.atlassian.net/browse/AMT`). | Hvor user stories, bugs og tekniske opgaver styres. |
| **Permissions** | De konkrete rettigheder en brugerkonto har tilknyttet (f.eks. adgang til live sport, on-demand, TV 2 Regionerne). | Styrer hvornår en bruger møder et "paywall"- eller "opgradering"-flow. |
| **Concurrency Limit** | Grænsen for, hvor mange enheder der kan streame fra samme TV 2 Play konto samtidig. | Kræver gennemtænkt UX, når grænsen rammes: Hvordan smider man en enhed af uden unødig vrede? |
| **Børneprofil & PIN** | En underprofil begrænset til børneindhold med valgfri eller obligatorisk 4-cifret PIN for at forlade profilen. | Balance mellem børns selvbetjening og forældrenes tryghed/kontrol. |
| **Soft error** | En fejl forårsaget af brugerens input (f.eks. forkert formateret e-mail eller svagt kodeord). | Skal håndteres inline med tydelig, handlingsanvisende microcopy. |
| **Hard error** | En teknisk fejl (f.eks. Auth0 nede, token udløbet, netværksfejl). | Skal have beroligende fallback-skærm med mulighed for at genprøve uden datatab. |
| **Samtykke (Consent)** | Brugerens eksplicitte accept af vilkår, dataindsamling eller marketing-kommunikation. | Kræver juridisk korrekthed (GDPR) uden at ødelægge konvertering. |
