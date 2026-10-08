# Data notice

This repository contains privacy-minimized samples derived from public restaurant and menu observations returned or published by the audited Actor.

- `01_verified_menu_item_output.json` is a field-preserving projection of the first visible row in dataset `hDVcOZ11Mfyt2hIMR`, produced by public Example run `WqgwqjrdXgdavKAmH`.
- `02_verified_run_summary_output.json` and `03_verified_postcode_matrix_output.json` are field-preserving projections of records that the Actor's public Store README identifies as live-run output observed on 2026-07-28.
- Fields whose values were not visible in the audited dataset JSON are omitted rather than inferred.
- Street addresses, coordinates, restaurant URLs with request-correlation parameters, source product IDs, image URLs, menu descriptions, and detailed opening hours are omitted.
- Public restaurant names, product names, prices, offers, ratings, and delivery terms remain because they are central to the sample's data utility.
- Prices, availability, offers, fees, ETAs, ratings, and menus are point-in-time source observations. They can change after collection.
- Normalized names, chain keys, comparable product IDs, inferred cuisines, quality status, and price-change fields are Actor-generated analytical outputs. They are not official Lieferando fields.
- Lieferando and Just Eat Takeaway.com are trademarks of their respective owners. This independent project is not affiliated with, endorsed by, or sponsored by either company.

Before collecting or retaining data, confirm that your use complies with applicable laws, platform terms, privacy obligations, and your own retention policy. Source availability, markup, and fields can change.

## Listing update on September 30, 2026

The Store title, description and search metadata were checked against the owned Actor and synchronized with this repository. This documentation update does not alter executable code, input or output schemas, recorded test outputs, artifact hashes, billing or runtime builds. Existing examples retain their original dates and validation limits. A public listing is not evidence of successful output, network acceptance or an achieved search ranking.

## Pricing documentation check on October 6, 2026

The billing explanation was reconciled with the saved active event configuration and frozen source charge locations. The actual price configuration was not changed. This pricing check started no Actor run, collected no new source data and proves no customer payment or satisfaction. Historical sample records and dates remain unchanged. See [`pricing-verification-2026-10-06.json`](pricing-verification-2026-10-06.json).

## October 6 lifecycle repair

The same publication also changes runtime failure exits. Lifecycle QA used synthetic SDK, crawler and storage fixtures. No new source scrape, customer dataset, payment, satisfaction result or refund is claimed. Historical samples were preserved.

## October 8 cost-control scope

Resource-blocking, direct-only URL defaults, result-budget scheduling and navigation readiness were published in public latest 1.0.22. Local regression fixtures are synthetic and use no source traffic. A separate dated owner source acceptance is described below. Historical menu examples retain their original timestamps. Images matching the blocked patterns are omitted from network loading; their published source URLs are still extracted from the DOM. Documents, CSS, JavaScript and API responses are retained. The optimization is not a guarantee of source access, complete menus or profit. Known exhausted budgets prevent additional history writes, but concurrent history and delivery are not atomic. A later failure can retain prior delivered rows and automatic startup charges.

## October 8 dated owner samples

- `10_2026-10-08_bounded_direct_menu_input.json` preserves the exact one-restaurant owner input. History, analytics and notifications were disabled. No credential or personal account identifier is present in that input.
- `11_2026-10-08_bounded_menu_sample.json` contains three field-preserving projections from source indices 0, 1 and 106 of the owner dataset, observed on October 8, 2026. The full private owner export was not copied into this repository.
- These new projections omit source product IDs, full restaurant URLs, addresses, coordinates, image URLs, descriptions, rating/review and delivery fields. Product and restaurant names, dated prices, categories and generated normalization fields remain to demonstrate the output contract.
- `12_2026-10-08_bounded_run_summary.json` preserves the exact summary: 107 menu rows, one restaurant, spending limit reached, quality degraded. Platform FAILED was caused by the strict quality flag and cap warning; it was not relabeled successful.
- The sample does not prove complete source/menu coverage, 107 unique dishes, postcode delivery coverage, current prices, paid customer use, revenue, satisfaction or general profit. Accounted owner events were zero.
- Multiple displayed price amounts and repeated source-category observations are retained honestly. A zero source rating or review count is not an independently authenticated absence of reviews.
- Owner run/build identifiers in `runtime-verification-2026-10-08.json` provide dated provenance. API tokens, account IDs, private storage identifiers, full logs and the full raw dataset are not included.
- Synthetic tests cover limited lifecycle and navigation paths. The source acceptance disabled history and analytics and does not freshly validate those features or integrations.

## October 8 completed-menu owner check

The later 1.0.23 check used one restaurant and a USD 1.00 run charge limit, with the same input feature scope as the earlier capped sample. It delivered 308 records, including nine explicitly unavailable items. File 13 is the exact input; file 14 contains only three field-preserving projections from indices 0, 254 and 307; file 15 is the exact run summary. The same omitted fields and privacy limits apply. The full raw dataset and account/storage identifiers are not published.

The prior 107-row sample remains unchanged. This newer session shared 106 of those source identities; one promotional row was absent and four image URLs differ. Exact live-snapshot parity and the cause of those differences were not proved. The changed fallback executes after menu extraction. Synthetic checks establish narrow code parity, not universal current source correctness. Owner accounted events were zero. One healthy source check is not customer adoption, satisfaction or a general margin guarantee.
