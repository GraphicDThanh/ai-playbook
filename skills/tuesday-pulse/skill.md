---
name: tuesday-pulse
description: Balanced mid-week tech pulse (Tue). Mix of security, tech updates, and career growth. 2-3 items max. Pairs with Friday weekly digest. ~$0.20/run = ~$0.80/month.
---

# Tuesday Pulse — Mid-Week Balanced Check-In

A **balanced** mid-week digest mixing critical security (if any), interesting tech updates, and career/skill growth. Tone: informative but not stressful. Pairs with Friday comprehensive weekly.

**Philosophy:** Balance necessary (security) with inspiring (new tech, learning). Readers should feel informed AND excited, not just anxious.

## Config

- **Timezone:** Asia/Ho_Chi_Minh (UTC+7)
- **Slack channel:** #dev-news, ID `C0CDJBYAXAM`
- **Run day:** Tuesday only
- **Window:** Sat 00:00 → Tue 09:00 (weekend + Mon + Tue morning)
- **Target mix:** 1 critical (if any) + 1-2 interesting/inspiring items

## 1. Settle the run

| | SCHEDULED (Tue) | ON_DEMAND |
|---|---|---|
| WINDOW | Sat 00:00 → Tue 09:00 | Last 72 hours |
| Header | `⚡ *TUESDAY PULSE \| {date}*` | `⚡ *TUESDAY PULSE \| {date}*` |
| PUBLISH | Auto if ≥1 item scores ≥6 | No — return draft |

`DRY_RUN`: treat "test", "dry run", "đừng đăng" as DRY_RUN.

**Important:** If today is NOT Tuesday (for scheduled runs), skip and say "Tuesday Pulse runs on Tuesdays only. Use my-dev-digest for Friday weekly."

## 2. Scope — balanced mix

**Target ratio (2-3 items total):**
- 30% critical/security — CISA KEV, critical CVEs, supply-chain (if any in window)
- 50% tech updates — AI tools, model releases, framework updates, new features
- 20% career/learning — best practices, patterns, tutorials, community discussions

**Categories:**

**🔒 Security (include if score ≥8):**
- CISA KEV additions
- Critical CVEs (CVSS ≥9.0) with active exploitation
- Supply-chain incidents (trojanized packages)

**🚀 Tech Updates (pick 1-2 scoring ≥6):**
- AI coding tools: Claude Code, Copilot, Cursor, Codex updates
- LLM APIs: pricing changes, new capabilities, GA releases
- Frameworks: React, Next.js, Vue, Angular major/breaking releases
- Languages: Node.js, Python, TypeScript, Go, Rust releases
- MCP: new servers, standards updates

**💡 Career/Learning (pick 1 if space):**
- New patterns/best practices (e.g., React 19 hooks patterns)
- Community tools (e.g., Trail of Bits Brotli checker skill)
- Learning resources from reputable sources
- Interesting GitHub projects solving real problems

**Selection strategy:**
1. Always include 1 critical security if score ≥8
2. Fill remaining slots (max 3 total) with highest-scoring tech/learning items
3. Prefer diversity: don't pick 2 items from same company
4. Tone test: "Will this make readers feel informed AND excited?" If just anxious → reconsider

## 3. Research — lightweight

**Skip agent-reach** to save tokens. Check primary sources for WINDOW (Sat-Tue):

**Security (quick scan):**
- CISA KEV: https://www.cisa.gov/known-exploited-vulnerabilities-catalog
- GitHub Advisories: https://github.com/advisories (high/critical only)
- Node.js security: https://nodejs.org/en/blog/vulnerability

**Tech Updates:**
- Claude Code: https://code.claude.com/docs/en/changelog
- Copilot: https://github.blog/changelog/label/copilot/
- OpenAI: https://developers.openai.com/api/docs/changelog
- Anthropic: https://www.anthropic.com/news
- Node.js: https://nodejs.org/en/blog/release
- React: https://react.dev/blog
- TypeScript: https://devblogs.microsoft.com/typescript/

**Broad searches (2 max):**
- "AI coding tools news {range}"
- "developer news {range}"

**Verification:**
- Confirm date on page
- Outside WINDOW → drop
- Primary sources preferred
- Use only verified URLs

**Target: 5-8 candidates** before scoring.

## 4. Score and filter

Score out of 10:
- **Impact** 0-3 — How much it changes work/workflow
- **Interest** 0-3 — Will developers want to try/learn this? (Replaces "Stack fit" for more balanced scoring)
- **Urgency** 0-2 — Must-act now = 2; act this quarter = 1; FYI = 0
- **Actionability** 0-2 — Clear action = 2; explore/evaluate = 1

**Tone bonus:** +1 if the item is inspiring/positive (new capability, learning opportunity, problem solved)

**Selection:**
- Max 3 items total
- Always include 1 critical security if score ≥8
- Fill remaining with highest-scoring tech/learning (must score ≥6)
- Post if ≥1 item qualifies

## 5. Write post (English only)

Slack format, <1000 characters, balanced tone:

```
⚡ *TUESDAY PULSE | {date}*

_{One-line highlight of the most interesting item}_

{emoji} *{Headline}*
{What + why it matters, 1 sentence}
→ {Action or opportunity, 1 sentence}
{plain URL}

{emoji} *{Second item...}*
...

*💡 This week:* {Encouraging note or tip}
```

**Emoji by category:**
- 🔒 Security · 🤖 AI Tools · 🧠 Models · 🧩 Languages/Frameworks · 💡 Learning · 🚀 New Tool

**Tone guidelines:**
- Security: factual, clear action, not alarmist
- Tech: "Check this out" not "You must migrate"
- Learning: inspiring, "opportunity to level up"
- Avoid: "URGENT", "CRITICAL" unless truly critical
- End on positive note

**Format rules:**
- Plain URLs only
- Slack mrkdwn: `*bold*`, `_italic_`
- Self-contained blocks
- English only (Friday weekly has Vietnamese)

## 6. Publish (scheduled Tuesday + ≥1 item scores ≥6 + not DRY_RUN)

1. Post to #dev-news
2. Get permalink
3. Verify URLs

**Do not post if:**
- Not Tuesday (for scheduled)
- ON_DEMAND mode
- No items scored ≥6
- DRY_RUN = true

## Output

**Format:** `MODE · DATE · Status`

**Status:**
- `POSTED {permalink}`
- `DRAFT` — for review
- `QUIET` — no items scored ≥6 (rare, but OK)
- `DRY_RUN`
- `SKIPPED_NOT_TUESDAY`

**Log:**
- Included: score — headline — category — source
- Dropped: score — headline — reason
- Tone: note if all items were negative/stressful (adjust next time)

---

## Usage

**Scheduled (cron):**
```bash
# Tuesday 9:00 AM Asia/Ho_Chi_Minh
0 9 * * 2 cd ~/.claude && claude-skill tuesday-pulse "run tuesday pulse"
```

**Manual:**
```
Run tuesday pulse, dry run
```

---

## Cost & Pairing

**Tuesday Pulse:** ~$0.20/run × 1/week = **~$0.80/month**
**Friday Weekly (my-dev-digest):** ~$0.60/run × 1/week = **~$2.40/month**

**Total: ~$3.20/month** for balanced coverage without spam.

**Content split:**
- **Tuesday:** Mid-week check-in covering Sat-Tue, balanced, 2-3 items
- **Friday:** Comprehensive review Mon-Fri, 4-5 items + radar, with agent-reach
- **Together:** Nothing important missed, no content fatigue, balanced tone
