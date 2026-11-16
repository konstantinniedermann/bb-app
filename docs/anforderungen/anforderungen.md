[← Anforderungen](README.md)

# Anforderungen mit IDs

Jede Anforderung aus dem [Anforderungsdokument](2026-11-16-anforderungsdokument.md) mit fester
ID, dazu wenige aus der Website des Vereins und Vorgaben des Projektleiters. ADRs, Fragen und
später Issues und Tests verweisen auf diese IDs. Offene Fragen stehen in den
[Abklärungen](../abklaerungen.md), die Begriffe im [Glossar](../glossar.md).

## Lesehilfe

**ID-Schema:** `A-<BEREICH>-NN` für funktionale, `N-<THEMA>-NN` für nicht-funktionale
Anforderungen. Eine ID bleibt fest, auch wenn sich die Anforderung ändert; eine gestrichene ID
wird nie neu vergeben. Neue Anforderungen bekommen die nächste freie Nummer im Bereich.

**Quelle:** `DOK 3` = Abschnitt im Anforderungsdokument · `Web` = badibeach.ch, Stand
16.11.2026 · `PL` = Vorgabe des Projektleiters · `K-NN` = Antwort des Vereins in den
[Abklärungen](../abklaerungen.md#beantwortet).

**Status:** `erfasst` (aus der Quelle übernommen, ohne offene Frage) · `offen` (wartet auf die
Antwort in Spalte *Hängt an*) · `zurückgestellt` (Detail, das die erste Entwicklung nicht
verändert; Vorschlag in den [Abklärungen](../abklaerungen.md#zurückgestellt)) · `geplant` ·
`umgesetzt` · `verworfen` (mit Begründung).

**Etappe:** Eine Spalte *Etappe* kommt dazu, sobald K-01 beantwortet ist und es eine Roadmap gibt.

## Funktionale Anforderungen

### TURNIER — Clubturniere

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-TURNIER-01 | Der Vorstand schreibt Clubturniere aus und veröffentlicht sie | DOK 2 | offen | K-14 |
| A-TURNIER-02 | Mitglieder melden sich zu einem Clubturnier an und ab | DOK 2 | offen | K-15 |
| A-TURNIER-03 | Übersicht der angemeldeten Spielerinnen und Spieler | DOK 2 | erfasst | |
| A-TURNIER-04 | Angaben zu Datum, Zeit, Spielmodus und Teilnahmebedingungen | DOK 2 | erfasst | |
| A-TURNIER-05 | Die Teilnehmerzahl lässt sich begrenzen | DOK 2 | offen | K-15 |
| A-TURNIER-06 | Automatische Erinnerung vor einer Veranstaltung (Turnier und Open Court) | DOK 2 | zurückgestellt | |

### OPENCOURT — Open Court

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-OPENCOURT-01 | Open-Court-Termine werden veröffentlicht | DOK 2 | offen | K-14, K-16 |
| A-OPENCOURT-02 | Interessierte Mitglieder melden sich an | DOK 2 | offen | K-16 |
| A-OPENCOURT-03 | Übersicht über die angemeldeten Teilnehmenden | DOK 2 | erfasst | |
| A-OPENCOURT-04 | Anzeige der Mindestzahl der Teilnehmenden | DOK 2 | offen | K-16 |
| A-OPENCOURT-05 | Anzeige der verfügbaren Plätze | DOK 2 | erfasst | |

### FELD — Feldreservation und Feldfreigabe

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-FELD-01 | Übersicht über die verfügbaren Spielfelder und Reservationen | DOK 3 | offen | K-03 |
| A-FELD-02 | Reservationen erfassen und verwalten | DOK 3 | offen | K-02, K-14 |
| A-FELD-03 | Anzeige, welche Mitglieder ein Feld reserviert haben | DOK 3 | erfasst | |
| A-FELD-04 | Übersicht über die Belegung der Felder an den jeweiligen Abenden | DOK 3 | offen | K-03 |
| A-FELD-05 | Ein reserviertes Feld lässt sich freigeben, wenn es nicht genutzt wird | DOK 3 | offen | K-17 |
| A-FELD-06 | Freigegebene Felder sind für andere Mitglieder sichtbar | DOK 3 | erfasst | |
| A-FELD-07 | Andere Mitglieder übernehmen ein freigegebenes Feld | DOK 3 | offen | K-17 |
| A-FELD-08 | Anzeige der aktuell verfügbaren Felder | DOK 3 | offen | K-03 |
| A-FELD-09 | Pro reservierendem Spieler ist ein Helfereinsatz zu leisten; heute im Helfer:inneneinsatzplan | Web | offen | K-04 |
| A-FELD-10 | Turniere und Vereinsaktivitäten belegen Felder ganz oder teilweise | Web | offen | K-03 |

### SUCHE — Spielerinnen- und Spielersuche

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-SUCHE-01 | Kurzfristig eine Aushilfe für einen Spielabend suchen: Suchanfrage mit Datum und Uhrzeit | DOK 4.1 | erfasst | |
| A-SUCHE-02 | In der Suchanfrage das gewünschte Spielniveau angeben | DOK 4.1, 4.3 | offen | K-18 |
| A-SUCHE-03 | Andere Mitglieder melden sich als Aushilfe | DOK 4.1 | offen | K-13 |
| A-SUCHE-04 | Mitglieder mit dem gesuchten Niveau erhalten eine Nachricht | DOK 4.1 | offen | K-18 |
| A-SUCHE-05 | Spontan Mitspielende für einen Abend suchen | DOK 4.2 | erfasst | |
| A-SUCHE-06 | Eine eigene Spielgruppe erstellen; anderen Gruppen beitreten | DOK 4, 4.2 | erfasst | |
| A-SUCHE-07 | Mitspielende für Trainings suchen | DOK 4.3 | erfasst | |
| A-SUCHE-08 | Spielpartner für interne Turniere finden | DOK 4.3 | offen | K-15 |
| A-SUCHE-09 | In der Suche die jeweiligen Anforderungen angeben (über das Niveau hinaus) | DOK 4.3 | erfasst | |

### PROFIL — Spielerinnen- und Spielerprofil

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-PROFIL-01 | Jedes Mitglied erstellt und verwaltet sein eigenes Profil | DOK 4.4, 7 | erfasst | |
| A-PROFIL-02 | Profilangabe Name | DOK 4.4 | erfasst | |
| A-PROFIL-03 | Profilangabe Spielniveau / Level | DOK 4.4 | offen | K-18 |
| A-PROFIL-04 | Profilangabe Spielpräferenzen (freiwillig) | DOK 4.4 | erfasst | |
| A-PROFIL-05 | Profilangabe Verfügbarkeit (freiwillig) | DOK 4.4 | erfasst | |
| A-PROFIL-06 | Profilangabe Kontaktmöglichkeit | DOK 4.4 | offen | K-13 |

### AUSTAUSCH — Austausch unter Mitgliedern

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-AUSTAUSCH-01 | Mitglieder teilen Informationen und Neuigkeiten und veröffentlichen Beiträge | DOK 5.1 | offen | K-12 |
| A-AUSTAUSCH-02 | Austausch und Diskussionen unter den Mitgliedern | DOK 5.1, 5.2 | offen | K-12 |
| A-AUSTAUSCH-03 | Fragen stellen und Informationen weitergeben | DOK 5.1 | offen | K-12 |
| A-AUSTAUSCH-04 | Zentraler Ort für vereinsinterne Mitteilungen | DOK 1, 5.1 | erfasst | |

### INFO — Informationen des Vorstands

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-INFO-01 | Der Vorstand veröffentlicht wichtige Vereinsinformationen | DOK 5.2 | erfasst | |
| A-INFO-02 | Ankündigung von Veranstaltungen und Events | DOK 5.2 | erfasst | |
| A-INFO-03 | Mitteilungen zu Trainings, Turnieren und weiteren Vereinsaktivitäten | DOK 5.2 | erfasst | |
| A-INFO-04 | Informationen zur Organisation des Vereins | DOK 5.2 | erfasst | |
| A-INFO-05 | Wichtige Mitteilungen besonders hervorheben | DOK 5.2 | erfasst | |
| A-INFO-06 | Zentrale Übersicht über aktuelle und vergangene Informationen | DOK 5.2 | erfasst | |

### ROLLE — Benutzerrollen

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-ROLLE-01 | Rolle *Mitglied*: liest Informationen und Beiträge, tauscht sich aus, meldet sich zu Turnieren an, nutzt Feldreservation und Spielersuche | DOK 5.2, 6 | offen | K-05 |
| A-ROLLE-02 | Rolle *Vorstand*: veröffentlicht offizielle Mitteilungen, verwaltet Vereinsaktivitäten | DOK 5.2, 6 | offen | K-14 |
| A-ROLLE-03 | Rolle *Administration*: Benutzerkonten, Profile, Berechtigungen, grundlegende Einstellungen | DOK 6 | offen | K-14 |
| A-ROLLE-04 | Inhalte und Berechtigungen werden über definierte Rollen verwaltet | DOK 5.2 | erfasst | |

### MITGLIED — Mitglieder und Zugang

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| A-MITGLIED-01 | Jedes Mitglied hat einen eigenen, persönlichen Zugang zur App | DOK 7, PL | offen | K-06, K-07 |
| A-MITGLIED-02 | Der Vorstand verwaltet die Mitglieder der App einfach (Konten anlegen und pflegen) | DOK 7 | offen | K-05 |
| A-MITGLIED-03 | Mitglieder werden beim Vereinsaustritt aus der App entfernt | DOK 7 | offen | K-05 |

## Nicht-funktionale Anforderungen

| ID | Anforderung | Quelle | Status | Hängt an |
|----|-------------|--------|--------|----------|
| N-BEDIENUNG-01 | Benutzerfreundliche und übersichtliche Gestaltung | DOK 7 | erfasst | |
| N-APP-01 | Nutzung auf Smartphones mit iOS und Android | DOK 7 | offen | K-08 |
| N-APP-02 | Push-Benachrichtigungen bei relevanten Ereignissen | DOK 7 | erfasst | |
| N-DATENSCHUTZ-01 | Datenschutz und Schutz persönlicher Mitgliederdaten | DOK 7 | offen | K-07, K-19 |
| N-VERWALTUNG-01 | Einfache Verwaltung durch den Vorstand | DOK 7 | erfasst | |
| N-KOSTEN-01 | Laufende Kosten im Rahmen, den der Verein festlegt | PL | offen | K-09 |
| N-BETRIEB-01 | Entwicklung und Betrieb ehrenamtlich; die App lässt sich an eine Nachfolge übergeben | PL | erfasst | |
