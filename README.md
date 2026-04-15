```
███████╗████████╗██╗   ██╗██████╗ ██╗ ██████╗ 
██╔════╝╚══██╔══╝██║   ██║██╔══██╗██║██╔═══██╗
███████╗   ██║   ██║   ██║██║  ██║██║██║   ██║
╚════██║   ██║   ██║   ██║██║  ██║██║██║   ██║
███████║   ██║   ╚██████╔╝██████╔╝██║╚██████╔╝
╚══════╝   ╚═╝    ╚═════╝ ╚═════╝ ╚═╝ ╚═════╝ 
  Full-Stack Creator Suite
```

# studio-skill

19-command creator suite for YouTube, TikTok, and Instagram in Claude Code.

---

## Commands

| Command | Description |
|---|---|
| `/studio idea` | Generate video ideas from niche + trend data |
| `/studio research` | Deep research brief for any topic |
| `/studio hook` | 10 hooks via spy library — YouTube + Shorts + Reels versions |
| `/studio script` | Full script with spy hooks wired in, all 3 platform cuts |
| `/studio title` | 10 titles optimised for CTR + search |
| `/studio description` | SEO-ready description, timestamps, CTA |
| `/studio tags` | Keyword-rich tag set for YouTube + hashtags for TikTok/IG |
| `/studio thumbnail` | Generate via banana or output a production brief |
| `/studio shorts` | Cut a long script into a Shorts/Reels/TikTok vertical |
| `/studio repurpose` | Transcribe existing video → multi-platform content pack |
| `/studio checklist` | 22-point pre-upload audit — platform by platform |
| `/studio revenue` | CPM benchmarks + revenue forecast for your niche |
| `/studio analytics` | Read comment/metric data → actionable next-video insights |
| `/studio comments` | Mine comments for pain points + next video ideas |
| `/studio series` | Plan a multi-part series arc with episode briefs |
| `/studio sponsor` | Write sponsor reads (host-read, integrated, pre-roll) |
| `/studio community` | Draft community posts, polls, and membership content |
| `/studio ab` | A/B title + thumbnail variants with test rationale |
| `/studio plan` | Full channel calendar: ideas → scripts → upload schedule |

---

## What Makes It Different

- **Multi-platform by default** — every output ships YouTube long-form, Shorts, TikTok, and Reels cuts simultaneously
- **Spy hook library integration** — `/studio hook` and `/studio script` pull from the spy-skill hook database, not generic templates
- **Thumbnail generation** — calls banana-skill for actual image gen; falls back to a detailed art-direction brief if banana isn't installed
- **Three sub-skills not found elsewhere** — `/studio community`, `/studio sponsor`, and `/studio series` cover the revenue and retention layer most creator tools skip
- **No API key required** — works out of the box; YouTube Data API is optional (unlocks `/studio analytics` enrichment)

---

## Requirements

- **Claude Code** — required
- **yt-dlp + whisper** — required for `/studio repurpose` (transcription pipeline)
- **banana-skill** — optional, enables real thumbnail generation
- **spy-skill** — optional, enriches hooks with proven pattern library

---

## Install

```bash
cp -r studio-skill ~/.claude/skills/studio-skill
```

Then in Claude Code: `/studio help`

---

## Quick Examples

```
/studio idea niche:"personal finance for freelancers" format:long
```
```
/studio script topic:"how I paid off $40k debt" hook:curiosity length:12min
```
```
/studio repurpose url:https://youtu.be/abc123 outputs:shorts,thread,caption
```
```
/studio revenue niche:"home improvement DIY" views:50000/mo
```

---

## Works With

| Skill | How |
|---|---|
| [spy-skill](https://github.com/mikeoptimax/spy-skill) | Hooks and scripts pull from spy's proven pattern database |
| [banana-skill](https://github.com/mikeoptimax/banana-skill) | `/studio thumbnail` calls banana for AI image generation |

---

## License

MIT — by [mikeoptimax](https://github.com/mikeoptimax)
