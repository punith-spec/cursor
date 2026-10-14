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
