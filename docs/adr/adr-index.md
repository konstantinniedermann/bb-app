[← Übersicht](../index.md)

# Architektur-Entscheidungen (ADRs)

Architecture Decision Records halten Entscheidungen mit Tragweite fest, also *warum* etwas so
gebaut wird und nicht nur *wie*. Jede ADR nennt die geprüften Optionen, die Entscheidung, die
Konsequenzen und einen **Reevaluations-Trigger**: wann die Entscheidung neu zu bewerten ist.
Vorlage: [`vorlage.md`](vorlage.md). Dateiname: `adr-NNN-kurztitel.md`.

Wo eine Entscheidung der tco-app (MyTCO) übernommen wird, verweist die ADR auf deren ADR, statt
die Begründung zu kopieren. Sie hält nur fest, was bei Badibeach anders ist.

| ADR | Titel | Status | Datum |
|-----|-------|--------|-------|
| [ADR-001](adr-001-repo-oeffentlich.md) | Das Repo ist öffentlich | Entschieden | 2026-11-16 |
| [ADR-002](adr-002-erst-klaeren-dann-bauen.md) | Code entsteht erst, wenn die Fragen der Priorität 1 beantwortet sind und ADR-003 entschieden ist | Entschieden | 2026-11-16 |
| [ADR-003](adr-003-verhaeltnis-zur-tco-app.md) | Verhältnis zur tco-app: Kopie, gemeinsamer Kern oder eine App für zwei Vereine | Vorgeschlagen | 2026-11-16 |
| [ADR-004](adr-004-technik-wie-tco-app.md) | Die Badibeach-App nutzt dieselbe Technik wie MyTCO | Vorgeschlagen | 2026-11-16 |
