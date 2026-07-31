# The Revenue & GTM Systems Landscape
**Built:** 2026-07-10
**What this is:** the breadth layer. Every category of tool a revenue and go-to-market operation can have, so no whole category ever blindsides me again (the way metering did). Each entry: what it is, when you actually need one (the trigger / what breaks without it), and the real players to go deep on later.
**How to read the trigger:** the definition is trivia; the trigger is the operator judgment. "You need X the moment Y breaks" is the part that matters.
**Status of the player lists:** starting points, not gospel. Depth entries (the Agentforce-level ground truth) get built underneath each category over time.

---

## A. Get found & capture demand (top of funnel)

**Marketing automation / email**: nurtures leads, runs campaigns, hosts forms and landing pages.
*Need it when:* you're sending marketing email to a list and want to track who engages and hand hot ones to sales.
*Players:* HubSpot, Marketo, Pardot (Salesforce Account Engagement), Customer.io

**Data enrichment**: fills in the missing details on a company or person (size, industry, role, email).
*Need it when:* your inbound forms come in half-empty, or you're building outbound target lists from scratch.
*Players:* Clay, ZoomInfo, Apollo, Clearbit (now HubSpot Breeze)

**Intent & buying signals**: flags which accounts are showing buying behavior before they raise a hand.
*Need it when:* you want to prioritize accounts that are warming up instead of waiting for a form fill.
*Players:* 6sense, Demandbase, Common Room, Koala

**Website visitor de-anonymization**: turns anonymous website traffic into named companies (and sometimes people).
*Need it when:* you have real traffic but few form fills and want to know who's lurking.
*Players:* Leadfeeder/Dealfront, RB2B, Vector

**Ads & attribution**: runs paid campaigns and ties the spend back to pipeline and revenue.
*Need it when:* you spend real money on ads and can't say what it actually produced.
*Players:* Google Ads, Meta, HockeyStack, Dreamdata

## B. Route, sell & engage

**CRM (customer relationship management)**: the system of record for accounts, contacts, and deals. The spine everything else plugs into.
*Need it when:* almost always, the day you have more than a handful of deals to track.
*Players:* Salesforce, HubSpot

**Lead-to-account matching & routing**: matches an inbound lead to the right existing account and assigns the right owner.
*Need it when:* inbound volume is high enough that manual assignment drops balls or plays favorites.
*Players:* LeanData, Default, Traction Complete, Chili Piper

**Meeting scheduling**: qualifies and books inbound instantly, right on the form.
*Need it when:* speed-to-lead matters and reps are too slow to reach out first.
*Players:* Chili Piper, LeanData BookIt, Calendly

**Sales engagement**: runs the sequences of emails, calls, and tasks reps use for outbound and follow-up.
*Need it when:* reps are running cadences by hand and follow-up is inconsistent.
*Players:* Outreach, Salesloft, Apollo

**Partner management (PRM)**: tracks partner, reseller, and referral deals and overlaps with your accounts.
*Need it when:* a real share of revenue comes through partners, not just your own reps.
*Players:* Crossbeam, PartnerStack, Reveal

## C. Quote, contract & close

**CPQ (configure, price, quote)**: builds an accurate quote with the right products, pricing, discounts, and approvals.
*Need it when:* pricing is complex enough that reps make errors in spreadsheets, or you need approval control on discounts.
*Players:* Salesforce CPQ, Nue, DealHub, Subskribe

**Contract lifecycle management (CLM)**: drafts, redlines, stores, and tracks contracts and their terms.
*Need it when:* legal review is a bottleneck, or signed terms are scattered across folders and inboxes.
*Players:* Ironclad, SpotDraft, DocuSign CLM, Sirion

**E-signature**: gets the contract legally signed.
*Need it when:* you send anything that needs a signature (which is everything).
*Players:* DocuSign, Dropbox Sign, Adobe Acrobat Sign

## D. Bill, meter & collect

