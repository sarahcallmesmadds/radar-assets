# Metering / usage-based billing (Metronome vs Orb)
**Category:** Metering / usage aggregation
**Built:** 2026-07-10 (fast-moving: the whole category was bought out in H1 2026, verify ownership and pricing before quoting)
**Verdict:** The hardest, most underestimated box in the revenue stack, and as of 2026 every pure-play specialist got acquired, so your metering choice is now tangled up with who owns your payments.

## Say it cold (the two-sentence version)
Metering is the tool that counts what a customer used so you can bill them for it, and it is a genuinely hard engineering problem, because if it miscounts you either leak revenue or lose the customer's trust. The 2026 story is that the three leaders all got bought (Stripe took Metronome, Adyen took Orb, Salesforce took m3ter), so the real question now isn't just which tool is best, it's whether you want your usage data sitting inside your payment processor's competitor.

## What it actually is
Software that captures usage events (an API call, a credit spent, a gigabyte processed), adds them up accurately in near real time, and turns them into something you can bill. The plain-English hard parts:
- **Accurate capture.** Every event has to be counted once and only once. Miss events and you under-bill; double-count and you over-bill and erode trust.
- **Aggregation at scale.** Adding up millions or billions of events without dropping any, fast enough that a customer can't blow past their limit before anyone notices.
- **Reconciliation.** A clean audit trail so finance can prove the invoice is right. This is the part that makes it a real system, not a counter.

## The two names to know
**Metronome** (now owned by Stripe): the enterprise, infrastructure-grade choice. Built for very high event volume (pre-summarized ingestion at scale), plugs straight into infrastructure monitoring tools (CloudWatch, Datadog) so technical usage becomes billable without extra code, and handles complex enterprise contracts (commitments, credits, drawdowns). The catch: it leans on engineering. Most companies build custom data pipelines before going live.

**Orb** (now owned by Adyen): the developer-friendly, faster-to-launch choice. You define what you're metering in plain database queries, get real-time usage dashboards, and it has one feature Metronome doesn't document: pricing simulation, meaning you can test a pricing change against your real historical usage before you roll it out. Lighter engineering lift, guided setup.

**The honest one-liner:** Orb if you want speed and a good developer experience, Metronome if you're selling infrastructure with heavy enterprise contracts and huge event volume.

## What it really costs
Neither publishes pricing, which tells you it's enterprise sales-led and negotiable. Before Orb pulled its public page, third-party analysis pegged a platform fee around $720 per month as a floor, plus usage-based components on top. Metronome is fully opaque. Assume a meaningful platform fee plus a cut or per-event charge, and expect the real cost to include the engineering time to build and maintain the pipelines, which is often the bigger number.

## Where it breaks (the honest part)
- **It's an engineering project, not a purchase.** The concept is simple; the execution (idempotency so you don't double-count, deduplication, backfilling missed data, time-based aggregation across systems) is where teams sink months.
- **Metering lag causes bill disputes.** If the count runs behind, customers exceed limits without warning and then argue the invoice. Real-time is a requirement, not a nice-to-have.
- **Tax on variable amounts and "bill shock"** are recurring pain. When the bill changes every month, customers panic and finance scrambles, so you need alerts and caps built in.
- **Metering is not entitlements.** These tools count usage; they don't necessarily control access to features. Assuming metering also gates the product is a common and costly mistake (see the entitlements box on the map).

## The 2026 consolidation (the sharp, current fact)
In under six months, every major independent metering specialist was acquired:
- **Metronome to Stripe**, reported around $1 billion (Jan 2026). Stripe reportedly paid up rather than fix its own billing product.
- **Orb to Adyen**, about $335 million, closing around July 1, 2026.
- **m3ter to Salesforce**, price undisclosed, estimated around $150 million on under $10 million of revenue.

**Why this matters for a systems architect:** your metering tool now comes attached to a payments giant. If you run Stripe for payments, Metronome is natural; if you run a competitor (Adyen, GoCardless), putting your usage data inside Stripe-owned Metronome is a real consolidation risk, and the same logic runs in reverse for Orb under Adyen. The truly independent options left are smaller: Lago (open-source), Zenskar, Togai, Solvimon, Flexprice.

## How to think about it vs alternatives
- **Match it to your payments stack first.** Post-acquisition, that alignment is now a primary factor, not an afterthought.
- **Volume and contract complexity next.** Massive event volume and enterprise commitments point to Metronome; speed and pricing agility point to Orb.
- **Want independence?** The open-source and smaller players (Lago especially) exist precisely so your usage data isn't inside a payments competitor, at the cost of more self-management.

## Data & trust angle
Your metering tool holds a precise record of exactly how every customer uses your product, which is commercially sensitive. Post-acquisition, that data now lives with a payments company that may also serve your competitors. For any business handling sensitive client activity, where that usage data sits and who can see it is a real diligence question, not a technicality.

## Bottom line
Metering is the box people underestimate and the one most likely to quietly leak revenue or trigger customer fights. When someone says "let's just meter usage," the sharp questions are: how clean and real-time is our event capture, does our metering choice fit our payments processor now that the field consolidated, and have we separated counting usage from controlling access. The seam worth probing at any usage-priced vendor: whether they are stretching an infrastructure-grade meter like Metronome to drive customer-facing dashboards, which is not what it was built for.

## Sources
- Usage-based billing after the buyouts (UsageBox): https://usagebox.com/articles/independent-usage-based-billing-after-acquisitions-2026
- MGI Research, monetization deal deep dives (m3ter estimate): https://mgiresearch.com/the-margin/special-edition-monetization-deal-deep-dives/
- Stripe blog, Metronome acquisition: https://stripe.com/blog/metronome-stripe-building-the-future-of-billing
- Payments Dive, Stripe to buy Metronome: https://www.paymentsdive.com/news/stripe-to-buy-metronome/807055/
- Lago, why Stripe paid $1B for Metronome: https://getlago.com/blog/why-stripe-paid-1b-for-metronome-instead-of-fixing-billing
- Orb vs Metronome comparison (aibilling): https://www.aibilling.dev/compare/orb-vs-metronome
- Lago vs Orb vs Metronome (PkgPulse): https://www.pkgpulse.com/guides/lago-vs-orb-vs-metronome-usage-based-billing-apis-2026
- Why usage-based billing is an engineering problem (Flexprice): https://flexprice.io/blog/why-usage-based-billing-is-an-engineering-problem
- Metronome alternatives and the entitlements gap (Stigg): https://www.stigg.io/blog-posts/metronome-alternatives
- Best billing alternatives 2026 (Solvimon): https://www.solvimon.com/blog/best-billing-systems-in-2026
