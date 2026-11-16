[← Übersicht](index.md)

# Abklärungen beim Verein

Fragen an den Vorstand, deren Antwort die **erste Entwicklung** verändert: Datenmodell, Login,
Hosting, Kosten, Umfang der ersten Etappe, Übernahme aus MyTCO. Detailfragen, die sich beim Bau
eines Bereichs klären lassen, stehen unter [Zurückgestellt](#zurückgestellt).
Ansprechpersonen sind das **Co-Präsidium** und die **Kommunikation**. Für Anlässe ist das Ressort
**Events** zuständig, für Turniere das Ressort **Turniere**. Fragen haben eine feste ID (`K-NN`),
auf die Anforderungen und ADRs verweisen. Personen werden mit ihrer Rolle benannt, nicht mit
Namen.

**So wird die Liste gepflegt:**

- Beantwortete Fragen wandern mit Datum und Antwort nach [Beantwortet](#beantwortet). Was sich
  an den Anforderungen ändert, kommt ins
  [Änderungsprotokoll](anforderungen/README.md#änderungsprotokoll).
- Wer ohne Antwort weiterarbeitet, markiert die Annahme dort, wo sie wirkt:
  `Annahme K-NN: <was angenommen ist>`.
- Zusammengesetzte Fragen haben Unterfragen (`K-03.2`). Die ID der ganzen Frage bleibt gültig.
- **Priorität 1:** gebraucht für den Entscheid über die Übernahme aus MyTCO
  ([ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md)) und den Umfang der ersten Etappe. Erst
  danach entsteht Code ([ADR-002](adr/adr-002-erst-klaeren-dann-bauen.md)).
  **Priorität 2:** gebraucht, bevor der betroffene Bereich gebaut wird.

**Einsammeln:** wie bei MyTCO über eine Google-Tabelle im Drive des Projektleiters, ein Blatt pro
Adressat, mit Auswahlliste und Freitext. Immer wählbar sind auch «Noch offen» und «Weiss ich
nicht – bitte jemand anderen fragen». Diese Seite bleibt die Hauptliste. Welche Person im
Verein welche Aufgabe hat, steht nur in der Tabelle, nicht im Repo.

## Priorität 1 — vor dem Entscheid über Übernahme und erste Etappe

| ID | Frage | An wen | Wozu |
|----|-------|--------|------|
| K-01 | Was soll die App als Erstes können, und ab wann? (K-01.1) Welcher der vier Bereiche macht heute am meisten Mühe: Turniere und Open Court, Feldreservation, Spielersuche oder Kommunikation? (K-01.2) Muss etwas zur Saisoneröffnung 2027 bereit sein? | Co-Präsidium | Erste Etappe und Roadmap; [ADR-002](adr/adr-002-erst-klaeren-dann-bauen.md) |
| K-02 | Feldreservation heute: Antrag per Google-Formular mit drei Wunschzeiten, Zuteilung «first in, first served», Plan als PDF. (K-02.1) Soll die App diesen Ablauf **ersetzen**, also Antrag und Zuteilung in der App? Oder bleibt die Zuteilung beim Formular, und die App zeigt nur den Plan und erlaubt Freigabe und Übernahme? (K-02.2) Wer teilt die Felder heute zu, und mit welchem Werkzeug (Google-Tabelle)? | Co-Präsidium, zuständige Person Feldreservation | A-FELD-02; Umfang des grössten neuen Bereichs |
| K-03 | Wie sieht eine Reservation aus? (K-03.1) Gilt sie für einen festen Wochentag und eine feste Zeit die ganze Saison, oder für einzelne Abende? (K-03.2) Wie viele Felder gibt es, und in welchen Zeitfenstern wird reserviert (Website: Mo–Fr 17:00–21:30, blaues Feld ab 20:30)? (K-03.3) Wie werden Felder an Turnier- und Anlasstagen gesperrt? Ein kurzer Blick auf den Plan 2026 (gerne mit geschwärzten Namen) würde die Fragen weitgehend beantworten. | Zuständige Person Feldreservation | A-FELD-01, -04, -08, -10; Datenmodell der Reservation |
| K-04 | Helfereinsätze: Heute leistet jeder reservierende Spieler einen Einsatz, der Plan kommt als PDF. Im Anforderungsdokument fehlen sie. (K-04.1) Soll die App auch die Helfereinsätze führen (Einsätze ausschreiben, sich eintragen, Pflicht erfüllt ja/nein)? (K-04.2) Was ist ein Einsatz (Art, Dauer, bei welchen Anlässen)? (K-04.3) Muss die App bei einer Übernahme eines freigegebenen Feldes auch einen Einsatz verlangen? | Co-Präsidium, Events | A-FELD-09; Umfang und Datenmodell |
| K-05 | Mitgliederliste: (K-05.1) Wo führt der Verein heute die Mitglieder (Excel, Google-Tabelle, Programm, Formular auf der Website), und wer pflegt sie? (K-05.2) Lässt sie sich als Datei ausgeben? Gefragt ist nur, ob es geht. Eine echte Liste kommt nicht ins Repo. (K-05.3) Bekommen auch Passivmitglieder einen Zugang, und was dürfen sie (z. B. lesen, aber keine Felder reservieren)? | Co-Präsidium | A-MITGLIED-02, -03, A-ROLLE-01; ob die App ihre eigene Liste führt, wie bei MyTCO ([ADR-006 der tco-app](https://github.com/konstantinniedermann/tco-app/blob/main/docs/adr/adr-006-eigenstaendig-ohne-fairgate.md)) |
| K-06 | Kennt der Verein von allen Mitgliedern eine E-Mail-Adresse, die sie auch lesen? Dann genügt ein Login mit Code per E-Mail, ohne Passwort und ohne Brief. MyTCO braucht für den Start einen Brief per Post. | Co-Präsidium | A-MITGLIED-01; Login; wie viel aus MyTCO passt ([ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md)) |
| K-07 | Gibt es Mitglieder unter 18 Jahren (die Jugend-Mitgliedschaft gilt bis 20), und ab welchem Alter? Bekommen sie ein eigenes Konto? | Co-Präsidium | A-MITGLIED-01, N-DATENSCHUTZ-01; Einwilligung, Sichtbarkeit von Profilen |
| K-08 | Erwartet der Verein, dass die App im App Store und bei Google Play steht? Oder genügt eine Web-App, die man vom Browser auf den Startbildschirm legt? Mit ihr gehen auch Push-Mitteilungen, und sie kostet keine Store-Gebühren. | Vorstand | N-APP-01; [ADR-004](adr/adr-004-technik-wie-tco-app.md) |
| K-09 | Wie viel darf die App pro Jahr höchstens kosten (Server, Mailversand; bei MyTCO geschätzt ca. CHF 95–175 pro Jahr)? Wer gibt die Kosten frei: Vorstand oder Budget der GV? | Vorstand | N-KOSTEN-01; Hosting, [ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md) |
| K-10 | Domain und E-Mail: (K-10.1) Darf die App unter einer Adresse von badibeach.ch laufen (z. B. `app.badibeach.ch`; die DNS-Einträge liegen bei Hostpoint)? (K-10.2) Darf sie Mails von einer Adresse @badibeach.ch über das Google-Workspace-Konto des Vereins senden (Login-Codes, Benachrichtigungen)? (K-10.3) Wer verwaltet Hostpoint und Google Workspace? | Kommunikation | Hosting, Mailversand, Kosten; [ADR-004](adr/adr-004-technik-wie-tco-app.md) |
| K-11 | Wäre der Vorstand einverstanden, wenn die App Code oder sogar Server mit MyTCO teilt, der App des Tennis-Club Olten? Die Daten der beiden Vereine blieben getrennt, die Kosten würden eventuell geteilt. Gibt es Bedenken, etwa zu Datenschutz oder Abhängigkeit von einem anderen Verein? | Vorstand | [ADR-003](adr/adr-003-verhaeltnis-zur-tco-app.md) |
| K-12 | Austausch unter Mitgliedern: (K-12.1) Worüber tauschen sich die Mitglieder heute aus (z. B. WhatsApp-Gruppe), und soll die App das ersetzen? (K-12.2) Wenn alle Mitglieder Beiträge veröffentlichen und kommentieren können: Wer moderiert und löscht unpassende Beiträge? (K-12.3) Genügen Beiträge mit Kommentaren, oder braucht es getrennte Bereiche (z. B. Vorstand, Mitglieder, Themen)? | Kommunikation | A-AUSTAUSCH-01 bis -03; Umfang: ein Forum ist ein eigener grosser Bereich |
| K-13 | Wie sollen sich Mitglieder kontaktieren, etwa auf eine Suchanfrage hin: (a) Nachrichten innerhalb der App (Chat), oder (b) Telefon oder E-Mail des anderen werden angezeigt, wenn er das im Profil erlaubt? Ein Chat ist deutlich aufwendiger und braucht mehr Datenschutz. | Kommunikation | A-SUCHE-03, A-PROFIL-06; Umfang, Datenschutz |
| K-14 | Wer verwaltet was in der App? (K-14.1) Wer legt Clubturniere und Open-Court-Termine an? (K-14.2) Wer pflegt Mitglieder und Zugänge? (K-14.3) Wer teilt Felder zu oder korrigiert Reservationen? (K-14.4) Wer vergibt die Rollen? Reichen die Rollen Mitglied, Vorstand und Administration, oder braucht es pro Ressort eigene Rechte? | Vorstand | A-ROLLE-02, -03, A-TURNIER-01, A-OPENCOURT-01, A-FELD-02; Rollenmodell |

## Priorität 2 — vor dem Bau des betroffenen Bereichs

| ID | Frage | An wen | Wozu |
|----|-------|--------|------|
| K-15 | Clubturniere: (K-15.1) Meldet man sich einzeln oder als Team an, und wie gross ist ein Team (z. B. 2er, 4er)? (K-15.2) Gibt es eine Warteliste, wenn ein Turnier voll ist? | Turniere | A-TURNIER-02, -05, A-SUCHE-08 |
| K-16 | Open Court: Was ist ein Open-Court-Termin genau (wer leitet, für wen, kostet er etwas)? Was passiert, wenn die Mindestzahl nicht erreicht ist (Absage, Frist, Benachrichtigung)? | Events, Turniere | A-OPENCOURT-01, -02, -04; [Glossar](glossar.md) |
| K-17 | Feldfreigabe: (K-17.1) Bis wann muss ein Feld freigegeben werden? (K-17.2) Wer ein freigegebenes Feld will: Bekommt es, wer zuerst klickt? (K-17.3) Sollen Mitglieder benachrichtigt werden, wenn ein Feld frei wird (alle, nur Interessierte)? | Zuständige Person Feldreservation | A-FELD-05, -07 |
| K-18 | Spielniveau: (K-18.1) Wie wird das Niveau beschrieben (z. B. Level 1–5, Einsteiger bis Lizenz)? (K-18.2) Legt es jedes Mitglied selbst fest, oder bestimmt es der Verein? | Turniere | A-PROFIL-03, A-SUCHE-02, -04 |
| K-19 | Wer ist im Verein Ansprechperson für den Datenschutz? Darf die Datenschutzerklärung auf badibeach.ch um die App ergänzt werden, oder bekommt die App eine eigene? | Vorstand | N-DATENSCHUTZ-01 |

## Zurückgestellt

Die übrigen «Noch zu klärenden Anforderungen» aus dem Anforderungsdokument verändern die erste
Entwicklung nicht. Sie werden geklärt, wenn ihr Bereich gebaut wird. Bis dahin gilt der Vorschlag.

| Frage im Dokument | Abschnitt | Wo sie geklärt wird / Vorschlag |
|-------------------|-----------|---------------------------------|
| Anmeldung einzeln oder als Team? | DOK 2 | K-15.1 |
| Warteliste bei ausgebuchten Veranstaltungen? | DOK 2 | K-15.2 |
| Wer darf Turniere und Open-Court-Termine erstellen und verwalten? | DOK 2 | K-14.1 |
| Automatische Erinnerungen vor den Veranstaltungen? | DOK 2 | Vorschlag: ja, eine Push-Mitteilung am Vortag, abschaltbar (A-TURNIER-06) |
| Wer darf Spielfelder reservieren? | DOK 3 | K-05.3 und K-02 |
| Reservationen selbstständig bearbeiten oder löschen? | DOK 3 | Vorschlag: ergibt sich aus K-02. Freigeben darf jedes Mitglied seine eigene Reservation, ändern und löschen nur, wer die Felder zuteilt (K-14.3) |
| Bis wann muss ein Feld freigegeben werden? | DOK 3 | K-17.1 |
| Wie wird verhindert, dass ein Feld doppelt genutzt wird? | DOK 3 | Vorschlag: Die App lässt pro Feld und Zeitfenster nur eine Reservation zu, auch bei der Übernahme (K-17.2) |
| Benachrichtigung bei freigegebenem Feld? | DOK 3 | K-17.3 |
| Wie wird das Spielniveau definiert? | DOK 4.4 | K-18.1 |
| Level selbst festlegen oder durch den Verein? | DOK 4.4 | K-18.2 |
| Suchanfragen für alle Mitglieder sichtbar? | DOK 4.4 | Vorschlag: ja, für alle eingeloggten Mitglieder, nie öffentlich |
| Kontaktaufnahme per Chat, Direktnachricht oder Kontaktdaten? | DOK 4.4 | K-13 |
| Suchanfragen verschwinden nach dem Spieltermin? | DOK 4.4 | Vorschlag: ja, automatisch am Tag danach |
| Sollen alle Mitglieder Beiträge veröffentlichen können? | DOK 5 | K-12.2 |
| Separate Bereiche für Vorstand und Mitglieder? | DOK 5 | K-12.3 |
| Kommentarfunktion? | DOK 5 | K-12.2 |
| Push-Benachrichtigungen für neue Beiträge? | DOK 5 | Vorschlag: Push für Mitteilungen des Vorstands, für Beiträge der Mitglieder einzeln abschaltbar |
| Wichtige Informationen dauerhaft anpinnen? | DOK 5 | Vorschlag: ja, der Vorstand pinnt an (deckt A-INFO-05) |

## Beantwortet

| ID | Frage | Antwort | Von, am | Folgen |
|----|-------|---------|---------|--------|
