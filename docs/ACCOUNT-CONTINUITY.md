# Stable accounts, campaigns and hotel reporting

Reviewed September 9, 2026. This is a recommended operating model, not a claim that accounts have been created, migrated, linked or connected to an API.

## Keep what already works

Improve an existing campaign in place when its type and purpose remain appropriate. Change keywords, exclusions, assets and settings with a dated change log; do not recreate it for each optimization. Record its customer ID and campaign ID privately so reporting remains stable even when names change.

Google cannot convert a campaign to a different campaign type after creation. A decision to replace PMax with Search therefore requires a separate Search campaign once. Keep the old campaign paused and retain its historical ID in the reporting map. Avoid deleting history or repeatedly rebuilding the replacement. [Campaign-type rule](https://support.google.com/google-ads/answer/6340536?hl=en)

Copying or moving a campaign is not a transfer of performance history: impressions and clicks do not transfer into the new campaign. Treat any later account separation as an explicit migration with a cutoff date and old-to-new mapping. [Copy/move behavior](https://support.google.com/google-ads/editor/answer/38654?hl=en)

## Preferred future account structure

For a multi-hotel service, we recommend one agency manager account (MCC) with a separate client Ads account for each hotel when ownership and billing arrangements permit. This separates permissions, billing context and reporting while allowing central management. It is our operational recommendation, not a Google requirement to create an account for every property.

```text
Agency manager account (MCC)
+-- Hotel A client Ads account
|   +-- Stable Search campaign
|       +-- Related ad group(s)
|           +-- Ad(s) and relevant assets
+-- Hotel B client Ads account
    +-- Stable Search campaign
        +-- Related ad group(s)
            +-- Ad(s) and relevant assets
```

Link an existing suitable hotel account rather than recreating it. Linking to an MCC preserves that client account and its history. Existing access and billing remain in place unless deliberately changed, such as arranging consolidated billing. Confirm ownership and authorized access before sending link requests. [Manager linking](https://support.google.com/google-ads/answer/7456530?hl=en)

An existing account containing several hotels cannot be separated merely by linking it to an MCC: the linked account still contains all its campaigns. Keep a private campaign-to-hotel mapping for its historical and current reporting. Decide separately whether future separation is worth the migration cost; do not migrate solely to make a diagram look cleaner.

## Multiple ads do not mean multiple daily budgets

Ads and ad groups within a campaign share its campaign budget. Adding a second ad does not automatically grant another daily allowance. Google determines delivery; a common campaign budget does not promise equal spend for each ad. [Account organization](https://support.google.com/google-ads/answer/1704396?hl=en)

For multiple independently budgeted campaigns belonging to the same hotel, allocate the hotel's limit across them. Under the standard unchanged average-daily-budget rules, a `$5` hotel daily billed-ad-cost ceiling means their combined averages must be no more than `$2.50`. For example, `$1.50 + $1.00` averages imply up to `$3 + $2` daily billed ad cost. This assumes eligible campaign types, no higher same-day budgets and separate treatment of taxes/fees. Do not give every new campaign its own `$2.50` and call the total `$5`. [Budget limits](https://support.google.com/google-ads/answer/10486637?hl=en)

Shared budgets can allocate one budget across eligible campaigns in an account, but compatibility and bid strategy must be verified. They do not provide per-hotel isolation if shared across hotels. Prefer clearly owned budgets; never assume a manager account provides a daily spending cap across its clients. [Shared budgets](https://support.google.com/google-ads/answer/10487241?hl=en)

## Private reporting map

Keep a mapping outside this public repository. A stable internal hotel key is the business identity; customer and campaign IDs identify Google's records. Names and labels help people but should not be the only join keys.

| Field | Purpose |
| --- | --- |
| Internal hotel key | Connect all approved historical and future records for one property |
| Customer ID + campaign ID | Identify each campaign within its owning account |
| Campaign role/type | Distinguish Search, PMax, brand defense or other approved roles |
| Valid-from / valid-to dates | Preserve ownership and migration boundaries |
| Prior/replacement campaign references | Join a justified one-time replacement without overwriting history |
| Currency and account time zone | Interpret spend and daily boundaries correctly |
| Status and budget resource reference | Locate paused history and current spending controls |

For daily operational reporting, retrieve the appropriate client account's campaign IDs, dates and cost metrics, then map them to the hotel. Preserve the account currency and convert API micro-units correctly. Compare campaign-level totals before drilling into ad groups or ads; do not sum campaign totals again with their child rows. Asset, conversion-action and other segment reports may have different aggregation behavior. [Reporting overview](https://developers.google.com/google-ads/api/docs/reporting/overview), [segmentation](https://developers.google.com/google-ads/api/docs/reporting/segmentation)

Operational ad-cost metrics are not automatically an invoice allocation. Reconcile billing adjustments, taxes and fees separately using an agreed client allocation method. If old mixed campaigns cannot be reliably assigned to a single property, disclose the unresolved amount rather than inventing a precise split.

## Future API access: one integration, authorized client access

A developer token identifies the API application and is obtained through a manager account. Google says a company generally needs one developer token; a separate token per hotel is not the standard requirement. Its access level determines permitted environments and limits. Possessing a token alone does not authorize access to every hotel. [Developer token](https://developers.google.com/google-ads/api/docs/api-policy/developer-token)

API requests also need an authorized OAuth identity with access to the target account. When accessing a hotel through its manager, the manager's ID is the `login-customer-id`; the target hotel's client customer ID identifies the account being queried or changed. Direct authorized access to a client account does not require the manager header. Use the permission path actually granted, not a guessed ID. [Authorization and headers](https://developers.google.com/google-ads/api/rest/auth?hl=en)

This model can serve several hotel accounts through one approved integration, provided access is granted for each. It does not require sharing client passwords or placing tokens in this repository. Keep credentials in approved secret storage, establish client-specific access checks, and start with a verified read-only report before any future automated changes.

## Change record for the team

Before a structural change, record the business reason, current IDs, proposed IDs/account, budget allocation, date/time zone, measurement continuity, rollback state and authorized owner. Afterward verify the saved state and reporting map. Until that verification exists, describe the change as proposed or prepared, not completed.
