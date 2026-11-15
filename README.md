# SEO Skills for Claude Code: Showcase

I build SEO workflow skills for [Claude Code](https://claude.com/claude-code) that turn agency processes into repeatable, AI-run workflows. The skills themselves live in a private repo; this page shows what they do and the kind of output they produce. All examples are anonymised.

**Want access or a demo?** Open an issue on this repo or message me on GitHub.

---

## Skill 1: Keyword Research & Mapping (e-commerce)

Runs collection- and product-level keyword research for an online store, maps every keyword to exactly one page, and delivers a ready-to-implement workbook.

### What it does

1. **Page inventory:** reads the collection and every product inside it (title tag, H1, canonical, status).
2. **Google Search Console:** pulls real queries per collection and per product, then buckets them: striking distance (position 8–20), high impressions / low CTR, relevant-but-untargeted, branded, irrelevant.
3. **Cannibalization check:** finds queries where 2+ URLs compete (collection vs products vs landing pages) and picks one owner.
4. **SEMrush:** exact volume, KD, intent and question keywords for the target country.
5. **Manual SERP check:** keeps a keyword for a collection only if collection pages actually rank for it. Recipe/blog SERPs become content gaps instead.
6. **Mapping:** 8–10 keywords per collection, 5–7 per product, one owner URL per keyword.
7. **Placement briefs:** title tag, H1, meta description, H2s, FAQs, image alt, internal links.
8. **Tracking:** baseline now, re-check at 30 and 60 days.

### Built to be efficient

- **Parallel agents:** for large sites it splits GSC analysis, cannibalization scanning, SERP checks and competitor gaps across agents that run at the same time, with one coordinator as the only writer of the keyword list (so two agents can never assign the same keyword to two pages).
- **Token-light:** filters out branded and irrelevant queries before any paid lookup, passes file paths instead of data between agents, and writes the workbook once.

### Sample output (anonymised)

*Client: a food brand in West Africa. One collection of a seasoning-mix product and its 4 products.*

**Key findings**

| Finding | Impact | Fix |
|---|---|---|
| Brand query ranks on 4 URLs (collection, 2 product variants, an old landing page) | Pages split clicks and rankings | Pack-specific product titles, 301 the landing page, link products to the collection |
| A bundle product outranks its own collection for the main product name | Collection loses its primary keyword | Retitle the bundle around "5-pack" instead of the product name |
| Old collection URL returns 404 but still gets impressions | Lost traffic | 301 to the live collection |
| Generic product term (2.4K/mo) shows only recipe blogs on page 1 | A collection page cannot rank for it | Content gap: a recipe blog post that links to the collection |

**Collection mapping (excerpt)**

| Placement | Keyword type | Example |
|---|---|---|
| Title tag / H1 | Primary (brand product name + "buy online") | Buy [Product] Online in [Country] |
| H2s | Secondary (category + attribute) | [Flavour] rice mix, rice seasoning, spice mix |
| FAQs | Questions with real volume | "What spices do I need for [dish]?" (110/mo) |

**Product mapping (excerpt)**

| Product | Primary | Secondary |
|---|---|---|
| Single pack | [brand] [product] 1 pack | [product] price, single sachet price |
| 10-pack | [brand] [product] 10 packs | bulk price, wholesale |
| Bundle | [brand] best seller bundle | [product] bundle, 5 pack |

**Workbook tabs delivered:** Page Inventory · GSC Raw Data · Keyword Research · Master Keyword List · Collection Mapping · Product Mapping · Cannibalization · Content Gaps · Tracking

---

## Coming next

More SEO skills are in progress: technical audits, content briefs and on-page optimisation. They'll be added here as they ship.
