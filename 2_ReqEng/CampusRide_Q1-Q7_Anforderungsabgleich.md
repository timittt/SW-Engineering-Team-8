# CampusRide – Anforderungsabgleich Q1–Q7

**Grundlage:** *CampusRide – Inception Document*, Version 1.1, 24.11.2026, und *Software Engineering – Program Design Part I*.  
**Zweck:** Die sieben Fragen aus Abschnitt 3.5 des Inception Documents in deren Originalreihenfolge erfassen und für jede Frage zwischen bereits benannten Anforderungen, noch nicht ausgearbeiteten Anforderungen und offenen Fragen unterscheiden.  
**Wichtig:** Das Aufgabenpapier enthält keine eigene Q1–Q7-Liste. Die Q1–Q7-Wortlaute stehen im Inception Document, Abschnitt 3.5, S. 4; sie werden unten unverändert auf Englisch wiedergegeben. Die Inhalte des Aufgabenpapiers werden als Vorgaben für die weitere Spezifikation herangezogen, nicht als Antworten auf die offenen Punkte.

## Q1 — Matching

> “Matching: How precisely shall routes and times be matched, e.g. start and destination only or also intermediate stops and detours, and within which time window?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Angebote und Fahrtgesuche sollen anhand von **Route, Zeit und freien Sitzplätzen** zusammengeführt bzw. gesucht werden (Inception Document, § 3.2, S. 2; § 3.3, Tabelle 2, S. 3).
- Fahrgäste können nach passenden Fahrten suchen; falls keine passende Fahrt vorhanden ist, können sie ein Fahrtgesuch einstellen, auf das Fahrer mit Fahrten in derselben Richtung reagieren (Inception Document, § 3.2, S. 2).
- Die Plattform verwaltet Sitzplatzkapazitäten, damit eine Fahrt nicht überbucht wird (Inception Document, § 3.2, S. 3).

### Nicht ausgearbeitete Requirements
- Der Matching-Begriff „passend“ bzw. „dieselbe Richtung“ ist nicht operationalisiert: Es gibt keine Kriterien oder Algorithmen für Routennähe, Umwege, Zwischenhalte oder zeitliche Toleranzen.
- Es ist nicht beschrieben, wie freie Sitzplätze in Suche oder Rangfolge der Treffer einfließen.
- **Ableitung:** Die geforderten Such-/Matching-Funktionen benötigen spezifizierbare Eingaben, Regeln und Ergebnisse; diese Detailanforderungen sind im Inception Document noch nicht festgelegt.

### Offene Fragen
- Welche Routenbestandteile werden verglichen (nur Start/Ziel oder auch Zwischenhalte/Umwege)?
- Welches Zeitfenster gilt für passende Abfahrtszeiten?
- Wie werden verfügbare Plätze bei Suche und Zuordnung berücksichtigt?

## Q2 — Cost contribution

> “Cost contribution: On which basis shall the suggested contribution be calculated (e.g. distance, fuel costs, flat rate)?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Für jede Fahrt soll die Plattform einen **fairen Beitrag je Fahrgast vorschlagen**; die Zahlung findet außerhalb des Systems statt (Inception Document, § 3.2, S. 2).
- Transparente und faire Kostenteilung ist als Ziel genannt (Inception Document, § 2, Tabelle 1, G4, S. 2).
- Zahlungsabwicklung zwischen Nutzern ist ausdrücklich außerhalb des Umfangs (Inception Document, § 3.4, S. 3).

### Nicht ausgearbeitete Requirements
- Es gibt keine Berechnungsformel, Eingabedaten, Rundungsregeln oder Erläuterung, wie „fair“ bestimmt wird.
- Nicht festgelegt ist, ob der Vorschlag verbindlich, veränderbar oder nur ein unverbindlicher Richtwert ist.
- **Ableitung:** Da Zahlung extern erfolgt, ist mindestens die Ermittlung/Anzeige des Vorschlags im System relevant; ob und wie Nutzer den Betrag anpassen dürfen, bleibt offen.

### Offene Fragen
- Welche Berechnungsgrundlage gilt (zum Beispiel Strecke, Kraftstoffkosten oder Pauschale)?
- Welche weiteren Daten/Annahmen werden für die Berechnung benötigt?
- Welchen Status hat der vorgeschlagene Betrag (Richtwert oder verbindlicher Beitrag)?

## Q3 — Cancellations

> “Cancellations: Which deadlines and consequences apply to late or repeated cancellations?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Fahrer können Fahrten bearbeiten oder stornieren; Fahrgäste können Buchungen stornieren (Inception Document, § 3.2, S. 2; § 6, Use-Case-Diagramm, S. 5).
- Beteiligte sollen automatisch über Änderungen und Stornierungen informiert werden (Inception Document, § 3.2, S. 2).
- Der Buchungslebenszyklus umfasst angefragt, bestätigt oder abgelehnt und anschließend storniert oder abgeschlossen (Inception Document, § 3.2, S. 3).

