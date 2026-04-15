---
name: studio
description: Full-stack creator suite for YouTube, TikTok, and Instagram — scripts, hooks, thumbnails, SEO, monetization, and cross-platform publishing in one workflow.
version: 1.0.0
author: mikeoptimax
---

```
███████╗████████╗██╗   ██╗██████╗ ██╗ ██████╗ 
██╔════╝╚══██╔══╝██║   ██║██╔══██╗██║██╔═══██╗
███████╗   ██║   ██║   ██║██║  ██║██║██║   ██║
╚════██║   ██║   ██║   ██║██║  ██║██║██║   ██║
███████║   ██║   ╚██████╔╝██████╔╝██║╚██████╔╝
╚══════╝   ╚═╝    ╚═════╝ ╚═════╝ ╚═╝ ╚═════╝ 
  Full-Stack Creator Suite
```

# STUDIO — Full-Stack Creator Suite

Multi-platform content engine: YouTube, TikTok, and Instagram Reels. One suite, every output. Built for speed.

---

## Commands

| Command | What it does |
|---------|-------------|
| `/studio audit` | Full channel health across 5 dimensions |
| `/studio ideate` | 10 ranked ideas with spy hook integration |
| `/studio script` | Retention-engineered script + TikTok + Reels versions |
| `/studio hook` | 5 hook variants scored + pulled from spy library |
| `/studio thumbnail` | Generate actual thumbnail (banana) or detailed brief |
| `/studio seo` | Title variants, description, tags, chapters for all platforms |
| `/studio strategy` | Positioning, pillars, cadence for YouTube + short-form |
| `/studio calendar` | Monthly calendar with CPM timing + cross-platform schedule |
| `/studio shorts` | Shorts/Reels/TikTok production package |
| `/studio analyze` | Funnel diagnosis — paste your analytics screenshot or data |
| `/studio repurpose` | One video → cross-platform package (YT + TT + IG + blog + LinkedIn) |
| `/studio monetize` | Revenue strategy across 8 income streams with forecasting |
| `/studio competitor` | Gap analysis with 4 parallel agents |
| `/studio metadata` | Copy-paste upload package for all platforms |
| `/studio community` | YouTube community post ideas + engagement hooks |
| `/studio sponsor` | Sponsorship rate card, pitch templates, brand brief analyzer |
| `/studio series` | Plan multi-part series with SEO clustering + view compounding |
| `/studio crosspost` | Generate platform-native metadata from any existing video |
| `/studio checklist` | Pre-upload quality gate — 22 checks before you publish |

---

## Step 0 — First-Run Setup

Check for config at `~/.studio/config.json`. If missing, run the setup interview before proceeding with any command.

**Setup interview — ask each question in sequence:**

1. Channel name + YouTube handle (e.g. @yourchannel)
2. Niche + audience in one sentence (e.g. "personal finance for UK 25-35s")
3. Upload frequency (weekly / 2x week / daily)
4. Primary revenue goal (AdSense / sponsorships / course / community)
5. YouTube Data API key — optional, skip if not available (all commands work without it)
6. Check for banana skill: `ls ~/.claude/skills/banana/SKILL.md` (enables thumbnail generation)
7. Check for spy hook library: `~/.spy/hooks.md` (enables proven hook injection)

Save to `~/.studio/config.json`:
```json
{
  "channel": "...",
  "handle": "...",
  "niche": "...",
  "audience": "...",
  "frequency": "...",
  "goal": "...",
  "api_key": null,
  "banana": false,
  "spy_hooks": false
}
```

Confirm setup complete. Proceed.

---

## Orchestrator Logic

When user runs `/studio [command]`:
1. Load `~/.studio/config.json` — if missing, run Step 0 first
2. If spy hook library exists (`~/.spy/hooks.md`) — load and surface top matching hooks for the current topic
3. Route to the correct section below
4. Default: all outputs are multi-platform (YouTube + TikTok + Reels) unless `--youtube-only` flag is passed

---

## /studio audit

Evaluate the channel across 5 dimensions. Ask user to paste or describe recent data if API key is absent.

