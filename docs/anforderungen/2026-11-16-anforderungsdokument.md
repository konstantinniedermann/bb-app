[← Anforderungen](README.md)

# Anforderungsdokument «Badibeach-App» (Abschrift)

Wortgetreue Abschrift des Dokuments, das das Co-Präsidium am 16.11.2026 übergeben hat. Das
Original (Word-Datei) liegt nur lokal im gitignorierten Ordner `intern/`, weil seine
Metadaten Personennamen enthalten. Die Anforderungen mit IDs stehen in
[`anforderungen.md`](anforderungen.md); dort verweist die Spalte *Quelle* auf die Abschnitte
hier (z. B. `DOK 3`).

---

## 1. Ziel und Zweck der App

Ziel ist die Entwicklung einer zentralen Plattform für alle Vereinsmitglieder, welche die
Organisation des Spielbetriebs vereinfacht, die Kommunikation innerhalb des Vereins verbessert
und das Finden von Mitspielerinnen und Mitspielern erleichtert.

Die App soll sowohl für die Organisation durch den Vorstand als auch für die aktive Nutzung
durch die Mitglieder einen Mehrwert bieten.

Die App soll folgende Hauptbereiche umfassen:

- Interne Turnierorganisation
- Spielfeldverwaltung
- Spielerinnen- und Spielersuche
- Intranet und Vereinskommunikation

## 2. Turnierorganisation

Die App soll die Organisation und Anmeldung zu vereinsinternen Spielveranstaltungen
ermöglichen.

Gewünschte Funktionen:

- Interne Clubturniere
  - Ausschreibung und Veröffentlichung von Clubturnieren
  - Anmeldung und Abmeldung durch die Mitglieder
  - Übersicht der angemeldeten Spielerinnen und Spieler
  - Informationen zu Datum, Zeit, Spielmodus und Teilnahmebedingungen
  - Möglichkeit zur Begrenzung der Teilnehmerzahl
- Open Court
  - Veröffentlichung von Open-Court-Terminen
  - Anmeldung für interessierte Mitglieder
  - Übersicht über die angemeldeten Teilnehmenden
  - Anzeige der Mindestzahl der Teilnehmenden
  - Anzeige der verfügbaren Plätze

Noch zu klärende Anforderungen:

- Soll die Anmeldung einzeln oder als Team erfolgen?
- Soll eine Warteliste bei ausgebuchten Veranstaltungen möglich sein?
- Wer darf Turniere und Open-Court-Termine erstellen und verwalten?
- Sollen automatische Erinnerungen vor den Veranstaltungen verschickt werden?

## 3. Spielfeldverwaltung

Die App soll die Organisation und Verwaltung der Spielfeldreservationen vereinfachen und eine
optimale Auslastung der Spielfelder ermöglichen.

Gewünschte Funktionen:

- Feldreservationen
  - Übersicht über die verfügbaren Spielfelder und Reservationen
  - Möglichkeit, Reservationen zu erfassen und zu verwalten
  - Anzeige, welche Mitglieder ein Feld reserviert haben
  - Übersicht über die Belegung der Spielfelder an den jeweiligen Abenden
- Feldfreigabe
  - Möglichkeit, ein reserviertes Spielfeld freizugeben, wenn es nicht genutzt wird
  - Freigegebene Felder werden für andere Mitglieder sichtbar
  - Andere Mitglieder können ein freigegebenes Feld übernehmen bzw. nutzen
  - Anzeige der aktuell verfügbaren Spielfelder

Noch zu klärende Anforderungen:

- Wer darf Spielfelder reservieren?
- Können Mitglieder ihre Reservationen selbstständig bearbeiten oder löschen?
- Bis wann muss ein Feld freigegeben werden?
- Wie wird verhindert, dass ein Feld gleichzeitig von mehreren Gruppen genutzt wird?
- Soll eine Benachrichtigung erfolgen, wenn ein Feld freigegeben wird?

## 4. Spielerinnen- und Spielersuche

Die App soll das Finden von Mitspielerinnen und Mitspielern erleichtern. Mitglieder sollen
unkompliziert Spielpartner suchen, sich bestehenden Gruppen anschliessen oder kurzfristig
Unterstützung für einen Spieleinsatz finden können.

Gewünschte Funktionen:

### 4.1 Kurzeinsatz / Aushilfe suchen

- Möglichkeit, kurzfristig eine Aushilfe für einen Spielabend zu suchen
- Veröffentlichung einer Suchanfrage mit Datum und Uhrzeit
- Angabe des gewünschten Spielniveaus
- Möglichkeit für andere Mitglieder, sich als Aushilfe zu melden
- Spielerinne- und Spieler mit gesuchtem Niveau erhalten eine Nachricht

### 4.2 Spontanes Spielen / eigene Gruppe bilden

