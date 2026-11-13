# AMP Design System Gap Analysis

Kortlægning af mangler og behov i TV 2's designsystem specifikt for Identity-, Permission- og Account-flows.

## Status på komponenter i AMP

| Komponent / Behov | Findes i Designsystem? | Behov i AMP | Status / Note |
| :--- | :--- | :--- | :--- |
| **PIN-kode input (4/6 cifre)** | Delvist / Nej | Børnesikring, profilskift, hurtiglogin på TV | Undersøges: Findes der standardkomponent? |
| **Password styrkemåler** | ? | Nykontooprettelse & kodeordsskift | Skal overholde gældende sikkerhedskrav |
| **Enhedsoversigt (Device Card)** | Nej | "Administrer dine enheder" / Stream limits | Designes specifikt til AMP med 'Fjern enhed'-knap |
| **Samtykke/Cookie switch** | Ja | Juridiske indstillinger og marketing permissions | Sikre ensartet sprog og tilstande |
| **Nedluknings-/Timeout banner** | Ja | Udløbet session eller session overtaget | Tydelig handlingsknap "Log ind igen" |

## Næste skridt med DesignOps-teamet
* [ ] Check-in med DesignOps om køreplan for komponent-udvidelser.
* [ ] Validering af om AMP's behov kan løftes generisk i `@tv2/afui-components`.
