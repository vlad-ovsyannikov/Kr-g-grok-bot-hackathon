# Demo script — Pani Halina's day

For the presenter and judges. Wrocław hackathon, invented demo parent.
This is a prototype of the experience, not an alarm and not a medical service.

## Where she sits

Pani Halina (the presenter, playing her) opens the **1:1 chat with Krąg** only.

She does not join **Zespół Krąg**. That group is backstage: Informator, Rodzina, Kronika, Apteczka, and Strażnik. Family (Ania, Marek, Zosia, Kuba) stay outside the app; outbound notes to them are simulated.

Speak as Halina in polite Polish. Tap the suggested replies when they appear.

## Beat 1 — Morning check-in

Krąg (already drafted and approved by Strażnik):

> Dzień dobry, Pani Halino. Dziś 2 stopnie i mgła. Imieniny obchodzi Marek. Pora na poranną tabletkę, biała, jedna, jak na recepcie. Czy wszystko dobrze i czy poranne leki wzięte?

Suggested taps: **Tak, wszystko dobrze** · **Proszę o telefon**

If a judge asks what happened backstage: Informator read IMGW (2.3°C at station 12424, hour 19) and the dense-fog warning for Wrocław; the name day comes from `namedays.csv` (Marek on 11-05); Apteczka copied the words *biała* and *jedna* from the mock schedule, and did not calculate a dose; Strażnik approved a fact-only greeting with no advice and no streak language.

## Beat 2 — Happy path (tap "Tak, wszystko dobrze")

What she should see next, once the flow is wired:

1. A short thanks. No score, no streak, no comment on a missed day.
2. A family photo (from Zosia or Kuba, handed over by Rodzina) — the "photo behind the tap."
3. One memory question, in order, never repeated after an answer:

> Jak wyglądała Pani droga do szkoły?

Sample answer she can give: *Szłam przez park, a potem długą aleją. Pamiętam kasztany przy bramie.*

Krąg listens and does not invent extra memoir details. Kronika stores her words. She may skip; the skip is not mentioned.

## Beat 3 — Call path (tap "Proszę o telefon")

Krąg answers briefly and kindly, without medical questions.

Backstage, Rodzina prepares a simulated request for **Ania** (daughter, Wrocław, first on the call rota). Marek in Berlin is next if she cannot. Quiet hours for both are 21:00–08:00 Europe/Warsaw. Family email and phone are placeholders; the send is written to `outbox/` as simulated, never actually mailed or texted.

## Beat 4 — Evening tablet (same day, later)

Krąg (already drafted and approved):

> Pora na wieczorną tabletkę (biała, jedna, jak na recepcie).

Tap: **Wzięłam**

Stock note for the presenter only, never said as advice to her: 20 tablets counted on the morning of 5 November before today's doses; two a day; runs out on 14 November.

## Beat 5 — Optional, if she asks about the doctor

Not a visit day today. Next booked visit: Thursday 12 November 2026 at 10:30, ortopeda in Wrocław, Marek driving. Say only those facts. No clinic or treatment advice.

## What not to do

- Do not present Zespół Krąg as her conversation.
- Do not calculate a dose, or say what happens if a tablet is missed.
- Do not invent weather, air, photos, or memoir details.
- Do not send email or SMS to the placeholder family contacts.

## Build status at time of writing (5 November 2026, evening)

Ready to show as copy: morning greeting, evening tablet reminder, Strażnik approval notes, question bank (12), simulated family-contact mode.

Not yet wired for a live play-through: photo appearing in the 1:1 chat, memoir chapter after her answer, live call-me handoff into the simulated outbox, generated weather avatar, and the 07:00 / 09:00 routines.