**Dimension 1 — Content Health**
- Average video length vs niche benchmark
- Upload consistency score (last 90 days)
- Topic diversity vs niche focus score

**Dimension 2 — Hook Performance**
- Average CTR vs benchmark (3-4% typical, 6%+ strong)
- Thumbnail style assessment (face / text / graphic)
- Title formula patterns in top vs bottom performers

**Dimension 3 — Retention**
- Average view duration %
- Estimated drop-off moment (ask user: "where do viewers leave?")
- Pattern interrupt frequency assessment

**Dimension 4 — Conversion**
- Subscriber conversion rate (views → subs)
- CTA placement and frequency
- Community + social cross-promotion activity

**Dimension 5 — Monetization**
- Active income streams (count and estimate revenue mix)
- Revenue diversification score
- Biggest gap vs niche benchmark

Output: scored summary (each dimension /10), top 3 priority fixes, and next recommended `/studio` command.

---

## /studio ideate

Generate 10 ranked video ideas with spy hook integration.

Process:
1. Load config niche + audience
2. If `~/.spy/hooks.md` exists — surface hook patterns that map well to idea angles
3. Generate 10 ideas ranked by: search volume potential, hook availability, production simplicity

Each idea includes:
- Working title
- Hook angle (from spy library if available, otherwise original)
- Target keyword
- Format: talking head / tutorial / list / story / reaction
- Estimated difficulty: Easy / Medium / Hard
- Platform fit: YouTube ✓/✗  TikTok ✓/✗  Reels ✓/✗

Rank by combined score. Bold the top 3. Ask: "Which idea do you want to develop? I'll route to /studio script."

---

## /studio script

**Input:** topic or brief (or output from `/studio ideate`)

**Process:**

Step 1 — Hook selection:
- If `~/.spy/hooks.md` exists: search for hooks matching the topic, show top 3 with scores
- Ask user: "Which hook do you want to build from? Or should I generate originals?"
- If spy library absent: generate 3 original hook options (talking head / text-on-screen / pattern interrupt)

Step 2 — Write full YouTube script:

```
[HOOK — 0-8s]
[Hook text — no intro, no "hey guys", no context. Tension first.]

[PATTERN INTERRUPT — 15s]
[Reframe or unexpected statement]

[SETUP — 30s]
[Why this matters to viewer. Stakes.]

[CORE VALUE — body]
[WHAT, not HOW. Free content teaches what; products teach how.]
[Use [B-ROLL: description] markers]
[Use [GRAPHIC: description] markers]
[Use [PAUSE] for breath moments]

[PATTERN INTERRUPT — 60s]
[Tension / payoff cycle reset]

[CORE VALUE CONTINUED]

[CTA — final 30s]
[One ask. Specific. Low friction. E.g. "Comment the word X below"]
```

Step 3 — Produce all 3 versions:

**YouTube version (3-8 min):** Full script with markers above.

**TikTok version (30-60s):** Trimmed to hook + single insight + CTA. No intro. Opens on tension. Ends on action.

**Reels version (15-30s):** Hook (2s hard cut) + one punchy insight + text CTA overlay. Silent-viewer friendly — every key point has on-screen text noted.

---

## /studio hook

**Input:** video topic

**Process:**
1. Load `~/.spy/hooks.md` — extract hooks matching topic
2. Show top 3 from library with historical performance context: "Proven: similar hooks in this niche averaged Xk views"
3. Generate 2 original hooks to complement library options
4. Total output: 5 hooks

**Each hook output:**
```
Hook #N — [title]
Spoken: "[hook text]"
On-screen: "[3-5 word text overlay]"
Score:       ████████░░  78/100
Drop-off risk: Low / Medium / High
Platform fit:  YouTube ✓  TikTok ✓  Reels ✓
Why it works: [one-line reasoning]
```

Bold the top scorer. Recommend it for `/studio script`.

---

## /studio thumbnail

**Process:**

Step 1 — Check for banana skill:
```bash
ls ~/.claude/skills/banana/SKILL.md
```

