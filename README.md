# Vintage Market Research (Internal)

Internal, read-only market-research project maintained by a small team.
We study the **public** vintage / secondhand apparel market on Etsy to produce
aggregate statistics for an investment research report.

## What this project does

We query the **official Etsy Open API v3** for public, active listing metadata —
titles, prices, taxonomy categories, tags, and shop-level fields — and aggregate
them into descriptive statistics such as:

- price-band distribution of vintage apparel listings
- category and tag frequency (e.g. 90s / Y2K, nylon jacket, sweatshirt)
- shop concentration within the vintage segment

The output is a static spreadsheet and summary report used internally. No
interactive product is offered to end users.

## How Etsy data is accessed

- Exclusively through the **official Etsy Open API v3** (`openapi.etsy.com/v3`)
  with a registered application key.
- **Read-only**: only public listing and shop metadata endpoints are called.
- Requests stay **within Etsy's published rate limits** (QPD / QPS); the job runs
  in small daily batches and caches results locally.
- We do **not** scrape Etsy web pages, and we do not automate any action on
  behalf of buyers or sellers.

## Data handling

| | |
|---|---|
| Collected | Public listing metadata (id, title, price, category, tags, shop id/name) |
| Not collected | Any buyer or seller personal data; no messages, no orders, no addresses |
| Retention | Aggregated statistics only; raw responses kept briefly for verification |
| Redistribution | None — Etsy content is never republished, resold or shared |

## Scope and status

- Non-commercial: the project is not sold and does not charge for access.
- Used only by the project owner and colleagues.
- No shop management, no purchases, no listing creation.

## Notes

This repository exists to document the research scope and to host the
data-collection scripts and the resulting aggregate tables. It does not contain
any Etsy user data.

*Maintainer: dulindulin-svg*
