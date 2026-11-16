[← ADR-Index](adr-index.md)

# ADR-004: Die Badibeach-App nutzt dieselbe Technik wie MyTCO

**Status:** Vorgeschlagen · **Datum:** 2026-11-16

## Kontext

Die Anforderungen gleichen denen von MyTCO: Nutzung auf iOS und Android (N-APP-01), Push
(N-APP-02), Verwaltung durch den Vorstand (N-VERWALTUNG-01), kleines Budget (N-KOSTEN-01),
ehrenamtlicher Betrieb mit Übergabe (N-BETRIEB-01). Für MyTCO sind die Technik-Fragen mit
Begründung entschieden. Jede Option aus [ADR-003](adr-003-verhaeltnis-zur-tco-app.md) ausser D
setzt dieselbe Technik voraus.

## Optionen

| Option | Dafür | Dagegen |
|--------|-------|---------|
| A: Technik von MyTCO übernehmen | Begründung und Erfahrung liegen vor; Voraussetzung für Kopie, Kern oder gemeinsame App; ein Projektleiter, ein Stack | Was bei MyTCO auf den TCO zugeschnitten ist, passt nicht automatisch (Brief, Hosting) |
| B: eigene Technik wählen | Freie Wahl | Schliesst die Übernahme aus MyTCO praktisch aus; zwei Stacks für einen ehrenamtlichen Projektleiter |

## Entscheidung (vorgeschlagen)

**Die Badibeach-App übernimmt die Technik-Entscheide von MyTCO (A), soweit nicht unten anders
vermerkt.** Entschieden wird zusammen mit ADR-003.

| Thema | Übernommen aus MyTCO | Was bei Badibeach anders ist |
|-------|---------------------|------------------------------|
| App-Form | Installierbare Web-App mit Web Push, Store-App über Capacitor bei Bedarf ([ADR-001 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-001-web-app-zuerst.md)) | Hängt an K-08 |
| Sprache, Framework, Datenbank | TypeScript, SvelteKit, PostgreSQL, Drizzle ([ADR-002 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-002-sveltekit-postgresql.md)) | — |
| Login | Einmal-Code ohne Passwort, Sitzung in einer Tabelle ([ADR-004 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-004-login-einmal-code.md)), freiwilliger Passkey ([ADR-005 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-005-passkey-simplewebauthn.md)) | Start per E-Mail statt per Brief, falls K-06 das bestätigt |
| Hosting | MyTCO: eigener Server in der Schweiz bei Infomaniak ([ADR-003 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-003-hosting-infomaniak-vps.md)) | Nicht übernommen. Eigener oder gemeinsamer Server hängt an ADR-003 (dieses Repo), K-09 und K-11 |
| Mailversand | MyTCO: Postfach des Vereins oder Scaleway (EU) | Der Verein nutzt Google Workspace; Versand darüber hängt an K-10.2 |
| Mitgliederliste | MyTCO führt eine eigene Liste ([ADR-006 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-006-eigenstaendig-ohne-fairgate.md)) | Woher die Liste kommt, hängt an K-05 |

## Konsequenzen

- Bei Entscheid gelten die Bauregeln der tco-app auch hier. Sie kommen mit dem ersten Code in
  die `CLAUDE.md` dieses Repos.
- Kosten bei eigenem Server wie MyTCO, ca. CHF 95–175 pro Jahr (Schätzung der tco-app); bei
  gemeinsamem Server (ADR-003 C) geteilt.

## Reevaluations-Trigger

- K-08 verlangt eine Store-App von Anfang an.
- ADR-003 wird mit Option D entschieden.
