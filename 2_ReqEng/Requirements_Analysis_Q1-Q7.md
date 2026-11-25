# CampusRide – Requirements Analysis Q1–Q7

**Basis:** CampusRide – Inception Document, Version 1.1, 24 Nov 2026; Software Engineering – Program Design Part I; Interview with Team 7, 24 Nov 2026.

**Purpose:** Record the seven questions from Section 3.5 of the Inception Document in their original order and, for each question, distinguish between requirements already stated, decisions taken in the interview with Team 7 on 24 Nov 2026, requirements not yet worked out, and open questions.

**Important:** The assignment paper does not contain its own Q1–Q7 list. The wording of Q1–Q7 is taken from the Inception Document, § 3.5, p. 4, and is quoted unchanged below. The contents of the assignment paper are used as guidelines for the further specification, not as answers to the open points. All still-open questions are also collected in [Open_Questions.md](Open_Questions.md).

---

## Q1 — Matching

> "Matching: How precisely shall routes and times be matched, e.g. start and destination only or also intermediate stops and detours, and within which time window?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* Offers and ride requests shall be matched or searched by route, time and free seats (Inception Document, § 3.2, p. 2; § 3.3, Table 2, p. 3).
* Passengers can search for suitable rides; if no suitable ride exists, they can post a ride request to which drivers with rides in the same direction can respond (Inception Document, § 3.2, p. 2).
* The platform manages seat capacities so that a ride is not overbooked (Inception Document, § 3.2, p. 3).

### Decisions from the interview

* A ride offer shall contain only the start city, the destination city, the number of seats, a checkbox "willing to make stop-overs" and the price. No street addresses, intermediate stops or detailed routes are stored (Interview with Team 7, 24 Nov 2026).
* The number of free seats shall be updated live as bookings are made or cancelled (Interview with Team 7, 24 Nov 2026).
* Matching is therefore based on start city and destination city; intermediate stops are only indicated by the stop-over checkbox and can be filtered (Interview with Team 7, 24 Nov 2026; see UI-5).

### Requirements not yet worked out

* With the interview decisions the matching criteria are settled at city level. No further detailed requirements remain for Q1.

### Open questions

* None.

---

## Q2 — Cost contribution

> "Cost contribution: On which basis shall the suggested contribution be calculated (e.g. distance, fuel costs, flat rate)?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* For each ride the platform shall suggest a fair contribution per passenger; payment takes place outside the system (Inception Document, § 3.2, p. 2).
* Transparent and fair cost sharing is stated as a goal (Inception Document, § 2, Table 1, G4, p. 2).
* Payment processing between users is explicitly out of scope (Inception Document, § 3.4, p. 3).

### Decisions from the interview

* The price per seat shall be set by the driver when creating an offer. This replaces the "suggested contribution" from the Inception Document; the system does not calculate a price (Interview with Team 7, 24 Nov 2026).
* Payment shall not be handled in the app; passengers pay the driver privately (Interview with Team 7, 24 Nov 2026).
* There shall be no upper limit for the price per seat set by the driver (Interview with Team 7, 24 Nov 2026).
* If a passenger does not pay, the driver can contact the moderators; the person is then rated badly and suspended for a period (Interview with Team 7, 24 Nov 2026; see Ratings and suspension below).

### Requirements not yet worked out

* None. Since no price is calculated, no calculation basis, formula or rounding rules are needed.

### Open questions

* None.

---

## Q3 — Cancellations

> "Cancellations: Which deadlines and consequences apply to late or repeated cancellations?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* Drivers can edit or cancel rides; passengers can cancel bookings (Inception Document, § 3.2, p. 2; § 6, use case diagram, p. 5).
* Participants shall be informed automatically about changes and cancellations (Inception Document, § 3.2, p. 2).
* The booking life cycle comprises requested, confirmed or rejected, and then cancelled or completed (Inception Document, § 3.2, p. 3).

### Decisions from the interview

* No decision yet; Q3 was left open in the interview (Interview with Team 7, 24 Nov 2026).
* Notifications shall be delivered as push notifications and tab badges; there is no separate notifications tab (Interview with Team 7, 24 Nov 2026; see UI-1).

