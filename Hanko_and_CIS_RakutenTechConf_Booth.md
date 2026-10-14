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

Every design choice in this document is subordinate to that one point. If a visitor leaves the booth remembering two sentences, we want them to be: *"The first game was a head-to-head annotation duel for Hanko — I labeled real competitive signals as fast as I could. The second was a three-minute detective case with CIS where I had to crack a competitor's next move using chat, and one of the signals it cited was one I'd labeled myself a minute earlier."*

### Booth jobs, in order

1. **Pull from the aisle** — RTC is a loud, crowded floor; a passive demo loses to a neighbour's espresso machine. Our pull has to be visibly interactive and visibly fast.
2. **Teach three things in under five minutes** — what Hanko does, what CIS does, and why the pairing matters.
3. **Produce a lead and a souvenir** — scanned badge, a personalized **Case File** (filled in across both games, printed at exit), a leaderboard spot. Sales / BD get a warm, well-qualified handoff.

### Audience we're designing for

- External engineers, ML engineers, data scientists, PMs who build AI products.
- Enterprise BU leads evaluating competitive intelligence tooling.
- Internal Rakuten BUs — potential first-party customers for both products.
- Japanese- and English-speaking visitors in roughly equal proportion; every surface is bilingual.

---

## 2. Primary concept — **Rush & Hunt** (two distinct games, played back-to-back in one booth)

One booth. Two **separate games** with their own identity, rules, pace, and feel. Every visitor plays Game 1 (Hanko) then Game 2 (CIS). The two games are tied together by a single physical object — **the Case File** — that each visitor carries from one game to the next and takes home at the end.

The explicit design decision: **do not merge the two products into one hybrid "pipeline" experience.** Each product deserves to be remembered as its own thing. Visitors should walk away able to say *"the first game was the fast annotation duel for Hanko; the second was the three-minute detective case for CIS"* — two sentences, two memories, two products.

```
   ┌──────────────────────────┐   ┌──────────────────────────┐
   │  GAME 1 — LABEL RUSH     │ → │  GAME 2 — INSIGHT HUNT   │
   │  (Hanko)                 │   │  (CIS)                   │
   │  Head-to-head arcade     │   │  Solo detective case     │
   │  annotation duel, 90s    │   │  with CIS chat, 3 min    │
   │  Loud, bright, aisle-    │   │  Quiet pod, focused,     │
   │  facing, spectator-ready │   │  aha-moment-driven       │
   └──────────────────────────┘   └──────────────────────────┘
           └──────  The Case File (carried between games,  ──────┘
                     printed and taken home at exit)
```

### 2.1 Game 1 — **Label Rush** (Hanko)

**Format:** head-to-head arcade annotation duel. Two mirrored stations side-by-side, facing the aisle. Each station is an iPad in a landscape kiosk mount running a real Hanko project, flanked by two oversized soft-touch classify buttons and a 4-way subtype dial. Two visitors play against each other; solo visitors play against a bot opponent calibrated to a 70th-percentile human baseline.

