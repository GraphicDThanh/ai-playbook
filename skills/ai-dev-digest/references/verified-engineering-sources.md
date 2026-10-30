# Verified engineering information diet

Checked: **30 October 2026 (Asia/Saigon)**. Active window: **1 August–30 October 2026**.

This is a source audit, not a news digest. Accuracy limits are retained rather than filled with plausible URLs. **VERIFIED** means the source page loaded, a dated recent item was observed, and any listed feed returned parseable RSS/Atom. **UNVERIFIED** means a required check did not pass; it does not mean a source is fake or permanently unavailable. Channel identities can be confirmed even when their feed fails.

“no feed” means no official feed was discovered and validated in this audit, not proof that no endpoint exists. Dates use publication timestamps where available; GitHub release feeds expose updated timestamps. Date-only items retain their publisher’s date. Cadences are approximate observations, not publishing commitments. The OPML contains one selected canonical feed per verified source, deduplicates shared feeds, and excludes stale or failed feeds. Publisher pages and XML were fetched directly; XML root/entry parsing was used rather than accepting a 200 response or MIME type alone.

## A1. Primary sources

| Name | Area | URL | Feed URL (or no feed) | Latest item date | Cadence | Why it’s worth following | Status |
|---|---|---|---|---|---|---|---|
| Anthropic news | AI | [Source](https://www.anthropic.com/news) | no feed | 2026-10-28 | Several/week | Official launches; filter company and policy announcements. | VERIFIED |
| Claude Code | AI | [Source](https://code.claude.com/docs/en/changelog) | [Feed](https://code.claude.com/docs/en/changelog/rss.xml) | 2026-10-30 | Several/week | Operational changes to the agent you use daily. | VERIFIED |
| Anthropic API | AI | [Source](https://platform.claude.com/docs/en/release-notes/overview) | [Feed](https://platform.claude.com/docs/en/release-notes/feed.xml) | 2026-10-29 | Several/week | API behavior, models, tooling and deprecations. | VERIFIED |
| OpenAI API | AI | [Source](https://developers.openai.com/api/docs/changelog) | no feed | 2026-10-28 | Several/week | API changes and migration requirements; developer RSS found was stale, so omitted. | VERIFIED |
| OpenAI Codex | AI | [Source](https://learn.chatgpt.com/docs/changelog) | [Feed](https://learn.chatgpt.com/docs/changelog/rss.xml) | 2026-10-29 | Several/week | Agent, CLI and workflow changes; canonical page/feed redirect verified. | VERIFIED |
| GitHub Copilot | AI | [Source](https://github.blog/changelog/label/copilot/) | [Feed](https://github.blog/changelog/label/copilot/feed/) | 2026-10-28 | Several/week | Copilot-only filter reduces general GitHub noise. | VERIFIED |
| .NET Blog | .NET | [Source](https://devblogs.microsoft.com/dotnet/) | [Feed](https://devblogs.microsoft.com/dotnet/feed/) | 2026-10-29 | Several/week | Runtime, ASP.NET and tooling announcements. | VERIFIED |
| ASP.NET Core | .NET | [Source](https://github.com/dotnet/aspnetcore/releases) | [Feed](https://github.com/dotnet/aspnetcore/releases.atom) | 2026-10-23 | Monthly + patches | Framework release notes; filter supported .NET 10 versions. | VERIFIED |
| .NET release notes | .NET | [Source](https://github.com/dotnet/core/releases) | [Feed](https://github.com/dotnet/core/releases.atom) | 2026-10-13 | Monthly | SDK/runtime release inventory; complement the Blog for out-of-band fixes. | VERIFIED |
| Marten | .NET | [Source](https://github.com/JasperFx/marten/releases) | [Feed](https://github.com/JasperFx/marten/releases.atom) | 2026-10-28 | Several/week | Exact event-store and document-database changes. | VERIFIED |
| Wolverine | .NET | [Source](https://github.com/JasperFx/wolverine/releases) | [Feed](https://github.com/JasperFx/wolverine/releases.atom) | 2026-10-30 | Several/week | Messaging, durable execution and HTTP integration changes. | VERIFIED |
| Node.js | TS/Node | [Source](https://nodejs.org/en/blog/release) | [Feed](https://nodejs.org/en/feed/blog.xml) | 2026-10-29 | Weekly + patches | Runtime releases and security fixes; feed also includes other blog categories. | VERIFIED |
| TypeScript | TS/Node | [Source](https://devblogs.microsoft.com/typescript/) | [Feed](https://devblogs.microsoft.com/typescript/feed/) | 2026-10-20 | Release-driven | Compiler changes and migration notes. | VERIFIED |
| NestJS | TS/Node | [Source](https://github.com/nestjs/nest/releases) | [Feed](https://github.com/nestjs/nest/releases.atom) | 2026-10-28 | Several/week | Framework patch notes, with full change comparisons. | VERIFIED |
| React | TS/Node | [Source](https://react.dev/blog) | [Feed](https://react.dev/rss.xml) | 2026-09-09 | Release-driven | Framework releases and security notices. | VERIFIED |
| Python Insider | Python | [Source](https://blog.python.org/) | [Feed](https://blog.python.org/rss.xml) | 2026-10-26 | Release-driven | CPython maintenance and security releases. | VERIFIED |
| FastAPI | Python | [Source](https://github.com/fastapi/fastapi/releases) | [Feed](https://github.com/fastapi/fastapi/releases.atom) | 2026-10-23 | Several/week | Framework changes, compatibility and fixes. | VERIFIED |
| Django | Python | [Source](https://www.djangoproject.com/weblog/) | [Feed](https://www.djangoproject.com/rss/weblog/) | 2026-10-26 | Several/week | Official framework news; filter organizational posts. | VERIFIED |
| SQLAlchemy | Python | [Source](https://www.sqlalchemy.org/blog/) | [Feed](https://www.sqlalchemy.org/blog/feed/index.xml) | 2026-10-21 | Release-driven | ORM/Core fixes and compatibility changes. | VERIFIED |
| Pydantic | Python | [Source](https://github.com/pydantic/pydantic/releases) | [Feed](https://github.com/pydantic/pydantic/releases.atom) | 2026-10-29 | Release-driven | Validation behavior and compatibility changes. | VERIFIED |
| Next.js | TS/Node | [Source](https://nextjs.org/blog) | no feed | 2026-10-28 | Several/month | Release, security and migration announcements; no blog feed discovered. | VERIFIED |
| Python security announcements | Security | [Source](https://blog.python.org/) | [Feed](https://blog.python.org/rss.xml) | 2026-10-26 | As needed | Verified security-release coverage in Python Insider; dedicated mailing-list recency unresolved. | VERIFIED |
| Django security releases | Security | [Source](https://www.djangoproject.com/weblog/) | [Feed](https://www.djangoproject.com/rss/weblog/) | 2026-10-06 | As needed | Latest security-release post; broader weblog also contains reporting-policy updates. | VERIFIED |
| GitHub Advisory Database | Security | [Source](https://github.com/advisories) | no feed | 2026-10-29 | Daily | Filter npm, pip and NuGet advisories; no official per-advisory RSS found. | VERIFIED |
| CISA KEV — official mirror | Security | [Source](https://github.com/cisagov/kev-data) | no feed | 2026-10-29 | Weekdays/as needed | Official JSON/CSV mirror; canonical cisa.gov page returned 403. | VERIFIED |
| npm security | Security | [Source](https://github.blog/tag/npm/) | [Feed](https://github.blog/tag/npm/feed/) | 2026-08-06 | Irregular | Official npm-tagged GitHub posts; broader than security alone. | VERIFIED |
| PyPI security | Security | [Source](https://blog.pypi.org/) | [Feed](https://blog.pypi.org/feed_rss_created.xml) | 2026-10-26 | Several/month | Official package-index security and operational announcements. | VERIFIED |
| NuGet security | Security | [Source](https://devblogs.microsoft.com/dotnet/category/nuget/) | [Feed](https://devblogs.microsoft.com/dotnet/category/nuget/feed/) | 2026-10-13 | Release-driven | Official NuGet category, broader than security; cross-check advisories. | VERIFIED |
| AWS What’s New | Cloud | [Source](https://aws.amazon.com/about-aws/whats-new/) | UNVERIFIED — returned HTML | Unknown | Daily (expected) | Page loads, but advertised feed returned HTML and latest list was not exposed. | UNVERIFIED |
| Azure Updates | Cloud | [Source](https://azure.microsoft.com/en-us/updates/) | [Feed](https://www.microsoft.com/releasecommunications/api/v2/azure/rss) | 2026-10-29 | Daily | Service availability, previews and retirements. | VERIFIED |
| GitHub Changelog | Platform | [Source](https://github.blog/changelog/) | [Feed](https://github.blog/changelog/feed/) | 2026-10-29 | Daily | Platform, Actions and security changes; overlaps Copilot. | VERIFIED |
| PostgreSQL news | Platform | [Source](https://www.postgresql.org/) | [Feed](https://www.postgresql.org/news.rss) | 2026-10-28 | Several/week | Official news; includes community events, so filter release/security titles. | VERIFIED |
| Docker | Platform | [Source](https://www.docker.com/blog/) | [Feed](https://www.docker.com/feed/) | 2026-10-29 | Several/week | Container tooling and platform changes; filter product marketing. | VERIFIED |
| Stripe | Vendors | [Source](https://docs.stripe.com/changelog) | no feed | 2026-10-28 | Release-driven | Versioned API changes; essential for pinned API integrations. | VERIFIED |
| Adyen online payments | Vendors | [Source](https://docs.adyen.com/online-payments/release-notes/) | [Feed](https://docs.adyen.com/online-payments/release-notes.xml) | 2026-10-20 | Several/month | Checkout API and Drop-in/Components notes; other Adyen products have separate notes. | VERIFIED |
| Box | Vendors | [Source](https://developer.box.com/changelog/2026) | [Feed](https://developer.box.com/changelog/2026/rss.xml) | 2026-10-28 | Several/week | API/SDK and platform changes; feed is scoped to 2026. | VERIFIED |
| Auth0 | Vendors | [Source](https://auth0.com/changelog) | no feed | 2026-10-29 | Several/week | Authentication behavior, tenant features and deprecations. | VERIFIED |
| Clerk | Vendors | [Source](https://clerk.com/changelog) | [Feed](https://clerk.com/changelog/atom.xml) | 2026-10-29 | Several/week | Auth SDK, session and security changes. | VERIFIED |
| Resend | Vendors | [Source](https://resend.com/changelog) | [Feed](https://resend.com/changelog/rss.xml) | 2026-10-26 | Weekly | Email API, delivery tooling and webhook changes. | VERIFIED |
| Twilio | Vendors | [Source](https://www.twilio.com/en-us/changelog) | [Feed](https://www.twilio.com/en-us/changelog.feed.xml) | 2026-10-20 | Several/week | Communications API changes across products. | VERIFIED |
| SendGrid | Vendors | [Source](https://www.twilio.com/en-us/changelog) | [Feed](https://www.twilio.com/en-us/changelog.feed.xml) | 2026-10-16 | Irregular | Shared Twilio feed; latest SendGrid-specific item was Unified Login. Filter locally. | VERIFIED |
| DocuSign release notes | Vendors | [Source](https://community.docusign.com/product-updates) | no feed | 2026-10-27 | Monthly | Official Release Hub; product/developer change details and rollout stage. | VERIFIED |
| DocuSign Node SDK supplement | Vendors | [Source](https://github.com/docusign/docusign-esign-node-client/releases) | [Feed](https://github.com/docusign/docusign-esign-node-client/releases.atom) | 2026-10-15 | Release-driven | Verified SDK release feed; does not replace platform release notes. | VERIFIED |
| Zapier developer platform | Vendors | [Source](https://docs.zapier.com/integrations/news) | [Feed](https://docs.zapier.com/integrations/news.xml) | 2026-10-14 | Release-driven | CLI, runtime, auth and integration-platform changes. | VERIFIED |

**Scope notes:** Python Insider is the verified fallback for Python security announcements; the dedicated security-announce archive loaded, but its current activity/feed was not established. Django’s latest security-release post was 6 October (a security-reporting policy update followed on 8 October). PyPI/npm/NuGet feeds are broader official announcement streams, not exhaustive package-vulnerability feeds. Use the Advisory Database alongside them. CISA’s canonical page returned 403; its official mirror and JSON loaded, with `dateReleased` 2026-10-29 and newest `dateAdded` 2026-10-29. DocuSign SDK notes are explicitly supplemental. AWS’s advertised RSS endpoint returned an HTML document in direct checks, despite the web reader reporting an RSS MIME type; it was excluded. OpenAI’s general developer RSS was parseable but last showed 30 April, so it is not used as API-changelog coverage. The Codex feed was larger than 4 MB and passed after a complete fetch.

## A2. Independent written voices

| Name | Area | URL | Feed URL (or no feed) | Latest item date | Cadence | Why it’s worth following | Status |
|---|---|---|---|---|---|---|---|
| Simon Willison | AI engineering | [Source](https://simonwillison.net/) | [Feed](https://simonwillison.net/atom/everything/) | 2026-10-29 | Daily | Hands-on model/tool experiments, security and agent workflow analysis. | VERIFIED |
| Latent Space | AI engineering | [Source](https://latent.space/) | [Feed](https://latent.space/feeds/all.xml) | 2026-10-29 | Several/week | Interviews with builders of AI infrastructure and production systems. | VERIFIED |
| Jeremy D. Miller | .NET | [Source](https://jeremydmiller.com/) | [Feed](https://jeremydmiller.com/feed/) | 2026-10-29 | Several/week | Directly relevant Marten/Wolverine design and release context; maintainer perspective. | VERIFIED |
| Andrew Lock | .NET | [Source](https://andrewlock.net/) | [Feed](https://andrewlock.net/rss.xml) | 2026-10-20 | Every 1–2 weeks | Detailed ASP.NET/runtime internals with reproducible examples. | VERIFIED |
| Milan Jovanović | .NET | [Source](https://milanjovanovic.tech/blog) | [Feed](https://milanjovanovic.tech/rss/feed.xml) | 2026-10-24 | Weekly | Applied backend patterns; select substantive articles over course promotion. | VERIFIED |
| Node Weekly | TypeScript/Node | [Source](https://nodeweekly.com/) | [Feed](https://nodeweekly.com/rss/) | 2026-10-29 | Weekly | Independent editorial filter for Node releases, performance and ecosystem changes. | VERIFIED |
| Brett Cannon | Python | [Source](https://snarky.ca/) | [Feed](https://snarky.ca/rss/) | 2026-08-16 | Irregular | Packaging, reproducibility and language design from a core practitioner. | VERIFIED |
| James Bennett | Python | [Source](https://www.b-list.org/weblog/) | [Feed](https://www.b-list.org/feeds/entries/) | 2026-08-10 | Irregular | Django/Python security and engineering tradeoffs; publication date excludes old-post updates. | VERIFIED |
| Martin Fowler | Architecture & practice | [Source](https://martinfowler.com/) | [Feed](https://martinfowler.com/feed.atom) | 2026-10-29 | Several/week | Architecture, delivery and AI-assisted engineering analysis; includes guest authors. | VERIFIED |
| Architecture Notes | Architecture & practice | [Source](https://architecturenotes.co/) | [Feed](https://architecturenotes.co/feed) | 2026-10-04 | Roughly weekly | Architecture case studies and curated technical reading; select depth over roundups. | VERIFIED |
| The Pragmatic Engineer | Leadership/mentoring | [Source](https://newsletter.pragmaticengineer.com/) | [Feed](https://newsletter.pragmaticengineer.com/feed) | 2026-10-29 | Several/week | Engineering organizations, delivery and career practices; some content paywalled. | VERIFIED |
| Charity Majors | Leadership/mentoring | [Source](https://charity.wtf/) | [Feed](https://charity.wtf/feed) | 2026-10-08 | Irregular | Production ownership, observability and practical engineering management. | VERIFIED |
| Julia Evans | Leadership/mentoring | [Source](https://jvns.ca/) | [Feed](https://jvns.ca/atom.xml) | 2026-09-27 | Irregular | Excellent technical explanation models for mentoring; mixed personal/technical feed. | VERIFIED |

These are independent authors/publications, not necessarily commercially neutral. Jeremy Miller maintains Marten/Wolverine; treat that overlap as useful implementation context, not independent product evaluation. Julia Evans’ latest item is personal; retain her feed only if that mixed scope is acceptable. James Bennett’s newest observed *published* item was 10 August; a 1 September update to an older post was not counted as a new post. Total TypeScript’s discovered RSS was stale and was not used to fill the TS quota.

## A3. YouTube voices and conference channels

| Name | Area | URL | Feed URL (or no feed) | Latest item date | Cadence | Why it’s worth following | Status |
|---|---|---|---|---|---|---|---|
| Milan Jovanović | .NET | [Source](https://www.youtube.com/@MilanJovanovicTech/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-28 | Weekly | Applied .NET/backend delivery; select technical videos. Channel ID: `UCC_dVe-RI-vgCZfls06mDZQ`. | UNVERIFIED |
| Zoran Horvat | .NET | [Source](https://www.youtube.com/@zoran-horvat/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-07 | Several/month | C# type modeling and deeper object-oriented design. Channel ID: `UCxsWfh8LCcn55mFB6zGBT1g`. | UNVERIFIED |
| CodeOpinion | Architecture | [Source](https://www.youtube.com/@CodeOpinion/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-28 | Weekly/irregular | DDD, messaging and distributed-systems tradeoffs. Channel ID: `UC3RKA4vunFAfrfxiJhPEplw`. | UNVERIFIED |
| Matt Pocock | TS/Node | [Source](https://www.youtube.com/@mattpocockuk/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-05 | Irregular | TypeScript expertise; recent output emphasizes agent skills/workflows. Channel ID: `UCswG6FSbgZjbWtdf_hMLaow`. | UNVERIFIED |
| ArjanCodes | Python | [Source](https://www.youtube.com/@ArjanCodes/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-23 | Weekly | Python design, refactoring and third-party integration boundaries. Channel ID: `UCVhQ2NnY5Rskt6UjCUkJ_DA`. | UNVERIFIED |
| Latent Space | AI engineering | [Source](https://www.youtube.com/@LatentSpacePod/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-28 | Several/week | Conversations with engineers shipping AI systems. Channel ID: `UCxBcwypKK-W3GHd_RZ9FZrQ`. | UNVERIFIED |
| NDC Conferences | Conference | [Source](https://www.youtube.com/@NDC/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-28 | Batch/daily | Deep practitioner talks across .NET, cloud, security and architecture. Channel ID: `UCTdw38Cw6jcm0atBPA39a0Q`. | UNVERIFIED |
| GOTO Conferences | Conference | [Source](https://www.youtube.com/@GOTO-/videos) | UNVERIFIED — HTTP 404/500 | 2026-10-29 | Several/week | Architecture, distributed systems and engineering practice talks. Channel ID: `UCs_tLP3AiwYKwdUHpltJPuA`. | UNVERIFIED |

All eight channel pages and recent video pages loaded, and channel IDs were extracted from first-party page metadata. **Their RSS requests repeatedly returned HTTP 404/500, so no YouTube feed is in the OPML.** This distinguishes verified channels/activity from unverified feed delivery. To avoid printing failed URLs as working links, the requested feed format is recorded only as a template: `https://www.youtube.com/feeds/videos.xml?channel_id=CHANNEL_ID`. Insert an ID from the table and revalidate before enabling ingestion. Zoran’s upload is 6 October in its original UTC−07 timestamp and 7 October in UTC.

## A4. X accounts

Every attempted candidate profile returned HTTP 403. Under your “open it yourself” rule, **there are zero VERIFIED X accounts in this audit**. Failed profile URLs are deliberately not presented as working links. Identity, activity and cadence must not be inferred from reputation or search snippets. The rows below preserve your candidate list for follow-up; the reasons are selection hypotheses, not verified endorsements.

| Name | Area | URL | Feed URL (or no feed) | Latest item date | Cadence | Why it’s worth following | Status |
|---|---|---|---|---|---|---|---|
| @simonw | AI engineering | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for hands-on AI tooling and security. | UNVERIFIED |
| @swyx | AI engineering | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for AI engineering ecosystem context. | UNVERIFIED |
| @karpathy | AI engineering | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for practitioner explanations and research context. | UNVERIFIED |
| @AndrewYNg | AI engineering | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for applied-AI perspective; broad scope. | UNVERIFIED |
| @addyosmani | Web engineering | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for web performance and engineering practice. | UNVERIFIED |
| @alexalbert__ | Claude | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for first-party Claude developer context. | UNVERIFIED |
| @bcherny | Claude Code | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for first-party coding-agent workflow context. | UNVERIFIED |
| @AnthropicAI | Official AI | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for official announcements; overlaps primary sources. | UNVERIFIED |
| @OpenAIDevs | Official AI | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for API and developer announcements. | UNVERIFIED |
| @dotnet | Official .NET | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for platform announcements; overlaps .NET Blog. | UNVERIFIED |
| @nodejs | Official Node | Blocked (403) | no feed verified | Unknown | Unknown | Candidate for runtime announcements; overlaps release feed. | UNVERIFIED |
| @ghchangelog | Official GitHub | Blocked (403) | no feed verified | Unknown | Unknown | Actual handle linked from GitHub Changelog; recent X activity remains unverified. | UNVERIFIED |

**Correction:** GitHub Changelog’s own page links to **@ghchangelog**, not the proposed @GitHubChangelog. The former was attempted and blocked. This verifies the publisher’s outbound identity reference, not a recent X post.

## A5. Vietnamese-language sources

| Name | Area | URL | Feed URL (or no feed) | Latest item date | Cadence | Why it’s worth following | Status |
|---|---|---|---|---|---|---|---|
| TienNHM | Vietnamese | [Source](https://tiennhm.io.vn/) | [Feed](https://tiennhm.io.vn/blog/rss.xml) | 2026-10-24 | Several/month | .NET/backend, PostgreSQL and MCP/agent skills; recent homepage and feed verified. | VERIFIED |
| ManhPT | Vietnamese | [Source](https://manhpt.com/) | [Feed](https://manhpt.com/rss.xml) | 2026-10-17 | Several/month | First-person RAG, knowledge systems and coding-agent operations; recent homepage and feed verified. | VERIFIED |
| TungDaDev | Vietnamese | [Source](https://tungbt.vercel.app/) | [Feed](https://tungbt.vercel.app/feed.xml) | 2026-10-14 | Several/week | Backend practitioner writing about agent tooling, evaluation and AI security; full recent article loaded. | VERIFIED |

Only three sources met the page/activity/feed checks and the initial practitioner-content screen. TienNHM and ManhPT expose substantial recent content on their homepages, but direct requests for the newest individual articles returned 403; their editorial quality assessment is consequently limited to that visible material. TungDaDev’s newest full article loaded. These are a small trial shortlist, not a claim that all their technical statements have been independently validated. Broad community homepages were not treated as consistently high-signal editorial feeds.

## B. Dropped or excluded

“Not found” below includes required evidence not found or not retrievable in this audit; it does not assert that a publication/account has ceased to exist. Dates are last observed publication dates, unless explicitly marked as feed dates.

| Name | Reason (inactive / beginner / hype / not found) | Last activity date |
|---|---|---|
| [Nick Chapsas](https://www.youtube.com/@nickchapsas/videos) | inactive — newest item on loaded Videos tab is outside 90 days | 2026-07-21 |
| [Andrej Karpathy — YouTube](https://www.youtube.com/@AndrejKarpathy/videos) | inactive — useful archive, fails weekly-diet activity rule | 2025-02-27 |
| [Fireship](https://www.youtube.com/@Fireship/videos) | hype — current bubble/news commentary does not fit this practitioner diet | 2026-10-28 |
| [AI Explained](https://www.youtube.com/@aiexplained-official/videos) | hype — broad lab/race commentary rather than production engineering | 2026-10-12 |
| [ByteByteGo](https://www.youtube.com/@ByteByteGo/videos) | beginner — overview/interview-prep emphasis; occasional deep items may still be useful | 2026-10-22 |
| Continuous Delivery | not found — requested channel returned 404 here; not evidence of inactivity | Unknown |
| [2ality](https://2ality.com/) | not found — explicit temporarily-offline notice; recent posts unavailable | Unknown |
| [Hynek Schlawack](https://hynek.me/articles/) | inactive — newest published feed item outside 90 days; old-post edits do not qualify | 2025-09-19 |
| [Total TypeScript written RSS](https://www.totaltypescript.com/articles) | not found — recent written publication evidence unresolved; discovered feed stale | 2023-11-30 (feed item) |
| [Ehkoo](https://ehkoo.com/) | inactive — even later observed feed entries are from 2018 | 2018-04-15 (latest among observed entries) |
| [Huy Rocks](https://www.huy.rocks/) | inactive — also largely English-language, so weak fit for task 5 | 2026-05-29 |
| [Fullstack Station](https://fullstackstation.com/) | inactive — latest feed item outside 90 days | 2026-04-10 (publisher issue date) |
| [Kipalog](https://kipalog.com/) | not found — returned generic site and an empty feed, no recent practitioner posts | Unknown |
| [Grokking Vietnam](https://www.grokking.org/) | not found — mission/newsletter pages load, but a dated recent issue was not established | Unknown |
| [Viblo — global newest feed](https://viblo.asia/newest) | beginner — mixed-author portal; high-volume tutorials need author-level curation | 2026-10-30 |
| [Tôi đi code dạo](https://toidicodedao.com/) | beginner — latest item promotes an introductory automation course; limited senior signal in sample | 2026-08-20 |
| [Văn Ngọc Tân](https://www.vanngoctan.com/) | beginner — short introductory system-design series in observed sample | 2026-10-23 |

## C. OPML

**48 unique verified feeds.** Empty YouTube outline is intentional. Only feeds selected in A1, A2 and A5 are included; duplicates, alternate encodings, stale feeds and failed endpoints are excluded.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<opml version="2.0">
  <head>
    <title>Verified engineering information diet — 2026-10-30</title>
  </head>
  <body>
    <outline text="Act" title="Act">
      <outline text="Claude Code" title="Claude Code" type="rss" xmlUrl="https://code.claude.com/docs/en/changelog/rss.xml" htmlUrl="https://code.claude.com/docs/en/changelog" />
      <outline text="Anthropic API" title="Anthropic API" type="rss" xmlUrl="https://platform.claude.com/docs/en/release-notes/feed.xml" htmlUrl="https://platform.claude.com/docs/en/release-notes/overview" />
      <outline text="OpenAI Codex" title="OpenAI Codex" type="rss" xmlUrl="https://learn.chatgpt.com/docs/changelog/rss.xml" htmlUrl="https://learn.chatgpt.com/docs/changelog" />
      <outline text="GitHub Copilot" title="GitHub Copilot" type="rss" xmlUrl="https://github.blog/changelog/label/copilot/feed/" htmlUrl="https://github.blog/changelog/label/copilot/" />
      <outline text=".NET Blog" title=".NET Blog" type="rss" xmlUrl="https://devblogs.microsoft.com/dotnet/feed/" htmlUrl="https://devblogs.microsoft.com/dotnet/" />
      <outline text="ASP.NET Core" title="ASP.NET Core" type="rss" xmlUrl="https://github.com/dotnet/aspnetcore/releases.atom" htmlUrl="https://github.com/dotnet/aspnetcore/releases" />
      <outline text=".NET release notes" title=".NET release notes" type="rss" xmlUrl="https://github.com/dotnet/core/releases.atom" htmlUrl="https://github.com/dotnet/core/releases" />
      <outline text="Marten" title="Marten" type="rss" xmlUrl="https://github.com/JasperFx/marten/releases.atom" htmlUrl="https://github.com/JasperFx/marten/releases" />
      <outline text="Wolverine" title="Wolverine" type="rss" xmlUrl="https://github.com/JasperFx/wolverine/releases.atom" htmlUrl="https://github.com/JasperFx/wolverine/releases" />
      <outline text="Node.js" title="Node.js" type="rss" xmlUrl="https://nodejs.org/en/feed/blog.xml" htmlUrl="https://nodejs.org/en/blog/release" />
      <outline text="TypeScript" title="TypeScript" type="rss" xmlUrl="https://devblogs.microsoft.com/typescript/feed/" htmlUrl="https://devblogs.microsoft.com/typescript/" />
      <outline text="NestJS" title="NestJS" type="rss" xmlUrl="https://github.com/nestjs/nest/releases.atom" htmlUrl="https://github.com/nestjs/nest/releases" />
      <outline text="React" title="React" type="rss" xmlUrl="https://react.dev/rss.xml" htmlUrl="https://react.dev/blog" />
      <outline text="Python Insider" title="Python Insider" type="rss" xmlUrl="https://blog.python.org/rss.xml" htmlUrl="https://blog.python.org/" />
      <outline text="FastAPI" title="FastAPI" type="rss" xmlUrl="https://github.com/fastapi/fastapi/releases.atom" htmlUrl="https://github.com/fastapi/fastapi/releases" />
      <outline text="Django" title="Django" type="rss" xmlUrl="https://www.djangoproject.com/rss/weblog/" htmlUrl="https://www.djangoproject.com/weblog/" />
      <outline text="SQLAlchemy" title="SQLAlchemy" type="rss" xmlUrl="https://www.sqlalchemy.org/blog/feed/index.xml" htmlUrl="https://www.sqlalchemy.org/blog/" />
      <outline text="Pydantic" title="Pydantic" type="rss" xmlUrl="https://github.com/pydantic/pydantic/releases.atom" htmlUrl="https://github.com/pydantic/pydantic/releases" />
      <outline text="npm security" title="npm security" type="rss" xmlUrl="https://github.blog/tag/npm/feed/" htmlUrl="https://github.blog/tag/npm/" />
      <outline text="PyPI security" title="PyPI security" type="rss" xmlUrl="https://blog.pypi.org/feed_rss_created.xml" htmlUrl="https://blog.pypi.org/" />
      <outline text="NuGet security" title="NuGet security" type="rss" xmlUrl="https://devblogs.microsoft.com/dotnet/category/nuget/feed/" htmlUrl="https://devblogs.microsoft.com/dotnet/category/nuget/" />
      <outline text="Azure Updates" title="Azure Updates" type="rss" xmlUrl="https://www.microsoft.com/releasecommunications/api/v2/azure/rss" htmlUrl="https://azure.microsoft.com/en-us/updates/" />
      <outline text="GitHub Changelog" title="GitHub Changelog" type="rss" xmlUrl="https://github.blog/changelog/feed/" htmlUrl="https://github.blog/changelog/" />
      <outline text="PostgreSQL news" title="PostgreSQL news" type="rss" xmlUrl="https://www.postgresql.org/news.rss" htmlUrl="https://www.postgresql.org/" />
      <outline text="Docker" title="Docker" type="rss" xmlUrl="https://www.docker.com/feed/" htmlUrl="https://www.docker.com/blog/" />
      <outline text="Adyen online payments" title="Adyen online payments" type="rss" xmlUrl="https://docs.adyen.com/online-payments/release-notes.xml" htmlUrl="https://docs.adyen.com/online-payments/release-notes/" />
      <outline text="Box" title="Box" type="rss" xmlUrl="https://developer.box.com/changelog/2026/rss.xml" htmlUrl="https://developer.box.com/changelog/2026" />
      <outline text="Clerk" title="Clerk" type="rss" xmlUrl="https://clerk.com/changelog/atom.xml" htmlUrl="https://clerk.com/changelog" />
      <outline text="Resend" title="Resend" type="rss" xmlUrl="https://resend.com/changelog/rss.xml" htmlUrl="https://resend.com/changelog" />
      <outline text="Twilio" title="Twilio" type="rss" xmlUrl="https://www.twilio.com/en-us/changelog.feed.xml" htmlUrl="https://www.twilio.com/en-us/changelog" />
      <outline text="DocuSign Node SDK supplement" title="DocuSign Node SDK supplement" type="rss" xmlUrl="https://github.com/docusign/docusign-esign-node-client/releases.atom" htmlUrl="https://github.com/docusign/docusign-esign-node-client/releases" />
      <outline text="Zapier developer platform" title="Zapier developer platform" type="rss" xmlUrl="https://docs.zapier.com/integrations/news.xml" htmlUrl="https://docs.zapier.com/integrations/news" />
    </outline>
    <outline text="Voices – Written" title="Voices – Written">
      <outline text="Simon Willison" title="Simon Willison" type="rss" xmlUrl="https://simonwillison.net/atom/everything/" htmlUrl="https://simonwillison.net/" />
      <outline text="Latent Space" title="Latent Space" type="rss" xmlUrl="https://latent.space/feeds/all.xml" htmlUrl="https://latent.space/" />
      <outline text="Jeremy D. Miller" title="Jeremy D. Miller" type="rss" xmlUrl="https://jeremydmiller.com/feed/" htmlUrl="https://jeremydmiller.com/" />
      <outline text="Andrew Lock" title="Andrew Lock" type="rss" xmlUrl="https://andrewlock.net/rss.xml" htmlUrl="https://andrewlock.net/" />
      <outline text="Milan Jovanović" title="Milan Jovanović" type="rss" xmlUrl="https://milanjovanovic.tech/rss/feed.xml" htmlUrl="https://milanjovanovic.tech/blog" />
      <outline text="Node Weekly" title="Node Weekly" type="rss" xmlUrl="https://nodeweekly.com/rss/" htmlUrl="https://nodeweekly.com/" />
      <outline text="Brett Cannon" title="Brett Cannon" type="rss" xmlUrl="https://snarky.ca/rss/" htmlUrl="https://snarky.ca/" />
      <outline text="James Bennett" title="James Bennett" type="rss" xmlUrl="https://www.b-list.org/feeds/entries/" htmlUrl="https://www.b-list.org/weblog/" />
      <outline text="Martin Fowler" title="Martin Fowler" type="rss" xmlUrl="https://martinfowler.com/feed.atom" htmlUrl="https://martinfowler.com/" />
      <outline text="Architecture Notes" title="Architecture Notes" type="rss" xmlUrl="https://architecturenotes.co/feed" htmlUrl="https://architecturenotes.co/" />
      <outline text="The Pragmatic Engineer" title="The Pragmatic Engineer" type="rss" xmlUrl="https://newsletter.pragmaticengineer.com/feed" htmlUrl="https://newsletter.pragmaticengineer.com/" />
      <outline text="Charity Majors" title="Charity Majors" type="rss" xmlUrl="https://charity.wtf/feed" htmlUrl="https://charity.wtf/" />
      <outline text="Julia Evans" title="Julia Evans" type="rss" xmlUrl="https://jvns.ca/atom.xml" htmlUrl="https://jvns.ca/" />
    </outline>
    <outline text="Voices – YouTube" title="Voices – YouTube" />
    <outline text="Vietnamese" title="Vietnamese">
      <outline text="TienNHM" title="TienNHM" type="rss" xmlUrl="https://tiennhm.io.vn/blog/rss.xml" htmlUrl="https://tiennhm.io.vn/" />
      <outline text="ManhPT" title="ManhPT" type="rss" xmlUrl="https://manhpt.com/rss.xml" htmlUrl="https://manhpt.com/" />
      <outline text="TungDaDev" title="TungDaDev" type="rss" xmlUrl="https://tungbt.vercel.app/feed.xml" htmlUrl="https://tungbt.vercel.app/" />
    </outline>
  </body>
</opml>
```

## D. Verified primary-source URLs

One URL per line; shared sources deduplicated. AWS is excluded because its activity/feed checks did not pass. These are source pages, not feed URLs.

https://www.anthropic.com/news
https://code.claude.com/docs/en/changelog
https://platform.claude.com/docs/en/release-notes/overview
https://developers.openai.com/api/docs/changelog
https://learn.chatgpt.com/docs/changelog
https://github.blog/changelog/label/copilot/
https://devblogs.microsoft.com/dotnet/
https://github.com/dotnet/aspnetcore/releases
https://github.com/dotnet/core/releases
https://github.com/JasperFx/marten/releases
https://github.com/JasperFx/wolverine/releases
https://nodejs.org/en/blog/release
https://devblogs.microsoft.com/typescript/
https://github.com/nestjs/nest/releases
https://react.dev/blog
https://blog.python.org/
https://github.com/fastapi/fastapi/releases
https://www.djangoproject.com/weblog/
https://www.sqlalchemy.org/blog/
https://github.com/pydantic/pydantic/releases
https://nextjs.org/blog
https://github.com/advisories
https://github.com/cisagov/kev-data
https://github.blog/tag/npm/
https://blog.pypi.org/
https://devblogs.microsoft.com/dotnet/category/nuget/
https://azure.microsoft.com/en-us/updates/
https://github.blog/changelog/
https://www.postgresql.org/
https://www.docker.com/blog/
https://docs.stripe.com/changelog
https://docs.adyen.com/online-payments/release-notes/
https://developer.box.com/changelog/2026
https://auth0.com/changelog
https://clerk.com/changelog
https://resend.com/changelog
https://www.twilio.com/en-us/changelog
https://community.docusign.com/product-updates
https://github.com/docusign/docusign-esign-node-client/releases
https://docs.zapier.com/integrations/news

## E. Five observations

- **Security coverage requires data, not just blogs.** npm/PyPI/NuGet announcement streams do not cover every vulnerable package; use ecosystem-filtered GitHub advisories and the CISA mirror alongside them. No official per-advisory RSS was established here.
- **Deduplicate overlapping sources.** Copilot is a subset of GitHub Changelog; Python security shares Python Insider; Django security shares its weblog; SendGrid shares Twilio. Marten/Wolverine releases overlap Jeremy Miller’s explanation posts. Ingest broadly, publish one item per underlying change.
- **Feed existence does not imply useful coverage.** OpenAI’s general developer RSS is stale, Box’s feed is year-scoped, and AWS returned HTML at its advertised endpoint. Recheck feed validity, entry dates, redirects and scope at each run; revisit Box at year rollover.
- **YouTube and X remain delivery gaps.** Recent YouTube activity can be verified from video pages, but its feeds failed; X blocked direct verification. Do not convert these watchlists into automated inputs without a passing fetch. Python/TS YouTube coverage is deliberately sparse rather than filled with weaker channels.
- **Vietnamese senior content is thinner and less consistently verifiable.** Three small practitioner blogs passed basic source checks, with article-access limits on two. No Vietnamese leadership/mentoring publication was established with enough recent, senior-level evidence; no additional TS written voice was forced into the shortlist after 2ality went offline and Total TypeScript’s RSS proved stale.

## Verification trail

First-party pages/feed responses were opened during this run. A 200 HTML response was not accepted as a feed. Feed bodies were parsed as XML, with RSS/Atom roots and entries checked. Latest dates were compared with the 90-day window, using published dates over edits when available. Unavailable sources are retained as unverified/excluded, never silently replaced by third-party mirrors. The CISA fallback is its own official repository, explicitly labeled.

First-party explanatory references: GitHub Changelog (outbound @ghchangelog link); CISA official kev-data README (mirror/update schedule); Zapier Platform News (RSS subscription link); Adyen online-payment release notes (RSS link); 2ality’s current offline notice. All corresponding working URLs appear above. This audit validates source identity/access/activity/feed structure, not every factual claim published by a source, full RSS standards conformance, or an exhaustive absence of undiscovered feeds.
