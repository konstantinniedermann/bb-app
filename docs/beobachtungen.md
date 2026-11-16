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

### 2026-11-16 — Bei der tco-app fehlt eine Frage wie K-11 an den TCO-Vorstand

**Thema:** Übernahme aus MyTCO

**Fundort:** tco-app `docs/abklaerungen.md`; hier [ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md)

**Beobachtung:** ADR-003 Option C (eine App für zwei Vereine) braucht auch die Zustimmung des
TCO-Vorstands. In den Abklärungen der tco-app gibt es dazu noch keine Frage.

**Ursprung:** Initialisierung des Repos.

**Einschätzung:** In einer Session der tco-app als neue Frage aufnehmen, wenn Option C nach den
Antworten von Badibeach noch im Rennen ist.

### 2026-11-16 — Die Namensprüfung vor dem Push steht in ADR-001, aber nirgends als Regel oder Hook

**Thema:** Öffentliches Repo

**Fundort:** [ADR-001](adr/adr-001-repo-oeffentlich.md), Konsequenzen; `CLAUDE.md`

**Beobachtung:** ADR-001 sagt, vor jedem Push werde nach Personennamen gesucht. Die Zeile in der
`CLAUDE.md` wurde nach der Aufnahmeregel entfernt (Ablauf, keine Dauerregel). Ein Pre-Push-Hook
oder ein Schritt im Wrap-up fehlt.

**Ursprung:** Review der Initialisierung.

**Einschätzung:** Ein kleiner Pre-Push-Hook mit einer Namensliste aus `intern/` wäre der robuste
Weg; bis dahin hängt es an der Disziplin beim Push.
