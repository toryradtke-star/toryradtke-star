## Tory Radtke

I build production web applications and the AI automation around them.

Most of my work sits where marketing meets engineering: I ship Next.js sites for
clients, then build the agentic pipelines that keep content, campaigns, and
reporting running against them. I come from a marketing and analytics
background, so I tend to judge a system by what it moved — traffic, leads,
conversions — rather than by whether it shipped.

**Currently:** AI Marketing Strategist & Automation Builder at Lakes Area
Graphix and Signworx, working across Banners.com, Decals.com, and Stickers.com.

### What's here

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

**[omnia-pt](https://github.com/toryradtke-star/omnia-pt)** — The Sanity Studio behind it, deployed separately so editors
get a stable editing surface independent of site releases.

### Work I can't put in a repo

At LAG I built a content audit pipeline that reaches the Semrush and Google
Search Console APIs through MCP servers in Claude Code — it processes a
~600-page site and emits per-page findings plus an optimized rewrite in about
20 minutes. Also an end-to-end AI video pipeline (Google Flow/Veo → ffmpeg)
for batch-producing ad creative in vertical and horizontal cuts.

### Stack

Next.js · React · TypeScript · Tailwind · Sanity · Vercel · Node · Python
Claude Code · Codex · MCP servers · REST APIs · ffmpeg
GA4 · Google Search Console · Semrush · Google Ads

📍 Minneapolis, MN · Open to remote roles · toryradtke@gmail.com
