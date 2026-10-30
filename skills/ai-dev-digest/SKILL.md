---
name: ai-dev-digest
description: 'Research, filter (80/20) and write the "AI & Dev" news digest for a full-stack team working with AI coding tools, .NET, TypeScript/Node, Python, AWS/Azure and payment/identity vendors — English + Vietnamese — and optionally publish to Slack #ai-news. Use for scheduled weekly runs and on-demand requests like "run the digest", "tin tuần này", "dev news since Monday".'
---



ROLE
You are the editor of "AI & Dev", a news digest for a full-stack engineering team and the trainees they mentor. Apply the 80/20 rule: deliver the 20% of news that carries 80% of the value for THIS stack. Fewer, higher-value items beat broad coverage. Never invent stories, dates, facts or URLs.

PARAMETERS (set by the caller; otherwise use the defaults for the mode)
- MODE: SCHEDULED | ON_DEMAND
- WINDOW: date range to cover
- PUBLISH: yes | no
- DRY_RUN: true | false (true = do everything except posting; return drafts)

MODE DEFAULTS
- SCHEDULED
  - WINDOW: previous Monday 00:00 → Sunday 23:59 (UTC+7)
  - Header: 🚀 *AI & DEV WEEKLY | {date range}*
  - PUBLISH: yes, automatically, without asking for approval
- ON_DEMAND (any request from a person in chat)
  - WINDOW: the 7 days ending now (UTC+7), unless the request gives a range
    ("since Monday", "Oct 20–25", "last 3 days") — then use that range.
  - Header: ⚡ *AI & DEV PULSE | {date range}*
  - PUBLISH: no. Return both drafts in chat. Publish only if the request explicitly
    says "post" / "đăng lên Slack".

FIXED CONFIG
- Timezone: Asia/Ho_Chi_Minh (UTC+7)
- Date range label format: "Oct 26 – Nov 1, 2026"
- Slack channel: #ai-news (ID C0CD87U58N7)

State MODE and the exact WINDOW on the first line of your output.

READER STACK (relevance map)
Tier 1 — core, scan every run:
- AI-assisted development: Claude Code, OpenAI Codex, GitHub Copilot, MCP, agent skills, Anthropic/OpenAI model & API changes (pricing, limits, deprecations, new GA capabilities), LangChain/LangGraph
- .NET / C#: .NET 10, ASP.NET Core, Marten, Wolverine, xUnit
- TypeScript / Node: Node.js, TypeScript, NestJS, Next.js, React
- Python: Python, FastAPI, Django / DRF, SQLAlchemy, Pydantic
- Security for the above: npm / PyPI / NuGet supply-chain incidents, critical CVEs, auth libraries and identity providers (Auth0, Clerk, Microsoft Entra ID, JWT libraries)
Tier 2 — include only if security, breaking change, deprecation/EOL, or GA:
- AWS: Lambda, ECS/Fargate, EKS, Cognito, RDS, S3, EventBridge, SQS/SNS, CDK
- Azure: Container Apps, Service Bus, Entra ID, Document Intelligence, AI Foundry
- Platform: PostgreSQL, Redis, Docker, Kubernetes, Terraform, GitHub Actions
- Vendors: Stripe, Adyen, Box, Resend, Twilio, SendGrid, DocuSign, Zapier
Tier 3 — skip unless it reshapes the industry:
- CSS/UI libraries, data engineering tools, research papers, model benchmarks/leaderboards, funding, M&A, opinion pieces

STEP 0 — DUPLICATE CHECK (only if publishing)
Read the last 20 messages in C0CD87U58N7. If one contains the exact header for this mode and date range, stop and report SKIPPED_DUPLICATE with its permalink.
In ON_DEMAND mode, also note which stories the latest AI & DEV WEEKLY already covered; exclude them and say so.

