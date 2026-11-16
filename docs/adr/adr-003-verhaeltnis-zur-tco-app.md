[← ADR-Index](adr-index.md)

# ADR-003: Verhältnis zur tco-app: Kopie, gemeinsamer Kern oder eine App für zwei Vereine

**Status:** Offen · **Datum:** 2026-11-16

## Kontext

Der Projektleiter baut mit MyTCO ([tco-app](https://github.com/konstantinniedermann/tco-app))
schon eine Mitglieder-App für den Tennis-Club Olten. Beide Apps sind ehrenamtlich, für Vereine
mit 150 bis einigen hundert Mitgliedern, mobil zuerst, mit kleinem Budget (N-BETRIEB-01, N-KOSTEN-01).
Wer beide Apps pflegt, will Login, Sicherheit und Datenschutz nicht zweimal bauen und zweimal
nachführen.

**Legende:** **B** = belegt (README, ADRs und Anforderungen der tco-app, Stand 16.11.2026) ·
**S** = Schätzung · **V** = Vermutung, am Code der tco-app zu prüfen.

MyTCO ist noch nicht live: Die Funktionen sind gebaut und lokal nachgewiesen, die Testgruppe
und der Server folgen. Betriebserfahrung gibt es noch keine.

### Was in MyTCO gebaut ist und was Badibeach braucht

| Badibeach braucht | In MyTCO | Passt? |
|-------------------|----------|--------|
| Persönlicher Zugang (A-MITGLIED-01) | Login per Einmal-Code, Start per Brief, danach Code per E-Mail; freiwilliger Passkey (B) | Weitgehend. Ohne Brief, falls K-06 alle E-Mail-Adressen bestätigt (V) |
| Mitglieder verwalten, Austritt (A-MITGLIED-02, -03) | Mitgliederverwaltung, Einlesen per CSV, Austritt, Löschen mit Bedenkzeit, Auskunft, Löschfristen (B) | Weitgehend; hängt an K-05 (V) |
| Rollen Mitglied, Vorstand, Administration (A-ROLLE-01 bis -04) | Rollen mit Rechteprüfung im Server, *Ansicht als …* (B) | Prinzip ja, Rollen anders (K-14) |
| Profil (A-PROFIL-01 bis -06) | Eigene Angaben ändern, Rufname (B) | Teilweise. Level, Präferenzen und Verfügbarkeit sind neu |
| Informationen des Vorstands, Push (A-INFO-01 bis -06, N-APP-02) | Mitteilungen per Push und E-Mail an den Verein und zu Anlässen (B) | Weitgehend. Übersicht vergangener Mitteilungen und Hervorheben prüfen (V) |
| Open Court, Anmeldung mit Plätzen (A-OPENCOURT-01 bis -05) | Anlässe mit An- und Abmeldung, Kalenderdatei (B; dort selbst noch ein Vorschlag an den TCO-Vorstand) | Teilweise. Begrenzung und Mindestzahl neu (V) |
| Clubturniere (A-TURNIER-01 bis -06) | Clubmeisterschaft mit Kategorien, Einzel und Doppel mit Partner-Anfrage, Wildcard (B) | Teilweise. Die CM ist auf Tennis und Swiss Tennis zugeschnitten; ein einfaches Clubturnier ist kleiner (V) |
| Spielpartner für Turniere (A-SUCHE-08) | Auswahl eines bekannten Doppelpartners per Namenssuche in der CM (B) | Nein. Jemand Unbekannten mit passendem Niveau finden ist neu |
| Feldreservation und -freigabe (A-FELD-01 bis -10) | — | Neu |
| Aushilfe, spontanes Spielen, Gruppen (A-SUCHE-01 bis -07, -09) | — | Neu |
| Kontakt unter Mitgliedern (A-SUCHE-03, A-PROFIL-06) | Gespräch mit der Turnierleitung: Nachrichten in der App mit Antwort (B) | Ansatz für Nachrichten in der App, falls K-13 sie verlangt (V) |
| Austausch unter Mitgliedern (A-AUSTAUSCH-01 bis -04) | — | Neu |
| Helfereinsätze (A-FELD-09) | — | Neu, falls K-04 sie in die App holt |

Etwa die Hälfte der Grundlagen gäbe es schon (S). Die Kernfunktionen von Badibeach sind aber neu:
Felder, Spielersuche und Austausch.

## Optionen

| Option | Dafür | Dagegen |
|--------|-------|---------|
| A: **Kopie.** Das Gerüst von MyTCO kopieren (Login, Rollen, Mitglieder, Mitteilungen, Bauregeln, CI), danach getrennt weiterentwickeln | Schnellster Start; volle Freiheit für Badibeach; kein Verein hängt vom anderen ab | Sicherheits- und Datenschutz-Korrekturen zweimal; die Apps laufen mit der Zeit auseinander |
| B: **Gemeinsamer Kern.** Die gemeinsamen Teile (Login, Sitzung, Rollen, Mitglieder, Push, Mitteilungen) als eigener Baustein, den beide Apps nutzen; jeder Verein hat seine App und seinen Server | Pflege der Grundlagen einmal; jede App bleibt eigenständig | Der Schnitt kostet Aufwand in der laufenden tco-app; Änderungen am Kern müssen beiden passen; mehr Abstimmung |
| C: **Eine App für zwei Vereine.** Ein Code und ein Server, Daten pro Verein getrennt; jeder Verein sieht nur seine Bereiche | Ein Betrieb, eine Sicherung, Kosten teilbar | Die Trennung der Vereinsdaten ist sicherheitskritisch; beide Vorstände müssen zustimmen (K-11 hier, Gegenstück bei TCO); Verträge zur Auftragsbearbeitung und Übergabe an eine Nachfolge werden schwieriger |
| D: **Neu bauen.** Nur Erfahrungen und Bauregeln übernehmen | Passt genau zu Badibeach | Teuerste Option; baut Login und Datenschutz noch einmal |

## Entscheidung

**Offen.** Entschieden wird, wenn die Fragen der Priorität 1 beantwortet sind; die Tabelle
zeigt, welche davon die Wahl am stärksten verschieben. Bleibt Option C im Rennen, braucht es
zusätzlich die Zustimmung des TCO-Vorstands; die Frage dazu fehlt in der tco-app noch
([Beobachtungen](../beobachtungen.md)). Vorher entsteht kein Code
([ADR-002](adr-002-erst-klaeren-dann-bauen.md)).

Was die Wahl entscheidet:

| Frage | Was sie verschiebt |
|-------|--------------------|
| K-01 (erste Etappe, Termin) | Ein naher Termin spricht für A |
| K-05, K-06, K-07 (Mitgliederliste, E-Mail, Minderjährige) | Je ähnlicher dem Ablauf von MyTCO, desto mehr trägt B oder C |
| K-08, K-09, K-10 (Store, Budget, Domain und Mail) | Ein knappes Budget spricht für C, eine Store-App betrifft beide gleich |
| K-11 (Zustimmung zu geteiltem Code oder Server) | Ein Nein schliesst C aus |
| Bei TCO: Budget und Hosting ([Abklärungen der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/abklaerungen.md), dort K-03, K-09, K-10) und die Zustimmung des TCO-Vorstands zu C | Ein Nein des TCO schliesst C aus; ein geklärtes Hosting bei TCO macht C günstiger |

## Konsequenzen

Folgen erst mit der Entscheidung. Schon jetzt gilt: Die Anforderungen der Badibeach-App stehen
unabhängig von MyTCO, damit jede Option offen bleibt.

## Reevaluations-Trigger

- Die Fragen der Priorität 1 sind beantwortet, und, falls C im Rennen ist, auch die Zustimmung
  des TCO-Vorstands. Dann wird diese ADR entschieden.
