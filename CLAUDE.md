# Badibeach-App — Projektkontext für Claude Code

> Worum es geht → `README.md`, alle Dokumente → `docs/index.md`.

## Code — Dauerregel

- Kein Produktcode, keine Dependencies, kein Build, solange
  `docs/adr/adr-002-erst-klaeren-dann-bauen.md` gilt. Erlaubt sind Doku, Fragen, ADRs und
  Klickentwürfe.

## Mitgliederdaten — Dauerverbote

- Nie echte Mitgliederdaten (Namen, Adressen, Geburtsdaten, Kontaktdaten) in Repo, Tests,
  Fixtures, Seed-Daten, Issues, Logs oder Screenshots. Testdaten zu Personen sind erfunden.
- Nie Exporte, Mitgliederlisten, Reservations- oder Helferpläne mit Namen ins Repo kopieren.
  Echte Vereinsunterlagen, auch Originaldokumente mit Metadaten, liegen nur im gitignorierten
  Ordner `intern/`.
- Personen aus dem Verein werden in Doku, Commits und Issues mit ihrer Rolle benannt
  (Co-Präsidium, Kommunikation, Events, Turniere, Projektleiter), nie mit Namen.

## Fragen an den Verein

- Fragen an den Verein stehen nur in `docs/abklaerungen.md` (Aufbau und Prioritäten dort).
  Wer ohne Antwort weiterarbeitet, markiert die Annahme mit `Annahme K-NN:`.

## Context-Scopes

Welche Pfade bei welcher Aufgabe zu laden sind → `docs/context-scopes.md`.
