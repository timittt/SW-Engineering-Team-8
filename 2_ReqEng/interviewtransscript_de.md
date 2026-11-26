# Gesprächsprotokoll – Anforderungen Mitfahr-App (WhatsApp-Audio vom 26.11.2026)

Bereinigte Fassung des Transkripts (ca. 15 Min.). Unverständliche Stellen sind nach Rücksprache korrigiert oder weggelassen. Zeitmarken sind ungefähr.

## Kurzfassung der Entscheidungen

- **Stornieren:** bis ca. 1 Tag vorher ohne Konsequenzen; danach schlechtere Bewertung – für Fahrer *und* Mitfahrer. Alle Beteiligten werden benachrichtigt.
- **Buchung:** Mitfahrer stellt Anfrage → Chat öffnet sich → Fahrer muss jede Anfrage bestätigen.
- **Chat:** Einzelchats (Fahrer ↔ Mitfahrer), kein Gruppenchat; Ende-zu-Ende-verschlüsselt; Security übernimmt die DHBW.
- **Daten:** Chats und Buchungen werden nach 14 Tagen gelöscht, bei offenen Zahlungen nach 30 Tagen. Keine Fahrthistorie, keine Statistiken pro Account.
- **Moderation:** langfristig durch die StuV, inkl. Einsprüchen. Moderatoren können nur sperren; Gesperrte können keine Fahrten mehr machen.
- **Bewertung:** 1–5 Sterne, nur nach gemeinsamer Fahrt, bis 14 Tage danach. Grenzwerte und Dauer für Sperrungen: **teamintern noch zu klären**.
- **Zielgruppe:** alle mit DHBW-Mail (Ravensburg und Friedrichshafen). Android: alle noch unterstützten Versionen.
- **Prototyp-Scope:** Fahrten anbieten, Buchungsablauf mit Anfrage/Zustimmung, Bearbeiten, Stornieren. Chat mittelwichtig, Bewertungen später.

---

## [00:00] Stornieren

**Frage:** Gibt es einen Zeitpunkt, bis zu dem man ohne Konsequenzen stornieren kann – z. B. wenn man zwei Minuten vorher absagt?

**Antwort:** Konsequenzen sollte es auch für Mitfahrer geben, weil sie anderen einen Platz wegnehmen – also für beide: eine schlechtere Bewertung. Es kann aber immer etwas dazwischenkommen, deshalb ein Zeitfenster: bis etwa einen Tag vorher ist Stornieren kein Problem.

Wer öfter kurzfristig storniert, bekommt mit jeder Fahrt ein schlechteres Rating, bis er irgendwann gesperrt wird.

Bei einer Stornierung bekommen immer alle Beteiligten eine Benachrichtigung.

## [01:30] Chat und Buchungsablauf

**Frage:** Gibt es einen Gruppenchat, z. B. bei einem Fahrer mit drei Mitfahrern und mehreren Zwischenstopps, oder hat jeder einen Einzelchat mit dem Fahrer?

**Antwort:** Der Fahrer koordiniert alles über Einzelchats.

**Frage:** Ist die Buchung erst nach dem Chat fest, oder bucht man und landet dann im Chat?

**Antwort:** Stellt ein Mitfahrer eine Anfrage, geht der Chat auf. Fest gebucht ist erst, wenn der Fahrer die Anfrage genehmigt. Chatten soll aber jederzeit möglich sein, auch vorher, z. B. für Fragen zur Buchung.

Die Security des Chats übernimmt die DHBW.

**Verschlüsselung:** Muss schon jetzt festgelegt werden, weil sie in die App gehört → Ende-zu-Ende-Verschlüsselung wie bei WhatsApp.

## [03:00] Datenaufbewahrung und Moderation

**Frage:** Werden die Chatdaten nach der Fahrt gelöscht?

**Antwort:** Sie bleiben noch eine Weile gespeichert, falls Beschwerden kommen und man auf das Chat-Log zugreifen muss – etwa ein bis zwei Wochen, danach werden sie gelöscht.

Es gibt einen Melde-Button im Chat. Der Moderator hat ohnehin Zugriff auf alle Logs.

Außer Sperren kann ein Moderator eigentlich nichts tun. Wer gesperrt ist, kann keine Fahrten mehr machen.

Die Moderation wird langfristig komplett an die StuV übergeben – es braucht eine Institution, die dauerhaft da ist. Einsprüche laufen ebenfalls über die StuV.

## [04:30] Sichtbarkeit und Speicherung

Auch Fehlverhalten von Moderatoren wird über die StuV geregelt.

Daten sind nur für die Moderatoren und die Beteiligten im jeweiligen Chat sichtbar – jeder sieht nur, was er unbedingt sehen muss.