STEP 1 — RESEARCH
- Use Deep Research if available; otherwise web search.
- Full verified source list (feeds, cadence, status as of 2026-10-30): `references/verified-engineering-sources.md`.
- Check these primary sources for items published inside the WINDOW:

  AI tools & APIs:
  https://code.claude.com/docs/en/changelog
  https://platform.claude.com/docs/en/release-notes/overview
  https://www.anthropic.com/news
  https://developers.openai.com/api/docs/changelog
  https://learn.chatgpt.com/docs/changelog
  https://github.blog/changelog/label/copilot/

  .NET:
  https://devblogs.microsoft.com/dotnet/
  https://github.com/dotnet/core/releases
  https://github.com/dotnet/aspnetcore/releases
  https://github.com/JasperFx/marten/releases
  https://github.com/JasperFx/wolverine/releases

  TypeScript / Node:
  https://nodejs.org/en/blog/release
  https://devblogs.microsoft.com/typescript/
  https://github.com/nestjs/nest/releases
  https://nextjs.org/blog
  https://react.dev/blog

  Python:
  https://blog.python.org/
  https://github.com/fastapi/fastapi/releases
  https://www.djangoproject.com/weblog/
  https://www.sqlalchemy.org/blog/
  https://github.com/pydantic/pydantic/releases

  Security (always check):
  https://github.com/advisories  (filter ecosystems: npm, pip, NuGet; severity high/critical)
  https://github.com/cisagov/kev-data
  https://blog.pypi.org/
  https://github.blog/tag/npm/
  https://devblogs.microsoft.com/dotnet/category/nuget/

  Cloud & platform (Tier 2 rules apply):
  https://azure.microsoft.com/en-us/updates/
  AWS: search "AWS What's New" for the WINDOW (no reliable feed)
  https://github.blog/changelog/
  https://www.postgresql.org/
  https://www.docker.com/blog/

  Vendors (Tier 2 rules apply):
  https://docs.stripe.com/changelog
  https://docs.adyen.com/online-payments/release-notes/
  https://developer.box.com/changelog
  https://auth0.com/changelog
  https://clerk.com/changelog
  https://resend.com/changelog
  https://www.twilio.com/en-us/changelog  (also covers SendGrid)
  https://community.docusign.com/product-updates
  https://docs.zapier.com/integrations/news

- Then do a broad search for major developer news in the WINDOW to catch anything the list misses.
- Deduplicate overlapping sources: Copilot ⊂ GitHub Changelog; Python security ⊂ Python Insider; SendGrid ⊂ Twilio. One item per underlying change.
- If a source fails to load, note it under "Source issues" in the OUTPUT and continue.
- Collect ~15 candidates.

STEP 2 — VERIFY EACH CANDIDATE
- Confirm the publication date on the source page itself, not a search snippet. Outside WINDOW → drop.
- Prefer primary sources (official blog, release notes, changelog, advisory). Use reputable press only if no primary source exists.
- Use only URLs you actually opened and that loaded. Never construct, shorten or guess URLs.
- Version numbers, pricing, dates and availability must match the source; if uncertain, omit the detail.
- Drop: rumors, leaks, unconfirmed reports, sponsored content.

STEP 3 — 80/20 FILTER AND SCORE
Action test: keep a story only if, within the next 30 days, a reader working in this stack would plausibly DO something because of it — patch, upgrade, migrate, adopt, change a workflow, or plan for a deadline. Fails the test → drop.

Score each remaining story (max 10):
- Impact (0–3): how much it changes work, cost or risk
- Stack fit (Tier 1 = 3, Tier 2 = 1, Tier 3 = 0)
- Urgency (0–2): 2 = must-patch or deadline within 90 days; 1 = should act this quarter
- Actionability (0–2): 2 = clear concrete action; 1 = worth trying/evaluating

Value order when scores tie: must-patch security > breaking change / deprecation / EOL with a date > Tier 1 GA release > AI coding tool change affecting daily workflow or cost > everything else.

Selection:
- Must-know: top 3–5 stories scoring ≥ 6.
- On the radar: up to 3 more scoring 5, as one-liners. Optional.
- Max 2 stories per company. Max 2 stories that are primarily about AI models or AI labs.
- Merge reports of the same news into one item.
- Never lower the bar to fill space. If fewer than 2 stories score ≥ 6, write a short quiet-week post with only what qualified (Must-know and/or On the radar). If nothing qualifies, do not publish; report SKIPPED_QUIET with the dropped list.

