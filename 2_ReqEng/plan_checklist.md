# CampusRide – SRS Workflow & GitHub Issues (Handover: 01.12.2026)

## 1. Zeitplan bis zum Handover

| Tag | Phase | Ziel | Modus |
| :--- | :--- | :--- | :--- |
| **Di, 24.11.** | Setup & Prep | Google Doc (Wiegers-Template) & GitHub Board anlegen, Fragenkatalog erstellen, Termin mit Team 7 buchen | Kickoff + Einzelarbeit |
| **Mi, 25.11.** | **Phase 3: Elicitation** | Interview/Workshop mit Team 7 (60–90 Min.), Protokoll abstimmen | Meeting mit Team 7 |
| **Do, 26.11.** | **Phase 4: Elaboration** | Paralleles Ausformulieren der SRS-Kapitel in Google Docs, offene Punkte als `[TBD]` markieren | Einzelarbeit |
| **Fr, 27.11.** | **Phase 4: Elaboration** | Kapitel abschließen, kurzer interner Sync (30–45 Min.) | Einzelarbeit + Sync |
| **Sa, 28.11.** | Interne QS | Gegenseitiges Peer-Review, Draft v0.9 bis abends an Team 7 senden | Einzelarbeit |
| **So/Mo, 29.–30.11.** | **Phase 5: Negotiation & Validation** | Review- & Priorisierungs-Meeting mit Team 7, Anpassungen einarbeiten, `Version 1.0 approved` setzen | Meeting mit Team 7 |
| **Di, 01.12.** | **Phase 6: Handover** | Finaler PDF-Export, Übergabe der Baseline in der Vorlesung | Gemeinsamer Abschluss |

---

## 2. Arbeitsteilung im 4er-Team

* **Person A (Orga-Lead):** Kap. 1 (*Introduction*), Kap. 2 (*Overall Description* 2.1–2.4, 2.6–2.7), *Appendix A (Glossary)*, *Appendix C (TBD-Liste)*, *Revision History* & Moderation.
* **Person B (Features 1):** Kap. 4 – *Registrierung/Verifizierung & Profil*, *Fahrten anbieten (einzeln & wiederkehrend)*, *Suche, Matching & Fahrtgesuche* (Fokus: Q1).
* **Person C (Features 2):** Kap. 4 – *Buchungs-Lifecycle & Kapazität*, *Benachrichtigungen & Kommunikation*, *Kostenbeteiligung*, *Bewertungen & Moderation* (Fokus: Q2–Q5).
* **Person D (NFRs & QS-Lead):** Kap. 2.5 (*Constraints*), Kap. 3 (*External Interfaces*), Kap. 5 (*Nonfunctional Requirements*), Kap. 6 (*Other Requirements*) & optional *Appendix B* (Fokus: C1, Q6, Q7).

**GitHub Labels:** `meeting`, `elicitation`, `srs-draft`, `review`, `negotiation`, `tbd-blocker`

---

## 3. GitHub Issues: Gemeinsame Meetings (`@all`)

### Issue #1: Setup & Elicitation-Vorbereitung (`label: meeting`, `elicitation`)
- [ ] Google Doc nach Wiegers-Template (Kap. 1–6 + Appendix A–C + Revision History) aufsetzen
- [ ] Konventionen (Kap. 1.2) festlegen: ID-Schema (`FR-<MODUL>-01`, `NFR-<KAT>-01`), Prioritäten (`High/Medium/Low`), *"shall"*-Formulierungen, `[TBD-XX]`-Tags
- [ ] Rollen A–D zuweisen und Issues #2–#10 anlegen
- [ ] Interviewleitfaden zu Q1–Q7 und Randfällen erstellen
- [ ] Elicitation-Termin (Mi/Do) und Review-Fenster (So/Mo) mit Team 7 fixieren

### Issue #2: Elicitation-Workshop mit Team 7 (`label: meeting`, `elicitation`)
*Moderation: Person A | Protokoll: Person D | Fachfragen: Personen B & C*
- [ ] In-Scope vs. Out-of-Scope bestätigen
- [ ] **Q1 (Matching):** Zwischenstopps/Umwege & Zeitfenster klären
- [ ] **Q2 (Kosten):** Berechnungsbasis & Anpassbarkeit durch Fahrer klären
- [ ] **Q3 (Storno):** Fristen & Konsequenzen bei späten/wiederholten Absagen klären
- [ ] **Q4 (Kommunikation):** In-App-Chat vs. Kontaktdaten-Freigabe klären
- [ ] **Q5 (Moderation):** Befugnisse & Ernennung von Moderatoren klären
- [ ] **Q6 (Privacy/C1):** Datensichtbarkeit & Löschfristen (DSGVO) klären
- [ ] **Q7 (Plattform):** Web-App vs. Mobile-App (Machbarkeit C3) klären
- [ ] Grob-Priorisierung für den 1-Quartals-Prototyp (Part II) abfragen
- [ ] Protokoll noch am selben Tag von Team 7 bestätigen lassen

### Issue #3: Interner Elaboration-Sync (`label: meeting`)
- [ ] Vollständigkeit gegen Use-Case-Diagramm (Inception Doc Fig. 1) prüfen
- [ ] Begriffe vereinheitlichen und ins Glossar (Appendix A) eintragen
- [ ] Querverweise zwischen Kap. 4 (Features), Kap. 3 (Interfaces) und Kap. 5 (NFRs/Rules) abgleichen
- [ ] Offene `[TBD]`-Stellen in Appendix C bündeln und Klärung zuweisen

