[← ADR-Index](adr-index.md)

# ADR-001: Das Repo ist öffentlich

**Status:** Entschieden · **Datum:** 2026-11-16

## Kontext

Das Repo liegt auf GitHub im Konto des Projektleiters. Es enthält vorerst nur Doku:
Anforderungen, Fragen an den Verein, ADRs. Später kommt der Code dazu. Die tco-app hat dieselbe
Frage schon entschieden ([ADR-010 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-010-repo-oeffentlich.md)).

## Optionen

| Option | Dafür | Dagegen |
|--------|-------|---------|
| A: privat | Fragen und Abläufe des Vereins bleiben unsichtbar | Bei späterem Code: weniger kostenlose CI-Minuten, kein Schutz von `main` im Gratisplan; Wechsel später nötig, wenn Code von MyTCO geteilt wird |
| B: öffentlich | Gleich wie MyTCO; CI kostenlos und ohne Kontingent; teilbar mit der tco-app ohne Freigaben | Anforderungen, Fragen und später Issues sind für alle sichtbar |

## Entscheidung

**Das Repo ist öffentlich (B), Entscheid des Projektleiters.** Vertretbar, weil die
Dauerverbote der `CLAUDE.md` echte Mitgliederdaten und Personennamen aus dem Repo fernhalten.

## Konsequenzen

- Das Original des Anforderungsdokuments liegt nur im gitignorierten Ordner `intern/`, weil
  seine Metadaten Personennamen enthalten. Ins Repo kommt eine Abschrift.
- Personen aus dem Verein stehen nur mit ihrer Rolle in Doku, Commits und Issues.
- Vor jedem Push wird nach Personennamen gesucht (`git grep`).

## Reevaluations-Trigger

- Der Verein wünscht, dass Anforderungen oder Fragen nicht öffentlich sind.
- Ins Repo müsste etwas Vertrauliches, das sich nicht nach `intern/` auslagern lässt.