### Requirements not yet worked out

* There are no deadlines, cancellation conditions or consequences for drivers or passengers.
* Handling of repeated or short-notice cancellations, a possible suspension, or an effect on ratings is not defined.
* It is not specified which status transitions are allowed after a cancellation and whom a change affects.
* Derivation: The stated life cycle requires consistent handling of status changes; the document does not contain concrete rules for this.

### Open questions

* Until when may a ride or booking be cancelled without particular consequences?
* Which consequences apply to late or repeated cancellations?
* Which affected persons receive a notification for which cancellation?

---

## Q4 — Communication

> "Communication: How do driver and passengers coordinate details, e.g. via in-app messages or by sharing contact details after confirmation?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* Drivers can accept or reject seat requests; passengers can request seats on rides (Inception Document, § 3.2, p. 2; § 6, p. 5).
* Automatic notifications for new requests, confirmations, changes and cancellations are planned (Inception Document, § 3.2, p. 2).

### Decisions from the interview

* Drivers and passengers shall coordinate details via a chat integrated into the app (Interview with Team 7, 24 Nov 2026).
* The chat shall be encrypted (Interview with Team 7, 24 Nov 2026).
* The detail page of an offer shall have a Chat button next to the Book button (Interview with Team 7, 24 Nov 2026; see UI-7).

### Requirements not yet worked out

* The chat type (one chat per passenger or one group chat per ride) is not defined.
* It is not defined from which point a chat can be started (before or only after a booking).
* The kind of encryption (end-to-end or transport/server encryption), the retention of chat messages and protection against abuse are not specified.

### Open questions

* Is there one 1:1 chat between driver and each passenger, or one group chat per ride?
* From when can users chat: already before a booking, or only after the booking is confirmed?
* Does "encrypted" mean end-to-end encryption or only transport/server encryption?
* How long are chat messages stored?
* How can users report abusive chat messages?

---

## Q5 — Moderation

> "Moderation: Which measures may moderators take, and how are moderators appointed?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* Users can report misconduct; moderators handle reports (Inception Document, § 3.2, p. 2).
* Moderator is planned as a user role with extended rights, for example a member of the student council; the goal is the safety of the community (Inception Document, § 5, Table 4, p. 5).
* The use case diagram contains "Handle reports" for the moderator (Inception Document, § 6, p. 5).

### Decisions from the interview

* Moderation shall be handled by the StuV (student representation) (Interview with Team 7, 24 Nov 2026).
* In case of non-payment, users can contact the moderators; the person concerned is rated badly and suspended for a period (Interview with Team 7, 24 Nov 2026).
* The profile shall contain an entry to report a user / contact moderation (Interview with Team 7, 24 Nov 2026; see UI-9).

### Requirements not yet worked out

* Apart from suspension after non-payment, the concrete moderation measures, rights and limits are not described.
* Procedures for review, decision, escalation, notification or appeal are not defined.
* It is defined that the StuV moderates, but not who selects, authorises or removes the individual moderators, and whether there is a separate administrator role.

### Open questions

* Which measures can moderators take besides suspension, and under which conditions?
* Who appoints moderators within the StuV, how is their authorisation managed, and is there an administrator role?
* How many moderators are there, and how is a report processed, including a possible appeal?

---

## Q6 — Privacy

> "Privacy: Which personal data are visible to whom, and how long are they stored?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* Personal and location data must be processed in compliance with the GDPR (Inception Document, § 3.4, C1, p. 3).
* Access is restricted to DHBW students; verification is done via the university e-mail address (Inception Document, § 3.4, C2, p. 3).
* The system shall persistently store users, rides, bookings, ratings and reports (Inception Document, § 3.2, p. 3).
* The sections on scope and open points mention data protection in general; concrete role/visibility rules or deletion periods are missing (Inception Document, § 3.4 and § 3.5, pp. 3–4).

### Decisions from the interview

