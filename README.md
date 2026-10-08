**Live Actor and maintained API: [Run German Delivery Menu Price Intelligence on Apify](https://apify.com/kamerozkan/german-delivery-menu-price-intelligence)**

# Lieferando Menu Scraper - Restaurant Menus, Prices & Delivery: Samples

Scrape restaurant menus and dish prices from Lieferando.de, Germany's largest food delivery platform: menu, price, delivery fee and minimum order per German postcode, 90-day price history, postcode price matrix and a run-over-run menu change digest. Unofficial, independent tool.

[Run Lieferando Menu Scraper - Restaurant Menus, Prices & Delivery on Apify](https://apify.com/kamerozkan/german-delivery-menu-price-intelligence)

![Actor](https://img.shields.io/badge/Apify_Actor-public-00a67e)
![Latest build](https://img.shields.io/badge/latest_build-1.0.23-2563eb)
![Sample evidence](https://img.shields.io/badge/owner_sample-one_menu_healthy-00a67e)
![Schema](https://img.shields.io/badge/JSON_Schema-draft--07-f59e0b)

Turn postcode-routed Lieferando restaurant listings into normalized menu rows, delivery economics, comparable product IDs, cross-postcode price matrices, 90-day history, and run-quality records.

> **Independent and unofficial.** This project is not affiliated with, endorsed by, sponsored by, or an official integration of Lieferando or Just Eat Takeaway.com. Platform names identify the public data source only.


## Current billing checked on October 8, 2026

The October 8 release retained the active pricing previously recorded on October 6, 2026. These are Free-tier event rates; use the [Pricing tab](https://apify.com/kamerozkan/german-delivery-menu-price-intelligence/pricing) for your plan and memory allocation. Historical samples below keep their original dates and do not prove current source availability.

Delivered menu items, restaurant fallback rows and menu-change summary rows cost $0.003 each. Postcode matrices, inflation summaries and the run summary have no result event. The active pricing has no `menu-change-digest` event; a successfully stored digest is marked `UNPRICED_FREE`. Startup is $0.005 per GB, minimum one event; default 2 GB adds $0.01. For 400 billable rows, event charges are $1.21 per run. A later failure or abort can retain earlier delivered and charged rows. The current Pricing tab shows platform costs included; the publisher still incurs compute and proxy costs. Row limits and charge limits do not prove complete menus or cap the publisher costs.

See [`pricing-verification-2026-10-06.json`](pricing-verification-2026-10-06.json) for the saved event configuration and scope.

## October 8, 2026: completed one-menu owner check

Public `latest` is `1.0.23`, build `hfAW1S9wOWopLSWT7`. The only runtime change skips the unused DOM image lookup when a structured JSON-LD image is already available. The fallback still runs when needed. All 34 frozen source hashes were verified; 32 source files are identical to 1.0.22. Prices, schemas, memory, proxy, retries and required-content checks are unchanged.

One dated direct-menu owner run completed with **308 menu records**, `SUCCEEDED` platform status and `healthy` application quality. It contains 299 available items with finite nonnegative EUR prices and nine explicitly unavailable items with null prices. Source failures, retries and available-item missing-price rate were zero. The run did not hit its charge limit. This is one observed menu, not an independently exhaustive source-coverage or uptime guarantee.

The exact input is [`13_2026-10-08_completed_menu_input.json`](13_2026-10-08_completed_menu_input.json). Use `postalCodes: []` for direct-only collection. The dated run options were 2 GB, 180 seconds and `maxTotalChargeUsd: 1.00`; the charge limit is a run option, not an input field or publisher resource-cost cap. A smaller budget may intentionally stop before the menu finishes. Requested history and analytics should remain enabled when those features are needed; this sample requests neither.

See [`14_2026-10-08_completed_menu_sample.json`](14_2026-10-08_completed_menu_sample.json) for three field-preserving projections, including an unavailable item, and [`15_2026-10-08_completed_menu_summary.json`](15_2026-10-08_completed_menu_summary.json) for the exact summary. The owner resource cost was USD 0.0558920. All accounted owner events were zero; this is not customer revenue or a customer profit result.

Local checks covered nine branches with 18 actual compiled baseline/candidate executions and 60 independent selection cases. Synthetic dataset, summary and identity parity passed. In the two live snapshots, 106 prior source identities and their non-image business fields match; one previous promotional row was absent and four shared image URLs changed. Their live source/session cause was not established. Menu extraction occurs before the modified fallback. Do not describe the live snapshots as identical, or attribute their different row counts, runtime or costs solely to this change. Full evidence and limitations are in [`chain-image-verification-2026-10-08.json`](chain-image-verification-2026-10-08.json).

## Earlier October 8, 2026 capped owner output

At that earlier publication, public `latest` was `1.0.22`, build `TCUjgwTwpOlwz4T7J`. All 34 frozen source hashes and protected settings were verified. Event prices, retry defaults, proxy settings, input constraints and memory defaults were preserved. Initial navigation now waits for `domcontentloaded`, followed by the required visible content checks.

A dated owner acceptance collected 107 menu rows from Sushi Yana plus one free run-summary row on October 8. Every delivered row has a product name, source identity and finite EUR price; observed prices ranged from EUR 2.00 to EUR 74.95. No failed source request, retry or missing price was recorded. This is one restaurant's bounded snapshot, not a complete menu or a general availability guarantee.

The run reached its USD 0.30 charge cap. Its summary is `degraded` with `SPENDING_LIMIT_REACHED`; platform status is **`FAILED`** because `failOnQualityIssues: true` deliberately rejects non-healthy quality. The 107 delivered records remain useful within that incomplete scope. Do not label this run fully successful or infer complete requested coverage from its row count.

The event counts are 107 result events and two automatic startup events. Both owner accounted event counts are zero, so this is not customer revenue or a customer profit result. The finalized owner resource cost was USD 0.0501465; one owner test does not prove customer margins, satisfaction or future prices.

| Dated artifact | Scope |
|---|---|
| [`10_2026-10-08_bounded_direct_menu_input.json`](10_2026-10-08_bounded_direct_menu_input.json) | Exact owner input for one direct menu, history and analytics disabled |
| [`11_2026-10-08_bounded_menu_sample.json`](11_2026-10-08_bounded_menu_sample.json) | Three field-preserving menu-row projections; not the full 107-row dataset |
| [`12_2026-10-08_bounded_run_summary.json`](12_2026-10-08_bounded_run_summary.json) | Exact free summary retaining the cap warning and degraded quality |
| [`runtime-verification-2026-10-08.json`](runtime-verification-2026-10-08.json) | Build, owner provenance, checks, event counts, costs and limitations |

The run options were build `1.0.22`, 2 GB RAM, timeout 180 seconds and `maxTotalChargeUsd: 0.30`. The charge cap is a run option, not an input field or a publisher resource-cost cap. Changing `failOnQualityIssues` can change the platform exit behavior; always inspect the quality summary.

Nine `priceText` values contain two displayed amounts. `price` retains the first displayed amount and the original text retains both; list-price, promotion and checkout semantics were not independently authenticated. One product name and price occurs in two categories with distinct source IDs, so 107 identities do not mean 107 unique dishes. Direct-menu delivery fields are mostly null, and observed zero rating/review values should not be treated as independently confirmed absence.

## October 6, 2026 publication

The owner release check confirmed public `latest` build `1.0.20` (`eE9sRgiSUvumj6lg7`), its complete frozen source hashes and unchanged protected Actor settings. This publication did not run a new scrape. Older snapshots and sample outputs below retain their original dates; they are not evidence of current source availability, customer payment or satisfaction.


## Historical July 28, 2026 snapshot

Audited through the public Store/API and the authenticated owner account on 2026-07-28.

| Evidence | Verified value |
|---|---|
| Store slug | `kamerozkan/german-delivery-menu-price-intelligence` |
| Actor ID | `dHYh0fcMQaXw4LS29` |
| Visibility | Public |
| `latest` at the July 28 audit | `1.0.13`, build ID `xwV0cEjYP2mAMH8Os`, succeeded 2026-07-28 20:54:19 UTC |
| Public Store Examples | Exactly 1 |
| Public Example | [`monitor-berlin-restaurant-menu-prices`](https://apify.com/kamerozkan/german-delivery-menu-price-intelligence/examples/monitor-berlin-restaurant-menu-prices), Task ID `rMqmZE2BnOWQvaABo` |
| Public Example run count | 3 |
| Latest successful public Example run | `WqgwqjrdXgdavKAmH`, build `1.0.11` |
| Example run window | 2026-07-28 14:54:48 UTC to 14:56:33 UTC |
| Verified Example dataset | `hDVcOZ11Mfyt2hIMR`, 158 rows |
| Actor activity at audit time | 13 builds, 14 runs, 2 users; 2 successful public runs in the previous 30 days |

At the July 28 audit, `latest` was `1.0.13`, while the audited successful public Example run used build `1.0.11`. Output sample 1 is a privacy-minimized projection of the first visible row in the audited Example dataset. Samples 2 and 3 are privacy-minimized projections of real live-run records published in the Actor's Store README as observed at that historical audit.

## Public and recipe inputs

| Sample | Status | What it demonstrates |
|---|---|---|
| [`01_public_store_example_input.json`](01_public_store_example_input.json) | Public | Exact saved input of the only public Store Example and its audited successful run |
| [`02_quick_postcode_coverage_recipe_input.json`](02_quick_postcode_coverage_recipe_input.json) | Recipe, not run | Restaurant-list coverage without full-menu extraction or analytics |
| [`03_multi_postcode_price_matrix_recipe_input.json`](03_multi_postcode_price_matrix_recipe_input.json) | Recipe, not run | Two-postcode menu collection, comparable products, price history, and analytics |

## Buyer questions and guardrails

| Buyer question | Evidence available | Required guardrail |
|---|---|---|
| What menu prices and delivery terms are shown for a postcode? | `menu_item` and `restaurant` rows preserve the observed postcode context | Treat every value as a point-in-time source observation |
| Can equivalent products be compared? | Deterministic canonical and comparable product IDs include size, quantity, dietary, and variant attributes | Review normalization confidence and product attributes before commercial decisions |
| Is the same product priced differently by postcode? | `postcode_price_matrix` reports per-postcode min, average, max, branches, and spread | A matrix needs at least two inputs and an overlapping chain and comparable product |
| Can price movement be monitored? | Named-store history retains up to 90 days and exposes item and basket changes | The first run has no prior baseline, so change fields can be `null` |
| Can collection quality be monitored? | `run_summary` exposes failures, retries, missing-price rate, cuisine coverage, and issues | `healthy` is an Actor quality result, not a guarantee of complete market coverage |

## Pipeline

```mermaid
flowchart LR
    A["German postal codes or menu URLs"] --> B["Postcode-routed restaurant discovery"]
    B --> C["Restaurant and menu extraction"]
    C --> D["Product and chain normalization"]
    D --> E["90-day named-store history"]
    D --> F["Postcode price matrix"]
    E --> G["Item and basket change metrics"]
    F --> H["Dataset, CSV, JSON, and report"]
    G --> H
    C --> I["Run-quality audit"]
    I --> H
```

## Input examples

<details>
<summary><strong>1. Public Store Example: monitor Berlin menu prices</strong></summary>

```json
{
  "failOnQualityIssues": false,
  "generateAnalytics": true,
  "includeMenus": true,
  "maxRestaurantsPerPostalCode": 2,
  "postalCodes": ["10115"],
  "sendSuccessWebhook": false,
  "trackPriceHistory": true
}
```

Full file: [`01_public_store_example_input.json`](01_public_store_example_input.json)
</details>

<details>
<summary><strong>2. Recipe: quick postcode restaurant coverage</strong></summary>

```json
{
  "postalCodes": ["10115"],
  "maxRestaurantsPerPostalCode": 10,
  "includeMenus": false,
  "trackPriceHistory": false,
  "generateAnalytics": false
}
```

The complete current-schema recipe, including quality and proxy settings, is in [`02_quick_postcode_coverage_recipe_input.json`](02_quick_postcode_coverage_recipe_input.json). It was not executed as part of this audit.
</details>

<details>
<summary><strong>3. Recipe: two-postcode price matrix</strong></summary>

```json
{
  "postalCodes": ["10115", "10435"],
  "maxRestaurantsPerPostalCode": 2,
  "includeMenus": true,
  "trackPriceHistory": true,
  "generateAnalytics": true
}
```

The complete current-schema recipe is in [`03_multi_postcode_price_matrix_recipe_input.json`](03_multi_postcode_price_matrix_recipe_input.json). It was not executed as part of this audit.
</details>

## Verified and privacy-minimized outputs

Street addresses, coordinates, image URLs, menu descriptions, source product IDs, and request-correlation parameters are omitted. See [`DATA_NOTICE.md`](DATA_NOTICE.md).

<details>
<summary><strong>1. Menu item with postcode-specific delivery economics</strong></summary>

```json
{
  "recordType": "menu_item",
  "observedAt": "2026-07-28T12:54:55.070Z",
  "searchPostalCode": "10115",
  "chainName": "Burgermeister",
  "restaurantName": "Burgermeister Eberswalder",
  "deliveryTimeMin": 30,
  "deliveryTimeMax": 50,
  "deliveryFee": 2.99,
  "minimumOrder": 10,
  "category": "Lieferando Specials",
  "productName": "Lieferandomeister",
  "canonicalName": "lieferandomeister",
  "comparableProductId": "de-menu-v3:175fde3409fc8839c0289009",
  "normalizationVersion": "de-menu-v3",
  "price": 10.59,
  "isAvailable": true,
  "priceChange90d": 0,
  "priceChangePercent90d": 0
}
```

Full record: [`01_verified_menu_item_output.json`](01_verified_menu_item_output.json)
</details>

<details>
<summary><strong>2. Self-auditing run summary</strong></summary>

```json
{
  "recordType": "run_summary",
  "observedAt": "2026-07-28T12:27:40.624Z",
  "completedAt": "2026-07-28T12:29:09.422Z",
  "status": "healthy",
  "expectedPostalCodes": ["10115"],
  "resolvedPostalCodes": ["10115"],
  "scrapedRestaurantCount": 2,
  "menuItemCount": 79,
  "unavailableItemCount": 7,
  "failedRequestCount": 0,
  "failedRequestRate": 0,
  "retryRate": 0,
  "nullPriceRate": 0,
  "issues": [],
  "failures": []
}
```

Full record: [`02_verified_run_summary_output.json`](02_verified_run_summary_output.json)
</details>

<details>
<summary><strong>3. Cross-postcode comparable-product matrix</strong></summary>

```json
{
  "recordType": "postcode_price_matrix",
  "observedAt": "2026-07-28T20:31:44.957Z",
  "chainName": "Burgermeister",
  "canonicalName": "hamburger",
  "postalCodeCount": 2,
  "branchCount": 1,
  "lowestPrice": 7.1,
  "highestPrice": 7.1,
  "priceSpread": 0,
  "priceSpreadPercent": 0
}
```

Full record: [`03_verified_postcode_matrix_output.json`](03_verified_postcode_matrix_output.json)
</details>

## API quick start

```bash
curl -X POST \
  "https://api.apify.com/v2/acts/kamerozkan~german-delivery-menu-price-intelligence/runs?token=YOUR_APIFY_TOKEN" \
  -H "Content-Type: application/json" \
  --data-binary @01_public_store_example_input.json
```

Use [`dataset_record.schema.json`](dataset_record.schema.json) to validate consumer-facing dataset records. The schema covers `restaurant`, `menu_item`, `postcode_price_matrix`, `menu_inflation_summary`, and `run_summary` rows.

## Source and interpretation limits

- The Actor reads publicly displayed Lieferando restaurant and menu information. It does not provide an official Lieferando API.
- Markup, access controls, availability, menu contents, prices, fees, offers, ratings, and delivery estimates can change.
- Results are observations from requested postcodes and restaurant limits. They are not proof of nationwide completeness or real-time coverage.
- Lieferando can block data-center traffic. The current input defaults to a German residential Apify Proxy profile. The current Pricing tab shows platform costs included for customers; the publisher still incurs those resource costs.
- A restaurant can serve multiple search postcodes. Branch count and postcode count describe the observed run, not the platform's full service area.
- Comparable-product matching is deterministic but can still require review. Size, quantity, dietary, and variant attributes are included to reduce false matches.
- A first run does not prove a price change. Retain the same named key-value store across later runs to build history.
- Run-quality status reports configured thresholds and observed collection health. It is not an uptime SLA or a guarantee that every source field was available.
- Use conservative concurrency and confirm applicable laws, platform terms, data rights, privacy obligations, and retention requirements.

## License

Sample code and repository documentation are available under the [MIT License](LICENSE). Source data remains subject to its original rights, terms, and applicable law.

## October 6 failure-status repair

Input, crawler or storage exceptions and strict quality failures now preserve a nonzero process exit instead of being masked by a default successful shutdown. `failOnQualityIssues: false` still permits a completed run with failed or degraded quality in its summary. The caller must inspect summary quality and dataset contents. Partial records and their earlier charges can remain after a later failure. Eight author cases and eight independent cases passed with simulated SDK, crawler and storage behavior, without a live scrape. See [`lifecycle-verification-2026-10-06.json`](lifecycle-verification-2026-10-06.json).

The current [`input_schema.json`](input_schema.json) includes the corrected billing field descriptions; input types, defaults and validation constraints were preserved.

## October 8, 2026 runtime checks

TypeScript build, thirteen synthetic regression scenarios and three additional navigation scenarios passed. Independent actual local Chromium/Crawlee checks confirmed resource blocking, navigation readiness and rejection of missing menu content. Those fixtures do not prove real source reliability. The single dated source acceptance is documented above with its spending-cap degradation and owner-only accounting. See [`cost-control-verification-2026-10-08.json`](cost-control-verification-2026-10-08.json) and [`runtime-verification-2026-10-08.json`](runtime-verification-2026-10-08.json).

## Resource controls and direct menu requests

For API calls with `restaurantUrls` and no `postalCodes` field, only the supplied menus are requested. Calls with neither field retain the default Berlin postcode. In the Console, set `postalCodes` to `[]` for a direct-only run because the form may include its default postcode. Explicitly supplied postcodes still add their requested postcode searches.

The browser blocks image, font and media URL patterns to reduce residential-proxy traffic. Documents, CSS, JavaScript and API responses remain available for menu hydration. Published image URLs still come from the page; matching image resources are not downloaded. This is an optimization, not a guarantee of source access or a publisher cost cap.

Initial browser navigation waits for `domcontentloaded`, then the existing visible heading, menu-list or restaurant-card checks and menu stabilization determine extraction readiness. A slow remaining page asset cannot by itself hold navigation until the full `load` event. Missing required content still fails the request; this does not bypass a block or prove current source access.

When no result event fits the remaining charge limit, the Actor skips browser crawling. If the limit is reached during collection, it stops dispatching new requests while already running requests can finish. No extra result event is added. The run summary includes `stoppedBySpendingLimit: true`, the `SPENDING_LIMIT_REACHED` warning, and an incomplete-coverage warning instead of presenting a capped run as healthy. Previously delivered rows and the automatic memory-based startup charge can remain charged.

The history precheck prevents writes after a known exhausted result limit. It does not make concurrent history and result delivery atomic; in-flight work and a failure can retain earlier history or delivered rows. Publisher profitability depends on actual runtime, residential-proxy traffic, delivered charge events and the user pricing tier. These controls do not guarantee a nonnegative margin.
