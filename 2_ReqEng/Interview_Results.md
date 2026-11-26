# CampusRide – Interview Results (Team 7)

Results of the elicitation interviews that Team 8 (Tim, Fridolin) held with Team 7 (Requirement Rebels) about their idea "CampusRide".

| | Interview 1 | Interview 2 |
| --- | --- | --- |
| **Date** | 24 Nov 2026 | 26 Nov 2026 |
| **Technique** | Interview / walkthrough of the Inception Document (v1.1), questions Q1–Q7 (§ 3.5, p. 4) | Follow-up interview along the list of open questions OQ-1 to OQ-27 |
| **Form** | Oral; notes in [history.md](history.md) | Oral (WhatsApp audio, approx. 15 min); cleaned German transcript in [interviewtransscript_de.md](interviewtransscript_de.md), summarised here |
| **Result** | Q1, Q2, Q7 decided; Q4, Q5 decided in principle; Q3, Q6 open | Answers to almost all open questions; suspension thresholds are still to be clarified by Team 7 (Section 4) |

English transcript and summary of interview 2: [interviewtransscript.md](interviewtransscript.md). Detailed analysis per question: [Requirements_Analysis_Q1-Q7.md](Requirements_Analysis_Q1-Q7.md). List of open questions with answers: [Open_Questions.md](Open_Questions.md). SRS handover: 1 Dec 2026.

**Note on interview 2:** The decisions are based on the cleaned transcript (unclear passages were corrected after consultation). Where it differs from the first, raw speech-to-text version or from Tim's quick notes in Open_Questions.md, the cleaned transcript is used.

## 1. Status of Q1–Q7

| Q | Topic | After interview 1 | After interview 2 |
| --- | --- | --- | --- |
| Q1 | Matching | **Decided** | Decided |
| Q2 | Cost contribution | **Decided** | Decided |
| Q3 | Cancellations | Open | **Decided** (D-16 to D-19) |
| Q4 | Communication | Decided in principle | **Decided** (D-20 to D-23) |
| Q5 | Moderation | Decided in principle | **Decided** (D-24 to D-27) |
| Q6 | Privacy | Open | **Decided** (D-28 to D-31) |
| Q7 | Platform | **Decided** | Decided, incl. supported OS versions (D-32) |

## 2. Decisions from interview 1 (24 Nov 2026)

| ID | Topic | Decision |
| --- | --- | --- |
| D-1 | Q1 Matching | A ride offer contains only start city, destination city, number of seats, a checkbox "willing to make stop-overs" and the price. No street addresses or detailed routes. |
| D-2 | Q1 Matching | The number of free seats is updated live when bookings are made or cancelled. |
| D-3 | Q2 Cost | The driver sets the price per seat. This replaces the "suggested contribution" of the Inception Document (§ 3.2, p. 2). |
| D-4 | Q2 Cost | There is no upper limit for the price. |
| D-5 | Q2 Cost | Payment is not handled in the app; passengers pay the driver privately. |
| D-6 | Q4 Communication | Driver and passengers coordinate via a chat integrated into the app. |
| D-7 | Q4 Communication | The chat is encrypted. |
| D-8 | Q5 Moderation | Moderation is done by the StuV (student representation). |
| D-9 | Q5 Moderation | In case of non-payment the driver can contact the moderators; the person concerned is rated badly and suspended for a period. |
| D-10 | Q6 Privacy | All data are stored on DHBW servers. |
| D-11 | Q6 Privacy | Users are verified via their DHBW e-mail address. |
| D-12 | Q7 Platform | CampusRide is a cross-platform mobile app for Android and iOS, written in Flutter. There is no web application. |
| D-13 | Accounts | One account can act as both driver and passenger; there are no separate accounts. |
| D-14 | Ratings | Driver and passengers rate each other after a ride. |
| D-15 | Ratings | Too many bad ratings lead to a temporary suspension. |

Further decisions recorded after interview 1 (marketplace principle, recurring rides, star ratings (changed to 1–5 stars in interview 2, see D-43), English and German, luggage pieces, UI concept UI-1 to UI-10) are listed in [Requirements_Analysis_Q1-Q7.md](Requirements_Analysis_Q1-Q7.md).

## 3. Decisions from interview 2 (26 Nov 2026)