* Q6 as a whole was left open in the interview (Interview with Team 7, 24 Nov 2026). The following individual points were decided:
* All data shall be stored on DHBW servers (Interview with Team 7, 24 Nov 2026).
* Users shall be verified via their DHBW e-mail address (Interview with Team 7, 24 Nov 2026).
* Individual ratings shall be visible only to their author; other users only see the average rating and the number of ratings (Interview with Team 7, 24 Nov 2026; see UI-9).
* No car make or model shall be shown in the profile or on the driver card (Interview with Team 7, 24 Nov 2026; see UI-7).
* No street addresses are stored for rides, only cities (Interview with Team 7, 24 Nov 2026; see Q1).

### Requirements not yet worked out

* Data categories and visibility per user role and booking status are not defined beyond the points above.
* There are no retention and deletion periods, no deletion rules for accounts or for data after the end of a ride, and no rule for backup/archiving.
* Data minimisation, consent/information, right of access or other concrete data protection processes are not described.
* Derivation: The requirement "GDPR-compliant" is a framework, but it does not replace concrete requirements on visibility and storage, which Q6 explicitly asks for.

### Open questions

* Which personal data are collected, and to whom are they visible?
* How long are the respective data stored, and when are they deleted?
* Which visibility applies in particular to ride details, profile data, chat messages and reports?
* What happens to an account when the student is exmatriculated?

---

## Q7 — Platform

> "Platform: Shall CampusRide be a web application, a mobile app, or both?"
> — Inception Document, § 3.5, p. 4

### Existing requirements

* As a usage assumption, all students are assumed to have a DHBW e-mail address and a smartphone or computer with internet access (Inception Document, § 3.4, A1, p. 3).
* The architecture is deliberately not defined in the inception (Inception Document, § 3.2, p. 3).
* The assignment paper places the later architecture and implementation work in Part II / Q1, but first requires a complete SRS in Part I (Project Part I, Section 1, pp. 1–2; §§ 2.1, 2.5 and 2.10, pp. 3, 5 and 7).

### Decisions from the interview

* CampusRide shall be a cross-platform mobile app for Android and iOS. There is no web application (Interview with Team 7, 24 Nov 2026).
* The app shall be written in Flutter (Interview with Team 7, 24 Nov 2026).
* Data shall be stored on DHBW servers (Interview with Team 7, 24 Nov 2026).

### Requirements not yet worked out

* The minimum supported Android and iOS versions are not defined.

### Open questions

* Which minimum Android and iOS versions must be supported?

---

## Ratings and suspension

This item is not one of the questions from the Inception Document, § 3.5. It results from the interview and is listed separately here.

### Existing requirements

* The system shall persistently store ratings and reports (Inception Document, § 3.2, p. 3).

### Decisions from the interview

* Driver and passengers shall rate each other after a ride (Interview with Team 7, 24 Nov 2026).
* A rating shall be given on a scale of 1 to 10 stars (Interview with Team 7, 24 Nov 2026).
* A user who receives too many bad ratings shall be suspended temporarily (Interview with Team 7, 24 Nov 2026).
* After confirmed non-payment, the person concerned is rated badly and suspended for a period (Interview with Team 7, 24 Nov 2026).

### Requirements not yet worked out

* The thresholds for an automatic suspension and the duration of a suspension are not defined.
* It is not defined until when after a ride a rating can be given.
* It is not defined what happens to the upcoming rides and bookings of a suspended user.

### Open questions

* From which threshold of bad ratings is a user suspended?
* How long does a suspension last, both after bad ratings and after non-payment?
* What happens to the upcoming rides and bookings of a suspended user?
* Until when after a ride can a rating be given?

---

## Further decisions from the interview

These decisions do not belong directly to one of Q1–Q7 but are part of the requirements.

* One user can be both driver and passenger; there are no separate accounts for the two roles (Interview with Team 7, 24 Nov 2026).
* The platform shall work like a marketplace (similar to eBay): users publish both ride offers and ride requests, and both can be filtered. No driver is asked directly for a ride; a passenger who finds no suitable offer publishes a ride request in the public list of requests instead (Interview with Team 7, 24 Nov 2026).
* Drivers shall be able to offer recurring rides in addition to single rides (Interview with Team 7, 24 Nov 2026).
* A ride shall count as completed only after it has been confirmed; it is not completed automatically at the departure time (Interview with Team 7, 24 Nov 2026).
* The app shall be available in English and German (Interview with Team 7, 24 Nov 2026).
* When creating an offer, the driver shall state how many pieces of luggage can be taken in total; ride requests state how many pieces of luggage are needed (Interview with Team 7, 24 Nov 2026).