### Nicht ausgearbeitete Requirements
- Es gibt keine Fristen, Stornierungsbedingungen oder Folgen für Fahrer bzw. Fahrgäste.
- Nicht definiert sind der Umgang mit wiederholten/kurzfristigen Stornierungen, eine etwaige Sperre oder ein Einfluss auf Bewertungen.
- Nicht spezifiziert ist, welche Statusübergänge nach einer Stornierung zulässig sind und wen eine Änderung jeweils betrifft.
- **Ableitung:** Der genannte Lebenszyklus verlangt eine konsistente Behandlung von Statusänderungen; konkrete Regeln dafür enthält das Dokument nicht.

### Offene Fragen
- Bis wann darf eine Fahrt oder Buchung ohne besondere Folgen storniert werden?
- Welche Folgen gelten bei verspäteten oder wiederholten Stornierungen?
- Welche betroffenen Personen erhalten bei welcher Stornierung eine Benachrichtigung?

## Q4 — Communication

> “Communication: How do driver and passengers coordinate details, e.g. via in-app messages or by sharing contact details after confirmation?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Fahrer können Sitzplatzanfragen akzeptieren oder ablehnen; Fahrgäste können Fahrtplätze anfragen (Inception Document, § 3.2, S. 2; § 6, S. 5).
- Automatische Benachrichtigungen bei neuen Anfragen, Bestätigungen, Änderungen und Stornierungen sind vorgesehen (Inception Document, § 3.2, S. 2).
- Ein Kommunikationskanal für die Abstimmung konkreter Fahrtdetails ist nicht als Funktion aufgeführt.

### Nicht ausgearbeitete Requirements
- Es ist nicht festgelegt, ob In-App-Nachrichten, Kontaktfreigabe oder ein anderer Kommunikationsweg bereitgestellt wird.
- Nicht spezifiziert sind Zeitpunkt und Umfang einer möglichen Kontaktfreigabe, Nachrichtenfunktionen, Aufbewahrung oder Missbrauchsschutz.
- **Ableitung:** Benachrichtigungen über Ereignisse lösen die Abstimmung zwischen den Beteiligten nicht notwendigerweise; aus der Nennung von Notifications lässt sich kein In-App-Chat ableiten.

### Offene Fragen
- Wie koordinieren Fahrer und Fahrgäste praktische Details?
- Falls Kontaktdaten geteilt werden: wann, welche Daten und mit wem?
- Falls In-App-Nachrichten vorgesehen sind: welche grundlegenden Funktionen und Regeln gelten?

## Q5 — Moderation

> “Moderation: Which measures may moderators take, and how are moderators appointed?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Nutzer können Fehlverhalten melden; Moderatoren bearbeiten Meldungen (Inception Document, § 3.2, S. 2).
- Moderator ist als Nutzerrolle mit erweiterten Rechten vorgesehen, beispielhaft ein Mitglied des Studierendenrats; Ziel ist die Sicherheit der Community (Inception Document, § 5, Tabelle 4, S. 5).
- Das Use-Case-Diagramm enthält „Handle reports“ für Moderator (Inception Document, § 6, S. 5).

### Nicht ausgearbeitete Requirements
- Die konkreten Moderationsmaßnahmen, Rechte und Grenzen sind nicht beschrieben.
- Verfahren für Prüfung, Entscheidung, Eskalation, Benachrichtigung oder Einspruch sind nicht festgelegt.
- Das Dokument benennt mögliche Moderatoren, legt aber nicht fest, wer sie auswählt, autorisiert oder abberuft.
- **Ableitung:** Eine Rolle mit erweiterten Rechten legt ohne explizite Autorisierung keine konkrete Rechtevergabe oder Maßnahme fest.

### Offene Fragen
- Welche Maßnahmen können Moderatoren ergreifen und unter welchen Voraussetzungen?
- Wer ernennt Moderatoren, und wie wird deren Berechtigung verwaltet?
- Wie läuft die Bearbeitung einer Meldung einschließlich einer möglichen Überprüfung ab?

## Q6 — Privacy

> “Privacy: Which personal data are visible to whom, and how long are they stored?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Personen- und Standortdaten müssen DSGVO-konform verarbeitet werden (Inception Document, § 3.4, C1, S. 3).
- Zugang ist auf DHBW-Studierende beschränkt; die Verifizierung erfolgt über die Hochschul-E-Mail-Adresse (Inception Document, § 3.4, C2, S. 3).
- Das System soll Nutzer, Fahrten, Buchungen, Bewertungen und Meldungen persistent speichern (Inception Document, § 3.2, S. 3).
- Die Abschnitte zu Geltungsbereich und offenen Punkten nennen Datenschutz allgemein; konkrete Rollen-/Sichtbarkeitsregeln oder Löschfristen fehlen (Inception Document, § 3.4 und § 3.5, S. 3–4).

