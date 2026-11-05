# Krąg: ideation process log

Summary of the planning session that led to the Krąg care-team idea. Wrocław, Thursday 5 November 2026, 18:27 to 20:38 local time.

**What this is.** A record of how the idea was chosen and shaped before the build, written for the team and the judges. The session was a conversation between the founder and an AI assistant (Claude). It produced ideas, research, a spec and a pitch. No project code was written in it.

**Evidence marks.** "Checked" means opened or searched during the session. "From memory" means not checked. "Estimate" means arithmetic on checked figures.

## 1. Starting point (18:27)

Inputs: three photos of the organisers' slides.

- **Prizes:** subscription plans per team member, plus LEGO for the top three teams.
- **Judging:** working prototype; technical complexity and integration (depth of Grok Bot and SpaceXAI API use, tools, collaborative workflows); innovation and creativity; real-world impact; theme alignment (people plus AI, or multiple agents, working toward a shared goal). Tracks: Multiplayer AI, Multi-agent Systems.
- **Submission:** private repository with judges invited; AI session exports in `/sessions`; commit history reviewed; ideas may come before the event, implementation must happen in the sprint.

First framing by the founder: a Grok Bot for business that uses public Google data (Maps, Trends) to work on the top social issues in Polish cities, with no personal data.

First correction. A public-data dashboard does not match the theme line on the slide, which asks for people and AI, or several agents, working together. Google was also the weaker source: Trends has an official API only for approved testers (checked), and Maps needs a billing key (from memory). Polish public feeds are free. The data became the fuel; a shared chat with several agents became the product.

## 2. Timeline of ideas and decisions

| Time | Step | Outcome |
|------|------|---------|
| 18:27 | Five first ideas | Flood room, doctor queue finder, estate petition builder, shift and commute planner, outbreak staffing alert |
| 18:35 | Flood room explained | Liked for how it can be shown on a map and replayed |
| 18:36 | Parked | Not timely in November. Kept the pattern: live public feed, changing picture, people and agents agreeing one plan, replay of a real bad day |
| 18:37 | Five sibling ideas | Smog room, tram breakdown room, dark-route room, Christmas market room, doctor queue room |
| 18:37 | Data sources | Ten sources listed, six checked the same hour |
| 18:50 | Top ten social issues in Poland | Draft list, then a full verification (section 3) |
| 18:59 | Ideas for the ageing population | Parent's care room, weather-health guardian, nurse round planner, bad-day errands, after-hospital room |
| 19:04 | Widened to all problems | Flat-hunt room, newcomer room and tram commute room stood out; security, polarisation and youth mental health ruled out as hard to show or too sensitive |
| 19:10 | Founder's insight: a bot is a habit builder | Research into habit mechanics (section 4) |
| 19:24 | Decision: the family care circle | First spec and three-minute pitch, working name Krąg |
| 19:25 | Market size and willingness to pay | Added to the spec (section 5) |
| 19:30 | How to make it enjoyable for the parent | Five ideas: photo behind the tap, memory question, she sets the question, guess mum's answer, morning programme |
| 19:38 | Chosen: memory question and photo behind the tap | Spec rewritten for Grok Bot with a storyteller Bot |
| 19:46 | Does the platform support a chat with several people? | Not as assumed (section 6) |
| 19:50 | WhatsApp group? | Possible for a demo through a linked number, fragile; official route capped at 8 people and needs a verified business |
| 19:57 | Pivot: a care team of Bots for one ageing person | Family moves outside the app; Bots ask relatives to call and collect photos |
| 19:59 | Tablets as the hook | Remind and count only; never work out a dose. Sixth Bot added |
| 20:01 | Pitch reframed | Not a replacement for a carer: cover for the hours between visits |
| 20:06 | Extra connections | Eight candidates ranked; phone calls set aside in favour of in-app voice |
| 20:08 | Chosen: voice, morning picture by weather, text messages, six more connections | Spec Rev E, with a strict build order |

