# Barbershop Booking App - Product Concept

Design concept for a booking and payments app for a barbershop with several barbers. One app serves both sides: clients book and pay, barbers manage their schedule, clients and earnings.

**Live mockup:** https://migueldiegues24.github.io/barbershop-booking-app/

> The interface is in Portuguese. All names, addresses and figures in the mockup are fictional.

## What it covers

**Client side**
- Sign in with email, phone, Apple or Google; phone number confirmed by SMS
- Barbershop home with the next bookings and a one-tap "repeat last cut"
- Choose a barber (or "anyone"), services, day and time, then pay in the app
- Reschedule or cancel, with automatic refunds when cancelled in time

**Barber side**
- Daily overview and a live agenda per barber
- Manual bookings for phone and walk-in clients
- Client list with visit history and notes
- Monthly earnings per barber, split by prepaid, plans and in-store payments
- Services, team permissions and booking rules, all configurable without a developer

**Tablet**
- Shared agenda with all barbers side by side, plus wide-screen views for clients, payments and settings

## Product decisions

- **"Anyone" option:** the client sees the free slots of every barber combined. If two barbers are free at the same time, the booking goes to the one with fewer clients that day, to balance the workload.
- **Money goes straight to each barber:** every payment is routed to the account of the barber who does the cut, so there is no manual splitting at the end of the month.
- **Subscription plans:** clients on a weekly or fortnightly plan get a fixed day, time and barber booked for the whole year, skipping days off and holidays, with exceptions for skipped weeks or pauses.
- **Cancellation rules in the product, not in conversation:** full automatic refund up to a set number of hours before the booking; late cancellations and no-shows stay with the barber.
- **Some services are phone-only:** longer services such as colouring are hidden from the client app and booked by the barbers.
- **Privacy by role:** clients only see their own data and each barber only sees their own earnings.

## Planned stack

- React Native with Expo (iOS, Android and tablet from one codebase)
- Supabase (PostgreSQL, authentication, row-level security for per-role access)
- eupago for MB WAY, Apple Pay and Google Pay, with payment confirmation via webhooks
- Push notifications and SMS reminders

## Status

Design concept. The mockup shows the main screens and flows; the app itself has not been built.

## Author

Miguel Diegues — [LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/migueldiegues24)
