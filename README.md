# Somesh Samanta

I build the systems behind B2B demand generation — lead capture and routing, attribution, list
hygiene, campaign infrastructure, and the reporting that says which of it actually worked — and then
I run them.

Six of those systems are rebuilt here as **working demos**. Not screenshots and not mockups: each
one runs in the browser, has a real test suite, and sits on a deterministic engine, so identical
input always produces identical output. Every dataset in them is synthetic. They are clean-room
reconstructions of systems I built and operated in production — none of them contain any employer's
code, data or customers.

**One-page index of all six: [somesh-systems.vercel.app](https://somesh-systems.vercel.app)**

## The demos

| System | What it does | |
|---|---|---|
| **LeadFlow** | Multi-channel capture → canonical-source attribution → identity resolution → routing. Solves "same person, three forms, two email addresses" without fuzzy-matching strangers into one record. | [Live](https://leadflow-demo-someshs-projects-04586766.vercel.app) · [Code](https://github.com/callmesomesh/leadflow) |
| **Funnel Doctor** | Finds the internal traffic polluting your product analytics, and the tracking that silently stopped firing. Reports evidence for each finding, not a verdict you have to trust. | [Live](https://funnel-doctor-demo.vercel.app) · [Code](https://github.com/callmesomesh/funnel-doctor) |
| **Daily Pulse** | One daily marketing report a founder will actually read: funnel-leak detection, SLA watch, and a flat refusal to compute a day-over-day change against a stale snapshot. | [Live](https://daily-pulse-demo.vercel.app) · [Code](https://github.com/callmesomesh/daily-pulse) |
| **ListForge** | Segment before you load. Live DNS MX lookups and catch-all detection, so the clean cohort sends first instead of the whole list burning a sending domain. | [Live](https://listforge-demo.vercel.app) · [Code](https://github.com/callmesomesh/listforge) |
| **SafeSend WA** | A broadcast engine you can stop. Opt-in enforced, opt-outs permanently suppressed, cross-run dedup, hard daily cap, rate limit, dry-run by default — and a kill switch that leaves resumable state. | [Live](https://safesend-wa-demo.vercel.app) · [Code](https://github.com/callmesomesh/safesend-wa) |
| **HeroMatch** | One landing URL whose hero rewrites to match the paid click that brought the visitor — while organic traffic and search engines always see the one canonical page. Click IDs beat UTMs; unknown signals fall back loudly. | [Live](https://heromatch-demo.vercel.app) · [Code](https://github.com/callmesomesh/heromatch) |

## Why these six

Each one exists because the underlying problem cost me something first.

- **Attribution** is decided by a click ID that most setups throw away in favour of whatever UTM
  happened to be last. LeadFlow resolves source in a fixed precedence and shows its reasoning for
  every lead.
- **Funnel Doctor** exists because I once audited a funnel that looked like it was growing and
  found a large share of the events were our own engineering team's localhost traffic — and that a
  revenue-related event had stopped firing weeks earlier. A step everyone believed was measured was
  unmeasured, not zero.
- **Daily Pulse** refuses to compare against a stale snapshot rather than quietly returning a
  number. A confidently wrong metric does more damage than a missing one.
- **ListForge** exists because catch-all domains accept mail for any address, so per-mailbox
  verification tools mark every guess as valid. On one list, 41 of 147 contacts were catch-all —
  held back rather than sent to.
- **SafeSend WA** exists because the production version ran on a company's *real inbound* WhatsApp
  number. A bug there would not have cost a campaign, it would have cost the channel — so the
  refusals, not the sending, are the product.
- **HeroMatch** exists because a paid click is a promise, and a generic homepage under every
  campaign breaks it. The production original rewrote the hero for paid arrivals while search
  engines always saw one canonical page.

## What I do

Four years in B2B marketing. I started as an SDR — 130+ demos booked cold, hundreds of rejections —
then moved into building everything around the sale: positioning and messaging, outbound, paid,
events, the CRM and the automation underneath. Currently running GTM at a spatial-intelligence
platform. Before that I built a construction-SaaS demand-generation motion largely solo; it kept
running after I left, which is the test I hold this work to.

Published in [NBM&CW](https://www.nbmcw.com/product-technology/technologies-digitilization-software/digital-technologies-bridging-the-gap-between-plan-and-execution.html)
(June 2026), carried alongside the Managing Directors of JCB India, Sany India, Terex India and
CASE Construction.

**Stack I actually ship in:** TypeScript, Next.js, Node, Vitest, Vercel · HubSpot, Apollo,
Smartlead, n8n · GA4, Google Search Console, Mixpanel

---

Gurugram, Delhi NCR — open to relocating · [someshsamanta6@gmail.com](mailto:someshsamanta6@gmail.com) · [LinkedIn](https://www.linkedin.com/in/somesh-samanta-visitmyprofile)
