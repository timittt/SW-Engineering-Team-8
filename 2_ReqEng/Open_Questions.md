# CampusRide – Open Questions

**Status:** after the interview with Team 7 on 24 Nov 2026.
**Purpose:** All questions that are still open and must be clarified with Team 7 before the SRS is finalised (handover 1 Dec 2026). The analysis behind them is in [Requirements_Analysis_Q1-Q7.md](Requirements_Analysis_Q1-Q7.md).

**Already decided in the interview (no longer open):** Q1 Matching, Q2 Cost contribution (driver sets the price, no upper limit), Q7 Platform (incl. English and German); the basic decisions for Q4 (encrypted in-app chat) and Q5 (moderation by the StuV); ratings on a scale of 1 to 10 stars; recurring rides; a ride is completed only after confirmation.

| ID | Topic | Open question | Answer Team 7 |
| --- | --- | --- | --- |
| OQ-1 | Q3 Cancellations | Until when may a driver cancel a ride or a passenger cancel a booking without particular consequences? |schlechte Bewertung 1tag  |
| OQ-2 | Q3 Cancellations | Which consequences apply to late or repeated cancellations (e.g. note on the profile, bad rating, suspension)? |bad rating blocked an dmoderator  |
| OQ-3 | Q3 Cancellations | Which affected persons receive a notification for which cancellation? | |
| OQ-4 | Q4 Communication | Is there one 1:1 chat between the driver and each passenger, or one group chat per ride? | one n done chats|
| OQ-5 | Q4 Communication | From when can users chat: already before a booking, or only after the booking is confirmed? | booking chat, aber es muss genehmigt. Aber es sollte auch direkt einen chat geben  |
| OQ-6 | Q4 Communication | Does "encrypted" mean end-to-end encryption or only transport/server encryption? | end zu en dverschlüsseng  |
| OQ-7 | Q4 Communication | How long are chat messages stored? | daten 1-2 wovhen  |
| OQ-8 | Q4 Communication | How can users report abusive chat messages? |report button moderatpr zugriff auf alls |
| OQ-9 | Q5 Moderation | Which measures can moderators take besides suspension, and under which conditions? | keine sanderen sachen |
| OQ-10 | Q5 Moderation | Who appoints the moderators within the StuV, how is their authorisation managed, and is there an administrator role? | only stu |
| OQ-11 | Q5 Moderation | How many moderators are there, and how is a report processed, including a possible appeal? | |
| OQ-12 | Q6 Privacy | Which personal data are collected, and to whom are they visible? | only seen as needed |
| OQ-13 | Q6 Privacy | How long are the respective data (rides, bookings, ratings, reports, accounts) stored, and when are they deleted? |chats are delted after 1-2 weeks, drives are deleted  |
| OQ-14 | Q6 Privacy | Which visibility applies in particular to ride details, profile data, chat messages and reports? | |
| OQ-15 | Q6 Privacy | What happens to an account when the student is exmatriculated? | not important |
| OQ-16 | Q7 Platform | Which minimum Android and iOS versions must be supported? |jetzige sicherheiupated |
| OQ-17 | Ratings and suspension | From which threshold of bad ratings is a user suspended automatically? | zeitlich sperrung wenn man über eine zeit |
| OQ-18 | Ratings and suspension | How long does a suspension last, both after bad ratings and after non-payment? | bei report gibt es vorgefertige strafen je nach tat |
| OQ-19 | Ratings and suspension | What happens to the upcoming rides and bookings of a suspended user? |there er cancceld  |
| OQ-20 | Luggage | Does a passenger state their luggage pieces when booking, and is the driver's free luggage capacity reduced per booking like the seats? |ys  |
| OQ-21 | Booking | No driver is asked directly for a ride (marketplace principle). Is booking a seat on an offer therefore immediately binding, or must the driver still confirm each booking, as the Inception Document (§ 3.2, p. 2) describes? | confirm |
| OQ-22 | Booking | What happens to existing bookings when the driver changes the time or the price of a ride afterwards? |possible and everyone gets a notifcation (mit zeitfesntwe) |
| OQ-23 | Booking | Who confirms that a ride is completed: the driver, the passengers, or both? |beide, keine konsquenzen |
| OQ-24 | Ratings | Until when after a ride can a rating be given? | same as chat|
| OQ-25 | Access | Are all DHBW locations and their e-mail domains admitted, or only one location? | all mit dhbw email |
| OQ-26 | Performance | How many registered and simultaneously active users are expected? | es muss eine umfrage es müssen genug sein |
| OQ-27 | Scope | Which functions are mandatory for the prototype (one quarter, four developers), and which can follow in a later release? |fahrten bereitsellen, buchen, (in app chat,) not essiantial ratings. Bearbeiten und cancellen wichtig.  |

## Sources

1. CampusRide – Inception Document, Requirement Rebels (Team 7), Version 1.1, 24 Nov 2026, § 3.5, p. 4 (Q1–Q7).
2. Interview with Team 7 (Requirement Rebels), 24 Nov 2026, oral; notes in `2_ReqEng/history.md`.