### Conflict to clarify: seat requests

The Inception Document says that passengers "request a seat, which the driver accepts or declines" (Inception Document, § 3.2, p. 2) and lists the use case "Accept or decline seat request" (§ 6, p. 5). This can contradict the decision that no driver is asked directly for a ride. It must be clarified whether booking a seat on an offer is immediately binding or still needs the driver's confirmation (see Open_Questions.md, OQ-21).

## UI requirements from the interview

Team 7 asked Team 8 for a proposal for the user interface. The following requirements were agreed with Team 7 (Interview with Team 7, 24 Nov 2026). The wireframes in `2_ReqEng/wireframes/` illustrate them but are not part of this list.

* **UI-1 Navigation:** The app shall have a bottom tab bar with the tabs Rides (home), My Bookings and Chats. There shall be no separate notifications tab; notifications shall be shown as push notifications and as badges on the tabs.
* **UI-2 Profile access:** The profile shall be opened via an avatar button in the top-right corner of the main screens.
* **UI-3 Home:** The Rides tab shall show the list of all upcoming offers. Offers and requests shall be shown in two separate lists, between which the user switches with a toggle.
* **UI-4 Add button:** Each of the two lists shall have a "+" button that opens the form for a new offer or a new request.
* **UI-5 Filter:** Both lists shall be filterable by start city, destination city, date, time, maximum price, free seats, stop-overs (yes/no), minimum rating and type (offer/request).
* **UI-6 Sorting:** The lists shall be sorted by departure time.
* **UI-7 Detail page:** The detail page of an offer shall show a driver card with a Book button and a Chat button. The driver card shall not show a car make or model.
* **UI-8 Luggage:** Offers shall show how many pieces of luggage the driver can take; requests shall show how many pieces of luggage are needed.
* **UI-9 Profile:** The profile shall contain the user's own offers and requests, the ratings the user has written, the ride history, settings, log out and an entry to report a user. Other users shall see only the average rating and the number of ratings, not the individual ratings.
* **UI-10 Design:** The wireframes show layout only; branding (colours, logo) is not specified.

---

## Completeness check and classification

* The list above covers all seven Q items in the order and with the wording from the Inception Document, § 3.5, p. 4.
* For each item, explicit statements from the Inception Document are listed as existing requirements, and decisions from the interview with Team 7 on 24 Nov 2026 are listed separately with their source. Missing details are named separately as not yet worked out and/or as open questions. Derivations are explicitly marked and not phrased as decisions.
* After the interview, Q1, Q2 and Q7 are decided, Q4 and Q5 are decided in principle with details open, and Q3 and Q6 are still open.
* The Inception Document itself marks the detailed rules as deliberately open (§ 3.2, p. 2) and requires them to be clarified in requirements engineering (§ 3.5, p. 4). This analysis therefore contains no invented answers; all new decisions come from the interview with Team 7.
* Among other things, the assignment paper requires functional and non-functional requirements, use cases, assumptions/constraints and supporting documentation for the SRS; it also requires ambiguities, gaps and contradictions to be clarified (Project Part I, §§ 2.4–2.6, pp. 4–6; § 2.10, p. 7). The remaining open questions are therefore open specification work.

## Sources

1. CampusRide – Inception Document, Requirement Rebels (Team 7), Version 1.1, 24 Nov 2026. References in the text by section, table/ID and PDF page.
2. Software Engineering – Program Design Part I, Prof. Dr. Christian Braunagel. References in the text by section and PDF page.
3. Interview with Team 7 (Requirement Rebels), 24 Nov 2026, oral; participants Tim and Fridolin (Team 8). Notes in `2_ReqEng/history.md`.
