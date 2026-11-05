# krag/ — shared workspace for the Krąg care-team prototype

This folder is the shared state on the cloud computer for the Wrocław hackathon
demo (Rev E / Step 1 Ground, 2026-11-05).

## Important

- **This is a prototype of the experience, not an alarm service and not a medical service.**
- The demo family (Pani Halina, Ania, Marek, Zosia, Kuba) is **invented**.
- **No real health data** is stored here. `DemoTablet` is a fictional medicine for the demo only.
- Email and phone values in `circle.json` are **PLACEHOLDERS** (`ania.demo@example.com`,
  `marek.demo@example.com`, `+48 000 000 001/002`). Replace them with the hackathon team's
  own addresses before any send test. Do not send to the placeholders.

## DemoTablet stock arithmetic

- `meds/stock.csv`: DemoTablet, **20** tablets, counted **2026-11-05**.
- Schedule: morning + evening = **2 tablets per day**.
- Counted on the morning of 5 Nov **before** today's doses.
- 20 ÷ 2 = **10 dose-days**, first day 5 Nov → last day **2026-11-14**.
- Therefore `runs_out_on=2026-11-14`.

## Name days

- `namedays.csv` is a full-year Polish name-day calendar (MM-DD), aggregated from
  [jancajthaml/polish-name-days](https://github.com/jancajthaml/polish-name-days)
  (`name-days.csv`). See `namedays.SOURCE.txt`.
- Halina appears on 07-01 (and 08-24 in that source). Elżbieta appears on 11-05 (among others).

## Samples

Raw replies from public sources, fetched 2026-11-05 (Europe/Warsaw), live in `samples/`.
Never invent weather, air, or forecast values; if a source fails later, reuse these files.

## Transit

`transit/` is ready for GTFS (her stop Krzyki, clinic stop, timetable). Files not yet added.

## Family contact

On 2026-11-05 the owner chose to keep placeholder addresses and **simulate** family sends.
Do not email `ania.demo@example.com` or `marek.demo@example.com`, and do not text the placeholder numbers.
Write simulated outbound drafts to `outbox/` and log them in `events.jsonl` and `sent.jsonl` with `"simulated": true`.
