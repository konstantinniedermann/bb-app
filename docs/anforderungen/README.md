[← Übersicht](../index.md)

# Anforderungen

## Quellen

| Datum | Quelle | Datei |
|-------|--------|-------|
| 16.11.2026 | Anforderungsdokument «Badibeach-App» vom Co-Präsidium | Abschrift: [`2026-11-16-anforderungsdokument.md`](2026-11-16-anforderungsdokument.md); Original nur lokal in `intern/` (Metadaten mit Personennamen) |
| 16.11.2026 | Website badibeach.ch: Feldreservation, Helfer:inneneinsatzplan, Vereinsregeln, Mitgliedschaft, Saisonplan | Auszug unten |

Jede Anforderung steht mit fester ID in [`anforderungen.md`](anforderungen.md); darauf
verweisen ADRs, Fragen und später Issues und Tests.

## Heutiger Ablauf laut Website (Stand 16.11.2026)

Belegt von badibeach.ch, soweit nicht anders markiert (**V** = Vermutung).

- **Verein:** Badi.Beach Volleyball Verein Olten, seit 1997, laut Website über 150 Mitglieder.
  Gespielt wird auf den Beachfeldern im Stadtbad Olten.
- **Saison:** Saisoneröffnung im Frühling (2026: 09.05.) bis zur Generalversammlung im Herbst
  (2026: 06.11.), im Winter Pause.
- **Feldreservation:** Antrag über ein Google-Formular mit drei unterschiedlichen
  Wunschzeiten. Zugeteilt wird nach «first in, first served», für alle Mitglieder inklusive
  Vorstand. Reserviert werden kann Montag bis Freitag zwischen 17:00 und 21:30. Das blaue Feld
  ist für Badigäste offen und erst ab 20:30 reservierbar. Der Plan erscheint als PDF, wenn das
  Reservationsfenster geschlossen ist. Die Reservation gilt die ganze Saison (**V**: als fester
  wöchentlicher Termin; K-03). Wie viele Felder es gibt, nennt die Website nicht.
- **Helfereinsätze:** Für jedes reservierte Feld leistet jeder gemeldete Spieler einen
  Helfereinsatz, pro Feld mindestens vier. Der Einsatzplan erscheint ebenfalls als PDF.
- **Regeln vor Ort:** Jede Spielgemeinschaft bestimmt einen *Chief Field Officer* (CFO). Auf
  nicht reservierten Feldern gilt die 20-Minuten-Regel. Um 21:30 ist Nachtruhe.
- **Mitgliedschaft:** Antrag über ein Formular auf der Website (Name, Geburtsdatum, Geschlecht,
  E-Mail, Telefon freiwillig, Adresse, Art der Mitgliedschaft). Arten: Aktiv, Aktiv für
  Jugendliche bis 20, Studierende und Lernende, Passiv. Wo die Mitgliederliste geführt wird,
  nennt die Website nicht (K-05).
- **Technik:** Die Website läuft mit WordPress bei Hostpoint, E-Mail über Google Workspace
  (öffentliche DNS-Einträge). Kontaktadresse des Vereins: badi.beach@badibeach.ch.

## Änderungsprotokoll

| Datum | Änderung | Quelle |
|-------|----------|--------|
| 16.11.2026 | Anforderungen mit IDs aus dem Anforderungsdokument erfasst; dazu aus der Website die Helfereinsätze (A-FELD-09) und die Belegung der Felder durch Anlässe (A-FELD-10), vom Projektleiter Kosten (N-KOSTEN-01), Betrieb (N-BETRIEB-01) und der persönliche Zugang (A-MITGLIED-01). Die offenen Fragen des Dokuments sind Fragen in den [Abklärungen](../abklaerungen.md) oder dort zurückgestellt | Projektleiter |
