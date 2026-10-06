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
