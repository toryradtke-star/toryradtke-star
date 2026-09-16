## Tory Radtke

I build production web applications and the AI automation around them.

Most of my work sits where marketing meets engineering: I ship Next.js sites for
clients, then build the agentic pipelines that keep content, campaigns, and
reporting running against them. I came up through marketing and analytics, so I
tend to judge a system by what it moved — traffic, leads, conversions — rather
than by whether it shipped.

**Currently:** AI Marketing Strategist & Automation Builder at Lakes Area
Graphix and Signworx, working across Banners.com, Decals.com, and Stickers.com.

### What's here

**[seo-agent-system](https://github.com/toryradtke-star/seo-agent-system)** — Multi-agent pipeline that takes a product catalog from URL to optimized page content.
Crawl → route → SERP intent → generate → score → retry, as queue-backed jobs that
survive a restart. A ~600-page catalog completes a full pass in about 20 minutes.
The interesting parts aren't the prompting: scraped pages are untrusted input
that reach a model, so there's an injection-sanitizing boundary with tests behind
it; a crawler that accepts URLs is an SSRF hole, so hostnames resolve and
private ranges are refused; and "the model returned something" isn't success, so
output is scored against explicit rules and regenerated when it fails — bounded,
so a page that can't pass fails loudly instead of burning tokens.

**[workout247-site](https://github.com/toryradtke-star/workout247-site)** — Multi-location gym site, WordPress → Next.js 16 + Sanity.
One dynamic route serves every location from its CMS document. A Sanity webhook
purges only the cache tags that actually changed, so a price edit is live in
seconds without a rebuild. The contact form pairs a honeypot with a Redis-backed
sliding-window limiter that fails *open* — silently dropping real enquiries is a
worse failure than no rate limiting at all.

**[omnia-pt-web](https://github.com/toryradtke-star/omnia-pt-web)** — Physical therapy clinic site where the lead pipeline is the product.
Ad click → form → normalized upsert into the CRM → opportunity opened at the
right pipeline stage. Pipelines resolve by name rather than by id so renaming a
stage fails loudly instead of misfiling leads, and the conversion fire is guarded
against double-reporting, because an inflated count corrupts the bid signal the
Ads account optimizes against.

**[omnia-pt](https://github.com/toryradtke-star/omnia-pt)** — The Sanity Studio behind it, deployed separately so editors get a
stable editing surface independent of site releases.

### Stack

**Web** — Next.js · React · TypeScript · Tailwind · Sanity · Vercel · Node · Python

**AI & automation** — Claude Code · Codex · MCP servers · BullMQ · REST APIs · ffmpeg

**Analytics** — GA4 · Google Search Console · Semrush · Google Ads

📍 Minneapolis, MN · Open to remote roles · toryradtke@gmail.com