**Metering / usage aggregation**: counts consumption for usage-based pricing (credits, API calls, seats actually used).
*Need it when:* you charge by usage and your billing tool can't count it accurately or in real time. (This is the one that blindsided you.)
*Players:* Metronome, Orb, Amberflo, m3ter (Salesforce)

**Billing / subscription management**: turns contracts and usage into invoices and manages renewals, upgrades, and downgrades.
*Need it when:* you have recurring revenue and manual invoicing is starting to break.
*Players:* Nue, Stripe Billing, Zuora, Maxio, Chargebee

**Payments**: actually moves the money.
*Need it when:* you collect card or bank payments online.
*Players:* Stripe, Adyen, GoCardless

**Sales tax / VAT**: calculates and files the right tax by state and country.
*Need it when:* you sell across jurisdictions and owe tax you aren't tracking.
*Players:* Avalara, Anrok, Stripe Tax

**Dunning & collections**: chases failed payments and overdue invoices.
*Need it when:* revenue leaks from failed cards or slow-paying customers.
*Players:* built into most billing tools, plus Churnkey, Upflow

**Entitlements & provisioning**: flips product access on and off to match what was actually bought.
*Need it when:* what a customer paid for needs to line up with what they can use in the product.
*Players:* often custom-built, plus Stigg, Schematic

## E. Recognize revenue & run finance

**Revenue recognition**: calculates when revenue counts as earned under the accounting rules (ASC 606), separate from when you bill or collect.
*Need it when:* you have contracts spanning time and auditors or investors need clean recognized-revenue numbers.
*Players:* Leapfin, Light, Maxio, NetSuite ARM

**ERP / accounting**: the books: general ledger, the monthly close, financial controls.
*Need it when:* you've outgrown basic bookkeeping and need real controls and an audit trail.
*Players:* NetSuite, Sage Intacct, Campfire, QuickBooks (smaller companies)

**Financial planning (FP&A)**: budgets, forecasts, headcount plans, and models.
*Need it when:* the forecast has outgrown a spreadsheet and too many people touch it.
*Players:* Pigment, Cube, Mosaic, Anaplan

## F. Store, move & understand the data

**Data warehouse**: the central store where data from every tool lands so it can be analyzed together.
*Need it when:* your data lives in silos and no single tool can answer a cross-system question.
*Players:* Snowflake, BigQuery, Databricks

**ETL / data pipelines**: moves data out of your tools and into the warehouse (and transforms it).
*Need it when:* you're exporting spreadsheets by hand to get data into one place.
*Players:* Fivetran, Airbyte, dbt (for the transform step)

**Reverse ETL**: pushes warehouse data back into the tools reps actually work in.
*Need it when:* your best data (health scores, usage) is trapped in the warehouse and reps need it in the CRM.
*Players:* Census, Hightouch

**BI / reporting**: dashboards and analysis on top of the data.
*Need it when:* leadership needs one shared, trusted source for the numbers.
*Players:* Looker, Tableau, Omni, Sigma

**Revenue intelligence / forecasting**: analyzes pipeline health and predicts the number.
*Need it when:* forecasting is gut-feel and pipeline hygiene is poor.
*Players:* Clari, BoostUp, Gong Forecast

**Conversation intelligence**: records, transcribes, and analyzes sales calls for coaching and deal signals.
*Need it when:* you want to learn from what's actually said on calls, not just what reps log.
*Players:* Gong, Chorus, Glyphic

**Data governance & observability**: watches data quality, ownership, and access; catches when the numbers silently break.
*Need it when:* people don't trust the numbers, or you have compliance and access requirements.
*Players:* Monte Carlo, Atlan, Metaplane

## G. The AI & automation layer (newest, fastest-moving)

**AI agents**: software that takes multi-step actions on its own (drafts, qualifies, updates records, answers questions).
*Need it when:* you have repetitive judgment work to hand off and clean enough data to trust it. (Agentforce is the first depth entry to build here.)
*Players:* Salesforce Agentforce, Sierra, Clay agents, 11x, Regie

