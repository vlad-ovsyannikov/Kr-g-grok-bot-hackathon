# Demo script — Pani Halina’s day

For the presenter and judges. Wrocław hackathon, invented demo parent.
This is a prototype of the experience, not an alarm and not a medical service.

## Where she sits

Pani Halina (the presenter, playing her) opens the **1:1 chat with Krąg** only. Voice is welcome: she can start voice mode and talk; Krąg treats what she says as the conversation. Suggested taps are a backup.

She does not join the care-team group. That group is backstage: Informator, Rodzina, Kronika, Apteczka, and Strażnik. Family (Ania, Marek, Zosia, Kuba) stay outside the app; outbound notes to them are simulated.

Speak as Halina in polite Polish.

## Beat 0 — First meeting (voice)

Krąg greets her and does not list features:

> Dzień dobry, Pani Halino. Cieszę się, że możemy się poznać. Jestem Krąg — będę codziennie w pobliżu, żeby zagadać rano, przypomnieć o tabletce i oddzwonić do rodziny, gdy Pani tego potrzebuje. Dziś nigdzie się nie śpieszymy. Możemy chwilę porozmawiać, żebym lepiej Panią poznała?

Then five questions, one at a time: how to address her; who is close and who to call first; morning and evening tablet times; what she enjoys talking about; what not to ask.

After that, the offer of help:

> Od jutra mogę rano zagadać, powiedzieć jaka jest pogoda, przypomnieć o białej tabletce i zapytać, czy wszystko dobrze. Jeśli Pani powie, że chce telefon, poproszę Anię. Czasem pokażę zdjęcie od rodziny i zapytam o jedno wspomnienie — tylko jeśli będzie Pani miała na to ochotę. A dziś, czy mogę jeszcze jakoś pomóc, czy wolimy skończyć na teraz?

Full wording: `first-meeting/session.md`. Notes go to `first-meeting/portrait.json`.

## Beat 1 — Morning check-in

Krąg (already drafted and approved by Strażnik), spoken as part of an ongoing conversation, not as a task list:

> Dzień dobry, Pani Halino. Dziś 2 stopnie i mgła. Imieniny obchodzi Marek. Pora na poranną tabletkę, biała, jedna, jak na recepcie. Czy wszystko dobrze i czy poranne leki wzięte?

If she has already met Krąg, add one remembered thread when there is one, for example a phrase from Beat 0.

Suggested taps: **Tak, wszystko dobrze** · **Proszę o telefon**

If a judge asks what happened backstage: Informator read IMGW (2.3°C at station 12424, hour 19) and the dense-fog warning for Wrocław; the name day comes from `namedays.csv` (Marek on 11-05); Apteczka copied the words *biała* and *jedna* from the mock schedule, and did not calculate a dose; Strażnik approved a fact-only greeting with no advice and no streak language.

## Beat 2 — Happy path (tap “Tak, wszystko dobrze”)

What she should see next, once the flow is wired:

1. A short thanks. No score, no streak, no comment on a missed day.
2. A family photo (from Zosia or Kuba, handed over by Rodzina) — the “photo behind the tap.”
3. One memory question, in order, never repeated after an answer:

> Jak wyglądała Pani droga do szkoły?

Sample answer she can give: *Szłam przez park, a potem długą aleją. Pamiętam kasztany przy bramie.*

Krąg listens and does not invent extra memoir details. Kronika stores her words. The interviewer adds “kasztany przy bramie” (or whatever she said) to unfinished threads. She may skip; the skip is not mentioned.

## Beat 3 — Call path (tap “Proszę o telefon”)

Krąg answers briefly and kindly, without medical questions.

Backstage, Rodzina prepares a simulated request for **Ania** (daughter, Wrocław, first on the call rota). Marek in Berlin is next if she cannot. Quiet hours for both are 21:00–08:00 Europe/Warsaw. Family email and phone are placeholders; the send is written to `outbox/` as simulated, never actually mailed or texted.

## Beat 4 — Evening tablet (same day, later)

Krąg (already drafted and approved):

> Pora na wieczorną tabletkę (biała, jedna, jak na recepcie).

Tap: **Wzięłam**

Stock note for the presenter only, never said as advice to her: 20 tablets counted on the morning of 5 November before today’s doses; two a day; runs out on 14 November.

## Beat 5 — Optional, if she asks about the doctor

Not a visit day today. Next booked visit: Thursday 12 November 2026 at 10:30, ortopeda in Wrocław, Marek driving. Say only those facts. No clinic or treatment advice.

## What not to do

- Do not present the care-team group as her conversation.
- Do not calculate a dose, or say what happens if a tablet is missed.
- Do not invent weather, air, photos, news, or memoir details.
- Do not send email or SMS to the placeholder family contacts.

## Build status at time of writing (5 November 2026, evening)

Ready to show as copy: first-meeting script, companion style, morning greeting, evening tablet reminder, Strażnik approval notes, question bank (12), simulated family-contact mode.

Not yet wired for a live play-through: photo appearing in the 1:1 chat, memoir chapter after her answer, live call-me handoff into the simulated outbox, generated weather avatar, and the 07:00 / 09:00 routines.
