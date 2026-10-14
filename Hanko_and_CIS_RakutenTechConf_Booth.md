# Hanko + CIS at Rakuten Tech Conference — Gamified Booth Proposal

**Event:** Rakuten Technology Conference (https://tech.rakuten.co.jp/)
**Products on show:**
- **Hanko** — annotation platform. Annotation jobs, labelers, review/QA workflow, task routing, inter-annotator agreement, gold tasks.
- **CIS** — Competitive Intelligence Service. Chat-to-insights interface sitting on top of a corpus of competitive signals (pricing, hiring, product launches, patents, exec moves, earnings, app-store reviews, ads).

**Note:** An earlier draft of this proposal (git history) was built around a wrong product understanding (Japanese hanko / approval workflows). That framing is discarded. This document starts from the correct product definitions above and designs the booth around them.

**Brief:** Showcase both products in a gamified way engaging to the RTC audience. The user initially floated a Monopoly-style card game; that cue is honored as one of the alternatives, not the headline, because the strongest asset we actually have is **the product pipeline itself** (Hanko labels → CIS answers questions over the labeled corpus). A booth that makes visitors *do* that pipeline in five minutes will land harder than any tabletop metaphor.

---

## 1. The one thing the booth has to prove

Both products are useful on their own. They are dramatically more useful together: **Hanko gives CIS the ground truth that makes its chat answers trustworthy, and CIS gives Hanko a visible payoff beyond "a cleaner dataset."**

Every design choice in this document is subordinate to that one point. If a visitor leaves the booth remembering only one sentence, we want it to be: *"I labeled a few signals at the first station, and ninety seconds later I was asking a chatbot questions over the dataset I just helped build."*

### Booth jobs, in order

1. **Pull from the aisle** — RTC is a loud, crowded floor; a passive demo loses to a neighbour's espresso machine. Our pull has to be visibly interactive and visibly fast.
2. **Teach three things in under five minutes** — what Hanko does, what CIS does, and why the pairing matters.
3. **Produce a lead and a souvenir** — scanned badge, a one-page personalized "Insight Report," a leaderboard spot. Sales / BD get a warm, well-qualified handoff.

### Audience we're designing for

- External engineers, ML engineers, data scientists, PMs who build AI products.
- Enterprise BU leads evaluating competitive intelligence tooling.
- Internal Rakuten BUs — potential first-party customers for both products.
- Japanese- and English-speaking visitors in roughly equal proportion; every surface is bilingual.

---

## 2. Primary concept — **The Insight Factory**

A visible, aisle-facing **three-station assembly line**. Visitors walk in at Station 1 and walk out of Station 3 with a printed insight report and a story. From the aisle it looks like a mini production line, which is exactly the metaphor we want to teach: *competitive intelligence is a pipeline, not a chatbot by itself.*

```
   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
   │  STATION 1   │ → │  STATION 2   │ → │  STATION 3   │
   │  Hanko:      │   │  Hanko:      │   │  CIS: chat   │
   │  annotate    │   │  review / QA │   │  the dataset │
   │  10 signals  │   │  someone     │   │  you helped  │
   │  (60–90s)    │   │  else's work │   │  build (90s) │
   │              │   │  (60s)       │   │              │
   └──────────────┘   └──────────────┘   └──────────────┘
          └─────────  Insight Report printed on exit  ─────────┘
```

### 2.1 Station 1 — Hanko Floor (annotate)

Visitor is handed an iPad running a live Hanko project. The project contains a pre-seeded batch of 10 competitive signals drawn from a curated demo corpus (safely genericized screenshots of pricing pages, job postings, patent abstracts, product release notes, exec LinkedIn moves, earnings-call snippets, app-store reviews, ad creative).

Their task — a real Hanko annotation job — is to:
- **Classify** each signal (Pricing / Hiring / Product / M&A / Legal / Noise).
- **Draw a bounding box** on screenshots to extract the key region.
- **Tag the subject entity** (which competitor is this about).

The screen shows a live timer, running accuracy against a gold-standard key, and a "throughput" counter. 60–90 seconds. On submit the data is written to the shared demo Hanko project.

**What the visitor just experienced that is the Hanko pitch:** task UI, hotkeys, gold-standard scoring, submit-and-continue flow, how a job batch feels at scale.

### 2.2 Station 2 — Hanko Review (QA someone else's work)

Visitor moves to the next iPad. They are now given a batch that **the previous visitor** just submitted. Their job is to accept, correct, or escalate each label. The screen shows live **inter-annotator agreement** — a number that moves as they go. If they disagree with the previous visitor, a short animation shows how Hanko's workflow would route the item to a tiebreaker.

**What the visitor just experienced that is the Hanko pitch:** review workflow, consensus, escalation, how a dataset actually gets to production quality — the thing that separates a toy labeling tool from a platform.

### 2.3 Station 3 — CIS Chat (ask the dataset anything)

Visitor sits at a laptop running CIS. The corpus they just helped label is already indexed — meaning the signals they personally annotated are literally cited in the answers they are about to get. The screen seeds three starter prompts:

1. *"What has {Competitor A} launched in the last 30 days?"*
2. *"Where is {Competitor B} hiring aggressively, and what does it suggest?"*
3. *"Compare the pricing strategy of {Competitor A} and {Competitor B}."*

The visitor can run the seeded prompts or type their own. Every chat response visibly cites signals, including (where it genuinely applies) one the visitor themselves annotated 90 seconds earlier. A floating callout highlights the citation: *"← this one is yours."*

**What the visitor just experienced that is the CIS pitch:** the chat UX, the quality of answers when the underlying corpus is well-annotated, grounded citations, the specific aha of asking a free-form question and getting a sourced, defensible answer in seconds.

### 2.4 On exit — Insight Report

A small thermal printer at the exit prints a personalised one-page Insight Report with:
- Visitor's name (from badge scan).
- Their annotation stats (speed, accuracy, items contributed).
- Their inter-annotator agreement score from Station 2.
- Their final CIS chat transcript.
- A QR to book a real walkthrough for Hanko, CIS, or both.
- Rakuten branding, bilingual.

That printed page is the souvenir, the lead-capture artifact, and the thing they'll show a colleague back at the office.

### 2.5 Pacing and throughput

- One full lap: ≈ **4–5 minutes** per visitor.
- Four stations per side × two sides = **8 iPads at Hanko stations + 4 CIS laptops** in a 3 m × 4.5 m footprint supports roughly **80–100 full laps/hour** at peak.
- Visitors who only want to do one station are allowed; the Insight Report still prints with partial stats.

### 2.6 The ambient attractor — "Live Insight Wall"

A 55"–75" screen above the booth shows the **current CIS answer** streaming in real time from whichever Station 3 is active, cycling every ~15 seconds. From the aisle, people see a chatbot visibly answering a competitive-intelligence question with citations popping in, and they walk over to find out what it is. This is the pull. Spectators learn passively; participants earn the Insight Report.

### 2.7 The optional group hook — "Insight Challenge of the Hour"

Every top-of-the-hour, the Live Insight Wall announces one shared question (*"Which competitor is most likely to launch a payments product this quarter — defend your answer with 3 signals."*). Any Station 3 visitor can submit an answer; the host picks the best. Winner gets a small on-brand prize and a leaderboard spot. Builds a reason to come back.

### 2.8 Why this is the right primary bet

- It is **the product**, played as a game, not a metaphor for the product.
- The pipeline story (Hanko → CIS) is physically embodied in the floor plan — nobody has to narrate it.
- Each station is short enough that aisle hesitation doesn't kill engagement.
- It generates a per-visitor souvenir *and* a per-visitor lead *and* a leaderboard story.
- The demo corpus is a shared, growing artifact — later visitors genuinely benefit from earlier visitors' annotations, which doubles as a cute scaling demo for Hanko.

---

## 3. Alternative concepts (ranked for RTC fit)

Each is a credible headline act if a constraint (space, team, lead time, audience depth) rules out The Insight Factory. Several of them are strong **sidecar** acts alongside the Factory and are flagged as such.

### Alt A — **Signal Hunt** (Monopoly-style card game — honors the original cue)

A tabletop card game, 2–4 players, 15 minutes, playable by walk-ups and takeable home as a boxed set.

Decks:
- **Signal cards** — real-world competitive signal archetypes (pricing screenshot, job post, patent filing, exec move, earnings quote, app-store review, ad creative). Laid out face-up as a shared "market."
- **Specialist cards** — Hanko annotator archetypes (Pricing Specialist, Hiring Analyst, Legal Reviewer, Multimodal Specialist, Generalist). Each player holds a small hand.
- **Insight cards** — the goal deck. Each insight requires 3–5 processed signals of specific types to "unlock" (e.g. *"Competitor X is about to launch a payments product"* needs 2 Hiring + 1 Patent + 1 Pricing signal).
- **Market Event cards** — periodic shocks (*"Earnings call tomorrow — pricing signals double in value this turn"*).

Turn structure:
1. **Hanko turn** — assign a Specialist to a Signal to "process" it (tag the card). Specialists tire; high-value signals need multi-player consensus (a nod to Hanko's review workflow).
2. **CIS turn** — once you have the right 3–5 processed signals, you can submit a "chat query" — draw the top matching Insight card. If you can defend it (quick say-out-loud), you score; wrong insights cost points.
3. **Market Event** — every third turn.

Why this works as the "like Monopoly" answer: it keeps the card-game shape the user asked for, but the game loop is literally the product loop — label signals, submit a query, extract an insight. Zero wasted mechanic. Also packages as a souvenir deck.

Best for: when the user explicitly wants the card-game format; also strong as a sidecar table at the booth for visitors who want to linger.

### Alt B — **"Chat with the Data"** (Jeopardy-style gameshow)

A small stage area with three contestant podiums and a wall-sized screen running CIS live. During peak slots (post-keynote, lunch, mid-afternoon) a bilingual host runs **10-minute rounds** of 3 contestants. Each round features a different mock competitor's dataset. Questions escalate from simple ("What did Competitor X announce last quarter?") to deductive ("Based on hiring, patents, and ad spend, what is Competitor X's likely next bet — defend in 20 seconds"). First correct insight wins the round. Big crowd gathers; high social-media output.

Best for: pulling crowds in defined peak windows; converting the aisle into an audience; produces highlight clips for Rakuten Tech social channels.
Weakness: dead between rounds; needs a host with real energy; thin on hands-on learning.

### Alt C — **Competitive Intelligence Escape Room**

4 players, 20 minutes, 1 facilitator, one private corner table (or a small enclosed pod). Scenario: *"Rakuten's strategy team has 30 minutes before a board meeting. The CEO wants a defensible hypothesis about what Competitor X is about to launch."* Players move through three mini-phases: triage raw signals, annotate them in Hanko (physical cards *and* a real iPad), reconstruct a timeline on a whiteboard, then query CIS to extract a final defensible insight before the timer. The game ends with the team *writing* the one-paragraph board brief.

Best for: BU heads, enterprise visitors, CFO/CRO-adjacent personas. Highest learning depth per visitor-minute of any format here.
Weakness: low throughput (≈ 12 visitors/hour).

### Alt D — **Label & Learn Dojo** (rhythm / arcade annotation)

A standing arcade cabinet, loud, bright, aisle-facing. Signals scroll by in rhythm on a 55" screen; player hits one of two big physical buttons (*Keep / Discard*) plus a joystick for subtype in time with the music. Scoring rewards both speed and accuracy against a gold key. Teaches "annotation at scale" in a visceral way — the point lands that doing this well in the open world needs structured workflow, which is what Hanko provides. CIS is covered by a small nearby monitor and a floating SME.

Best for: aisle pull, zero reading, pure spectacle; bilingual-trivial.
Weakness: light on CIS story unless paired.

### Alt E — **Insight Vault** (take-home trading card deck)

A 36-card deck in a crimson tuckbox for every scanned visitor. Suits:
- **Signals (12):** canonical competitive-signal archetypes.
- **Specialists (8):** Hanko annotator roles.
- **Prompts (8):** reusable CIS chat prompt patterns, each a mini playbook ("Compare pricing posture", "Decode hiring intent", "Reconstruct a product roadmap from release notes").
- **Insights (8):** historical insights that moved markets, with the signal chain that could have predicted them in hindsight.

Printed one-page rules teach a 10-minute 2-player draft game. Pure take-home; smallest booth footprint; best "survives the plane ride home" artifact.

Best for: the universal leave-behind; works even when staffed by one person.
Weakness: no live experience in the booth on its own.

### Alt F — **Signal Hunt (digital 1v1)** — ambient attractor

A single big-screen 1v1 digital version of Signal Hunt running continuously, mirrored to a tablet queue for walk-ups. Lower setup cost than a tabletop deck for a short lead time; weaker souvenir.

### Trade-off summary

| Concept | Throughput / hour | Depth | Floor space | Staff | Souvenir | Social media | Sidecar fit with Factory |
|---|---|---|---|---|---|---|---|
| **Insight Factory (primary)** | ~80–100 | High (hands-on, both products) | Medium–Large | 3–4 | Printed report | Medium (via Live Wall + Challenge) | — |
| Signal Hunt (card game) | ~16 per table | Medium | Small per table | 1 per table | Boxed deck | Low | **Strong** |
| Chat with the Data (gameshow) | ~24 contestants, large audience | Medium | Large (stage area) | 1 host + 1 scorer | No | **High** | Strong (peak-hour only) |
| CI Escape Room | ~12 | **Highest** | Medium pod | 1 facilitator | Certificate | Low | Strong (back-corner exec table) |
| Label & Learn Dojo | ~40 | Medium | Small | 1 | No | **High** | Strong (aisle pull) |
| Insight Vault (deck) | n/a (handout) | Low in-booth | Small | 1 | **Yes (deck)** | Low | **Always include** |

### Recommended stacks

- **Default stack:** Insight Factory (primary) + Label & Learn Dojo (aisle pull) + Insight Vault (take-home) + a scheduled Chat with the Data round once per peak slot. Covers pull, depth, souvenir, and highlight clips with one coherent brand.
- **Small-booth stack:** Signal Hunt tabletop + Insight Vault. One shared table, two staff, small footprint, honors the user's Monopoly-style cue.
- **Enterprise-first stack:** Insight Factory + CI Escape Room in the back corner for exec visitors + Insight Vault. Lower overall throughput, but every lead is high-quality.

---

## 4. Booth logistics

Because these are software products, the booth is more "equipped demo lab" and less "printed board game." The implications are concrete.

### 4.1 Footprint

- **Minimum (small-booth stack):** 2 m × 3 m. One Signal Hunt table, one Insight Vault counter.
- **Default (recommended):** 3 m × 4.5 m. The Insight Factory assembly line (8 iPads + 4 laptops + exit printer + Live Insight Wall above), Label & Learn Dojo cabinet, Insight Vault counter.
- **Preferred:** 4 m × 5 m. Adds a back-corner CI Escape Room pod and a small stage apron for Chat with the Data.
- **Backdrop:** Rakuten crimson with bilingual tagline — *"ラベルから、インサイトへ。90秒で。 / From labels to insights, in 90 seconds."*

### 4.2 Hardware bill of materials (default stack)

Compute & display:
- 8× iPads (10"+), stands, cable-locked, with hardened kiosk mode.
- 4× laptops (15"+) at Station 3, external keyboard + mouse per station.
- 1× 55"–75" display for the Live Insight Wall (above the booth, visible from aisle).
- 1× tall display for the Dojo arcade cabinet with two giant arcade buttons + joystick.
- 1× 55" display + two podium mics for Chat with the Data peak slots.
- 1× thermal printer at exit for Insight Reports (continuous feed, bilingual template).
- Badge scanners (QR/NFC — whatever RTC issues).

Network (do not rely on venue WiFi):
- 2× bonded 5G routers with failover, dedicated SSID for the booth equipment.
- A pre-staged offline fallback mode on each iPad/laptop that uses cached signals and a cached CIS answer set, in case connectivity dies mid-event. **This is not optional.**

Demo environment (back-end):
- A dedicated **demo tenant** of Hanko with a pre-seeded project, gold-standard key, and a scripted reset-between-visitors flow.
- A dedicated **demo tenant** of CIS with an indexed curated corpus of ~2,000 signals across 4–6 mock competitors. Scripted "known-good" questions have been tested to produce impressive, cited answers in under 5 seconds.
- A small booth-ops dashboard that: tracks per-visitor stats, generates printable Insight Reports, drives the Live Insight Wall, keeps the leaderboard.
- An on-call engineer on both products reachable by Slack for the entire event (not on the booth, but reachable).

Physical game components (sidecar / take-home):
- 50× boxed Signal Hunt decks (if running Alt A sidecar).
- 500× Insight Vault decks + tuckbox + one-page rules insert.
- Sticker sheet + crimson lanyard pins.

### 4.3 Booth team (per shift, default stack)

| Role | Count | What they do |
|---|---|---|
| Factory host | 2 | Greet, hand out iPads, 15-second intro, keep the line moving |
| Station SME — Hanko | 1 | Floats Stations 1 and 2, answers product questions, catches annotator confusion |
| Station SME — CIS | 1 | Sits near Station 3, prompts visitors with better questions, catches the aha moment |
| Dojo/Sidecar operator | 1 | Keeps the arcade and Signal Hunt tables running, resets between players |
| Lead-capture host | 1 | Prints Insight Report, scans badge, confirms follow-up consent, hands out Insight Vault deck |
| Event ops / runner | 1 | Resets kit, swaps iPads if a battery dies, troubleshoots network, runs the Chat with the Data peak slots as host |

Rotate every 90 minutes; the Factory host and the game-show host roles are the two highest-energy slots.

### 4.4 Pre-event, event, post-event funnel

**Pre-event (T−6 weeks → T−1 day)**
- Curate and freeze the demo corpus; run three mock booth days internally to prove per-visitor timing and known-good CIS answers.
- Teaser landing page on tech.rakuten.co.jp: *"Build the dataset, then ask it anything. Booth XX at RTC."*
- Pre-register visitors for Chat with the Data contestant slots and CI Escape Room slots via QR.
- Internal all-hands brief: Rakuten BUs that use (or could use) Hanko / CIS send champions to drop in.

**During event**
- Hourly Insight Challenge announced on the Live Wall; winner recognized at the top of each hour.
- Two Chat with the Data gameshow rounds per peak slot.
- End-of-day prizes: highest annotation accuracy, best chat question, most-cited visitor annotation.
- Rakuten Tech social team captures highlight clips (gameshow rounds, aha moments at Station 3, Dojo-cabinet reaction shots).

**Post-event (T+1 → T+14 days)**
- Email every scanned badge: thanks, their Insight Report attached as PDF, a 90-second product video for whichever product they engaged most with, calendar link for a real walkthrough.
- Separate pipelines for Hanko leads and CIS leads (badge-scan exit question tags preference).
- Internal retro: which CIS questions did visitors actually type → direct input into CIS prompt-library and product roadmap.
- The demo-corpus annotations collected during RTC become a case study: *"800 external visitors annotated 8,000 signals in 2 days — here's what they got right and wrong, and what it taught us about Hanko's UX."* This is a blog post.

### 4.5 Prizes

- **Daily championship:** Rakuten crimson mechanical keyboard + 1 year of Rakuten service credits. One per day for the top Chat with the Data contestant.
- **Hourly Insight Challenge:** limited-edition "Insight Champion" acrylic desk piece.
- **Everyone:** Insight Vault deck + sticker set + printed Insight Report.

### 4.6 Budget (rough order of magnitude, JPY)

| Item | Est. cost |
|---|---|
| Demo environment engineering (both tenants, reset flow, printed-report generator, booth-ops dashboard, Live Wall, leaderboard) | ¥1.5M–¥2.5M |
| Demo corpus curation + bilingual rewriting + gold-standard labeling | ¥400k–¥800k |
| Hardware (12 iPads, 4 laptops, 2 displays, arcade cabinet, printer, 5G routers) — assume mostly rented | ¥800k–¥1.4M |
| Booth build + crimson backdrop + lighting | ¥600k–¥1.0M |
| Signal Hunt deck design + print (50 boxed) | ¥300k–¥500k |
| Insight Vault deck design + print (500) | ¥300k–¥500k |
| Prizes | ¥300k–¥500k |
| Staff T&E, training, dry-run day | ¥500k–¥900k |
| **Total (indicative)** | **¥4.7M–¥8.1M** |

Everything in the top three rows (demo environment + corpus + hardware base) is reusable at Rakuten Optimism, campus events, enterprise sales roadshows, and internal BU briefings for the following 12 months. The demo tenants, in particular, are a durable sales asset — not an RTC-only expense.

---

## 5. Success metrics

| Metric | Target at RTC |
|---|---|
| Insight Factory full laps completed | ≥ 400 over the event |
| Unique badges scanned | ≥ 500 |
| Signals annotated at Station 1 (cumulative) | ≥ 4,000 |
| Review items processed at Station 2 | ≥ 3,000 |
| CIS chat sessions started at Station 3 | ≥ 500 |
| Insight Reports printed | ≥ 400 |
| Chat with the Data contestants | ≥ 50 across the event |
| Qualified follow-up leads tagged **Hanko** | ≥ 30 |
| Qualified follow-up leads tagged **CIS** | ≥ 30 |
| Qualified follow-up leads tagged **Both** | ≥ 15 |
| Social clips published by Rakuten Tech channels | ≥ 8 |
| Post-event demo meetings booked within 14 days | ≥ 25 |

Instrument everything. Per-visitor annotation data, per-visitor chat transcripts, aggregated to the booth-ops dashboard. The dataset of "what questions did real conference visitors naturally type into CIS" is the single most valuable artifact we take home from the event, independent of lead count.

---

## 6. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Demo environment degrades or goes down mid-event | 5G failover; pre-cached offline mode on every device with scripted known-good content; on-call engineer per product |
| Venue WiFi unusable | Dedicated 5G bonded routers; nothing on the booth touches venue WiFi |
| CIS answers look weak because the demo corpus is thin or stale | Freeze the corpus 2 weeks before the event; run three internal booth days to find and fix every weak question; keep a tested known-good question list visible at Station 3 |
| Visitors treat Station 1 as "mechanical turk" and bounce | Scoreboard + accuracy counter + the direct narrative payoff at Station 3 ("the item you labeled is cited here") turns labor into agency |
| Visitors conflate Hanko and CIS as "one product" | Physical station flow is explicit; backdrop + printed report both tag the two products distinctly; lead-capture exit question tags product preference |
| Line forms at Station 1 and discourages new visitors | Dojo and Signal Hunt sidecars absorb the queue; aisle greeter can offer "Insight Vault + come back for the Factory" |
| Bilingual balance tilts to one language | Every UI surface, printed card, and Insight Report is JP + EN on the same face; two of the four SMEs are hired bilingual |
| Chat with the Data flops in a quiet slot | Keep it tightly scheduled (2–3 slots per day, not continuous); if a slot has fewer than 2 contestants, convert to a "host demo" with one audience volunteer |
| Enterprise visitors want more depth than the Factory offers | CI Escape Room back-corner pod; floating SMEs can escalate a hot conversation into an iPad-side deep dive |
| Legal / brand risk from showing real competitor data | Entire demo corpus uses safely genericized or fictionalised competitors; legal review of the corpus is a hard gate before RTC |

---

## 7. Decision ask

Approve for Rakuten Tech Conference:

1. **Primary format:** The Insight Factory (3-station Hanko → Hanko → CIS assembly line).
2. **Sidecar for aisle pull:** Label & Learn Dojo arcade cabinet.
3. **Scheduled sidecar for crowd + social clips:** Chat with the Data gameshow, 2 slots/day.
4. **Universal take-home:** Insight Vault trading card deck for every scanned visitor.
5. **Optional back-corner for enterprise visitors:** CI Escape Room pod.
6. **Budget envelope:** ¥5.5M–¥6.5M (mid-point of §4.6, assuming hardware rental and the Escape Room pod).
7. **Reuse plan:** demo tenants, corpus, Insight Report generator, and booth-ops dashboard become durable sales assets reused at Rakuten Optimism, campus events, enterprise roadshows, and internal BU briefings for the following 12 months.

### If the ask is to pick a single, lower-cost format

Fallback: **Signal Hunt tabletop + Insight Vault take-home**. One table, two staff, a 2 m × 3 m footprint, no demo-environment engineering required. Honors the user's original Monopoly-style cue, teaches both products through the game loop, produces a souvenir. Weaker than the Factory on hands-on product experience, but credible for a lean-staffed, short-lead-time scenario.

---

## 8. Appendix — showing two products without confusing visitors

A booth with two products is harder than a booth with one, because visitors default to pattern-matching everything to a single pitch. The Insight Factory handles this by making the pipeline physical — Hanko on the left two stations, CIS on the right — and by having **separate SMEs per product**, visibly standing in their halves. Three further guardrails:

- **Separate pipelines on the back-end from day one.** Lead-capture question at exit: *"Which do you want a follow-up on — Hanko / CIS / Both?"* One-tap, bilingual. Routes to the right PM.
- **Separate leaderboards on the Live Wall.** "Top annotator of the hour" (Hanko) and "Best chat question of the hour" (CIS). Each product's PM gets a clean metric.
- **Separate colour accents inside a single Rakuten crimson brand.** The crimson is the booth; a secondary accent per product keeps iconography distinct on signage, lanyards, and the Insight Report.

If, after piloting internally, the Hanko and CIS teams decide the pairing story overshadows one product's standalone pitch, the correct next move is **not** to split the booth — it's to split the game. Run the Factory as the shared pipeline story on the main floor, and reserve CI Escape Room (CIS-heavy) and Signal Hunt tabletop (Hanko-heavy) as the two single-product deep dives in the back of the booth, each with its own PM present.

---

## 9. What this document is not

- Not a design spec for the demo corpus (that needs product + legal input).
- Not a script for the Chat with the Data gameshow rounds (that needs an MC and a dry-run).
- Not a print-ready Signal Hunt or Insight Vault card deck (that needs an illustrator and a copywriter).
- Not a signed-off budget — the §4.6 figures are rough-order-of-magnitude for an initial go/no-go.

If this concept is approved, the next working document is **a two-week engineering spike plan for the demo tenants + Insight Report generator + booth-ops dashboard**, because that is the long-pole item for RTC readiness — not booth build, not print, not staffing.