**What happens in 90 seconds:**
1. Visitor hits START. 15–20 real competitive signals from the demo corpus scroll past, one at a time.
2. For each signal they: (a) classify (Pricing / Hiring / Product / M&A / Legal / Noise), (b) pick a subtype via the dial, (c) hit NEXT (or SKIP if they're not sure — skips cost score but keep the clock moving).
3. The screen shows live **items/min** and live **accuracy vs. the gold-standard key**. Score = items/min × accuracy, with a non-trivial multiplier on consecutive hits (a "combo" counter) so skilled hands pull away from merely fast ones.
4. On buzzer: the winner is the higher score across both stations. Winner animation; both scores land on the Rush Leaderboard.
5. Both players' annotations are saved to the shared demo Hanko project **and** attached to their individual Case File.

**What this teaches about Hanko:** the real UX principles (fast hotkeys, keyboard-first flow, undo, submit-and-continue), gold-standard scoring, and — most importantly — the visceral intuition that *annotating well at speed is hard*, which is the exact pain Hanko's platform (review workflow, consensus, guild of labelers, training mode, QA metrics) is built to absorb. The SME uses that intuition as the on-ramp for a deeper conversation when the visitor is ready.

**Why head-to-head:** spectators are the second pull. Two visitors visibly racing each other with buzzer sounds, big buttons, and a running scoreline draws a crowd far better than a solo demo.

**What goes on the Case File (Game 1 side):** visitor's score, items/min, accuracy, the signals they personally labeled (as a short list with icons).

### 2.2 Game 2 — **Insight Hunt** (CIS)

**Format:** a 3-minute solo detective case. Four laptop pods behind the Rush stations, with light visual dividers for focus. Each pod runs a dedicated CIS instance over the shared demo corpus — the same corpus that Rush visitors have been labeling all day, which keeps growing.

**What happens in 3 minutes:**
1. At the pod, the visitor hands over their Case File. The host stamps it with a **Case** chosen from a face-down deck of ~10 pre-authored cases (visitor sees three card backs, picks one blind — *"pick your case"* is a small ceremony). Case titles look like *"The Quiet Launch"*, *"The Hiring Tell"*, *"The Price War"*, *"The Delisted Feature"*.
2. The screen displays the case brief: *"Rumor says {Competitor X} is about to {something big}. You have 3 minutes with CIS to figure out WHAT and defend it with 2 cited signals. GO."* A 3-minute countdown starts.
3. The visitor types chat queries directly into CIS. Answers appear with citations — including, where it genuinely applies, a signal the visitor themselves labeled in Rush 60 seconds earlier. A floating callout flags that moment: *"← this one is yours."*
4. At the buzzer, the visitor speaks their verdict and names 2 signals to the floating CIS SME.
5. The SME checks against the pre-authored answer key and stamps the Case File with one of three outcomes:
   - **Case Cracked** (correct verdict + 2 valid signals) → leaderboard spot + Insight Vault deck.
   - **Lead Followed** (defensible-but-not-the-intended verdict, or 1 valid signal) → still a win; sticker.
   - **Red Herring** (wrong path) → comedy consolation sticker: *"I fell for the red herring."* The SME then shows them, in 30 seconds, how CIS would have cracked it. This is often the strongest conversion moment.

**What this teaches about CIS:** the chat UX itself; grounded, cited answers; the specific aha of typing a free-form question and getting a sourced, defensible answer in seconds; and — the thing visitors feel but rarely say out loud — that under time pressure, *citations are not a feature, they are the product.*

**Why solo-with-timer:** the 3-minute clock forces the visitor to actually use the product rather than hover and read; the spoken verdict to the SME creates a real, natural conversation moment that lead-capture emails can't replicate.

**What goes on the Case File (Game 2 side):** case title, visitor's verdict, their 2 cited signals, outcome stamp, SME's one-line note.

### 2.3 The connective device — **the Case File**

A A5-size card-stock sheet, bilingual, Rakuten crimson. Issued at the booth entrance when the visitor's badge is scanned. Carries them through both games and goes home with them.

Front (Game 1 / Hanko):
- Visitor name, badge scan timestamp.
- Rush score, items/min, accuracy, combo peak.
- "You personally labeled:" short illustrated list of their signals.

Back (Game 2 / CIS):
- Case title (pre-stamped).
- Visitor's verdict.
- 2 cited signals.
- Outcome stamp.
- SME's handwritten one-line note.
- QR to book a follow-up (one tap in the follow-up form picks Hanko / CIS / Both).

A thermal printer at the exit also prints a **digital-friendly** version of the same content (crisp PDF emailed to the badge address later) — so the physical card is the keepsake, and the PDF is the artifact they'll actually forward to a colleague.

**Why one object across two games:** it is the single device that stitches the two product memories into one story without smushing the games together. It's also the only thing the SMEs and sales / BD need to look at to know what to say in the follow-up.

### 2.4 Flow and pacing per visitor

```
   Entry (badge scan, Case File issued, pick a Case card)   ~30s
   → Game 1: Label Rush                                      90s
   → walk to pod                                            ~15s
   → Game 2: Insight Hunt                                   180s
   → spoken verdict + stamp                                  30s
   → exit (Insight Vault deck, printed Case File)           ~15s
   ─────────────────────────────────────────────────────────────
   Total per visitor                                     ~6 min
```

Visitors who only have time for one game play one; the Case File still prints with whichever side was completed. SMEs are briefed to never pressure a visitor into Game 2 — the Rush alone is a complete, satisfying booth visit.

### 2.5 Throughput

- Game 1: 2 stations × ~90s per round + ~30s reset = ~40 rounds/hour × 2 players = **~80 Rush players/hour**.
- Game 2: 4 pods × ~4 min per case (incl. verdict + stamp) = **~60 Hunt players/hour**.
- Expect ~60% of Rush players to continue to Hunt (the limiting factor); real sustained throughput ≈ **55 full laps/hour** plus ~25 Rush-only visitors/hour, totaling ~80 scanned badges/hour.
- Over an 8-hour event day: **~640 scanned badges/day**, well inside the §5 targets.

### 2.6 The ambient attractor — "Live Insight Wall"

A 55"–75" screen mounted above the booth, visible from the aisle. It cycles two things:
1. The **current Hunt pod's chat answer** streaming in real time with citations popping in (anonymized — no visitor name) — ~15 seconds per cycle. The visible chatbot-answering-a-strategy-question in real time is the pull.
2. The **Rush Leaderboard** between cycles — current top scores + a scrolling ticker of recent wins ("Taro K. just cracked *The Quiet Launch*").

Spectators learn passively; players earn the Case File.

### 2.7 Peak-slot bonus — "Championship Hunt"

Once per peak slot (post-keynote, lunch, mid-afternoon), the Live Wall announces a single harder public case (*"Which Rakuten-adjacent competitor is most likely to launch a payments product this quarter — defend with 3 signals."*). Any Hunt visitor during the slot plays that case. End-of-day Championship winner gets the big prize (§4.5). Builds a reason to come back for a second visit.

### 2.8 Why two distinct games is the right primary bet

- **Two memorable products instead of one hybrid blur.** Visitors can tell a colleague about each product in one sentence because they played a game that belonged to that product.
- **Two personalities, two moods.** Rush is loud, physical, head-to-head, aisle-facing. Hunt is quiet, focused, aha-driven. The booth has range; nothing competes with itself.
- **Lower bounce.** A visitor who only has 2 minutes can play Rush and leave happy. A visitor with 6 can play both. Nothing is wasted either way.
- **Clean lead segmentation.** The SME at the Hunt pod naturally hears whether the visitor cares more about Hanko (they talk about speed, hotkeys, QA) or CIS (they talk about citations, prompts, workflow) — and tags the Case File accordingly for the follow-up.
- **The pipeline story is still there, it's just carried by the Case File instead of the floor plan.** The best moment of Game 2 — the *"← this one is yours"* citation callout — is impossible without Game 1 having happened first. Visitors feel the pairing without having to be told about it.

---

## 3. Alternative concepts (ranked for RTC fit)

Each is a credible headline act if a constraint (space, team, lead time, audience depth) rules out Rush & Hunt. Several of them are strong **sidecar** acts alongside Rush & Hunt and are flagged as such.

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

| Concept | Throughput / hour | Depth | Floor space | Staff | Souvenir | Social media | Sidecar fit with Rush & Hunt |
|---|---|---|---|---|---|---|---|
| **Rush & Hunt (primary — two games)** | ~55 full laps + ~25 Rush-only | High (hands-on, both products) | Medium | 4–5 | Printed Case File | Medium–High (Rush duels + Live Wall) | — |
| Signal Hunt (card game) | ~16 per table | Medium | Small per table | 1 per table | Boxed deck | Low | **Strong** |
| Chat with the Data (gameshow) | ~24 contestants, large audience | Medium | Large (stage area) | 1 host + 1 scorer | No | **High** | Strong (peak-hour only) |
| CI Escape Room | ~12 | **Highest** | Medium pod | 1 facilitator | Certificate | Low | Strong (back-corner exec table) |
| Label & Learn Dojo | ~40 | Medium | Small | 1 | No | **High** | Weak — overlaps with Rush |
| Insight Vault (deck) | n/a (handout) | Low in-booth | Small | 1 | **Yes (deck)** | Low | **Always include** |

### Recommended stacks

- **Default stack:** Rush & Hunt (primary — two games, played back-to-back) + Insight Vault (universal take-home) + a scheduled Chat with the Data round once per peak slot. Covers pull, depth, souvenir, and highlight clips with one coherent brand. Label & Learn Dojo is intentionally dropped from the default stack because it overlaps with Rush and would dilute the "two distinct games" clarity.
- **Small-booth stack:** Signal Hunt tabletop + Insight Vault. One shared table, two staff, small footprint, honors the original Monopoly-style cue. No live Rush & Hunt experience; the game and the deck carry both products.
- **Enterprise-first stack:** Rush & Hunt + CI Escape Room in the back corner for exec visitors + Insight Vault. Lower overall throughput, but every lead is high-quality.

---

## 4. Booth logistics

Because these are software products, the booth is more "equipped demo lab" and less "printed board game." The implications are concrete.

### 4.1 Footprint

- **Minimum (small-booth stack):** 2 m × 3 m. One Signal Hunt table, one Insight Vault counter.
- **Default (recommended):** 3 m × 4.5 m. Rush & Hunt layout: 2 Rush stations facing the aisle (iPads + arcade buttons + buzzer), 4 Hunt pods behind them (laptops + light dividers), exit counter with thermal printer and Case File rack, Live Insight Wall mounted above the booth.
- **Preferred:** 4 m × 5 m. Adds a back-corner CI Escape Room pod and a small stage apron for Chat with the Data.
- **Backdrop:** Rakuten crimson with bilingual tagline — *"ラベルから、インサイトへ。90秒で。 / From labels to insights, in 90 seconds."*

### 4.2 Hardware bill of materials (default stack)

Compute & display:
- 2× iPads (12.9"), landscape kiosk mounts, cable-locked — the Rush stations. Each flanked by 2× oversized soft-touch classify buttons + 4-way subtype dial + mechanical buzzer.
- 4× laptops (15"+) at the Hunt pods, external keyboard + mouse per pod, light dividers for focus.
- 1× 55"–75" display for the Live Insight Wall (above the booth, visible from aisle).
- 1× 55" display + two podium mics for Chat with the Data peak slots (shares the Live Wall screen between rounds).
- 1× thermal printer at exit for the digital-friendly Case File reprint (continuous feed, bilingual template).
- Badge scanners (QR/NFC — whatever RTC issues).
- 1× iPad at entry for badge scan, Case File issuance, and Case card draw.

Network (do not rely on venue WiFi):
- 2× bonded 5G routers with failover, dedicated SSID for the booth equipment.
- A pre-staged offline fallback mode on each iPad/laptop that uses cached signals and a cached CIS answer set, in case connectivity dies mid-event. **This is not optional.**

Demo environment (back-end):
- A dedicated **demo tenant** of Hanko with a pre-seeded Rush project (gold-standard key, scoring hooks for items/min, accuracy, combo), and a scripted reset-between-rounds flow.
- A dedicated **demo tenant** of CIS with an indexed curated corpus of ~2,000 signals across 4–6 mock competitors. ~10 pre-authored Hunt cases, each with a tested answer key and a tested known-good question sequence.
- A small booth-ops dashboard that: tracks per-visitor stats across both games, generates the printable Case File reprint, drives the Live Insight Wall + Rush Leaderboard, keeps the Championship Hunt scoreboard.
- An on-call engineer per product reachable by Slack for the entire event (not on the booth, but reachable).

Physical game components (sidecar / take-home):
- 1,000× Case File A5 card-stock sheets (bilingual, pre-perforated for the exit-counter tear-off).
- Case card deck for the entry iPad (~10 case titles) + physical "outcome" rubber stamps (**Case Cracked** / **Lead Followed** / **Red Herring**).
- 50× boxed Signal Hunt decks (if running Alt A sidecar).
- 500× Insight Vault decks + tuckbox + one-page rules insert.
- Sticker sheet (incl. the "I fell for the red herring" sticker) + crimson lanyard pins.

### 4.3 Booth team (per shift, default stack)

| Role | Count | What they do |
|---|---|---|
| Entry greeter + Rush announcer | 1 | Scans badges, issues Case Files, runs the Case card draw, calls Rush rounds like a boxing match ("Red station vs. Blue station, 90 seconds, GO") |
| Rush SME (Hanko) | 1 | Floats the two Rush stations, resets rounds, answers product questions, uses Rush score as the on-ramp to the real Hanko conversation |
| Hunt SME (CIS) × 2 | 2 | One SME per pair of Hunt pods. Takes visitor verdicts, stamps outcomes, uses the "Red Herring" moment to show in 30s how CIS would have cracked the case |
| Lead-capture host | 1 | Reprints the Case File as PDF, confirms follow-up consent + Hanko/CIS/Both tag, hands out Insight Vault deck |
| Event ops / runner | 1 | Resets kit, swaps iPads if a battery dies, troubleshoots network, runs the Chat with the Data peak slots as host, drives the Live Wall + Championship Hunt |

Rotate every 90 minutes; the Rush announcer and the Chat-with-the-Data host roles are the two highest-energy slots.

### 4.4 Pre-event, event, post-event funnel

**Pre-event (T−6 weeks → T−1 day)**
- Curate and freeze the demo corpus; author and test the ~10 Hunt cases end-to-end against the real CIS instance (every case must have a known-good question path that cracks it inside 3 minutes).
- Run three mock booth days internally to time Rush rounds, time Hunt cases, and shake out the Case File flow.
- Teaser landing page on tech.rakuten.co.jp: *"Rush. Hunt. Crack the case. Booth XX at RTC."*
- Pre-register visitors for Chat with the Data contestant slots and (if running) CI Escape Room slots via QR.
- Internal all-hands brief: Rakuten BUs that use (or could use) Hanko / CIS send champions to drop in.

**During event**
- Championship Hunt case announced on the Live Wall at the top of each peak slot; running leaderboard across the day.
- Two Chat with the Data gameshow rounds per peak slot (shares the Live Wall screen between rounds).
- End-of-day prizes: top Rush score of the day, top Hunt score (fastest **Case Cracked**), best "Red Herring recovery" (judged by SMEs).
- Rakuten Tech social team captures highlight clips (Rush H2H duels, aha moments at the Hunt pods, Championship Hunt reveals).

**Post-event (T+1 → T+14 days)**
- Email every scanned badge: thanks, their Case File attached as PDF, a 90-second product video for whichever product they engaged most with, calendar link for a real walkthrough.
- Separate pipelines for Hanko leads and CIS leads (lead-capture exit tag + the SME's handwritten Case File note).
- Internal retro: which CIS questions did visitors actually type → direct input into CIS prompt-library and product roadmap; which Rush subtypes did visitors most confuse → direct input into Hanko's training/onboarding UX.
- The demo-corpus annotations collected during RTC become a case study: *"800 external visitors annotated 8,000 signals in 2 days — here's what they got right and wrong, and what it taught us about Hanko's UX."* This is a blog post.

### 4.5 Prizes

- **Daily championship:** Rakuten crimson mechanical keyboard + 1 year of Rakuten service credits. One per day for the top Championship Hunt crack and one per day for the top Chat with the Data contestant.
- **Rush top-of-the-hour:** limited-edition "Rush Champion" acrylic desk piece for the top head-to-head score each hour.
- **Everyone:** Insight Vault deck + sticker set + printed Case File. The "I fell for the red herring" sticker is deliberately the most asked-for item; make plenty.

### 4.6 Budget (rough order of magnitude, JPY)

| Item | Est. cost |
|---|---|
| Demo environment engineering (both tenants, Rush scoring layer, Hunt case flow, reset flow, Case File generator, booth-ops dashboard, Live Wall, leaderboards) | ¥1.8M–¥2.8M |
| Demo corpus curation + 10 Hunt cases authored + bilingual rewriting + gold-standard labeling + legal review | ¥500k–¥900k |
| Hardware (3 iPads for Rush and entry, 4 laptops for Hunt, 1–2 displays, arcade buttons + dials + buzzers, printer, 5G routers) — assume mostly rented | ¥600k–¥1.1M |
| Booth build + crimson backdrop + lighting + Hunt-pod dividers | ¥600k–¥1.0M |
| Case File print run (1,000 bilingual A5 cards + rubber stamps + case card deck) | ¥150k–¥300k |
| Signal Hunt deck design + print (50 boxed, if running sidecar) | ¥300k–¥500k |
| Insight Vault deck design + print (500) | ¥300k–¥500k |
| Prizes | ¥300k–¥500k |
| Staff T&E, training, dry-run day | ¥500k–¥900k |
| **Total (indicative)** | **¥5.0M–¥8.5M** |

Everything in the top two rows (demo environment + corpus + Hunt cases) is reusable at Rakuten Optimism, campus events, enterprise sales roadshows, and internal BU briefings for the following 12 months. The demo tenants and the Hunt-case library, in particular, are durable sales assets — not RTC-only expenses.

---

## 5. Success metrics

| Metric | Target at RTC |
|---|---|
| Unique badges scanned | ≥ 500 |
| Rush rounds played (incl. solo-vs-bot) | ≥ 600 over the event |
| Hunt cases attempted | ≥ 400 |
| Hunt cases scored **Case Cracked** | ≥ 150 |
| Full laps (Rush + Hunt by the same visitor) | ≥ 400 |
| Signals annotated at Rush (cumulative) | ≥ 6,000 |
| CIS chat sessions started at Hunt | ≥ 400 |
| Case Files printed | ≥ 500 |
| Chat with the Data contestants | ≥ 50 across the event |
| Qualified follow-up leads tagged **Hanko** | ≥ 30 |
| Qualified follow-up leads tagged **CIS** | ≥ 30 |
| Qualified follow-up leads tagged **Both** | ≥ 15 |
| Social clips published by Rakuten Tech channels | ≥ 8 |
| Post-event demo meetings booked within 14 days | ≥ 25 |

Instrument everything. Per-visitor Rush scores, per-visitor Hunt transcripts, per-case crack rates, aggregated to the booth-ops dashboard. The dataset of "what questions did real conference visitors naturally type into CIS" and the dataset of "which signal subtypes humans most confuse under time pressure" are the two most valuable artifacts we take home from the event, independent of lead count — one is the CIS prompt library, the other is Hanko onboarding UX feedback.

---

## 6. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Demo environment degrades or goes down mid-event | 5G failover; pre-cached offline mode on every device with scripted known-good content; on-call engineer per product |
| Venue WiFi unusable | Dedicated 5G bonded routers; nothing on the booth touches venue WiFi |
| CIS answers look weak on a given Hunt case because the corpus is thin or the question is awkward | Freeze the corpus 2 weeks before the event; author only cases that pass an internal 3-run smoke test; keep a short tested known-good question list visible at the Hunt pod |
| Rush feels like "mechanical turk" and visitors bounce after one round | The 90s timer + head-to-head + buzzer + big buttons make it feel arcade, not task; combo multiplier rewards skill, not just speed; SME uses score as the hook into the real Hanko conversation |
| Visitors conflate Hanko and CIS as "one product" | Two distinct games with their own identity and personality — this is the whole point of §2; backdrop names them separately; Case File has one side per product; lead-capture tag is one-tap |
| Line forms at Rush and discourages new visitors | Rush is only 90s per round so the line moves fast; waiting visitors can start a Case card draw at the entry iPad; Signal Hunt sidecar deck absorbs overflow |
| Bilingual balance tilts to one language | Every UI surface, Case File, Hunt case brief, and stamp is JP + EN on the same face; two of the SMEs are hired bilingual |
| Chat with the Data flops in a quiet slot | Keep it tightly scheduled (2–3 slots per day, not continuous); if a slot has fewer than 2 contestants, convert to a "host demo" using one audience volunteer and a live Hunt case |
| Enterprise visitors want more depth than Rush & Hunt offers | CI Escape Room back-corner pod; floating SMEs can escalate a hot post-Hunt conversation into a deeper walkthrough on the entry iPad |
| Hunt timer stresses visitors who don't like time pressure | Visitor can opt into "untimed mode" — no leaderboard spot, but the case still stamps; SME offers this proactively to visitors who look hesitant |
| Legal / brand risk from showing real competitor data | Entire demo corpus uses safely genericized or fictionalised competitors; legal review of the corpus AND the 10 Hunt cases is a hard gate before RTC |

---

## 7. Decision ask

Approve for Rakuten Tech Conference:

1. **Primary format:** Rush & Hunt — two distinct games played back-to-back in one booth. Game 1: **Label Rush** (Hanko, 90s head-to-head arcade). Game 2: **Insight Hunt** (CIS, 3-min solo detective case). Tied together by **the Case File**.
2. **Scheduled sidecar for crowd + social clips:** Chat with the Data gameshow, 2 slots/day, sharing the Live Wall screen.
3. **Universal take-home:** Insight Vault trading card deck for every scanned visitor, in addition to their printed Case File.
4. **Optional back-corner for enterprise visitors:** CI Escape Room pod.
5. **Budget envelope:** ¥5.8M–¥6.8M (mid-point of §4.6, assuming hardware rental and the Escape Room pod).
6. **Reuse plan:** demo tenants, corpus, Hunt-case library, Case File generator, and booth-ops dashboard become durable sales assets reused at Rakuten Optimism, campus events, enterprise roadshows, and internal BU briefings for the following 12 months.

### If the ask is to pick a single, lower-cost format

Fallback: **Signal Hunt tabletop + Insight Vault take-home**. One table, two staff, a 2 m × 3 m footprint, no demo-environment engineering required. Honors the user's original Monopoly-style cue, teaches both products through the game loop, produces a souvenir. Weaker than Rush & Hunt on hands-on product experience, but credible for a lean-staffed, short-lead-time scenario.

---

## 8. Appendix — showing two products without confusing visitors

A booth with two products is harder than a booth with one, because visitors default to pattern-matching everything to a single pitch. Rush & Hunt handles this at the format level — two games, two mechanics, two moods, two SME roles — so each product gets its own story. Four further guardrails:

- **Each game is complete on its own.** A visitor who only plays Rush still has a product memory for Hanko. A visitor who only plays Hunt still has one for CIS. We never force a merge.
- **Separate pipelines on the back-end from day one.** Lead-capture question at exit: *"Which do you want a follow-up on — Hanko / CIS / Both?"* One-tap, bilingual. The SME's handwritten Case File note is the second signal.
- **Separate leaderboards on the Live Wall.** The **Rush Leaderboard** (Hanko: top scores, items/min, accuracy, combo peak) and the **Hunt Scoreboard** (CIS: Cases Cracked, fastest crack of the hour, Championship Hunt standings). Each product's PM gets a clean metric.
- **Separate colour accents inside a single Rakuten crimson brand.** The crimson is the booth; a secondary accent per product keeps iconography distinct on signage, lanyards, the Case File, and each game's station.

If, after internal piloting, the two games feel too tightly bundled for one of the products' PMs, the correct next move is **not** to split the booth — it's to lengthen one game. Rush can grow a 60-second review round (showing Hanko's QA workflow explicitly) without touching Hunt; Hunt can grow a 60-second "multi-signal reasoning" extra round without touching Rush. Each product owns its own game and can evolve it independently across future events.

---

## 9. What this document is not

- Not a design spec for the demo corpus (that needs product + legal input).
- Not the authored text of the 10 Hunt cases (that needs product + a copywriter + a legal review pass).
- Not a script for the Chat with the Data gameshow rounds (that needs an MC and a dry-run).
- Not a print-ready Case File, Signal Hunt deck, or Insight Vault deck (each needs an illustrator and a copywriter).
- Not a signed-off budget — the §4.6 figures are rough-order-of-magnitude for an initial go/no-go.

If this concept is approved, the next working document is **an engineering spike plan for the two demo tenants + the Rush scoring layer + the Hunt case flow + the Case File generator + the booth-ops dashboard**, because that is the long-pole item for RTC readiness — not booth build, not print, not staffing. In parallel, product + copywriting authors the 10 Hunt cases and the demo corpus against the legal-review gate.
