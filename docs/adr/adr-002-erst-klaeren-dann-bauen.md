[← ADR-Index](adr-index.md)

# ADR-002: Code entsteht erst, wenn die Fragen der Priorität 1 beantwortet sind und ADR-003 entschieden ist

**Status:** Entschieden · **Datum:** 2026-11-16

## Kontext

Vieles aus dem [Anforderungsdokument](../anforderungen/2026-11-16-anforderungsdokument.md)
gibt es in MyTCO, der App des Tennis-Club Olten, schon oder in ähnlicher Form: Login, Rollen,
Mitgliederverwaltung, Austritt, Mitteilungen per Push, Anmeldung zu Anlässen und Turnieren,
Partnersuche ([ADR-003](adr-003-verhaeltnis-zur-tco-app.md)). Ob und wie viel davon die
Badibeach-App übernimmt, hängt an Fragen an beide Vereine. Bei Badibeach sind das die
[Abklärungen](../abklaerungen.md) der Priorität 1.

## Optionen

| Option | Dafür | Dagegen |
|--------|-------|---------|
| A: sofort ein eigenes Code-Gerüst bauen | Früh etwas zu zeigen | Baut womöglich nach, was MyTCO schon kann; ein späterer Wechsel zu einem gemeinsamen Kern wird teurer |
| B: erst klären, dann bauen | Übernahme lässt sich ohne Umbau entscheiden; kein Code, der wieder weg muss | Bis zu den Antworten gibt es nichts zum Ausprobieren |

## Entscheidung

**Bis die Fragen der Priorität 1 beantwortet sind und [ADR-003](adr-003-verhaeltnis-zur-tco-app.md)
entschieden ist, entsteht kein Produktcode (B), Entscheid des Projektleiters.** Erlaubt
sind Doku, Fragen und ADRs, auch Klickentwürfe (Mockups) zum Abstimmen mit dem Vorstand.

## Konsequenzen

- Die Zeit bis zu den Antworten geht in Anforderungen, Fachbegriffe und die Vorbereitung des
  Entscheids zu ADR-003.
- Keine Dependencies, kein Build, keine CI in dieser Phase.

## Reevaluations-Trigger

- Alle Fragen der Priorität 1 sind beantwortet und ADR-003 ist entschieden. Dann wird diese ADR
  durch die erste Etappe abgelöst.
- K-01 verlangt etwas auf einen Termin, der ohne Start vor den Antworten nicht zu halten ist.
