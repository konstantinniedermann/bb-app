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
- Das Repo ist öffentlich: vor jedem Push `git grep` nach Namen aus `intern/` und aus dem
  Gespräch.

## Fragen an den Verein

- Neue Fragen kommen nach `docs/abklaerungen.md` (ID `K-NN`, Priorität, Adressat als Rolle).
  Eine Frage gehört nur in Priorität 1 oder 2, wenn ihre Antwort Datenmodell, Login, Hosting,
  Kosten oder den Umfang einer Etappe verändert; sonst unter *Zurückgestellt* mit Vorschlag.
- Wer ohne Antwort weiterarbeitet, markiert die Annahme mit `Annahme K-NN:`.

## Context-Scopes

Welche Pfade bei welcher Aufgabe zu laden sind → `docs/context-scopes.md`.