## 3. Problem selection: what the research said

A verification pass on the top social issues in Poland (2025 and 2026 sources).

- Top three confirmed by at least two independent polls each: cost of living, access to healthcare, external security.
- Rising food and essentials prices worried 40.7% (October 2026 poll); improving healthcare access was a top priority for about two thirds in two national opinion-centre studies (checked).
- Dropped from the list: road safety (2025 had the fewest road deaths on record).
- Moved down: housing and smog (no national poll put them at the top).
- Added: energy and heating bills; quality of public services.
- Wrocław: 37.5% of residents report difficulty getting care (Wrocław Social Diagnosis 2025); 13 tram derailments counted in 2026.
- Why healthcare plus ageing won: the second biggest national concern, the top local health complaint, and free public data that updates at least weekly.

Limits recorded at the time: some European survey figures were read through a statistics aggregator, and Wrocław flood risk and parking were not researched.

## 4. Mechanic selection: what the habit research said

- Reminders are the best-proven mechanic. Text reminders roughly doubled the odds of taking medication (odds ratio 2.11, or 1.68 after bias correction; 16 trials, 2016) and raised appointment attendance by about 14% (Cochrane review, 2013).
- Most habit apps fail. A typical mental-health app keeps 3.3% of users at day 30 (2019 study of 93 apps). Habits take a median of about two months to form, and one missed day does not matter (2010 study).
- Family games worked in one trial (families met step goals on 53% of days against 32%); a messaging group alone did no better than plain texts in another.
- AI coaches: engagement improves, sustained behaviour change is not shown yet.
- Design consequences taken: one tiny action a day; a missed day is covered by a person and never punished; people are the accountability and the Bots are the organisers; no streaks or scores; a cap on messages.
- Stated limit: no trial has tested several agents coordinating care for one older person. The prototype tests a new combination.

## 5. Market and willingness to pay