**Workflow automation / orchestration**: connects tools and runs multi-step processes without custom code.
*Need it when:* work falls through the cracks between tools and people are copy-pasting between them.
*Players:* Zapier, Workato, n8n, Tray.ai

## H. Partner & marketplace channels

**Partner management (PRM)**: tracks partner, reseller, and referral deals and where partner accounts overlap with yours. (Also listed under Route/sell.)
*Need it when:* a real share of revenue runs through partners, not just your own reps.
*Players:* Crossbeam, PartnerStack, Reveal

**Cloud marketplaces & co-sell**: sells your product through the big cloud marketplaces (AWS, Azure, Google) and manages co-selling with them.
*Need it when:* enterprise buyers want to purchase through their existing cloud budget, or you co-sell with a hyperscaler.
*Players:* Tackle.io, Suger, AWS/Azure/GCP Marketplace

## I. Finance operations & back office

**Spend management & corporate cards**: issues cards, tracks and controls company spending, automates expense reports.
*Need it when:* employee spending and card reconciliation is manual and leaky.
*Players:* Ramp, Brex, Airbase

**Procurement & vendor management**: controls how new tools and vendors get requested, approved, and bought.
*Need it when:* software spend is sprawling and purchases happen with no approval trail.
*Players:* Zip, Vendr, Tropic

**AP / AR automation** (accounts payable and receivable, the money you owe out and the money owed to you): automates paying bills and collecting from customers.
*Need it when:* paying vendors and chasing customer payments is a manual slog.
*Players:* Bill.com, Tipalti, Ramp

**Treasury & business banking**: holds the cash, moves money, manages runway and yield.
*Need it when:* you've outgrown a basic business checking account and need real cash controls.
*Players:* Mercury, Brex, JPMorgan

**Close & reconciliation**: speeds up the monthly financial close and matches transactions so the books are right.
*Need it when:* the close drags and finance is buried in spreadsheets.
*Players:* Numeric, FloQast, BlackLine

**Cap table & equity**: tracks who owns what (shares, options, vesting) and handles equity grants.
*Need it when:* you have investors and employee equity to manage cleanly.
*Players:* Carta, Pulley

**SaaS management**: tracks every software tool the company actually owns, what it costs, and who uses it.
*Need it when:* nobody can say how many tools you pay for or which ones are dead weight.
*Players:* Zylo, Sastrify, Vendr

## J. People, legal & security

**HR / HRIS & payroll**: manages employees, payroll, benefits, and onboarding.
*Need it when:* you have more than a handful of employees to pay and onboard.
*Players:* Rippling, Gusto, Deel, Workday

**Legal, risk & compliance (GRC)**: manages policies, audits, and security certifications like SOC 2.
*Need it when:* customers demand security certifications or you face real regulatory requirements.
*Players:* Vanta, Drata, Secureframe

**Identity & access management**: controls who can log into what and switches accounts on and off as people join and leave.
*Need it when:* you have enough people and apps that manual account setup and offboarding becomes a security risk.
*Players:* Okta, Rippling, JumpCloud

---

## Notes for reading the map
- **Categories blur.** Some tools cover several boxes: Nue does CPQ and billing; HubSpot does CRM, marketing, and more. The map is the clean version; real stacks overlap.
- **Not every company needs every box.** The trigger tells you when a box turns on. A flat-rate seat business may never need metering; a usage business needs it on day one.
- **The seams between boxes are where a systems architect earns their keep.** The handoffs (contract terms into billing, usage into rev rec, warehouse scores back into the CRM) are where data breaks. Worth its own layer later.

## What's next
- **Depth entries** go under each category, starting with the AI ones: Agentforce first (what it really does vs the keynote, cost, where it breaks).
- **Verify & personalize the player lists** against your own network and honest third-party reads, not vendor sites.
- **Query layer:** once depth fills in, ask Claude/Codex across the whole map ("for a company with usage-based pricing and an enterprise sales motion, which boxes are non-negotiable and which can wait").