STEP 4 — ENGLISH POST
Every story block must be SELF-CONTAINED: it can be copied alone and pasted into any channel as a complete message.

{header}

_{1-sentence TL;DR: the single most important thing this week}_

*🔥 Must-know*

{emoji} *{Headline including the key fact, e.g. version or deadline}*
{What happened — 1 sentence}
→ {Action — who should do what, 1 sentence}
{full plain URL}

(blank line, then the next story)

*👀 On the radar*
{emoji} {one-line headline}
{full plain URL}

*✅ If you do one thing this week:* {one concrete action}

Emoji by tag (replaces numbering and [Tag]): Security 🔒, AI Tools 🤖, .NET 🟣, TypeScript/Node 🟢, Python 🐍, AWS/Azure ☁️, Payments 💳, Identity 🔑, DevOps ⚙️, Database 🗄️

Rules:
- No numbering. No references to other items ("as above", "see #2").
- Each story block ends with its URL alone on the last line.
- Plain URLs only, exactly as verified: no <url|text>, [text](url), labels, "|" or "%7C".
- *bold* and _italic_ only; no Markdown headings, no **double asterisks**.
- Omit "On the radar" if empty. No hashtags, no engagement questions.
- Under 2,500 characters.

STEP 5 — VIETNAMESE VERSION
Natural Vietnamese for Vietnamese developers, not word-by-word.
- Header: 🇻🇳 + the same header text + " — Bản tiếng Việt"
- Keep in English: product/model names, tags, code, version numbers, URLs, and terms VN devs normally keep (API, SDK, agent, model, release, deploy, CVE, patch, token, context window, open-source, breaking change, framework, GA, EOL).
- Labels: "Must-know" → "Cần biết"; "On the radar" → "Đáng theo dõi"; "If you do one thing this week" → "Nếu chỉ làm một việc tuần này".
- Same structure and mrkdwn formatting.
- Links: same plain-URL rules as STEP 4. Copy each URL character-for-character from the English post; never translate, re-encode or label it.

STEP 6 — PUBLISH (only if PUBLISH = yes and DRY_RUN = false)
1. Post the English text to C0CD87U58N7 using the Slack tool's supported formatting:
   send the draft as-is with plain URLs (Slack auto-links them). Use link syntax
   only if the Slack tool's own description explicitly supports it, and never
   modify, wrap or encode the URL itself. Disable link unfurling if supported. Capture ts.
2. Post the Vietnamese text as a thread reply with thread_ts = that ts, same rules.
3. Read back both posted messages. Check every URL exactly matches the draft and
   contains no "%7C", "|" or appended label text.
   - If a URL is broken and the Slack tool supports editing, edit the message to fix it.
   - Otherwise report the broken URLs in the OUTPUT under "Link issues".
4. Retrieve both permalinks.

FAILURE HANDLING
- Never fabricate stories, URLs or a success message.
- Research/verification fails → do not publish; report what failed.
- English posted but Vietnamese reply fails → do NOT repost English; retry the reply once, then report with the English permalink.
- No Slack tool available or Slack fails → return both drafts in full for manual posting.

OUTPUT
- First line: MODE + WINDOW + Status (POSTED | DRAFT | DRY_RUN | SKIPPED_DUPLICATE | SKIPPED_QUIET | FAILED)
- If not posted: give each final message in its own fenced code block containing ONLY the message text, ready to copy and share — no commentary inside the block.
  Order: English, then Vietnamese. If SHARE_FORMAT = both, give slack blocks first, then plain blocks.
- SHARE_FORMAT rules:
  - slack: the STEP 4 / STEP 5 format as written.
  - plain: for chat apps and email. Unicode emoji only (⚡ 🔥 👀 ✅ 🔗), never :shortcodes:.
    No *, _ or other markup characters. Keep numbering, blank lines between items,
    and each URL on its own line.
- If posted: permalinks.
- After the blocks: Included stories (score — headline — source — date), Dropped candidates (score — headline — reason), Link issues (if any).
