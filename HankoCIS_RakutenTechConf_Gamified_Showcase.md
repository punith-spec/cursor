# Hanko CIS at Rakuten Tech Conference — Gamified Showcase Proposal

**Event:** Rakuten Technology Conference (https://tech.rakuten.co.jp/)
**Product:** Hanko CIS — Rakuten's digital approval / stamp workflow module inside the Common Information System
**Deliverable in this doc:** Booth concept, mechanics, logistics, and a short-list of alternative formats

The brief was: *showcase Hanko CIS in a gamified way, like a Monopoly card game or similar*. This proposal takes that cue seriously, picks a primary concept, and lines up credible alternatives with trade-offs so the team can choose based on floor-space, headcount, and the audience we want to reach.

---

## 1. Why gamify this product at Rakuten Tech Conference

Hanko CIS is a workflow / compliance product. Workflow products demo badly in slide decks — they look like forms — but they *feel* great when the visitor physically experiences the delay of the old way vs. the speed of the new way. A gamified booth turns a dry workflow story into a 10-minute lived experience, which is what the Rakuten Tech Conference crowd (external engineers, PMs, enterprise architects, and curious Rakuten employees from other BUs) actually remembers after a long day of talks.

The booth has three jobs, in order:

1. **Pull people in** from the aisle — a visible, noisy, inviting game beats a monitor loop every time.
2. **Teach three things** in under 10 minutes: what Hanko CIS replaces, what it does, and what it unlocks for the business.
3. **Leave a trail** — a scanned badge, a ranked leaderboard entry, a souvenir card — so Sales / BD can follow up next week with a warm hand-off.

Design constraints we should respect for RTC:

- Rakuten brand: Crimson (#BF0000), Rakuten Sans JP, English + Japanese bilingual signage.
- Mixed audience: Japanese business decision-makers *and* English-speaking engineers. Zero-reading entry.
- Short dwell: median conference booth attention is 3–8 minutes. A longer game needs a visible "come back after your next talk" hook.
- Noise floor: a quiet puzzle will get drowned by neighbouring sponsor booths. Pick formats that benefit from the ambient energy.

---

## 2. Recommended concept — **Hanko Street** (Monopoly-style card + board game)

A tabletop board game inspired by Monopoly, re-skinned around the real-world pain of multi-party Japanese approval workflows. The game teaches Hanko CIS's value proposition by making players *feel* the cost of the paper workflow and *experience* the shortcut Hanko CIS provides.

### 2.1 Theme

The board is a loop of eight **Approval Districts** that mirror the real approver chain in a Japanese enterprise:

- 人事 HR
- 法務 Legal
- 財務 Finance
- 購買 Procurement
- IT セキュリティ IT Security
- コンプライアンス Compliance
- ベンダー管理 Vendor Management
- 内部監査 Internal Audit

Four "Hanko CIS Hub" squares sit on the corners — the equivalent of Monopoly's railway stations. Landing on a Hub lets you *digitize* workflows you own, which is where the central mechanic kicks in.

### 2.2 Core loop (one turn, ~45 seconds)

1. **Roll** two custom dice. One die is standard 1–6. The second die is a 日/CIS die with three "paper hanko" faces and three "digital hanko" faces.
2. **Move** your meeple to a district.
3. **Draw** the top **Workflow Card** for that district. The card describes a real Rakuten-style scenario (e.g. "新規SaaSベンダー契約 — approval needed from Legal, IT Security, and Procurement").
4. **Resolve** the card based on the second die:
   - 📄 Paper face → you must physically collect **three stamp tokens** from other players over the next two turns before the workflow "clears". Until it clears, your meeple sits idle (you still roll, but you don't collect income).
   - ⚡ CIS face → the workflow clears instantly. You draw an **Insight Chip** showing the real Hanko CIS feature that enabled the shortcut (parallel routing, delegated authority, audit trail, policy-as-code, etc.).
5. **Earn** ¥ Yen tokens for cleared workflows. Insight Chips are also worth bonus ¥ at end-game and are the only way to buy district upgrades.

### 2.3 The two special card decks

**Compliance Chest (コンプライアンス)** — replaces Monopoly's Community Chest.
Example cards:
- "SOX audit scheduled next week. All players with unresolved paper workflows lose one turn."
- "You discover a missing hanko on a 3-month-old contract. Pay ¥50 unless you have an Audit Trail Insight Chip."
- "Policy update: non-CIS workflows now require an extra approver. Draw an extra Workflow Card on your next paper roll."

**Urgency Cards (至急)** — replaces Chance.
Example cards:
- "急な取引先訪問. Immediately clear one Workflow — but only if it was digitized."
- "Vendor needs an answer today. The next paper workflow you draw costs you ¥100."
- "A manager is 出張 (on business travel) for a week. CIS mobile delegation clears all your pending approvals for free."

Every card is designed to create a *memorable micro-moment* that maps 1:1 to a real CIS feature or a real paper-workflow pain. These are the moments the visitor will quote to a colleague the next day.

### 2.4 Winning

Game ends when any player clears **4 end-to-end workflows** OR after a fixed 15-minute timer, whichever comes first. Winner = highest total of (¥ earned + Insight Chip bonuses). The game is tuned so a player who leans into Hanko CIS wins ~75% of the time — the lesson is in the win rate, not the lecture.

### 2.5 What the player walks away with

- **Souvenir card** — a 55×85 mm playing card listing the Insight Chips they collected, with QR → `tech.rakuten.co.jp/hanko-cis`.
- **Ranked spot** on a visible leaderboard screen (fastest win, highest ¥).
- **A memory** of being physically slowed down by paper, which is the *only* way a workflow pitch sticks.

### 2.6 Why this concept is the right primary bet

- It directly honours the user's "like a monopoly card game" cue.
- It is **learned by playing**, not by reading a sign.
- The paper-vs-digital mechanic is the pitch, baked into the dice. No one has to say it out loud.
- Scales from 2 to 6 players per table; multiple tables run in parallel.
- Produces a souvenir and a leaderboard story — natural social-media and follow-up fodder.

---

## 3. Alternative concepts (ranked for RTC fit)

Each alternative is a credible choice if a constraint (space, team size, visitor demographics, dev vs. exec audience) rules out Hanko Street.

### Alt A — **Stamp Rally (スタンプラリー)** — highest throughput

A classic Japanese stamp-rally re-skinned for CIS. Visitors get a 6-panel rally card at the entrance and move between **six micro-stations** inside the booth, each a 60-second demo of one Hanko CIS capability:

1. 承認ルーティング — route a mock contract through 3 approvers.
2. 代理承認 — delegate while an approver is 出張.
3. ポリシー自動チェック — try to sneak a non-compliant doc past the system.
4. 監査証跡 — reconstruct who stamped what, when, why.
5. モバイル承認 — approve from a phone in <10 seconds.
6. 外部ベンダー招待 — bring a vendor into the loop with least-privilege access.

Each station gives a different physical stamp. Fill all six → spin a prize wheel. Highest throughput of any format; lowest emotional stickiness.

### Alt B — **Approval Racer** — spectacle magnet

Two monitors side-by-side on a tall display. On one side, a visitor races through a paper-and-email approval chain (clicking, scanning, chasing). On the other, a second visitor races through the same chain in Hanko CIS. Live clock on both. Big screen above shows the daily leaderboard of fastest CIS clear times. The paper side is intentionally hard; it is *supposed* to lose. Audience watches, cheers, roasts.

Best for: pulling crowds from the aisle; social-video clips.
Weakness: light on substance for enterprise buyers.

### Alt C — **Hanko Heist (escape-room card game)** — best for exec visitors

4 players, 1 facilitator, 20 minutes. The team inherits a fictional Rakuten subsidiary's compliance backlog two days before an external audit. They must clear 12 workflows cooperatively while **Compliance Risk** cards tick up. Decision cards force genuine trade-offs: "Approve now and risk a policy violation, or escalate and risk missing the audit deadline?" Hanko CIS features appear as "Tool Cards" the team can unlock mid-game.

Best for: Rakuten BU heads, enterprise visitors, CFO/CRO personas who want to *reason* about the product.
Weakness: lower throughput; needs a dedicated facilitator.

### Alt D — **CIS Trading Card Deck** — best take-home

A collectible-style 36-card deck handed to every booth visitor. Cards are grouped: Approvers (HR, Legal, Finance...), Policies (SOX-J, J-SOX exceptions, vendor onboarding), Risks (rogue stamp, missing audit trail, unauthorised delegation), and Tools (Hanko CIS features). A printed one-page rules sheet teaches a 2-player 10-minute draft game.

Best for: swag that survives the plane ride home; booth is low-footprint; works even when staffed by one person.
Weakness: no live experience inside the booth.

### Trade-off summary

| Concept | Throughput / hour | Depth of learning | Floor space | Staff needed | Souvenir | Social-media appeal |
|---|---|---|---|---|---|---|
| **Hanko Street (primary)** | ~24 (4 tables × 6 players/15 min) | High | Medium–Large | 3–4 | Yes (card) | Medium |
| Stamp Rally | ~120 | Medium | Medium | 2 + 6 micro-stations unmanned | Yes (rally card) | Low |
| Approval Racer | ~60 (two seats, 2 min) | Medium | Small–Medium | 2 | No | High |
| Hanko Heist | ~12 | Highest | Medium (one table) | 1 facilitator | Yes (certificate) | Low |
| Trading Card Deck | n/a (handout) | Low in-booth | Small | 1 | Yes (deck) | Low |

**Recommendation:** Lead with **Hanko Street** on the main table, run **Stamp Rally** around it for walk-up throughput, and give every visitor the **Trading Card Deck** as the leave-behind. That stack covers crowd-pull, depth, and take-home with one coherent brand.

---

## 4. Booth logistics

### 4.1 Footprint

- **Minimum:** 3m × 3m. Fits one Hanko Street table (seating 6), a leaderboard screen, and a swag counter.
- **Preferred:** 3m × 4.5m or 4m × 4m. Adds two more Hanko Street tables (parallel sessions), the stamp-rally perimeter, and standing space for spectators.
- **Backdrop:** Rakuten crimson wall with the English + Japanese tagline *"ハンコの速度で、ビジネスをもう一度 / Rediscover business at the speed of Hanko (CIS)."*

### 4.2 Materials bill of materials

Physical game components (per Hanko Street table):

- 1× printed game board (A1 or A0, hard-mounted, matte finish, Rakuten crimson accent)
- 6× meeple-style player tokens (laser-cut acrylic in CI brand palette)
- 2× custom dice (one standard, one paper/CIS die)
- 60× Workflow Cards (8 districts × 6–8 scenarios, bilingual)
- 24× Compliance Chest cards
- 24× Urgency Cards
- 48× Insight Chips (physical poker-chip style, printed with feature name)
- Play-money ¥ tokens
- Facilitator cheat-sheet laminated

Shared across booth:

- 55" leaderboard display with simple web app (fastest win, highest ¥, Insight-Chip-of-the-day)
- Scanner for conference badges to auto-register scores
- Trading Card Deck boxes (print run sized to expected traffic — see §4.5)
- Rally cards + 6 stamp stations (if running Alt A in parallel)

### 4.3 Booth team (per shift)

| Role | Count | What they do |
|---|---|---|
| Game master | 1 per table | Teaches rules in 60s, keeps turns moving, injects theatre on dramatic cards |
| Product SME | 1 floating | Steps in when a visitor wants the real demo after the game |
| Lead-capture host | 1 at swag counter | Scans badge, hands over the Trading Card Deck, confirms follow-up consent |
| Floor runner | 1 | Resets tables, refills swag, keeps the leaderboard screen alive |

Shifts should rotate every 90 minutes; facilitating is high-energy work.

### 4.4 Pre-event, event, post-event funnel

**Pre-event (T−4 weeks → T−1 day)**
- Teaser post on tech.rakuten.co.jp and Rakuten Tech X/LinkedIn: "Beat the paper hanko. Booth XX at RTC."
- Pre-register for a Hanko Street tournament slot via QR landing page.
- Internal all-hands brief: BUs who use CIS can send champions to spectate / recruit.

**During event**
- Hourly Hanko Street "championship round" (15-min, posted on the leaderboard).
- End-of-day "fastest CIS clear" prize announced at the booth.
- Live short-form video clips of dramatic Urgency Card moments pushed to Rakuten Tech socials.

**Post-event (T+1 → T+14 days)**
- Email to every scanned badge: thanks, your leaderboard spot, a 90-second demo video, and a calendar link for a real walkthrough.
- Internal retro the week after: which Insight Chips were drawn most → which features resonate most → feed into roadmap storytelling.

### 4.5 Prizes

- **Championship prize** (one per day): a Rakuten Crimson mechanical keyboard + 1-year Rakuten service credit.
- **Round winners**: a limited-edition "Hanko CIS Champion" acrylic hanko token (practical and on-brand).
- **Everyone**: Trading Card Deck + sticker set.

Avoid gift-card-only prizes; the hanko token is the thing people will photograph.

### 4.6 Budget (rough order of magnitude, JPY)

| Item | Est. cost |
|---|---|
| Game design + bilingual copy + card illustrations (one-time) | ¥800k–¥1.2M |
| Print run (3 full table sets + 500 trading-card decks + rally cards) | ¥400k–¥700k |
| Booth build + crimson backdrop + 55" display + scanner | ¥600k–¥1.0M |
| Prizes (3 championships + round winners + 500 swag kits) | ¥300k–¥500k |
| Staff T&E and training | ¥400k–¥800k |
| **Total (indicative)** | **¥2.5M–¥4.2M** |

Everything except prizes and T&E is reusable at Rakuten Optimism, Rakuten Tech Day, campus recruiting events, and internal BU roadshows. The game is an asset, not an expense.

---

## 5. Success metrics

| Metric | Target at RTC |
|---|---|
| Hanko Street games played | ≥ 120 over the event |
| Unique badges scanned | ≥ 500 |
| Rally cards completed | ≥ 300 |
| Qualified follow-up leads (BU / vendor / partner) | ≥ 40 |
| Internal BU conversations initiated at the booth | ≥ 10 |
| Social clips published by Rakuten Tech channels | ≥ 8 |
| Post-event demo meetings booked within 14 days | ≥ 20 |

Instrument everything. The leaderboard app should log every game outcome and every Insight Chip drawn — that dataset is marketing gold for the next event.

---

## 6. Risks and mitigations

| Risk | Mitigation |
|---|---|
| Rules take too long to teach, visitors bounce | Keep teach-script to 60 seconds; laminated cheat-card at every seat; game master demos one turn before handing off |
| Game ends feeling anti-paper rather than pro-CIS | Insight Chips must be celebrated; game master calls out *why* each chip matters when drawn |
| Table dominated by one aggressive player | 15-minute hard timer prevents runaway; Compliance Chest cards include a mild rubber-band mechanic |
| Bilingual balance tilts to one language | Every card is JP + EN on the same face; game masters are hired bilingual |
| Visitors want the real product, not the game | Floating Product SME is explicitly for this; iPads loaded with the real Hanko CIS demo at the swag counter |
| Line forms and discourages new visitors | Stamp Rally runs as the "line entertainment"; visitors earn stamps while waiting for a Hanko Street seat |
| Game feels gimmicky to enterprise buyers | Hanko Heist (Alt C) table in the back corner for exec-level visitors who want depth |

---

## 7. Decision ask

Approve the following for Rakuten Tech Conference:

1. **Primary format:** Hanko Street (Monopoly-style) on 3 tables.
2. **Supporting format:** Stamp Rally around the perimeter for throughput.
3. **Leave-behind:** CIS Trading Card Deck for every scanned visitor.
4. **Budget envelope:** ¥3.0M–¥3.5M (mid-point of §4.6).
5. **Reuse plan:** game assets travel to Rakuten Optimism, campus events, and internal BU roadshows for the following 12 months.

If the ask is to pick a single, lower-cost format, the fallback recommendation is **Stamp Rally + Trading Card Deck**: it is the smallest-footprint, highest-throughput, lowest-staffing combination that still delivers a bilingual, physical, memorable experience aligned with Hanko CIS's value proposition.

---

## 8. Appendix A — Further creative formats to consider

Section 3 covered the four strongest alternatives to Hanko Street. The brief invited *"any similar engaging way you can suggest"*, so this appendix lists additional formats that are credible for RTC. They are grouped by what they are best at — pick one or two to mix into the booth stack if a slot in §3 does not fit, or swap one in as the headline act if the audience or floor space changes.

### 8.1 Culturally resonant formats (lean into Japan)

**A1 — ハンコかるた / Hanko Karuta**
Traditional Japanese karuta reimagined. A reader calls out a workflow scenario in Japanese (*"稟議書が3人の承認者を回り、1人が出張中…"*); 2–4 players race to slap the correct Hanko CIS **feature card** on the table. The person with the most cards at the end wins. Culturally native, bilingual-friendly (reader alternates JP/EN rounds), high clap-and-laugh factor. ~5 min/round, 2–4 players, 1 reader. Great complement to Hanko Street rather than a replacement.

**A2 — 承認パチンコ / Approval Pachinko**
A single themed pachinko machine on the booth floor. The ball represents a document; the pins and gates represent approvers, policies, and audit checks. In "Paper" mode (lever on the left) the ball bounces chaotically through all gates; in "CIS" mode (lever on the right) magnet-activated gates route the ball along the optimal path and the win-tray lights up. Pure spectacle, deeply Japanese, extremely filmable. 30 seconds per play, continuous throughput, zero reading required. Highest aisle-pull of any format in this document.

**A3 — Hanko Pub Quiz / 承認トリビア・ナイト**
An after-hours event at the booth on day 1 or day 2 of RTC. Teams of 4 compete on bilingual trivia about Japanese business culture (hanko etiquette, 稟議 history), compliance (SOX-J, J-SOX exceptions, audit cycles), and Hanko CIS features. Light drinks + snacks (budget permitting). Builds **relationships**, not just leads — most valuable for the enterprise and BU partnership funnel. One 90-minute slot, 1 host, 2 scorers.

### 8.2 High-depth formats (for enterprise and exec visitors)

**A4 — Compliance Clue / 承認ミステリー (Whodunit)**
A whodunit tabletop game. The premise: a hanko on a ¥500M contract turns out to have been forged. Players are given a dossier (ten approvers, five policies, the contract, a partial audit log) and must identify **who forged**, **which policy they violated**, and **which audit control should have caught it**. The twist: at every impasse, a player can "spend" a Hanko CIS feature card to reveal a clue — making the point that CIS features are what *prevent* this scenario in production. 20 minutes, 3–5 players, 1 facilitator. Highest learning depth per minute of any format proposed.

**A5 — Workflow Catan (co-op variant)**
Settlers-of-Catan-style board where districts produce three resources: **trust tokens**, **evidence tokens**, and **approval tokens**. Players trade and build "approval routes" between districts. Unlike Monopoly, Catan is positive-sum — which maps better to the Hanko CIS story that *the whole org gets faster*, not that one BU wins. Alternative headline game for teams who dislike the zero-sum feel of Monopoly or want a more collaborative narrative for internal BU champions.

**A6 — "Among Us" — Rogue Approver edition**
Social-deduction hybrid (tabletop with a companion tablet app). Among 6 players, one is secretly the **Rogue Approver** trying to push a non-compliant document through. The others are **Compliance Officers** using Hanko CIS "audit tools" (role-reveal cards, delegation logs, policy snapshots) to catch them. Highly modern, Gen-Z and engineer-crowd friendly, extremely replayable. 10 minutes/round. Risk: rules take longer to learn than §3 formats — needs an energetic game master.

### 8.3 Spectacle / high-throughput formats (pull from the aisle)

**A7 — "Who Wants to Be a Hanko Millionaire" / ハンコ・ミリオネア**
Gameshow format on a tall screen during the peak morning and post-lunch slots. 3 contestants per round, 15 questions escalating from *"What is a 稟議書?"* to *"In a 7-approver chain with 2 delegations and 1 policy override, who ultimately bears audit responsibility?"* MC with a mic, lifelines ("Ask the Audience" using crowd clickers, "Call a CIS Expert" = the Product SME), stingers and lighting. 10-minute rounds. The **crowd gathering is itself the pull**; the round is just the hook.

**A8 — CIS Dojo (rhythm / arcade stamping)**
Taiko-no-Tatsujin-style rhythm game. 55" LED screen, two giant physical "stamp" buttons (one 👍 *Approve*, one 👎 *Reject*). Workflow scenarios scroll by in time with music; the player slams the correct stamp in rhythm. Scoring rewards both accuracy *and* refusing the ones that should be refused (compliance literacy, not just reflexes). Pure physical joy, draws aisle crowds, bilingual-friendly, zero reading beyond the icon. 90 seconds per play.

**A9 — Hanko Jenga**
Each block is labeled with a workflow step (ex-ante policy check, delegation record, audit timestamp, approver signature, …). Visitors pull a block to "skip this step." Tower collapses = compliance violation. The game master then shows which steps Hanko CIS **makes safely skippable** (because the audit trail covers you) vs. which are structurally **load-bearing** (and why CIS enforces them). Fast (90s per round), tactile, memorable, extremely low cost.

### 8.4 Conference-wide / phygital formats

**A10 — Rakuten Hanko Hunt (AR treasure hunt across the venue)**
A lightweight web app (no install) that visitors open via QR at our booth. They are given a 12-stamp "digital rally card." Each stamp is unlocked by scanning a QR hidden at **other sponsor booths and session rooms** across the venue — negotiated in advance with partner sponsors. Each scan reveals one Hanko CIS feature as a short animated card. Complete all 12 → return to our booth for a championship prize draw. Drives **repeat visits** to our booth and gives visitors a reason to stay engaged across the whole day. Needs ~2 weeks of pre-event coordination with partner sponsors.

**A11 — Live multiplayer Hanko Street (tablet companion)**
A digital companion to the §2 physical game. 4 tablets at a dedicated table running the same game logic as Hanko Street, so visitors who miss a physical seat can still play — and so visitors who can't make RTC in person can join remotely via a public URL during the event. Doubles total throughput for the headline format and extends reach into the Rakuten Tech social audience.

### 8.5 Appendix-A trade-off summary

| Code | Format | Best at | Throughput / hour | Floor space | Staff | Novelty |
|---|---|---|---|---|---|---|
| A1 | Hanko Karuta | Cultural fit, bilingual | ~30 | Small | 1 reader | Medium |
| A2 | Approval Pachinko | Spectacle, filmability | ~90 | Small | 1 | **High** |
| A3 | Hanko Pub Quiz | Relationships, BU/exec | one 90-min slot | Medium | 1 host + 2 | Medium |
| A4 | Compliance Clue (whodunit) | Enterprise depth | ~15 | Medium | 1 facilitator | High |
| A5 | Workflow Catan | Collaborative narrative | ~16 | Medium | 1 facilitator | Low |
| A6 | Among Us: Rogue Approver | Engineer / Gen-Z crowd | ~24 | Small–Medium | 1 energetic GM | High |
| A7 | Hanko Millionaire | Crowd gathering, social clips | ~24 contestants, large audience | Large (needs stage area) | 1 MC + 1 scorer | Medium |
| A8 | CIS Dojo (rhythm) | Aisle pull, zero reading | ~40 | Small | 1 | **High** |
| A9 | Hanko Jenga | Teaching which steps matter | ~40 | Small | 1 | Medium |
| A10 | Hanko Hunt (venue-wide AR) | Repeat visits, cross-booth reach | ~200 unique players | n/a (phones) | 1 at base | **High** |
| A11 | Live multiplayer Hanko Street | Overflow + remote reach | +~24 to Hanko Street | Small (tablet table) | 1 | Low |

### 8.6 Expanded booth stack options

Given the appendix, three concrete booth stacks worth evaluating alongside §7:

- **Stack 1 — "Signature stack" (same as §7 recommendation):** Hanko Street + Stamp Rally + Trading Card Deck.
- **Stack 2 — "Spectacle stack":** Approval Pachinko (A2) + CIS Dojo (A8) + Hanko Millionaire (A7) once per peak slot + Trading Card Deck. Highest aisle-pull and social-media output; weakest on structured learning.
- **Stack 3 — "Depth stack":** Hanko Street + Compliance Clue (A4) at a reserved exec table + Hanko Pub Quiz (A3) after-hours on day 1. Highest learning depth per visitor; best for enterprise and BU partnership funnel.
- **Stack 4 — "Phygital stack":** Hanko Street (one table) + Hanko Hunt (A10) across the venue + Live multiplayer Hanko Street (A11) tablets. Smallest booth footprint, largest unique reach, requires the most pre-event coordination.

---

## 9. Appendix B — If Hanko and CIS are two separate products

The §1–§7 proposal reads *"Hanko CIS"* as a single named product. If the actual intent is to showcase **two distinct products side-by-side** — e.g. **Hanko** (a digital stamp / signature product) and **CIS** (a broader identity, approval, or common-information service) — the booth concept adapts cleanly rather than needing a rewrite:

- **Hanko Street board:** split the eight districts into **two colour-coded halves** — four Hanko districts (document signing, delegated signature, mobile sign, audit trail of a signature) and four CIS districts (identity, policy, routing, cross-system approval). Insight Chips are visibly tagged with the product they came from. The win condition rewards players who collect chips from **both** products, teaching the pitch that *Hanko and CIS are better together*.
- **Stamp Rally (§3 Alt A):** the six micro-stations split 3 Hanko / 3 CIS. The rally card graphically shows the two products meeting in the middle.
- **Trading Card Deck (§3 Alt D):** two sub-decks in one box, with a cross-product combo mechanic (certain Hanko + CIS card pairs score bonus points).
- **Insight-Chip taxonomy:** colour-code chips by product so the leaderboard can report *"Top Hanko player of the day"* and *"Top CIS player of the day"* alongside the overall champion. This gives each product's PM a clean metric to take back to their BU.
- **Appendix-A formats:** Pachinko (A2), Dojo (A8), and Hunt (A10) all accommodate two-product theming trivially — split the gates, buttons, and treasure-hunt stamps 50/50.
- **Lead capture:** the badge-scan screen asks a one-tap question — *"Which product do you want a follow-up on? Hanko / CIS / Both"* — so the two product teams get clean, separate pipelines out of a shared booth.

If the two products have significantly different buyer personas (e.g. Hanko → legal / ops; CIS → IT / security), consider the **Depth Stack** (§8.6 Stack 3) with Compliance Clue reserved for the CIS persona and Hanko Pub Quiz themed heavily around signature etiquette for the Hanko persona.

---

## 10. Concept-selection helper

A compact decision aid when the team sits down to pick the final booth stack.

**Pick by primary audience:**
- *External engineers and devs* → Hanko Street (§2) + CIS Dojo (A8) + Among Us: Rogue Approver (A6).
- *Enterprise buyers, CFO/CRO, BU heads* → Hanko Street (§2) + Compliance Clue (A4) + Hanko Pub Quiz (A3).
- *Partners, vendors, ecosystem* → Stamp Rally (§3 Alt A) + Trading Card Deck (§3 Alt D) + Hanko Hunt (A10).
- *Mixed general RTC crowd* → §7 Signature Stack.

**Pick by what we are optimising for:**
- *Leads at scale* → Stamp Rally + Approval Pachinko (A2) + Trading Card Deck.
- *Deep conversations with few, right people* → Hanko Street + Compliance Clue (A4).
- *Social media and brand buzz* → Approval Pachinko (A2) + Hanko Millionaire (A7) + CIS Dojo (A8).
- *Internal cross-BU champions* → Workflow Catan (A5) + Hanko Pub Quiz (A3).
- *Reach beyond our booth* → Hanko Hunt (A10) + Live multiplayer Hanko Street (A11).

**Pick by constraint:**
- *Tiny booth (≤ 2m × 2m)* → Trading Card Deck (§3 Alt D) + Hanko Jenga (A9) + Hanko Karuta (A1).
- *Small team (1–2 staff all day)* → Stamp Rally (§3 Alt A) + Trading Card Deck + Pachinko (A2, unmanned).
- *Short lead time (< 4 weeks to RTC)* → Trading Card Deck + Hanko Jenga (A9) + Hanko Karuta (A1); skip the custom board.
- *Need bilingual parity (JP/EN)* → anything in §8.1 plus Hanko Street (both are designed JP-first with English parity on the same card face).

The one-line principle underneath all of this: **make the visitor physically feel the paper workflow lose**, then let them walk away with proof — a card, a chip, a leaderboard spot, a story. Pick the stack that delivers that outcome within your actual constraints, and the booth will do its job regardless of which format label is on the box.
