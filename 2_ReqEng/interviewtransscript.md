# CampusRide – Interview 2 with Team 7: Transcript (English)

| | |
| --- | --- |
| **Date** | 26 Nov 2026 |
| **Customer** | Team 7 (Requirement Rebels), idea "CampusRide" |
| **Requirements engineers** | Team 8: Tim, Fridolin |
| **Technique** | Follow-up interview along the open questions OQ-1 to OQ-27 ([Open_Questions.md](Open_Questions.md)) |
| **Recording** | WhatsApp audio in German, approx. 15 minutes |

English translation of the cleaned German transcript ([interviewtransscript_de.md](interviewtransscript_de.md)). Unclear passages were corrected after consultation or left out. Time stamps are approximate. The structured decisions (D-16 to D-43) are in [Interview_Results.md](Interview_Results.md).

## Summary of the decisions

- **Cancelling:** without consequences until about one day before; after that a worse rating, for drivers *and* passengers. All participants are notified.
- **Booking:** the passenger sends a request, the chat opens, and the driver must confirm every request.
- **Chat:** 1:1 chats (driver and passenger), no group chat; end-to-end encrypted; the DHBW is responsible for security.
- **Data:** chats and bookings are deleted after 14 days, or after 30 days if a payment is still open. No ride history or statistics per account.
- **Moderation:** in the long term by the StuV, including appeals. Moderators can only suspend; suspended users cannot take part in rides any more.
- **Ratings:** 1–5 stars, only after a shared ride, up to 14 days after it. Thresholds and duration of suspensions: **still to be clarified within Team 7**.
- **Target group:** everyone with a DHBW e-mail address (Ravensburg and Friedrichshafen). Android: all versions that are still supported.
- **Prototype scope:** offering rides, booking flow with request and approval, editing, cancelling. Chat of medium importance, ratings later.

---

## [00:00] Cancelling

**Question:** Is there a point in time until which you can cancel without consequences, e.g. if you cancel two minutes before?

**Answer:** There should be consequences for passengers too, because they take a seat away from others, so for both: a worse rating. But something can always come up, so there is a time window: cancelling until about one day before is no problem.

Someone who cancels at short notice more often gets a worse rating with every ride until they are eventually suspended.

When a ride is cancelled, all participants always receive a notification.

## [01:30] Chat and booking flow

**Question:** Is there a group chat, e.g. for a driver with three passengers and several intermediate stops, or does everyone have a single chat with the driver?

**Answer:** The driver coordinates everything via single chats.

**Question:** Is the booking only fixed after the chat, or do you book and then end up in the chat?

**Answer:** When a passenger sends a request, the chat opens. The booking is only fixed when the driver approves the request. But chatting should be possible at any time, also before, e.g. for questions about the booking.

The DHBW is responsible for the security of the chat.

**Encryption:** This must be decided now because it is part of the app: end-to-end encryption, like WhatsApp.

## [03:00] Data retention and moderation

**Question:** Are the chat data deleted after the ride?

**Answer:** They stay stored for a while in case complaints come in and the chat log has to be accessed, about one to two weeks; after that they are deleted.

There is a report button in the chat. The moderator has access to all logs anyway.

Apart from suspending, a moderator can't really do anything. A suspended user cannot take part in rides any more.

In the long term, moderation is handed over completely to the StuV; it needs an institution that is there permanently. Appeals are also handled by the StuV.

## [04:30] Visibility and storage

Misconduct by moderators is also handled by the StuV.

Data are only visible to the moderators and to the participants of the respective chat; everyone only sees what they absolutely need to see.

**Question:** The bookings are stored on the DHBW server. Are they deleted together with the chats, or is there a ride history per account (e.g. how often someone cancelled or was late)?

**Answer:** No statistics are stored. Who rode with whom and when is not relevant; the bookings are deleted together with the chats, after 14 days.

If a payment is still open and it has to be proven that it was paid: 30 days.

## [06:00] Accounts and platform

During the ride, only the profile is visible.

Exmatriculation is not a use case. The verification via the DHBW e-mail address mainly ensures that no bots register and create masses of accounts.

**Android version:** all versions that are still supported (receive security updates).

## [07:30] Ratings and suspension

**Question:** We said that a user is suspended at some point if their rating is bad. For how long, and from which threshold?

**Answer:** Ratings are given with 1 to 5 stars. You can only rate if you rode along, so not everyone can rate arbitrarily. A user should not be suspended right after one bad rating, but only if they are rated badly consistently over a certain number of rides. Both temporary and permanent suspensions are conceivable.

**Open:** Team 7 clarifies internally below which average, after how many rides and for how long a user is suspended.

## [09:00] Reports, consequences of a suspension, luggage

Non-payment weighs more heavily than a simple bad rating.

When reporting, you select a main category (e.g. abuse, non-payment, risky driving) and can optionally write a text. The exact categories are still to be defined.

If a driver is suspended, all of their rides in the suspension period are cancelled automatically and the passengers are notified.

**Luggage:** When booking, you state whether you bring luggage. The occupied seats count up automatically until the ride is full. Luggage is not a reason to prevent a booking, though; for that, users are referred to the chat with the driver.

## [10:30] Confirmations and changes

The driver must confirm every request: you can book an offered ride, but only the driver's approval makes it fixed.

Times can be changed afterwards; all participants then receive a notification. If the driver changes something, the passengers can withdraw free of charge.

## [12:00] Start of the ride, arrival, rating deadline, target group

"Ride started" and "Ride completed" should be confirmed by one of the two persons. This is mainly for bookkeeping; if nobody does it, there are no consequences.

No fixed arrival time is stated, only an approximate one (estimated time).

**Question:** How long after the ride can you still give a rating?

**Answer:** Two weeks, as long as the chat exists. Once the chat is deleted, no rating is possible any more.

**Target group:** everyone with a DHBW e-mail address, i.e. Ravensburg and Friedrichshafen.

**Expected number of users:** Unclear; this would have to be found out with a survey, which will be difficult.

## [13:30] Scope for the prototype

What matters is a basic, working app. The core functions:

- offering rides
- the complete booking flow
- posting a ride request yourself ("I want to go from A to B") or applying for an offered ride
- the driver can accept or reject requests

The chat is something in between: important, but if necessary it also works without. Ratings and similar things are not essential for the first prototype. Editing and cancelling, on the other hand, are important. The functions that follow from them come later.

## [15:00] End

No further questions.