### Nicht ausgearbeitete Requirements
- Nicht festgelegt sind Datenkategorien und Sichtbarkeit je Nutzerrolle bzw. Buchungsstatus.
- Es gibt keine Aufbewahrungs- und Löschfristen, Löschregeln für Konten oder Daten nach Fahrtende und keine Regel für Sicherung/Archivierung.
- Nicht beschrieben sind Datenminimierung, Einwilligung/Information, Auskunft oder sonstige konkrete Datenschutzabläufe.
- **Ableitung:** Die Vorgabe „DSGVO-konform“ ist ein Rahmen, ersetzt aber keine konkreten Anforderungen an Sichtbarkeit und Speicherung, nach denen Q6 ausdrücklich fragt.

### Offene Fragen
- Welche personenbezogenen Daten werden erhoben und für wen sichtbar gemacht?
- Wie lange werden die jeweiligen Daten gespeichert, und wann werden sie gelöscht?
- Welche Sichtbarkeit gilt insbesondere für Fahrtdetails, Kontaktdaten, Bewertungen und Meldungen?

## Q7 — Platform

> “Platform: Shall CampusRide be a web application, a mobile app, or both?”  
> — Inception Document, § 3.5, S. 4

### Vorhandene Requirements
- Als Nutzungsannahme wird genannt, dass alle Studierenden eine DHBW-E-Mail-Adresse sowie ein Smartphone oder einen Computer mit Internetzugang haben (Inception Document, § 3.4, A1, S. 3).
- Die Architektur wird in der Inception bewusst nicht festgelegt (Inception Document, § 3.2, S. 3).
- Das Aufgabenpapier sieht die spätere Architektur- und Implementierungsarbeit in Part II / Q1 vor, verlangt in Part I jedoch zunächst eine vollständige SRS (Project Part I, Abschnitt 1, S. 1–2; §§ 2.1, 2.5 und 2.10, S. 3, 5 und 7).

### Nicht ausgearbeitete Requirements
- Es ist keine Zielplattform und kein unterstütztes Betriebssystem, Browser oder Gerät festgelegt.
- Es gibt keine Anforderungen an responsive Darstellung, Installierbarkeit, Offline-Nutzung oder plattformspezifische Funktionen.
- **Ableitung:** Die Annahme von Smartphone- und Computerzugang belegt die Verfügbarkeit solcher Geräte bei Nutzern, aber nicht die Entscheidung, eine native App, Webanwendung oder beides zu entwickeln.

### Offene Fragen
- Wird CampusRide als Webanwendung, mobile App oder beides angeboten?
- Welche Geräte und Umgebungen müssen unterstützt werden?
- Welche plattformübergreifenden Qualitätsanforderungen sind für die gewählte Lösung nötig?

## Vollständigkeitsprüfung und Einordnung

- Die Liste oben umfasst alle sieben Q-Punkte in der Reihenfolge und mit dem Wortlaut aus Inception Document, § 3.5, S. 4.
- Für jeden Punkt sind explizite Aussagen aus dem Inception Document als vorhandene Requirements aufgeführt; fehlende Details werden getrennt als nicht ausgearbeitet und/oder offene Fragen benannt. **Ableitungen** sind ausdrücklich markiert und nicht als bereits beschlossene Festlegungen formuliert.
- Das Inception Document kennzeichnet die Detailregeln selbst als bewusst offen (§ 3.2, S. 2) und verlangt deren Klärung im Requirements Engineering (§ 3.5, S. 4). Daher enthält diese Auswertung keine erfundenen Antworten oder neuen verbindlichen Entscheidungen.
- Das Aufgabenpapier verlangt für die SRS unter anderem funktionale und nicht-funktionale Anforderungen, Use Cases, Annahmen/Einschränkungen sowie unterstützende Dokumentation; es fordert außerdem die Klärung von Mehrdeutigkeiten, Lücken und Widersprüchen (Project Part I, §§ 2.4–2.6, S. 4–6; § 2.10, S. 7). Die sieben Punkte sind somit offene Spezifikationsarbeit, keine bereits validierte SRS.

## Quellen

1. **CampusRide – Inception Document**, Requirement Rebels (Team 7), Version 1.1, 24.11.2026. Verweise im Text nach Abschnitt, Tabelle/ID und PDF-Seite.
2. **Software Engineering – Program Design Part I**, Prof. Dr. Christian Braunagel. Verweise im Text nach Abschnitt und PDF-Seite.