- Möglichkeit, spontan Mitspielerinnen und Mitspieler für einen Abend zu suchen
- Möglichkeit, eine eigene Spielgruppe zu erstellen
- Besonders hilfreich für neue Mitglieder, um Kontakte zu knüpfen und Spielpartner zu finden

### 4.3 Training oder Turnier

- Möglichkeit, Mitspielerinnen und Mitspieler für Trainings zu suchen
- Möglichkeit, Spielpartner für interne Turniere zu finden
- Angabe des gewünschten Spielniveaus und der jeweiligen Anforderungen

### 4.4 Spielerinnen- und Spielerprofil

Jedes Mitglied soll ein eigenes Profil erstellen bzw. verwalten können.

Mögliche Profilangaben:

- Name
- Spielniveau / Level
- Spielpräferenzen (optional)
- Verfügbarkeit (optional)
- Kontaktmöglichkeit

Wichtig: Level-Angabe

Das Spielniveau soll im persönlichen Profil hinterlegt werden können. Bei einer Suchanfrage,
beispielsweise für eine Aushilfe, soll das gewünschte Level angegeben werden können.

Dadurch können gezielt Spielerinnen und Spieler mit einem passenden Spielniveau gefunden
werden.

Noch zu klärende Anforderungen:

- Wie wird das Spielniveau definiert (z. B. Level 1–5)?
- Kann jedes Mitglied sein Level selbst festlegen oder wird es durch den Verein bestimmt?
- Sollen Suchanfragen für alle Mitglieder sichtbar sein?
- Wie erfolgt die Kontaktaufnahme zwischen den Mitgliedern (Chat, Direktnachricht oder
  Kontaktdaten)?
- Sollen Suchanfragen automatisch nach Ablauf des Spieltermins verschwinden?

## 5. Intranet und Vereinskommunikation

Die App soll als zentrale Kommunikationsplattform für den Verein dienen. Informationen sollen
einfach geteilt und für alle Mitglieder zugänglich gemacht werden können.

### 5.1 Austausch unter Mitgliedern

- Möglichkeit, Informationen und Neuigkeiten zu teilen
- Möglichkeit, Beiträge zu veröffentlichen
- Austausch und Diskussionen unter den Mitgliedern
- Möglichkeit, Fragen zu stellen und Informationen weiterzugeben
- Zentraler Ort für vereinsinterne Mitteilungen

### 5.2 Informationen und Kommunikation durch den Vorstand

- Veröffentlichung von wichtigen Vereinsinformationen
- Ankündigung von Veranstaltungen und Events
- Mitteilungen zu Trainings, Turnieren und weiteren Vereinsaktivitäten
- Veröffentlichung von Informationen zur Organisation des Vereins
- Möglichkeit, wichtige Mitteilungen besonders hervorzuheben
- Zentrale Übersicht über aktuelle und vergangene Informationen

Rollen und Berechtigungen:

- Alle Mitglieder können Informationen und Beiträge lesen.
- Alle Mitglieder können sich im Mitgliederbereich austauschen.
- Der Vorstand kann offizielle Mitteilungen und wichtige Vereinsinformationen veröffentlichen.
- Die Verwaltung der Inhalte und Berechtigungen soll durch definierte Rollen geregelt werden.

Noch zu klärende Anforderungen:

- Sollen alle Mitglieder Beiträge veröffentlichen können?
- Soll es separate Bereiche für Vorstand und Mitglieder geben?
- Soll eine Kommentarfunktion möglich sein?
- Sollen Mitglieder Push-Benachrichtigungen für neue Beiträge erhalten?
- Können wichtige Informationen dauerhaft angepinnt werden?

## 6. Benutzerrollen und Zugriffsrechte

Für die App sollen unterschiedliche Benutzerrollen und entsprechende Berechtigungen definiert
werden.

Mögliche Rollen:

- Mitglied: Zugriff auf die Vereinsinformationen, Turnieranmeldungen, Spielfeldverwaltung und
  Spielersuche.
- Vorstand: Zusätzliche Berechtigungen zur Veröffentlichung offizieller Informationen und zur
  Verwaltung von Vereinsaktivitäten.
- Administration: Verwaltung von Benutzerkonten, Profilen, Berechtigungen und grundlegenden
  App-Einstellungen.

## 7. Übergreifende Anforderungen

Zusätzlich zu den einzelnen Funktionsbereichen sollten folgende Aspekte bei der Entwicklung
berücksichtigt werden:

- Benutzerfreundliche und übersichtliche Gestaltung
- Nutzung auf Smartphones (iOS und Android)
- Individuelle Benutzerprofile
- Push-Benachrichtigungen bei relevanten Ereignissen
- Datenschutz und Schutz persönlicher Mitgliederdaten
- Einfache Verwaltung durch den Vorstand
- Möglichkeit, Mitglieder beim Vereinsaustritt aus der App zu entfernen