**Frage:** Die Buchungen liegen auf dem DHBW-Server. Werden sie zusammen mit den Chats gelöscht, oder gibt es eine Fahrthistorie pro Account (z. B. wie oft jemand abgesagt hat oder zu spät war)?

**Antwort:** Es werden keine Statistiken gespeichert. Wer wann mit wem gefahren ist, ist nicht relevant – die Buchungen werden zusammen mit den Chats gelöscht, nach 14 Tagen.

Wenn noch eine Zahlung offen ist und nachgewiesen werden muss, dass bezahlt wurde: 30 Tage.

## [06:00] Accounts und Plattform

Während der Fahrt ist nur das Profil sichtbar.

Exmatrikulation ist kein Use Case. Die Verifizierung über die DHBW-Mail dient vor allem dazu, dass sich keine Bots registrieren und massenhaft Accounts anlegen.

**Android-Version:** alle Versionen, die noch unterstützt werden (Sicherheitsupdates bekommen).

## [07:30] Bewertung und Sperrung

**Frage:** Wir hatten gesagt, dass man bei schlechtem Rating irgendwann gesperrt wird – wie lange und ab welcher Grenze?

**Antwort:** Bewertet wird mit 1 bis 5 Sternen. Bewerten kann man nur, wenn man mitgefahren ist – es kann also nicht jeder beliebig bewerten. Man soll nicht gleich nach einer schlechten Bewertung gesperrt werden, sondern erst, wenn man über eine gewisse Anzahl an Fahrten durchgehend schlecht bewertet ist. Denkbar sind zeitliche und permanente Sperrungen.

**Offen:** Ab welchem Schnitt, nach wie vielen Fahrten und wie lange gesperrt wird, klärt das Team intern.

## [09:00] Meldungen, Sperrfolgen, Gepäck

Nicht-Zahlung wiegt schwerer als eine einfache schlechte Bewertung.

Beim Melden wählt man eine Überkategorie (z. B. Missbrauch, Nicht-Zahlung, riskantes Fahren) und kann optional einen Text schreiben. Die genauen Kategorien werden noch festgelegt.

Wird ein Fahrer gesperrt, werden alle seine Fahrten im Sperrzeitraum automatisch storniert und die Mitfahrer benachrichtigt.

**Gepäck:** Bei der Buchung gibt man an, ob man Gepäck mitnimmt. Die belegten Sitze zählen automatisch hoch, bis die Fahrt voll ist. Gepäck ist aber kein Grund, eine Buchung zu verhindern – dafür wird auf den Chat mit dem Fahrer verwiesen.

## [10:30] Bestätigungen und Änderungen

Der Fahrer muss jede Anfrage bestätigen: Man kann eine angebotene Fahrt buchen, aber erst die Zustimmung des Fahrers macht sie fest.

Zeiten können nachträglich geändert werden; dann bekommen alle Beteiligten eine Benachrichtigung. Ändert der Fahrer etwas, können die Mitfahrer kostenlos abspringen.

## [12:00] Fahrtbeginn, Ankunft, Bewertungsfrist, Zielgruppe

„Fahrt angetreten“ bzw. „Fahrt abgeschlossen“ soll von einer der beiden Personen bestätigt werden. Das dient eher der Buchhaltung – wenn es niemand macht, hat das keine Konsequenzen.

Eine feste Ankunftszeit wird nicht angegeben, nur eine ungefähre (Estimated Time).

**Frage:** Wie lange kann man nach der Fahrt noch bewerten?

**Antwort:** Zwei Wochen – solange der Chat existiert. Ist der Chat gelöscht, ist auch keine Bewertung mehr möglich.

**Zielgruppe:** alle mit einer DHBW-Mail, also Ravensburg und Friedrichshafen.

**Erwartete Nutzerzahl:** Unklar – müsste man mit einer Umfrage herausfinden, was aber schwierig wird.

## [13:30] Scope für den Prototyp

Wichtig ist eine grundlegende, funktionierende App. Die Kernfunktionen:

- Fahrten anbieten
- der komplette Buchungsablauf
- selbst ein Gesuch einstellen („ich will von A nach B“) oder sich auf eine angebotene Fahrt bewerben
- Anfragen kann der Fahrer annehmen oder ablehnen

Der Chat ist ein Mittelding – wichtig, aber zur Not geht es auch ohne. Nicht essenziell für den ersten Prototyp sind Bewertungen und Ähnliches. Bearbeiten und Stornieren sind dagegen wichtig. Die Funktionen, die daraus folgen, kommen später.

## [15:00] Ende

Keine weiteren Fragen.
