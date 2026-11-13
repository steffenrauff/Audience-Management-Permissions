# 04 – Prototypes & State Machines

Dette bibliotek rummer agentisk genererede interaktive kode-prototyper og tilstandsmaskiner (state machines).

## Hvorfor kode-prototyper i AMP?
Statiske Figma-skærme kan ikke fuldt ud validere komplekse tilstande som:
* Tastatur-interaktioner og PIN-kode input.
* Fejlbesked-håndtering ved afbrudt netværk.
* Omskiftning mellem roller (børn vs. voksne).

## Sådan arbejder du her:
1. Definér flowets tilstande i en `state-machine.md` (brug skabelonen i `templates/`).
2. Bed Copilot om at generere en selvstændig, klikbar `prototype.html` med indbygget State Switcher.
3. Brug prototypen til brugertest og til refinement med udviklerne i `AMT`.