### Issue #4: Negotiation & Validation mit Team 7 (`label: meeting`, `negotiation`)
*Vorbereitung: Draft v0.9 mind. 24h vorher an Team 7 senden*
- [ ] Walkthrough durch alle System Features (Kap. 4) und NFRs (Kap. 5) durchführen
- [ ] Umfang & Prioritäten für 1 Quartal / 4 Entwickler (C3) verhandeln und anpassen
- [ ] Alle Punkte aus Appendix C (TBD-Liste) auflösen oder final zuweisen
- [ ] Prüfen auf Vollständigkeit, Eindeutigkeit, Detailtiefe und Widerspruchsfreiheit
- [ ] Änderungen einarbeiten, Revision History aktualisieren und auf `Version 1.0 approved` setzen
- [ ] Schriftliche Freigabe (Approval) von Team 7 einholen

### Issue #5: Finales Handover (`label: meeting`)
- [ ] Formatierung, Inhaltsverzeichnis, Seitenumbrüche und Platzhalter final prüfen
- [ ] `CampusRide_SRS_v1.0_approved.pdf` exportieren und Team 7 bereitstellen
- [ ] Baseline am **01.12.2026** in der Vorlesung übergeben

---

## 4. GitHub Issues: Einzelarbeit

### Issue #6: SRS Kap. 1, Kap. 2 (Basis) & Anhänge A/C (`Assignee: Person A`, `label: srs-draft`)
- [ ] **1.1 & 1.4:** Purpose & Product Scope (Ziele G1–G5, In-/Out-of-Scope) ausarbeiten
- [ ] **1.2, 1.3 & 1.5:** Document Conventions, Intended Audience & References dokumentieren
- [ ] **2.1 & 2.2:** Product Perspective & Product Functions (High-Level-Überblick) beschreiben
- [ ] **2.3:** User Classes (*Student, Driver, Passenger, Moderator* inkl. Rollenwechsel) definieren
- [ ] **2.4, 2.6 & 2.7:** Operating Environment (Q7), User Documentation & Assumptions/Dependencies (A1–A2) festhalten
- [ ] **Appendix A & C:** Glossary und TBD-Liste laufend pflegen

### Issue #7: SRS Kap. 4 – Auth, Fahrtenangebot & Matching (`Assignee: Person B`, `label: srs-draft`)
*Pro Feature: Description & Priority → Stimulus/Response Sequences → Functional Requirements (ID + Traceability zu G1–G5/C2)*
- [ ] **4.1 Auth & Profil:** DHBW-E-Mail-Verifizierung (C2), Login/Logout, Profilverwaltung
- [ ] **4.2 Fahrten anbieten:** Einzelfahrten & wiederkehrende Fahrten (Serienlogik, Einzel- vs. Serienbearbeitung/-absage)
- [ ] **4.3 Suche, Matching & Gesuche:** Suchfilter, Matching-Logik (Q1), Ride Requests & Link-Sharing
- [ ] Fehler- und Randfälle (ungültige Mail, 0 freie Plätze, keine Treffer) abdecken

### Issue #8: SRS Kap. 4 – Buchung, Kosten, Notifications & Trust (`Assignee: Person C`, `label: srs-draft`)
*Pro Feature: Description & Priority → Stimulus/Response Sequences → Functional Requirements (ID + Traceability zu G1–G5)*
- [ ] **4.4 Buchung & Kapazität:** Lifecycle (`requested` → `confirmed`/`declined` → `cancelled`/`completed`), Überbuchungsschutz, Stornoregeln (Q3)
- [ ] **4.5 Notifications & Kommunikation:** Automatische Benachrichtigungen & Abspracheweg (Q4)
- [ ] **4.6 Kostenbeteiligung:** Berechnung Kostenvorschlag (Q2) & Hinweis auf externe Zahlung
- [ ] **4.7 Bewertungen & Moderation:** Gegenseitige Bewertungen, Meldungen & Moderationsmaßnahmen (Q5)
- [ ] Fehler- und Randfälle (Doppelbuchung, späte Stornos, unberechtigte Bewertungen) abdecken

### Issue #9: SRS Kap. 2.5, Kap. 3, Kap. 5 & Kap. 6 (`Assignee: Person D`, `label: srs-draft`)
- [ ] **2.5 Constraints:** C1 (DSGVO), C2 (DHBW-Mail), C3 (1 Quartal / 4 Personen) & Plattform (Q7)
- [ ] **3.1–3.4 External Interfaces:** User, Hardware, Software (E-Mail/Push, ggf. Routing-API) & Communications Interfaces (HTTPS/TLS)
- [ ] **5.1 & 5.2 Performance & Safety:** Messbare Antwortzeiten & Sicherheitsaspekte gegen Missbrauch
- [ ] **5.3 Security:** Auth, RBAC, Datensichtbarkeit & Löschfristen (C1, Q6)
- [ ] **5.4, 5.5 & 6:** Messbare Quality Attributes, Business Rules (u. a. keine kommerzielle Nutzung) & Other Requirements
- [ ] **Optional (Appendix B):** State Diagram für Booking Lifecycle ergänzen

### Issue #10: Internes Peer-Review (`Assignees: @all`, `label: review`)
*Rotation: A → B | B → C | C → D | D → A (Kommentare direkt in Google Docs)*
- [ ] **Necessary:** Bezug zu Projektzielen (`G1`–`G5`) vorhanden?
- [ ] **Unambiguous:** Eindeutig formuliert (keine vagen Adjektive wie *schnell, intuitiv*)?
- [ ] **Singular:** Genau eine Anforderung pro ID (keine Mehrfach-„und“-Ketten)?
- [ ] **Feasible:** In einem Quartal von 4 Personen umsetzbar (C3)?
- [ ] **Verifiable:** Objektiv testbar?
- [ ] **Traceable:** Eindeutige ID + Referenz auf Quelle/Goal?
- [ ] **Kein Design-Zwang:** Keine unnötigen technischen Implementierungsvorgaben?