- About 7.9 million people in Poland are 65 or over (2025 data, checked through a press summary).
- About 1.9 million of them live alone (estimate from a 2020 European labour survey: 33% of women, 13% of men).
- Families pay about 20 to 55 zł a month for an alarm wristband, plus 299 to 999 zł for the device; a voice checking service lists at 149 zł a month; home care starts from about 50 zł an hour (one vendor's price guide, June 2026).
- National 2026 budget line for remote care devices: 20 million zł.
- Reading: large need, low price point. Sold to families in Poland alone it is a small business (about 4.7 million zł a year if 1 family in 100 paid the lowest wristband fee). The platform's own plan costs more per month than families pay today. The idea is pitched as an experience, not yet as a business.
- Not found: adoption rates for this kind of product; smartphone use among older people living alone.

## 6. Platform findings that changed the design

Read from public docs and guides during the session; none confirmed with the organisers.

| Finding | Effect on the design |
|---------|----------------------|
| A group chat is two to six of one person's own Bots, plus that person | The "family in one chat" idea was dropped |
| A shared Bot gives each teammate a private chat; shared rooms exist in Slack | Considered as a hub, set aside: needs a team account and would not match how a family lives |
| WhatsApp groups: only through a linked personal number, or a verified business with an 8-person cap | Set aside as too fragile for a live demo |
| One person's Bots share a cloud computer and can run on a schedule | Plain files as shared state; routines for morning, tablets and evening |
| Handoffs between Bots in a group are text only; groups have no voice | She talks to one host Bot by voice; the other Bots work in the team group |
| Bots ask for approval before sending | Family addresses must be pre-approved, or call requests stall |

Resulting shape: one parent, one friendly host Bot, five more Bots behind it, and the family reached outside the app.

## 7. Where the idea stands (spec Rev E)

Care team: Krąg (host, her one voice), Informator (weather, air, forecast, visits), Rodzina (family link: call requests, photos, words both ways), Kronika (one memory question a day, memoir), Apteczka (tablet reminders, counting, refill requests), Strażnik (approves every message, fixed emergency text).

Her day: a morning picture that changes with the weather; one spoken question; her answer opens a photo from the family; one question about her life; tablet reminders at her own times; a named relative asked to call when she does not answer or asks for one.

Lines that are never crossed: no medical advice; no dose calculation or missed-dose guidance; no pressure or scores; no invented photos or invented details in her memoir; a drawn character, never a photo of an invented person.

Demo: thirty simulated days in about sixty seconds, then one live day. Simulation is announced as such.

## 8. Ideas considered and not taken

- Flood readiness room (wrong season).
- Smog room for school parents; tram breakdown room; dark-route room; Christmas market room.
- Flat-hunt room (a one-off decision, not a habit); newcomer room.
- Household cheap-hour energy game (saves money only on a dynamic tariff).
- Nurse round planner (the business angle; kept as a possible later buyer).
- Family group chat, Slack channel, WhatsApp group (platform limits, section 6).
- Phone calls to her landline (replaced by in-app voice for the sprint).
- Streaks, points and badges for the parent (pressure, and childish for the audience).

## 9. Open questions for the mentors

- Does voice mode work one-to-one on the phone, in Polish?
- Can a Bot show an image in chat, and can it make one?
- Can a routine message her first, with a phone notification?
- Can messages to fixed family numbers and addresses be approved once?
- Which text-message plugin sends to Polish numbers tonight?
- How are Bot sessions exported for `/sessions`?
- How long is the pitch, and when does the sprint end?

## 10. Untested assumptions

- That an older person enjoys a daily memory question and a tablet tap, and does not feel watched. Test: ask one older relative.
- That families would pay wristband-level prices without an alarm centre behind the product. Test: ten families, a manual version, two weeks.
- That six Bots in a chain answer fast enough for a live demo.
- That the clinic waiting-times feed accepts the parameters taken from its older documentation.

## 11. Files produced in the session

- `KRAG-GROKBOT-SPEC.md`: build spec for Grok Bot, Rev E (Bot setup messages, file layout, routines, tests, build order).
- A published page with the first spec, pitch and market section (four-agent family version, now superseded by Rev E).
- Two research reports: the social-issues verification and the habit-mechanics review.
- This log.

## 12. Main sources

- State weather institute public data: [danepubliczne.imgw.pl/api/data/synop](https://danepubliczne.imgw.pl/api/data/synop)
- Environment inspectorate air-quality API notes: [powietrze.gios.gov.pl/pjp/content/api](https://powietrze.gios.gov.pl/pjp/content/api)
- National Health Fund waiting-times API: [api.nfz.gov.pl/app-itl-api](https://api.nfz.gov.pl/app-itl-api)
- Statistics Poland figures on people aged 65 and over (press summary): [spidersweb.pl/2026/04/polska-sie-starzeje-gus-mediana-wieku-44-lata.html](https://spidersweb.pl/2026/04/polska-sie-starzeje-gus-mediana-wieku-44-lata.html)
- Batory Foundation report on care for older people (living alone)
- Remote-care price guide, June 2026 (published by a vendor): [eopiekun.pl/wpis/ile-kosztuje-teleopieka-dla-seniora](https://eopiekun.pl/wpis/ile-kosztuje-teleopieka-dla-seniora)
- Senior Support Corps programme 2026: [gov.pl/web/uw-podkarpacki/program-korpus-wsparcia-seniorow-na-rok-2026](https://www.gov.pl/web/uw-podkarpacki/program-korpus-wsparcia-seniorow-na-rok-2026)
- Shared Bots documentation: [docs.x.ai/grok-bot/shared-bots](https://docs.x.ai/grok-bot/shared-bots)
- Guides to Grok Bot groups, voice and plugins (Composio, Learn Cursor)
- WhatsApp group API overview (Unipile)
- Trials and reviews cited in section 4: Thakkar 2016; Cochrane 2013; Baumel 2019; Lally 2010; Patel 2017