| ID | Answers | Topic | Decision |
| --- | --- | --- | --- |
| D-16 | OQ-1 | Q3 Cancellations | Drivers and passengers can cancel without consequences until about one day (24 hours) before departure. |
| D-17 | OQ-2 | Q3 Cancellations | Later cancellations have consequences for both drivers and passengers, because a cancelling passenger also takes the seat away from someone else. |
| D-18 | OQ-2 | Q3 Cancellations | The consequence of a late cancellation is a worse rating. A user who repeatedly cancels at short notice gets a worse rating each time until they are eventually suspended. |
| D-19 | OQ-3 | Q3 Cancellations | On every cancellation, all participants of the ride receive a notification. |
| D-20 | OQ-4 | Q4 Communication | There is a separate 1:1 chat between the driver and each passenger; there is no group chat per ride. |
| D-21 | OQ-5 | Q4 Communication | When a passenger sends a booking request, the chat with the driver opens. Users can also chat at any time before that, e.g. to ask questions about the booking. |
| D-22 | OQ-6 | Q4 Communication | The chat is end-to-end encrypted (like WhatsApp). The security of the chat is the responsibility of the DHBW. |
| D-23 | OQ-8 | Q4 Communication | The chat has a report function. When a user reports, the chat is transferred to the moderators. This is compatible with D-22: the moderators do not read chats in general, they only receive a chat that a chat partner has reported. |
| D-24 | OQ-9 | Q5 Moderation | Moderators can only suspend users; they have no other measures. A suspended user cannot take part in rides any more. |
| D-25 | OQ-10 | Q5 Moderation | Moderation is handed over completely to the StuV as an institution; the moderators are StuV members. |
| D-26 | OQ-11 | Q5 Moderation | Appeals, and complaints about moderators, are handled by the StuV itself, outside the app. |
| D-27 | OQ-18 | Q5 Moderation | When reporting, the user selects a main category (e.g. abuse, non-payment, risky driving) and can optionally add a text. The exact categories are still to be defined. |
| D-28 | OQ-12, OQ-14 | Q6 Privacy | Need-to-know principle: every user sees only what they must see. Data are visible only to the moderators and to the participants of the respective chat; a chat reaches the moderators when it is reported. Of the other users, only the profile is visible. |
| D-29 | OQ-7, OQ-13 | Q6 Privacy | Chats and bookings are deleted 14 days after the ride. If a payment is still open and must be proven, they are kept for 30 days. No statistics per account are stored (who rode with whom is not relevant). The ride history in the profile (UI-9) shows a user's rides only until they are deleted. |
| D-30 | OQ-15 | Q6 Privacy | Exmatriculation is not a use case. The e-mail verification is mainly meant to prevent bots and mass accounts. |
| D-31 | OQ-25 | Access | All students with a DHBW e-mail address of DHBW Ravensburg (incl. Campus Friedrichshafen) are admitted. |
| D-32 | OQ-16 | Q7 Platform | The app supports all Android versions that are still supported, i.e. still receive security updates. (iOS was not discussed; the same rule is assumed.) |
| D-33 | OQ-17 | Ratings | A user is not suspended after a single bad rating, only if they are rated badly consistently over a certain number of rides. Both temporary and permanent suspensions are possible. Only users who took part in the ride can rate. |
| D-34 | OQ-18 | Ratings | Non-payment weighs more heavily than a simple bad rating. |
| D-35 | OQ-19 | Ratings | When a driver is suspended, all of their rides within the suspension period are cancelled automatically, and all affected passengers are notified. |
| D-36 | OQ-24 | Ratings | A rating can be given until two weeks after the ride, i.e. as long as the chat exists. After the chat is deleted, no rating is possible. |
| D-37 | OQ-20 | Luggage | When booking, a passenger states whether they bring luggage. Luggage is not a reason to block a booking; details are clarified in the chat with the driver. |
| D-38 | OQ-21 | Booking | Booking a seat is not immediately binding: the driver must confirm each booking (as in Inception Document § 3.2, p. 2). |
| D-39 | OQ-22 | Booking | The driver can change the time of a ride afterwards; all participants are notified. If the driver changes something, the passengers can withdraw from the booking free of charge and without consequences. |
| D-40 | OQ-23 | Booking | "Ride started" and "Ride completed" are confirmed by one of the two persons (driver or passenger). This is mainly for bookkeeping; if nobody confirms, there are no consequences. No fixed arrival time is stated, only an estimated arrival time. |
| D-41 | OQ-26 | Performance | The number of users is unclear; it would have to be found out with a survey, which will be difficult. |
| D-42 | OQ-27 | Scope | **Must for the prototype:** offer rides; the complete booking flow, i.e. posting a ride request ("from A to B") or applying for an offered ride, and the driver accepting or rejecting requests; editing and cancelling. **Should (medium):** in-app chat ("important, but it also works without"). **Later version:** ratings and the consequences that follow from them (e.g. penalties for late cancellations). |
| D-43 | – | Ratings | Ratings are given on a scale of 1 to 5 stars. This replaces the earlier 1–10 stars. |

## 4. Still open or to confirm

| ID | Topic | What is still open |
| --- | --- | --- |
| OQ-17, OQ-18 | Ratings and suspension | Below which average rating, after how many rides and for how long a user is suspended (temporarily or permanently). Team 7 clarifies this internally. |
| OQ-18 | Reports | The exact report categories. |
| OQ-11 | Moderation | Number of moderators. |
| OQ-22 | Booking | What happens when the driver changes the price afterwards. |
| OQ-26 | Performance | Expected user numbers. |
| New | Ratings | The scale changed from 1–10 to 1–5 stars (D-43); the SRS and Requirements_Analysis_Q1-Q7.md must be updated. |

## 5. Changes compared to the Inception Document

* **Price:** The system no longer suggests a contribution; the driver sets the price (D-3).
* **Route data:** Only cities are stored, no intermediate stops or addresses (D-1).
* **Platform:** Q7 is answered as mobile only (D-12).
* **Booking flow:** The driver still confirms each booking (D-38), as in the Inception Document; OQ-21 is therefore resolved without a conflict.
* **Moderation:** Moderators can only suspend (D-24); the Inception Document left the measures open.

## Sources

1. Interview 1 with Team 7 (Requirement Rebels), 24 Nov 2026, oral; participants Tim and Fridolin (Team 8). Notes in `2_ReqEng/history.md`.
2. Interview 2 with Team 7 (Requirement Rebels), 26 Nov 2026, oral (WhatsApp audio); cleaned German transcript in `2_ReqEng/interviewtransscript_de.md`, English translation in `2_ReqEng/interviewtransscript.md`.
3. CampusRide – Inception Document, Requirement Rebels (Team 7), Version 1.1, 24 Nov 2026.
