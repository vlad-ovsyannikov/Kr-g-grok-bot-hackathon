# Krąg

**Krąg** ("circle" in Polish) is a care team of Bots for one ageing parent. She talks only to Krąg, in chat or voice; the other five bots work in the team group. Family stays outside the app.

This is a prototype of the experience, not an alarm or a medical service. The demo family is invented. There is no real health data.

## For her

- A morning check-in with real weather and air (no invented figures), today's name day, and a tablet prompt
- A morning picture that changes with the weather
- Simple taps or her own words: she's well, she took the tablet, or she wants a call
- A family photo after she answers (the photo behind the tap)
- One memory question a day, then a memoir built from her answers — no invented details
- Tablet reminders at her times, described only as on the mock prescription (for the demo: biała, jedna, at 09:00 and 19:00)
- A visit reminder when there is one (next: Thursday 12 November 2026 at 10:30, ortopeda, Marek driving)

## For the family

Family contact is simulated in this demo (placeholder emails and phones; nothing is emailed or texted).

- A request that a named relative call when she doesn't answer or asks for one (Ania first, then Marek; quiet hours 21:00–08:00 Europe/Warsaw)
- A way to send photos and short words back to her
- A refill note when stock is running low (20 tablets counted 5 November, last day 14 November)

## Safety and limits

- Strażnik approves every message before it goes out
- No medical advice, no dose calculation, no missed-dose guidance
- No streaks, scores, or pressure
- A fixed emergency text only; this is not an alarm or a medical service
- Drawn weather character, never a photo of an invented person

## Care team

- **Krąg** — host; her one voice
- **Informator** — weather, air, forecast, visits
- **Rodzina** — family link
- **Kronika** — memory and memoir
- **Apteczka** — tablets and stock
- **Strażnik** — approval

## Repo

- `krag/` — shared workspace (see [`krag/README.md`](krag/README.md) for data sources and folder details)
- `sessions/ideation-process-log.md` — planning session that led to the idea

Ready to show now: the morning and evening lines. Not wired yet: the photo reveal, the memoir write-up, the live call-me handoff, the weather avatar, and the scheduled routines.
