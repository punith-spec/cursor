# Hanko + CIS at Rakuten Tech Conference — Gamified Booth Proposal

**Event:** Rakuten Technology Conference (https://tech.rakuten.co.jp/)
**Products on show:**
- **Hanko** — annotation platform. Annotation jobs, labelers, review/QA workflow, task routing, inter-annotator agreement, gold tasks.
- **CIS** — Competitive Intelligence Service. Chat-to-insights interface sitting on top of a corpus of competitive signals (pricing, hiring, product launches, patents, exec moves, earnings, app-store reviews, ads).

**Note:** Earlier drafts of this proposal (see git history) explored two mistaken framings and one half-step. This document is the current reference. It designs an **all-physical** booth: no iPads, no laptops, no screens at any game station. The only electronic device on the booth is the handheld **badge scanner** at the entry — standard conference equipment, not a game device.

**Brief:** Showcase both products in a gamified way engaging to the RTC audience. The user initially floated a Monopoly-style card game and then clarified two further constraints — both products in one booth as **two distinct games played back-to-back**, and **everything physical**. This document honors all three cues.

---

## 1. The one thing the booth has to prove

Both products are useful on their own. They are dramatically more useful together: **Hanko gives CIS the ground truth that makes its chat answers trustworthy, and CIS gives Hanko a visible payoff beyond "a cleaner dataset."**

Every design choice in this document is subordinate to that one point. If a visitor leaves the booth remembering two sentences, we want them to be: *"The first game was a head-to-head wall-sorting duel for Hanko — I slapped real competitive signals onto a giant magnetic wall as fast as I could. The second was a three-minute detective case for CIS, where I questioned a human Oracle who answered me with cited evidence cards, and some of the signals I pinned were ones I'd placed myself a minute earlier."*

### Booth jobs, in order

1. **Pull from the aisle** — RTC is a loud, crowded floor full of screens; a physical booth with a giant wall, a sand timer, a boxing bell, and a human Oracle in costume is a pattern-break that gets photographed before people even know what the products are.
2. **Teach three things in under eight minutes** — what Hanko does, what CIS does, and why the pairing matters.
3. **Produce a lead and a souvenir** — scanned badge, a personalized triplicate **Case File** (filled in across both games, taken home at exit), a Polaroid of the finished Signal Wall, a leaderboard spot. Sales / BD get a warm, well-qualified handoff.

### Audience we're designing for

- External engineers, ML engineers, data scientists, PMs who build AI products.
- Enterprise BU leads evaluating competitive intelligence tooling.
- Internal Rakuten BUs — potential first-party customers for both products.
- Japanese- and English-speaking visitors in roughly equal proportion; every physical surface is bilingual.

---

## 2. Primary concept — **Rush & Hunt** (two distinct **physical** games, played back-to-back in one booth)

One booth. Two **separate games** with their own identity, rules, pace, and feel. Every visitor plays Game 1 (Hanko) then Game 2 (CIS). The two games are tied together by a single physical object — **the Case File** — that each visitor carries from one game to the next and takes home at the end.

**Design principle: the booth is physical.** No iPads, no laptops, no screens at any game station. In a conference hall full of monitors, an all-physical booth is the pattern-break that gets photographed, lingered at, and talked about. It also eliminates every "demo environment degraded" and "venue WiFi dead" risk from the operational plan.

The explicit design decision: **do not merge the two products into one hybrid "pipeline" experience.** Each product deserves to be remembered as its own thing. Visitors should walk away able to say *"the first game was the wall-sorting duel for Hanko; the second was the three-minute detective case with the Oracle for CIS"* — two sentences, two memories, two products.

```
   ┌──────────────────────────┐   ┌──────────────────────────┐
   │  GAME 1 — LABEL RUSH     │ → │  GAME 2 — INSIGHT HUNT   │
   │  (Hanko)                 │   │  (CIS)                   │
   │  Two players race to     │   │  Visitor across from a   │
   │  sort magnetic signal    │   │  human Oracle. Pin to a  │
   │  tiles onto a giant      │   │  corkboard with yarn.    │
   │  wall. 90-second sand    │   │  3-minute sand hourglass │
   │  timer. Boxing-bell      │   │  Boxing-bell buzzer.     │
   │  buzzer. Scorekeeper.    │   │  Verdict spoken aloud.   │
   └──────────────────────────┘   └──────────────────────────┘
          └──  The Case File (triplicate carbon-copy,  ──┘
               carried between games, taken home with
               a Polaroid of the finished Signal Wall)
```

### 2.1 Game 1 — **Label Rush** (Hanko) — *The Signal Wall*

**Format:** a 2 m × 2.5 m **magnetic Signal Wall** at the aisle-facing edge of the booth, impossible to miss. The wall is divided into a visible 6-column × 4-row grid — **6 columns are the categories** (Pricing / Hiring / Product / M&A / Legal / Noise), **4 rows are the subtypes within each category** (e.g. for Pricing: Increase / Discount / Bundling / New Tier). Every cell is colour-coded and labelled bilingual. Two mirrored playing lanes face the wall side-by-side; each lane has its own hopper of ~80 printed magnetic **Signal Tiles** (postcard-size, bilingual, each one a real competitive signal: a redacted pricing screenshot, a job post excerpt, a patent abstract, an exec LinkedIn post, an earnings quote, an app-store review, an ad image). Tile backs are printed with the correct cell so the grading pass is instant.

**What happens in 90 seconds:**
1. Scorekeeper SME flips the big **sand timer** and rings the **boxing bell**. Two players grab the top tile from their own hopper.
2. For each tile the player: (a) reads it, (b) decides which cell on the wall it belongs in, (c) slaps it onto that cell. Next tile. Skipping is allowed by dropping into a *"Skip"* tray at their feet — skips cost no time but score nothing.
3. SMEs on each side watch and tally **misplaces** on a chalkboard behind each lane with hash marks. The player sees their running misplace count in real time.
4. On the bell: lanes are frozen. SMEs do a 15-second **grade pass**, flipping any misplaced tile to show the correct cell printed on the back. Final score = tiles correctly placed − 2 × misplaces. (The −2 penalty makes "slap everything in Pricing" a losing strategy, which is the whole point.)
5. Winner's name goes up on the hand-updated Rush Leaderboard. Both players' misplaces are discussed by the SME in one sentence each — the on-ramp for the real Hanko conversation.

**What this teaches about Hanko:** the visceral intuition that *annotating well at speed is hard*, and that the hard part isn't the obvious signals — it's the subtype decisions and the ambiguous edges. That is the exact pain Hanko's platform (gold-standard tasks, review workflow, consensus, inter-annotator agreement, training mode, guild of labelers) is built to absorb. The SME uses the player's own misplaces as the opener: *"That one you missed? Here's how Hanko catches it in production."*

**Why physical and why head-to-head:** the Signal Wall is a visible structure from across the aisle; two visitors visibly racing it with a bell, a sand timer, and tiles slapping onto a crimson wall draws crowds that a screen demo cannot. Spectators are the second pull.

**What goes on the Case File (Game 1 side):** scorekeeper handwrites final score, tiles-placed, misplaces, and lists 3–5 **"your tiles"** by title. The visitor also takes a **Polaroid instant print of their finished wall half** — captured by a staff Polaroid camera as they step away from the lane — and tapes it onto the Case File at the exit stand.

### 2.2 Game 2 — **Insight Hunt** (CIS) — *The Case Wall + The Oracle*

**Format:** a 3-minute solo detective case played **physically against a human Oracle**. The Oracle is an SME in a distinctive costume (crimson haori jacket, or a lab coat with a prominent **CIS** badge — the costume matters; it marks the role as theatrical and legitimises the ritual) who sits across from the visitor and literally **plays the role of CIS**. The Oracle holds a thick ring-bound **Oracle Binder** of pre-authored insights, and a cardboard slot sits in the table between them through which they slide physical **Citation Cards** across to the visitor as they answer questions.

Each of 2–3 **Case Booths** is a small curtained alcove (fabric walls, cosy, slightly theatrical) containing:
- A visitor stool and a 60 cm × 90 cm **Case Wall** (corkboard) on the back wall, with a cup of pushpins and a spool of coloured yarn.
- A visitor-side tabletop stocked with ~15 printed **Signal Cards** drawn from the same deck as the Signal Wall (plus any specific tiles called out by the Case Brief).
- The Oracle's side: the Oracle Binder, the Citation Card dispenser (a stack behind a slot), a 3-minute sand hourglass, a small boxing bell, an ink pad, and three rubber stamps (**Case Cracked** / **Lead Followed** / **Red Herring**).

**What happens in 3 minutes:**
1. The visitor hands over their Case File. The Oracle lets them pick a **Case card** blind from a face-down deck of ~10 pre-authored cases (*"The Quiet Launch"*, *"The Hiring Tell"*, *"The Price War"*, *"The Delisted Feature"*, …). The Oracle reads the case brief aloud, bilingual.
2. The Oracle flips the hourglass and rings the bell.
3. The visitor pins any Signal Cards they think are relevant to the Case Wall. They can get up and walk to the Signal Wall remnants (unused tiles from recent Rush rounds) to pick extra signals — a visible, deliberate design choice that stitches the two games.
4. The visitor asks the Oracle up to **5 questions** verbally during the 3 minutes. The Oracle flips to the matching page in the binder and reads the cited answer aloud — then slides a physical **Citation Card** through the slot (printed with the signal it cites and the source). The visitor pins it next to the related signal and runs **yarn** between them to form a case theory.
5. At the bell: visitor speaks their verdict and points to the 2 strongest pinned signals.
6. The Oracle checks the pre-authored answer key and stamps the Case File:
   - **Case Cracked** (correct verdict + 2 valid signals) → name goes on the Hunt Scoreboard, Insight Vault deck.
   - **Lead Followed** (defensible-but-not-the-intended verdict, or 1 valid signal) → still a win; sticker.
   - **Red Herring** (wrong path) → comedy consolation sticker: *"I fell for the red herring."* The Oracle then takes 30 seconds to show, with their own binder and Citation Cards, how CIS would have cracked it. This is often the strongest conversion moment.

**What this teaches about CIS:** that competitive-intelligence work is **asking the right question and getting a sourced, defensible answer in seconds**; that **citations are not a feature, they are the product**; and that this works at the pace of a conversation, not a database query. The Oracle isn't a cute chatbot cosplay — the Oracle *is* a human playing the role CIS plays in a real workflow, which lets the visitor physically experience the loop CIS is designed to shortcut.

**Why physical and why the Oracle:** no screen can convey what a human-across-the-table can. The Oracle makes the citation layer *tangible* (a card you hold); the Case Wall makes the reasoning layer *visible* (string you've pulled yourself). After the game, the SME can transition from Oracle to Product SME in a sentence (*"Everything the Oracle just did, CIS does in a chat window. Want a short real walkthrough back at my desk?"*) — and the real product demo lands on invited interest, not cold ambush.

**What goes on the Case File (Game 2 side):** Oracle writes case title (stamped from the Case deck), visitor's verdict, Citation Card indices they pinned, outcome stamp, and a handwritten one-line note.

### 2.3 The connective device — **the Case File**

A5 bilingual **carbon-copy form** on crimson card-stock, **triplicate**. Issued at the entry stand when the visitor's badge is scanned.

Front (Game 1 / Hanko):
- Visitor name (greeter fills in from badge).
- Rush final score, tiles placed, misplaces, lane colour.
- Scorekeeper initials.
- A blank taped-in panel for the Signal Wall Polaroid.

Back (Game 2 / CIS):
- Case title (rubber-stamped from the Case deck).
- Visitor's verdict (visitor hand-writes).
- 2 Citation Card indices (visitor hand-writes).
- Outcome stamp (Oracle).
- Oracle's handwritten one-line note.
- Three tick-boxes at the bottom — *follow up on: ☐ Hanko ☐ CIS ☐ Both* — ticked by the visitor at the exit stand.

Visitor copy goes home. Booth copy goes to the lead pipeline (digitised post-event by the ops runner — two typed fields per card: tick-box choice and Oracle note). Product-team copy goes to the retro envelope.

**Why one physical object across two games:** it is the single device that stitches the two product memories into one story without smushing the games together. It is also the only thing the SMEs and sales / BD need to look at to know what to say in the follow-up — handwritten, specific, and visibly human.

### 2.4 Flow and pacing per visitor

```
   Entry (badge scan, Case File issued, pick a Case card)  ~30s
   → Game 1: Label Rush at the Signal Wall                  90s
     (+ scorekeeper tally pass + Polaroid)                 ~45s
   → walk to a Case Booth                                  ~15s
   → Game 2: Insight Hunt with the Oracle                  180s
     (+ verdict + stamp)                                   ~30s
   → exit (tick-box, Insight Vault deck, stickers)         ~15s
   ─────────────────────────────────────────────────────────────
   Total per visitor                                     ~7 min
```

Visitors who only have time for one game play one; the Case File is still issued with whichever side was completed. SMEs are briefed to never pressure a visitor into Game 2 — the Rush alone is a complete, satisfying booth visit.

### 2.5 Throughput

- Game 1: 1 Signal Wall × 2 lanes × ~2.5 min per round (play + grade + reset) = **~48 Rush players/hour** across both lanes.
- Game 2: 3 Case Booths × ~4 min per case (incl. verdict + stamp + reset) = **~45 Hunt players/hour**.
- Expect ~60% of Rush players to continue to Hunt (the limiting factor); real sustained throughput ≈ **~28 full laps/hour** plus ~20 Rush-only visitors/hour, totaling ~**48 scanned badges/hour**.
- Over an 8-hour event day: **~380 scanned badges/day**. Lower than a digital-version booth, but with a higher souvenir-and-memory conversion rate per visitor — §5 targets reflect this trade-off deliberately.

### 2.6 The ambient attractor — **The Scoreboard** (hand-updated)

A 2 m × 1.5 m dark-stained **wooden Scoreboard** mounted above the booth, visible from across the aisle. A dedicated **Scribe** (staff role, bilingual, calligraphic-handed) updates it continuously throughout the day with slide-in name/score tiles and chalked annotations. Three sections:

1. **Rush Leaderboard** — top 10 scores of the day, name + lane + score, tiles sliding in and out as scores change.
2. **Hunt Scoreboard** — Cases Cracked today, each one as a slide-in tile that reads *"[name] cracked [case]"*.
3. **Championship** — the current peak-slot Championship Hunt case title and reigning champion.

The Scribe is a performance in its own right: visitors stop to watch tiles being slid in and names chalked. In a hall full of static digital displays, a human visibly updating a wooden Scoreboard is unusual enough to be the aisle pull by itself.

### 2.7 Peak-slot bonus — **"Championship Hunt"**

Once per peak slot (post-keynote, lunch, mid-afternoon), the Scribe chalks a single harder public case title onto the Championship section of the Scoreboard. Any Hunt visitor during the slot plays that case. End-of-day Championship winner gets the big prize (§4.5). The public case title doubles as a conversation starter among visitors in the aisle.

### 2.8 Why two distinct physical games is the right primary bet

- **Pattern-break at RTC.** A hall full of screens makes a crimson wooden-and-magnet booth with a sand timer, a boxing bell, and a costumed Oracle stand out visually and acoustically. People stop to find out what it is before they know what the products are.
- **Zero demo-environment risk.** No connectivity, no software, no reset flow to debug. The booth works the day the trucks arrive. Setup risk collapses to physical props arriving on time and the Oracle Binders being proofed.
- **Two memorable products, not one hybrid blur.** Visitors tell a colleague about each product in one sentence because they played a game that belonged to that product.
- **Two personalities, two moods.** Rush is loud, physical, head-to-head, aisle-facing. Hunt is quiet, focused, theatrical, aha-driven. The booth has range; nothing competes with itself.
- **Lower bounce.** A visitor who only has 2 minutes plays Rush and leaves happy. A visitor with 7 plays both. Nothing is wasted either way.
- **Clean lead segmentation.** The Oracle naturally hears whether the visitor talks like a Hanko lead (fast decisions, misplace patterns, workflow questions) or a CIS lead (prompt phrasing, citation reasoning, synthesis questions) — and the handwritten Case File note captures that.
- **The pipeline story is still there, carried by the Case File and by the shared Signal Cards.** The best moment of Game 2 — the visitor walking to the Signal Wall remnants and grabbing a tile *they themselves placed in Rush* — is impossible without Game 1 having happened first. Visitors feel the pairing without having to be told about it.
- **Reusable physical kit.** Every prop travels. The Signal Wall folds down into panels. The Case Booths pack flat. The Oracle Binders fit in a suitcase. This is a kit that goes to Rakuten Optimism, campus events, and internal BU roadshows for a year.

---

## 3. Alternative concepts (ranked for RTC fit)

Each is a credible headline act if a constraint (space, team, lead time, audience depth) rules out Rush & Hunt. Several are strong **sidecars** alongside Rush & Hunt and are flagged as such. All alternatives in this section are themselves physical — the digital arcade concept from an earlier draft is dropped entirely because it would break the booth's design principle.

### Alt A — **Signal Hunt** (Monopoly-style card game — honors the original cue)

A tabletop card game, 2–4 players, 15 minutes, playable by walk-ups and takeable home as a boxed set.

Decks:
- **Signal cards** — real-world competitive signal archetypes (pricing screenshot, job post, patent filing, exec move, earnings quote, app-store review, ad creative). Laid out face-up as a shared "market."
- **Specialist cards** — Hanko annotator archetypes (Pricing Specialist, Hiring Analyst, Legal Reviewer, Multimodal Specialist, Generalist). Each player holds a small hand.
- **Insight cards** — the goal deck. Each insight requires 3–5 processed signals of specific types to "unlock" (e.g. *"Competitor X is about to launch a payments product"* needs 2 Hiring + 1 Patent + 1 Pricing signal).
- **Market Event cards** — periodic shocks (*"Earnings call tomorrow — pricing signals double in value this turn"*).

Turn structure:
1. **Hanko turn** — assign a Specialist to a Signal to "process" it (place a tag on the card). Specialists tire; high-value signals need multi-player consensus (a nod to Hanko's review workflow).
2. **CIS turn** — once you have the right 3–5 processed signals, you can submit a "chat query" — draw the top matching Insight card. If you can defend it (quick say-out-loud), you score; wrong insights cost points.
3. **Market Event** — every third turn.

Honors the user's "like Monopoly" cue; game loop is literally the product loop — label signals, submit a query, extract an insight. Also packages as a souvenir deck. **Strong sidecar** at Rush & Hunt as a side table for visitors who want to linger or wait for a Rush slot.

### Alt B — **"Chat with the Data" live gameshow (physical)**

A small stage area with three contestant podiums and a **giant pin-board wall** (3 m × 2 m corkboard) instead of a screen. During peak slots a bilingual host runs **10-minute rounds** of 3 contestants. Each round features a fresh case brief read aloud. Contestants are each given 20 physical Signal Cards and the host plays the Oracle role for all three simultaneously, answering their questions with Citation Cards. Contestants pin signals and Citation Cards to their third of the pin wall and defend their verdict to the host, who adjudicates against a pre-authored answer key. Crowd votes with RED / GREEN paper paddles.

Best for: pulling crowds in defined peak windows; converting the aisle into an audience; produces highlight photos for Rakuten Tech social channels.
Weakness: thin on hands-on learning; needs a host with real energy.

### Alt C — **Competitive Intelligence Escape Room**

4 players, 20 minutes, 1 facilitator, one private curtained pod. Scenario: *"Rakuten's strategy team has 30 minutes before a board meeting. The CEO wants a defensible hypothesis about what Competitor X is about to launch."* Players move through three mini-phases: triage a stack of physical signal cards on a table, sort relevant ones onto a timeline wall, then interrogate an Oracle (just like Hunt but with more questions and a deeper binder) to extract a final defensible insight before the timer. The game ends with the team *writing* a one-paragraph board brief on carbon paper.

Best for: BU heads, enterprise visitors, CFO/CRO-adjacent personas. Highest learning depth per visitor-minute of any format here.
Weakness: low throughput (≈ 12 visitors/hour).

### Alt D — **Insight Vault** (take-home trading card deck)

A 36-card deck in a crimson tuckbox for every scanned visitor. Suits:
- **Signals (12):** canonical competitive-signal archetypes.
- **Specialists (8):** Hanko annotator roles.
- **Prompts (8):** reusable chat-with-the-data prompt patterns, each a mini playbook ("Compare pricing posture", "Decode hiring intent", "Reconstruct a product roadmap from release notes").
- **Insights (8):** historical insights that moved markets, with the signal chain that could have predicted them in hindsight.

Printed one-page rules teach a 10-minute 2-player draft game. Pure take-home; smallest booth footprint; best "survives the plane ride home" artifact.

Best for: the universal leave-behind; works even when staffed by one person.
Weakness: no live experience in the booth on its own.

### Trade-off summary

| Concept | Throughput / hour | Depth | Floor space | Staff | Souvenir | Social media | Sidecar fit with Rush & Hunt |
|---|---|---|---|---|---|---|---|
| **Rush & Hunt (primary — two physical games)** | ~28 full laps + ~20 Rush-only | High (hands-on, both products) | Medium–Large | 5–6 | Case File + Polaroid | High (physical booth is photogenic) | — |
| Signal Hunt (card game) | ~16 per table | Medium | Small per table | 1 per table | Boxed deck | Low | **Strong** |
| Chat with the Data (gameshow) | ~24 contestants, large audience | Medium | Large (stage area) | 1 host + 1 scorer | No | **High** | Strong (peak-hour only) |
| CI Escape Room | ~12 | **Highest** | Medium pod | 1 facilitator | Carbon-copy brief | Low | Strong (back-corner exec pod) |
| Insight Vault (deck) | n/a (handout) | Low in-booth | Small | 1 | **Yes (deck)** | Low | **Always include** |

### Recommended stacks

- **Default stack:** Rush & Hunt (primary) + Insight Vault (universal take-home) + a scheduled Chat with the Data round once per peak slot (reuses the Signal Wall after Rush is paused for the slot). Covers pull, depth, souvenir, and highlight photos with one coherent brand.
- **Small-booth stack:** Signal Hunt tabletop + Insight Vault. One shared table, two staff, small footprint, honors the original Monopoly-style cue. No live Rush & Hunt experience; the game and the deck carry both products.
- **Enterprise-first stack:** Rush & Hunt + CI Escape Room in the back corner for exec visitors + Insight Vault. Lower overall throughput, but every lead is high-quality.

---

## 4. Booth logistics

Because the booth is all-physical, "logistics" is overwhelmingly about **fabrication, print, props, and staff** — not about demo environments, networking, or kiosk management. The implications are concrete.

### 4.1 Footprint

- **Minimum (small-booth stack):** 2 m × 3 m. One Signal Hunt table, one Insight Vault counter.
- **Default (recommended):** 3 m × 4.5 m. Rush & Hunt layout: the Signal Wall as the aisle-facing structure (with its two playing lanes and scorekeeper chalkboards), 2–3 Case Booths behind it (curtained alcoves), entry stand with the Case File pad and Case card deck, exit stand with the Polaroid camera and Insight Vault swag, the wooden Scoreboard mounted high above the booth.
- **Preferred:** 4 m × 5 m. Adds a back-corner CI Escape Room pod and the Chat with the Data stage apron (which borrows the Signal Wall during its scheduled slots).
- **Backdrop:** Rakuten crimson wall-mounted panels with bilingual tagline — *"ラベルから、インサイトへ。90秒で。 / From labels to insights, in 90 seconds."*

### 4.2 Physical bill of materials (default stack)

Signal Wall and Rush lane props:
- 1× 2 m × 2.5 m magnetic Signal Wall, modular panels, Rakuten crimson, with a visible 6×4 grid, bilingual cell labels, printed in crimson/white/charcoal.
- ~200× printed magnetic **Signal Tiles** (postcard size, bilingual, both sides printed: front = the signal, back = the correct cell).
- 2× hoppers (one per lane), with a *"Skip"* tray at each lane.
- 2× large **sand timers** (90-second), mounted at scorekeeper eye-level.
- 2× **boxing bells** on wooden plinths, scorekeeper-operated.
- 2× lane-side **chalkboards** for live misplace tally, with chalk + eraser.
- 1× staff-held **Polaroid instant camera** (and ~1,000 film sheets for the event).

Case Booth props (×2–3):
- Fabric curtain alcoves, prefab or Velcro-mounted frames (packable).
- 1× 60 cm × 90 cm corkboard **Case Wall** per booth.
- Pushpins, coloured yarn spools, visitor stool, visitor-side tabletop.
- 1× ring-bound **Oracle Binder** per booth (~60 pre-authored insight pages, bilingual, laminated).
- 1× **Citation Card** dispenser slot + ~500 printed Citation Cards per booth.
- 1× 3-minute sand hourglass.
- 1× small boxing bell.
- 3× rubber stamps (Case Cracked / Lead Followed / Red Herring) + ink pad.
- 1× Oracle costume per Oracle (crimson haori or lab coat with CIS badge).

Scoreboard:
- 1× 2 m × 1.5 m dark-stained wooden Scoreboard with slide-in tile tracks (three sections: Rush Leaderboard, Hunt Scoreboard, Championship).
- ~200× blank slide-in tiles, chalk, calligraphy brush pens for the Scribe.

Entry and exit stands:
- 1× entry desk with a bilingual greeter, Case File carbon pads (triplicate), pencils, Case card deck.
- 1× handheld **badge scanner** (standard conference equipment — the only electronic device on the booth).
- 1× exit counter with the Polaroid camera, Insight Vault decks, sticker trays.

Take-home swag:
- 500× Insight Vault decks + tuckbox + one-page rules insert.
- 50× boxed Signal Hunt decks (if running Alt A sidecar).
- Sticker sheets (incl. *"I fell for the red herring"*) + crimson lanyard pins.

### 4.3 Booth team (per shift, default stack)

| Role | Count | What they do |
|---|---|---|
| Entry greeter + Rush announcer | 1 | Scans badges, issues Case Files, runs the Case card draw, calls Rush rounds like a boxing match ("Red lane vs. Blue lane, 90 seconds, GO") |
| Rush scorekeepers (Hanko) | 2 | One per lane. Flip the sand timer, ring the bell, tally misplaces on chalkboard, grade in 15 seconds, use misplaces as the opener for the real Hanko conversation |
| Oracles (CIS) | 2 | One per Case Booth (3 if running 3 booths — rotate so Oracles rest). In costume, in character. Reads briefs, flips binder, slides Citation Cards, stamps Case Files |
| Scribe | 1 | Updates the wooden Scoreboard continuously, chalks Championship cases at peak slots. Bilingual, calligraphic-handed. The Scribe is itself a visible performance |
| Lead-capture host | 1 | At the exit stand. Takes the booth copy of the Case File, hands over Polaroid + Insight Vault deck + sticker, confirms the tick-box choice |
| Event ops / runner | 1 | Resets Signal Wall tiles between rounds, reloads hoppers, swaps spent Oracle Binder pages, troubleshoots jams, hosts the Chat with the Data peak slots |

Total: **8 staff per shift** for the default stack. Rotate Oracle roles every 60 minutes (performing is tiring); rotate scorekeepers and the Rush announcer every 90 minutes.

### 4.4 Pre-event, event, post-event funnel

**Pre-event (T−8 weeks → T−1 day)**
- Author the ~200 Signal Tiles with product + legal review (every tile is a real-ish competitive signal; competitors are safely genericized).
- Author the Oracle Binder: ~10 cases × ~6 pre-authored questions-and-answers each, each answer tied to a Citation Card. Every case tested end-to-end in a mock booth day with real visitors from internal BUs.
- Fabricate the Signal Wall, Case Booth frames, Scoreboard, hoppers, bells, timers. Print tiles, Case Files, Citation Cards, Case card deck, Insight Vault decks, Signal Hunt decks.
- Teaser landing page on tech.rakuten.co.jp: *"Rush. Hunt. Crack the case. Booth XX at RTC."* Optional reservation link for Chat with the Data contestants.
- Run **three internal mock booth days** — one to time Rush, one to time Hunt, one combined — to shake out physical flow issues (hopper jams, Oracle fatigue, Scribe pacing).

**During event**
- Championship Hunt case chalked on the Scoreboard at the top of each peak slot; running leaderboard across the day.
- Two Chat with the Data gameshow rounds per peak slot (Rush paused during each round so the Signal Wall is free as the stage backdrop).
- End-of-day prizes: top Rush score of the day, top Hunt score (fastest **Case Cracked**), best "Red Herring recovery" (judged by Oracles).
- Rakuten Tech social team captures stills: Rush H2H duels, Oracle-in-costume moments, the Scribe updating the Scoreboard, visitors pinning yarn on their Case Walls, Championship winner holding their Case File.

**Post-event (T+1 → T+14 days)**
- Ops runner digitises the booth copies of the Case Files overnight (two typed fields per card: tick-box choice + Oracle note). Lead pipeline splits into **Hanko**, **CIS**, and **Both** queues.
- Email every scanned badge: thanks, a photo of the Signal Wall / Case Booth they played at, a 90-second product video for their chosen product(s), calendar link for a real walkthrough.
- Internal retro: which Hunt questions did visitors naturally ask the Oracle → directly feeds the CIS prompt-library and product roadmap; which Signal Wall subtypes did visitors most confuse → directly feeds Hanko's training / onboarding UX.
- Blog post: *"800 visitors sorted 8,000 tiles in two days — what RTC taught us about annotation UX, with photos of the booth."*

### 4.5 Prizes

- **Daily championship:** Rakuten crimson mechanical keyboard + 1 year of Rakuten service credits. One per day for the top Championship Hunt crack and one per day for the top Chat with the Data contestant.
- **Rush top-of-the-hour:** limited-edition "Rush Champion" acrylic desk piece for the top head-to-head score each hour.
- **Everyone:** Insight Vault deck + sticker set + Case File + Polaroid of their Signal Wall. The *"I fell for the red herring"* sticker is deliberately the most asked-for item; make plenty.

### 4.6 Budget (rough order of magnitude, JPY)

| Item | Est. cost |
|---|---|
| Signal Wall fabrication (modular panels, grid printing, mounting) | ¥600k–¥1.0M |
| Signal Tile print run (200 bilingual two-sided magnetic tiles, 2 full sets for safety) | ¥400k–¥700k |
| Case Booth fabrication × 3 (frames, curtains, corkboards, tabletops, packable) | ¥500k–¥900k |
| Oracle Binders (contents authored + bilingual rewrite + lamination, 3 copies + 1 spare), Citation Cards (~1,500), Case card decks (2) | ¥500k–¥900k |
| Scoreboard fabrication + slide-in tiles + Scribe tools | ¥300k–¥500k |
| Case File carbon-copy pads (1,000 triplicate forms, bilingual print), rubber stamps, ink pads, Polaroid camera + ~1,000 film sheets | ¥400k–¥700k |
| Backdrop + crimson booth build + lighting + bells + sand timers + hoppers + Oracle costumes | ¥600k–¥1.0M |
| Signal Hunt deck design + print (50 boxed) | ¥300k–¥500k |
| Insight Vault deck design + print (500) | ¥300k–¥500k |
| Prizes | ¥300k–¥500k |
| Staff T&E, training, three internal mock booth days, Oracle rehearsals | ¥700k–¥1.2M |
| **Total (indicative)** | **¥4.9M–¥8.4M** |

Everything in the top seven rows (fabrication + print + binders + stands + swag) is **physical, reusable kit**. It travels to Rakuten Optimism, campus events, enterprise sales roadshows, and internal BU briefings for the following 12 months. The Signal Wall folds down into panels, the Case Booths pack flat, the Oracle Binders fit in a suitcase. This is a **durable kit**, not an RTC-only expense.

---

## 5. Success metrics

| Metric | Target at RTC |
|---|---|
| Unique badges scanned | ≥ 400 |
| Rush rounds played | ≥ 400 over the event |
| Hunt cases attempted | ≥ 250 |
| Hunt cases scored **Case Cracked** | ≥ 100 |
| Full laps (Rush + Hunt by the same visitor) | ≥ 220 |
| Signal Tiles correctly placed at Rush (cumulative) | ≥ 5,000 |
| Chat with the Data contestants | ≥ 50 across the event |
| Case Files taken home | ≥ 400 |
| Signal Wall Polaroids handed out | ≥ 400 |
| Qualified follow-up leads tagged **Hanko** | ≥ 25 |
| Qualified follow-up leads tagged **CIS** | ≥ 25 |
| Qualified follow-up leads tagged **Both** | ≥ 15 |
| Social photos / clips published by Rakuten Tech channels | ≥ 10 |
| Post-event demo meetings booked within 14 days | ≥ 20 |

The two most valuable artifacts taken home from the event are **(1) the list of real questions visitors asked the Oracle** (directly feeds the CIS prompt-library and product roadmap) and **(2) the misplace heat-map of the Signal Wall** (which subtypes humans most confuse under time pressure — directly feeds Hanko's training / onboarding UX). Both are captured on paper during the event and digitised post-event by the ops runner.

---

## 6. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Signal Tiles get stolen or lost | Print 2 full sets (BOM already assumes this); ops runner audits the hopper every hour and re-stocks from reserves |
| Oracles burn out mid-day | Rotate Oracles every 60 minutes; keep 3 trained Oracles for 2 booths so one is always resting; Oracles are given a strict script "safety net" (binder is self-sufficient without improvisation) |
| Oracle Binder has a page error that misleads a visitor | Three internal mock booth days specifically to find and fix every binder page; each Oracle carries a highlighter and marks confusing pages for same-day proofing; errata printed and inserted overnight |
| Line forms at the Signal Wall and discourages new visitors | Rush is only 90s per round so the line moves fast; waiting visitors are given the Case File immediately and can draw a Case card early; Signal Hunt sidecar deck absorbs overflow |
| Rush feels like a kids' game to engineer visitors | The −2 misplace penalty and the Oracle's post-game breakdown of exactly *why* a given subtype was tricky makes it feel like a professional UX study, not a game show; the SMEs own that framing |
| Visitors conflate Hanko and CIS as "one product" | Two distinct games with their own identity, physical structure, and SME costume — this is the whole point of §2; Case File has one side per product; exit tick-box is one-tap |
| Hunt timer stresses visitors who dislike time pressure | Oracle can opt-in a visitor into "untimed mode" — no Scoreboard spot, but the case still stamps; Oracle offers this proactively to visitors who look hesitant |
| Enterprise visitors want more depth than Rush & Hunt offers | CI Escape Room back-corner pod; Oracles are briefed to escalate a hot post-Hunt conversation by booking a dedicated post-event walkthrough on the spot — tick the "Both" box on the Case File and hand-write *"HOT: book this week"* in the Oracle's note field. The real product demo happens next week at the lead's office or on video, not on the show floor |
| Legal / brand risk from showing real competitor data | Entire Signal Tile deck AND the 10 Oracle cases use safely genericized or fictionalised competitors; legal review is a hard gate before fabrication |
| Bilingual balance tilts to one language | Every tile, binder page, Citation Card, Case File form, and Scoreboard tile is JP + EN on the same face; two of the Oracles and the Scribe are hired bilingual |
| Chat with the Data flops in a quiet slot | Keep it tightly scheduled (2–3 slots per day, not continuous); if a slot has fewer than 2 contestants, convert to a "host demo" using one audience volunteer and a live Hunt case against the Signal Wall as backdrop |
| Props arrive damaged on load-in day | Spare set of the fragile items (hopper hardware, Scoreboard tile track, one Oracle Binder) travels in separate crate; booth build day T−1 is a hard-stop requirement, not an optional buffer |

Note: the risk categories "demo environment goes down", "venue WiFi unusable", "device battery dies", and "booth-ops dashboard breaks" are **not present on this physical booth by construction** — this is one of the quiet but material arguments for the all-physical design.

---

## 7. Decision ask

Approve for Rakuten Tech Conference:

1. **Primary format:** Rush & Hunt — two distinct physical games played back-to-back in one booth. Game 1: **Label Rush** at the Signal Wall (Hanko). Game 2: **Insight Hunt** with the Oracle (CIS). Tied together by **the Case File** (triplicate carbon-copy).
2. **Scheduled sidecar for crowd + social clips:** Chat with the Data physical gameshow, 2 slots/day, reusing the Signal Wall as the backdrop.
3. **Universal take-home:** Insight Vault trading card deck + Signal Wall Polaroid + Case File for every scanned visitor.
4. **Optional back-corner for enterprise visitors:** CI Escape Room pod.
5. **Budget envelope:** ¥5.5M–¥6.5M (mid-point of §4.6, assuming the Escape Room pod).
6. **Reuse plan:** the entire physical kit (Signal Wall panels, Case Booths, Oracle Binders, Scoreboard, Case File carbon pads, swag decks) is a durable asset reused at Rakuten Optimism, campus events, enterprise roadshows, and internal BU briefings for the following 12 months.

### If the ask is to pick a single, lower-cost format

Fallback: **Signal Hunt tabletop + Insight Vault take-home**. One table, two staff, a 2 m × 3 m footprint, no booth fabrication required. Honors the user's original Monopoly-style cue, teaches both products through the game loop, produces a souvenir. Weaker than Rush & Hunt on spectacle and hands-on product experience, but credible for a lean-staffed, short-lead-time, or very-small-footprint scenario.

---

## 8. Appendix — showing two products without confusing visitors

A booth with two products is harder than a booth with one, because visitors default to pattern-matching everything to a single pitch. Rush & Hunt handles this at the format level — two games, two mechanics, two moods, two SME roles with two distinct costumes (scorekeeper and Oracle). Four further guardrails:

- **Each game is complete on its own.** A visitor who only plays Rush still has a product memory for Hanko. A visitor who only plays Hunt still has one for CIS. We never force a merge.
- **Separate pipelines on the back-end from day one.** The Case File has three tick-boxes at the bottom — *Hanko / CIS / Both* — ticked by the visitor at the exit stand. The Oracle's handwritten one-line note is the second signal.
- **Separate sections on the Scoreboard.** The **Rush Leaderboard** (Hanko: top scores, lane, tiles placed) and the **Hunt Scoreboard** (CIS: Cases Cracked, fastest crack of the hour, Championship standings). Each product's PM gets a clean metric.
- **Separate secondary accent colours inside a single Rakuten crimson brand.** The crimson is the booth; a secondary accent per product keeps iconography distinct on Signal Tiles vs. Citation Cards, on scorekeeper vs. Oracle costumes, on each half of the Case File.

If, after internal piloting, the two games feel too tightly bundled for one of the products' PMs, the correct next move is **not** to split the booth — it's to lengthen one game. Rush can grow a 60-second "review" round (showing Hanko's QA workflow explicitly, with visitors re-sorting the previous player's wall) without touching Hunt. Hunt can grow a 60-second "multi-signal synthesis" extra round without touching Rush. Each product owns its own game and can evolve it independently across future events.

---

## 9. What this document is not

- Not an authored list of the ~200 Signal Tiles or the 10 Oracle cases (both need product + legal input and a copywriter).
- Not a fabrication spec for the Signal Wall, Case Booth frames, Scoreboard, or hoppers (needs a booth-build partner).
- Not a script for the Chat with the Data gameshow rounds (needs an MC and a dry-run).
- Not print-ready artwork for the Case File carbon pads, Signal Hunt deck, Insight Vault deck, or Citation Cards (each needs an illustrator and a copywriter).
- Not a signed-off budget — the §4.6 figures are rough-order-of-magnitude for an initial go/no-go.

If this concept is approved, the three parallel critical-path workstreams are:

1. **Content:** authoring and legal-reviewing the ~200 Signal Tiles and the 10 Oracle cases + Citation Cards.
2. **Fabrication:** booth-build partner for the Signal Wall, Case Booths, Scoreboard, Case File carbon pads, Oracle Binders.
3. **Rehearsal:** three internal mock booth days with real visitors (BU champions and friendly engineers) to shake out physical flow, Oracle fatigue, and binder accuracy before the trucks leave for Yokohama.

The long-pole item for RTC readiness is **(1) content authoring + legal review**, not fabrication. If content slips, no amount of great fabrication will save the booth.