**If banana is available:**
- Invoke `/banana` with prompt: `"YouTube thumbnail, [topic], high contrast background, [channel style from config], face expression: [emotion], CTR-optimized, bold 2-word text overlay"`
- Generate 3 variants (A, B, C) with different expressions / text / color treatments
- Save to `./thumbnails/thumb_A.png`, `thumb_B.png`, `thumb_C.png`
- Label: "Use A as default. Swap to B after 48h if CTR stays below 4%."

**If banana is NOT available:**
Output a structured thumbnail brief for a designer or Canva:

```
THUMBNAIL BRIEF
Topic: [topic]
Subject: [face/character/object — be specific]
Expression: [surprised / intense / curious — pick one]
Background: [color hex + texture]
Text overlay: [max 3 words — list options]
Text placement: [top-left / bottom-right / center]
Text color: [hex] on [background hex] — contrast ratio: high
Accent element: [arrow / circle highlight / sticker]
Reference style: [describe 2 existing thumbnails to mimic]
What to avoid: [generic stock, busy backgrounds, small text]
```

Always output: CTR prediction — Low / Medium / High — based on face visibility, text clarity, and contrast score.

---

## /studio seo

**Input:** video title working draft + topic

**Output for each platform:**

**YouTube:**
- 5 title variants (primary keyword front-loaded, emotional trigger, curiosity gap)
- Description: 150-word block (keyword in first 2 lines, CTA, timestamps, links)
- Tags: 5 broad + 5 specific + 5 long-tail (15 total)
- Chapter markers (if video is 8+ min — ask user for timestamps or estimate from script)
- Hashtags: 3 relevant

**TikTok:**
- Caption (150 chars max): hook + keyword + CTA
- Hashtags: 5 niche + 3 trending (flag: verify trending ones before publish)
- Sound suggestion: describe audio style (trending / original audio / voiceover)

**Instagram Reels:**
- Caption: hook line + 3-sentence value + CTA + line break + hashtags
- Hashtags: 10-15 (mix of niche, broad, and community tags)
- Alt text for accessibility

---

## /studio strategy

**Input:** config niche + audience + goal

**Output:**

**Channel Positioning:**
- One-line value proposition
- Audience avatar (name, age, pain, desire)
- Differentiation vs top 3 competitors in niche

**Content Pillars (3-5):**
For each pillar: name, description, example titles, % of upload schedule

**Cadence Plan:**
- YouTube: X videos/week, optimal days + times
- TikTok: X posts/week, format mix (original / repurposed / trending audio)
- Instagram Reels: X posts/week, format mix

**90-Day Growth Roadmap:**
- Month 1: Foundation (SEO-first content, pillar establishment)
- Month 2: Momentum (series launch, community activation)
- Month 3: Monetization (sponsorship pitch, lead magnet or product drop)

---

## /studio calendar

**Input:** current month + upload frequency from config

Generate a full monthly calendar. Columns: Date | Platform | Format | Topic | Hook | CPM Note | Status

**CPM timing rules (baked in):**
- YouTube: Thu/Fri 2-4pm audience local time = peak CPM window
- Avoid Dec 25-Jan 5 for monetized content (CPM crashes post-Q4)
- Q4 (Oct-Dec): max upload frequency — CPM is 2-4x average
- January: pull back or go educational (low CPM, high search intent)

**Cross-platform schedule:**
- YouTube upload day = same-day TikTok repurpose
- Following day = Reels version
- +2 days = LinkedIn post
- +3 days = Community post on YouTube

Output as a markdown table. Include CPM index for each week (Low / Medium / High / Peak).

---

## /studio shorts

**Input:** topic or timestamp from existing video

**Output package:**

**Script (60s max):**
- Hook: 0-3s (hard cut, no intro)
- Payoff: 4-45s (single idea, punchy delivery)
- CTA: 46-60s (comment / follow / watch next)

