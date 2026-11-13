# Audience Management & Permissions (AMP) – Design & Agent Workspace

Velkommen til det personlige agent- og design-workspace for **Steffen Klitlund Rauff** i AMP-teamet hos TV 2 Danmark.

Dette repository er bygget til at understøtte en **agentisk arbejdsgang** med GitHub Copilot, VS Code og MCP (Figma & Atlassian), med fokus på at forene stærk UX-research med strategisk produktledelse (PM-muskler).

---

## Mappestruktur

* [`.github/`](./.github/) — Agent-instruktioner (`copilot-instructions.md`) og genbrugelige prompt-workflows.
* [`01-domain-amp/`](./01-domain-amp/) — Domæneviden, systemarkitektur (Auth0, permissions), ansvarsområder og snitflader (Anja/PM, Malene, D&I).
* [`02-research-to-decisions/`](./02-research-to-decisions/) — Beslutningsdrevet research: Problem framing, evidenssyntese og beslutningsbriefs med klare trade-offs.
* [`03-designops-and-system/`](./03-designops-and-system/) — Praksis for TV 2's designsystem (`@tv2/afui-components`) i AMP, komponent-gaps og microcopy-standarder.
* [`04-prototypes-and-specs/`](./04-prototypes-and-specs/) — Interaktive kode-prototyper og udtømmende tilstandsmaskiner (State Machines).
* [`05-sparring-and-reflection/`](./05-sparring-and-reflection/) — Dit personlige refleksions- og sparringslaboratorium ("The Challenger", ugentlig 1:1 forberedelse til Jacob Ø og eksperimentlog).

---

## Hurtigstart: Sådan bruger du dine agenter
* **Vil du udfordres på et design eller en idé?** Kør prompten i [`.github/prompts/01-flow-stress-test.prompt.md`](./.github/prompts/01-flow-stress-test.prompt.md) eller [`05-sparring-and-reflection/sparring-prompts/challenge-my-flow.prompt.md`](./05-sparring-and-reflection/sparring-prompts/challenge-my-flow.prompt.md).
* **Skal du lave et beslutningsoplæg til Anja?** Kør [`.github/prompts/02-research-to-decision.prompt.md`](./.github/prompts/02-research-to-decision.prompt.md).
* **Skal du overlevere et flow til udvikling?** Kør [`.github/prompts/03-jira-spec-generator.prompt.md`](./.github/prompts/03-jira-spec-generator.prompt.md) mod Jira-projekt `AMT`.
* **Klar til ugentlig refleksion?** Kør [`05-sparring-and-reflection/sparring-prompts/weekly-reflection.prompt.md`](./05-sparring-and-reflection/sparring-prompts/weekly-reflection.prompt.md).
