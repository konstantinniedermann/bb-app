[← Übersicht](index.md)

# Beobachtungen

Posteingang für Befunde, die **kein eigener Vorgang** sind: Dinge, die beim Arbeiten an etwas
anderem auffallen, aber weder in den laufenden Scope gehören noch ein GitHub-Issue rechtfertigen.
Ausgewertet wird gemeinsam über den Skill `beobachtungen-auswerten`.

Form eines Eintrags:

```markdown
### JJJJ-MM-TT — Titel, der den Befund in einem Satz sagt

**Thema:** Kurzes Stichwort (bestehende wiederverwenden)

**Fundort:** Datei, Seite — worauf sich der Befund bezieht.

**Beobachtung:** Was auffiel.

**Ursprung:** Woraus der Befund fiel (Issue, Session).

**Einschätzung:** Erste Bewertung — ausdrücklich vorläufig.
```

## Offen

### 2026-11-16 — Die Vorstandsseite auf badibeach.ch zeigt noch die alte Besetzung

**Thema:** Website

**Fundort:** badibeach.ch/vorstand

**Beobachtung:** Die Seite führt das Ressort Kommunikation mit der früheren Besetzung, das neue
Ressort Events fehlt.

**Ursprung:** Initialisierung des Repos.

**Einschätzung:** Kein Thema der App. Hinweis an die Kommunikation, wenn sie die Tabelle der
Fragen bekommt.

### 2026-11-16 — Bei der tco-app fehlt eine Frage wie K-11 an den TCO-Vorstand

**Thema:** Übernahme aus MyTCO

**Fundort:** tco-app `docs/abklaerungen.md`; hier [ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md)

**Beobachtung:** ADR-003 Option C (eine App für zwei Vereine) braucht auch die Zustimmung des
TCO-Vorstands. In den Abklärungen der tco-app gibt es dazu noch keine Frage.

**Ursprung:** Initialisierung des Repos.

**Einschätzung:** In einer Session der tco-app als neue Frage aufnehmen, wenn Option C nach den
Antworten von Badibeach noch im Rennen ist.