**Production notes:**
- Vertical format (9:16)
- On-screen text: every key line has a text overlay (silent viewer rule)
- Trending audio recommendation (describe style — don't hallucinate track names)
- Jump cut cadence: cut every 3-5s max

**3-platform checklist:**
- YouTube Shorts: under 60s, no black bars, add to Shorts shelf
- TikTok: same cut, add TikTok-native caption style, suggest trending sound
- Reels: same cut, square-safe zone check, Reels cover frame set

---

## /studio analyze

**Input:** paste analytics data, describe what you're seeing in YouTube Studio, or describe a metric problem

**Funnel diagnosis framework:**

```
Impressions → CTR (target: 4-8%)
  Low CTR = thumbnail or title problem
  Fix: /studio thumbnail + /studio seo

CTR → Average View Duration (target: 40%+)
  Low AVD = hook or first-60s problem  
  Fix: /studio hook + re-examine pattern interrupts

AVD → Subscriber Conversion (target: 1 sub per 100 views)
  Low conversion = weak CTA or value mismatch
  Fix: audit CTA placement, rewrite end card script

Subscribers → Notification Open Rate (target: 15%+)
  Low opens = title/topic mismatch with subscriber expectations
  Fix: /studio strategy — realign pillars with what earned your subscribers
```

Output: ranked issue list (most impactful first), specific fix action for each, `/studio` command to run next.

---

## /studio repurpose

**Input:** YouTube video URL, transcript paste, or detailed summary

**Step 1 — Extract core assets:**
If URL provided: attempt `yt-dlp` + `whisper` transcription. If unavailable, ask user to paste transcript or summarize key moments.

**Identify:**
- Hook moment (0-15s)
- Core insight (strongest single idea)
- CTA moment
- Top 3 timestamp highlights

**Step 2 — Output full cross-platform package:**

**YouTube Shorts (3 clips):**
- Clip 1: [timestamp range] — reason: strongest hook
- Clip 2: [timestamp range] — reason: standalone insight
- Clip 3: [timestamp range] — reason: emotional peak or payoff

**TikTok version:**
Rewritten natively — shorter sentences, faster pace, trending audio style suggestion, caption under 150 chars

**Instagram Reels version (15-30s):**
Hook + single insight + on-screen text script for silent viewing + caption with hashtags

**LinkedIn post:**
Professional angle, insight-first opening (no hook fluff), 3 key takeaways, soft CTA

**Twitter/X thread (5-7 tweets):**
Tweet 1: hook statement. Tweets 2-6: one idea each. Tweet 7: CTA + link

**Blog post outline:**
H1 (keyword-optimized title), H2s (one per key section), 3 pull quotes from video, meta description

**Email newsletter snippet (150 words):**
Subject line option + body paragraph + CTA link

---

## /studio monetize

**Input:** config data + any revenue info user wants to share

**8 income streams with forecasting:**

For each stream: status (Active / Potential / Not viable for this channel), estimated monthly revenue at current views, action to activate.

1. **AdSense** — CPM × monthly views / 1000. Niche CPM benchmarks: Finance $12-25 | Health $8-15 | Gaming $2-5 | Education $6-12
2. **Sponsorships** — flat fee = (avg views / 1000) × $20-50 per integration type
3. **Affiliate** — commission-based, estimate 0.5-2% conversion on clicks
4. **Digital product** (course / template / preset) — one-time launch + evergreen
5. **Membership / Community** — recurring, estimate 1-3% of subscribers convert at $5-10/mo
6. **Consulting / Services** — direct from channel authority
7. **Speaking / Brand deals** — channel as portfolio, niche authority lever
8. **Licensing** — footage, music, templates to other creators

**Revenue forecast table:**
| Stream | Monthly (now) | Monthly (at 10k subs) | Monthly (at 100k subs) |
|--------|--------------|----------------------|----------------------|
| ... | ... | ... | ... |

**Priority recommendation:** top 2 streams to activate first based on niche + current stage.

---

## /studio competitor

**Input:** up to 3 competitor channel names or URLs

**Run 4 parallel analysis agents:**

Agent 1 — Content gap analysis:
- Topics they cover that you don't
- Topics you cover better
- Untapped angles in the niche

Agent 2 — Hook + title pattern audit:
- Their most common title formulas
- Average CTR signals (thumbnail style patterns)
- Hook types they default to

Agent 3 — Engagement analysis:
- Comment sentiment patterns
- Top recurring questions (= your next video ideas)
- Community complaints (= your differentiation opportunity)

Agent 4 — Monetization model:
- Visible revenue streams
- Product/service links in descriptions
- Sponsorship patterns

**Output:** consolidated gap report, top 5 opportunities, recommended `/studio ideate` seed topics.

---

## /studio metadata

**Input:** video title + description draft + tags (or ask user)

Generate the full copy-paste upload package:

**YouTube:**
```
TITLE: [final title — keyword front-loaded, under 70 chars]

DESCRIPTION:
[First 2 lines: keyword + CTA — visible before "show more"]
[Full description body with timestamps]
[Links section]
[Hashtags: max 3]

TAGS: [comma-separated list, 15 tags]

CHAPTERS:
00:00 Intro
[...]

PINNED COMMENT: [draft — question or CTA to post immediately after upload]
```

**TikTok:**
```
CAPTION: [under 150 chars, hook + keyword + CTA]
HASHTAGS: [5-8 tags]
SOUND NOTE: [style description for audio selection]
```

**Instagram Reels:**
```
CAPTION: [hook line + value + CTA + hashtags]
COVER FRAME NOTE: [describe ideal still frame for cover]
ALT TEXT: [accessibility description]
```

---

## /studio community

**Input:** recent video topics from config or user

Generate 5 YouTube community post ideas:

For each post:
- **Type:** Text / Poll / Image / GIF
- **Opening line:** (first line must earn the scroll-stop)
- **Body or poll options:** (max 3 poll options for clean engagement)
- **Engagement question:** (end with a direct question)
- **Best time to post:** same day as new video drop / mid-week fill / Sunday engagement reset
- **Goal:** views to new video / subscriber warmth / content research

Bonus: flag 1 post as a "content research" post — design it to surface the next video idea from audience responses.

---

## /studio sponsor

Sub-modes — ask user which they need:

**`/studio sponsor rate`**
Calculate a CPM-based rate card for the channel.
- Input: average views per video (ask if not in config)
- Formula: avg views / 1000 × CPM multiplier by integration type
  - Pre-roll (60s): × $25
  - Mid-roll mention (30s): × $20
  - Dedicated video: × $40
  - Pinned comment: × $5
  - Description link only: × $3
- Output: rate card table (integration type | recommended rate | negotiation floor)
- Package deals: suggest pre-roll + mention + pin bundle at 20% discount

**`/studio sponsor pitch`**
Write a cold outreach email to a specific brand.
- Ask: brand name + product + why it fits your audience
- Output: subject line + 150-word email + P.S. line
- Tone: confident, data-forward, not desperate

**`/studio sponsor brief`**
Analyze an incoming brand brief and flag issues.
- Ask user to paste the brief
- Flag: exclusivity clauses, low CPM implied rates, vague deliverables, IP traps
- Output: red flags list + suggested negotiation points + counter-brief language

---

## /studio series

**Input:** topic or seed idea

**Output:**

**Series identity:**
- Series name + tagline
- Positioning: why this series, why now, why your channel

**Episode outline (5-part default, adjustable):**
For each episode:
- Title (SEO-optimized)
- Hook angle
- Core keyword
- Internal link target (which previous episode to reference)
- Thumbnail visual theme (for series consistency)

**Playlist architecture:**
- Playlist title + description
- Auto-play order recommendation
- Featured video (episode 1 or strongest entry point)

**SEO clustering strategy:**
- Primary keyword cluster (all episodes target variations)
- Pillar keyword + spoke keywords map

**View compounding estimate:**
```
If Episode 1 = X views:
  Episode 2 (via suggested feed) ≈ 0.6X
  Episode 3 ≈ 0.4X
  Playlist completion bonus: +15% across all episodes after series hits 1k views
  Series total estimate: ~2.5X of Episode 1 views
```

**Publishing cadence:** weekly recommended for search feed; bi-weekly if production-constrained.

---

## /studio crosspost

**Input:** existing YouTube video — title, description, and URL (or transcript)

**Process:** Extract core metadata and rewrite natively for each platform.

Output platform-native packages for:
- TikTok (caption + hashtags + sound note)
- Instagram Reels (caption + cover note + hashtags)
- LinkedIn (professional reframe — insight-first, no creator fluff)
- Twitter/X (single tweet or thread starter)
- YouTube Community (teaser post to drive views)

Flag any platform where the content is NOT a good fit and explain why.

---

## /studio checklist

22-point pre-upload quality gate. Present as interactive checklist — user confirms each item.

```
PRE-UPLOAD CHECKLIST
Video: [title]
Platform: YouTube + TikTok + Reels

CONTENT
[ ] Hook delivers on the exact promise made in the thumbnail
[ ] Pattern interrupt lands before 30s
[ ] No dead air in the first 60s
[ ] Core value is WHAT (not full HOW — that's your product)
[ ] CTA is specific and low-friction (not "like and subscribe")

YOUTUBE METADATA
[ ] Title includes primary keyword, front-loaded, under 70 chars
[ ] Description first 2 lines contain keyword + CTA (visible before "show more")
[ ] Chapters added (required if video is 8+ min)
[ ] End screen configured (last 20s of video)
[ ] Cards placed at 2+ key moments
[ ] Tags: 5 broad + 5 specific + 5 long-tail

THUMBNAIL
[ ] Face visible (if applicable) with readable expression
[ ] Text overlay is 3 words max
[ ] High contrast — passes 10-foot test
[ ] A/B variant ready (swap if CTR < 4% after 48h)

SHORT-FORM
[ ] TikTok version ready (under 60s, caption drafted)
[ ] Reels version ready (cover frame set, caption drafted)

POST-UPLOAD ACTIONS
[ ] Pinned comment drafted (post within 5 min of going live)
[ ] Community post drafted (publish same day)
[ ] Reply plan for first 20 comments (first 30 min = algorithm signal)
[ ] LinkedIn post scheduled
[ ] Email newsletter snippet ready

COMPLIANCE
[ ] Sponsor disclosure added (if applicable — required by law)
[ ] Auto-captions reviewed and corrected
[ ] Cross-links to 2+ related videos in description

TIMING
[ ] Scheduled for Thu or Fri, 2-4pm in primary audience timezone
```

Tally score. Flag any unchecked items as blockers vs. nice-to-haves. Clear to publish when all CONTENT + YOUTUBE METADATA items are ticked.

---

## Multi-Platform Defaults

Unless `--youtube-only` is passed, every command that produces scripts, hooks, or metadata outputs all 3 platform versions.

**Platform-native rules applied automatically:**

| Rule | YouTube | TikTok | Reels |
|------|---------|--------|-------|
| Hook window | 0-15s acceptable | Must land by 3s | Must land by 2s |
| Optimal length | 8-15 min (ad breaks) | 30-60s | 15-30s |
| Silent viewing | Optional | Required | Required |
| Trending audio | N/A | Always suggest | Always suggest |
| Chapters | Yes (8+ min) | No | No |
| CTA placement | Final 30s | Final 5s | Final 3s |
| On-screen text | Occasional | Every key line | Every key line |

---

## Revenue Forecasting Reference

Niche CPM benchmarks (YouTube AdSense, UK/US blend):

| Niche | CPM Range | Notes |
|-------|-----------|-------|
| Finance / Investing | $12–$25 | Peak Q4 |
| Business / B2B | $10–$22 | |
| Health / Wellness | $8–$15 | |
| Education / How-to | $6–$12 | High search volume |
| Tech / Software | $8–$18 | |
| Lifestyle / Vlog | $3–$7 | |
| Gaming | $2–$5 | High volume, low CPM |
| Entertainment | $2–$6 | |

Q4 multiplier (Oct–Dec): apply 2-3x on above ranges.

---

*STUDIO by mikeoptimax. Build fast, post everywhere, grow compounding.*
