# CampusRide – Summary of Interview 2 (26 Nov 2026)

**From:** Team 8 (Tim, Fridolin), requirements engineering for CampusRide
**To:** Team 7 (Requirement Rebels)
**Subject:** Results of our follow-up interview on the open questions

Thank you for the interview. Below is our summary of what we agreed. Please check it and tell us if anything is wrong or missing. We will use these results in the SRS (handover 1 Dec 2026).

## Cancellations

* Drivers and passengers can cancel without consequences until about one day before departure.
* Later cancellations have consequences for both drivers and passengers: a worse rating. A user who cancels at short notice repeatedly gets a worse rating each time until they are suspended.
* All participants of a ride are notified of every cancellation.

## Booking and chat

* When a passenger sends a booking request, the chat with the driver opens. The booking is only fixed when the driver approves it.
* Users can chat at any time, also before a booking.
* There is a separate 1:1 chat between the driver and each passenger, no group chat.
* The chat is end-to-end encrypted (like WhatsApp). The DHBW is responsible for its security.
* The chat has a report button; a reported chat is transferred to the moderators.
* The driver can change the time of a ride afterwards. All participants are notified, and the passengers can withdraw free of charge.
* "Ride started" and "Ride completed" are confirmed by the driver or a passenger. This is for bookkeeping only; if nobody confirms, there are no consequences.
* No fixed arrival time is stated, only an estimated arrival time.
* When booking, a passenger states whether they bring luggage. Luggage never blocks a booking; details are clarified in the chat.

## Moderation

* In the long term, moderation is handed over completely to the StuV, including appeals and complaints about moderators.
* Moderators can only suspend users. A suspended user cannot take part in rides any more.
* When reporting, the user selects a main category (e.g. abuse, non-payment, risky driving) and can add an optional text.

## Ratings and suspension

* Ratings are given with **1 to 5 stars** (instead of 1 to 10 as noted before). Only users who took part in the ride can rate.
* Ratings can be given for two weeks after the ride, as long as the chat exists.
* A single bad rating does not lead to a suspension, only consistently bad ratings over a certain number of rides. Temporary and permanent suspensions are possible.
* Non-payment weighs more heavily than a simple bad rating.
* When a driver is suspended, all of their rides in the suspension period are cancelled automatically, and the passengers are notified.

## Privacy

* Every user sees only the data they need to see. Data are visible only to the moderators and to the participants of the respective chat.
* Chats and bookings are deleted 14 days after the ride, or after 30 days if a payment is still open and must be proven.
* No statistics per account are stored.
* Exmatriculation is not a use case. The DHBW e-mail verification mainly prevents bots and mass accounts.

## Platform, access and users

* The app supports all Android versions that still receive security updates.
* All students with a DHBW e-mail address of Ravensburg or Friedrichshafen can use the app.
* The number of users is unclear and would have to be found out with a survey.

## Scope of the prototype

* **Must:** offering rides; the complete booking flow (posting a ride request or applying for an offered ride, and the driver accepting or rejecting it); editing and cancelling.
* **Medium priority:** in-app chat.
* **Later version:** ratings and the consequences that follow from them.

## Still to be clarified by you

1. Below which average rating, after how many rides and for how long is a user suspended (temporarily or permanently)?
2. Which report categories are there exactly?
3. Does the iOS app follow the same rule as Android (all versions that still receive security updates)?
4. What happens to existing bookings if the driver changes the price afterwards?
