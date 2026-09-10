# Hotel Google Ads operating playbook

Use this sequence for one hotel at a time. Menu names can vary; verify the meaning of each control instead of blindly following an old screenshot.

## 1. Verify the hotel and business goal

Complete the [hotel brief](../templates/HOTEL-BRIEF.md) before editing Ads. Use the hotel's official site and authorized Business Profile to confirm its exact name, property code, street address, reservation phone, amenities, booking destination and photograph rights. Test the mobile booking journey through room/date selection without purchasing a room.

Prefer qualified reservation calls and confirmed direct reservations over raw click growth. Establish who answers the phone, how missed calls are handled, and how staff will record whether a call became a booking. Ask the owner for occupancy gaps, target stay dates, guest origin markets, average booking value and an acceptable acquisition cost. Do not invent these inputs.

Research local lodging intent, alternative hotels, the property's useful differentiators and events that actually affect its demand. Verify distance, travel-time, price and promotional claims before using them. A hotel outside downtown should not imply a downtown location.

## 2. Define the spend boundary

For most campaigns, Google's standard daily billed limit is twice the average daily budget. Example: `$2.50 × 2 = $5`; an unchanged full-month example is `$2.50 × 30.4 = $76`. Served cost can exceed billed cost after adjustments. Reconcile the billed-cost report rather than treating a dashboard snapshot as the final charge. [Google budget overview](https://support.google.com/google-ads/answer/10486536?hl=en).

A same-day reduction does not erase the day's earlier higher limit: Google uses the highest average daily budget chosen that day. A campaign total budget caps the flight, not each day. [Budget-change rules](https://support.google.com/google-ads/answer/10487143?hl=en).

Agree whether the ceiling means campaign ad charges, the whole account, or the complete invoice including taxes/fees. The example is not an all-in invoice guarantee. Do not enable if that distinction remains unresolved. Avoid budget-increasing recommendations, shared-budget surprises and overlapping duplicate campaigns. Alerts and pause rules help operations but reporting delays make them unsuitable as guaranteed hard caps.

All-day scheduling means eligibility, not continuous appearance or evenly divided hourly spend. Keep narrow intent and controlled bids to reduce waste; never claim the hotel will appear every hour. [Ad scheduling](https://support.google.com/google-ads/answer/2404244?hl=en).

## 3. Inspect existing campaigns before creating another

Check the active Google account and intended property. Review campaign status, budgets, dates, goals, ads, asset associations, recommendations and actual search terms. Find drafts and duplicate campaigns. Record the starting state privately.

On a mixed-business account, inspect inherited sitelinks, calls and locations. A hotel ad must not send guests to another property's address or a software demo page. Campaign-level sitelinks should not be assumed to suppress inherited account assets. Scope changes narrowly; preserve valid associations and obtain authority before modifying unrelated campaigns. [Sitelink guidance](https://support.google.com/google-ads/answer/2375416?hl=en).

## 4. Build the smallest useful Search campaign

The following is a conservative **example configuration**, not an automatic prescription:

| Setting | Initial approach | Reason / check |
| --- | --- | --- |
| Campaign | One property, Search | Easier to understand limited spend |
| Name | `PROPERTY - Hotel - Search Reservations` | Clear ownership and purpose |
| Networks | Search; Search Partners and Display off initially | Concentrate the initial test |
| Geography | Verified traveler-origin markets | A hotel-radius-only strategy can miss trip planners |
| Location option | Presence in chosen markets | Avoid unintentionally broad interest targeting |
| Language | Language of ads and supported booking journey | Match the guest experience |
| Schedule | All days, full day if required | Verify account time zone |
| Bidding | Maximize clicks with a reviewed CPC limit when conversion data is unproven | A $1 example limit may be too low for an actual market |
| Keywords | Focused exact/phrase hotel and city intent | Check close variants in search-term reports |
| AI expansion | Keep AI Max, text customization and URL expansion off for this controlled test | Reopen saved settings and confirm off dialogs |
| Destination | Exact property booking page | Prevent cross-property landings |
| Calls/location | Correct reservation phone; only this hotel's Business Profile | Avoid wrong-destination calls and directions |

Google documents CPC limits for [Maximize clicks](https://support.google.com/google-ads/answer/6268626?hl=en). Check bid adjustments and current behavior; the CPC limit and daily budget serve different purposes. Once reliable conversion data exists, evaluate conversion/value bidding rather than using clicks as a permanent proxy for bookings.

### Keyword examples to adapt

Replace the fictional hotel/city below; do not upload placeholders:

```text
[example hotel sample city]
"example hotel sample city"
[hotels in sample city]
"book hotel sample city"
"hotel rooms sample city"
```

Separate brand and non-brand intent in reporting, and use separate ad groups if their messages differ materially. Exact and phrase match can include close variants; they are not literal-only allowlists. [Match types](https://support.google.com/google-ads/answer/7478529?hl=en).

Review potential negatives such as jobs, careers, apartments and unrelated destinations against actual search intent. Do not blindly exclude words such as “free” that can also appear in a useful “hotel free breakfast” search. Add negatives at the narrowest appropriate scope and record why.

## 5. Write accurate ads and choose genuine images

Match the property and search intent in the headline. Combine hotel/city identification, a verified benefit, and a useful action such as checking availability or calling reservations. Stay within the live editor's limits; responsive Search headline/description limits are documented in [Google's guide](https://support.google.com/google-ads/answer/7684791?hl=en).

Example copy direction, only when verified:

- Hotel name + city.
- Check Rates & Availability.
- Free Hot Breakfast / Free WiFi.
- Description naming the exact property and booking destination.
- Pet-friendly wording with fees disclosed when applicable.

Do not invent discounts, room availability, ratings, “best price” claims or travel times. Use sitelinks only for useful, functioning property-specific destinations. If the website has no distinct useful pages, do not manufacture links merely to improve an optimization score.

### Photo selection

1. Start with a bright, current room photo showing the bed and usable room layout.
2. Add an accurate exterior/entrance so the guest recognizes the property.
3. Add genuinely differentiating amenities only when currently offered.
4. Review square and landscape crops; ensure the main subject is not cut off.
5. Record the source, permission and date. Website availability alone does not establish redistribution rights.

Use original photographs owned or licensed for the intended use. Do not synthesize a nicer room, remove a permanent defect, or add amenities. Avoid stock rooms, overlay-heavy graphics and misleading edits. Images are subject to eligibility/review and may not show on every impression. [Image requirements](https://support.google.com/adspolicy/answer/10347108?hl=en).

The “best” photo is a hypothesis until measured. Compare eligible assets after meaningful exposure; avoid declaring a winner from one click. Track qualified calls and reservations where attribution permits, acknowledging that asset reports do not always establish causality.

## 6. Establish honest measurement

Keep these states separate:

| Measure | What it establishes | What it does not establish |
| --- | --- | --- |
| Impression | An ad was served | It was the top result or caused a booking |
| Click | Someone interacted | A reservation was completed |
| Qualified reservation call | A relevant inquiry, according to an agreed rule | Revenue, unless staff/provider confirms it |
| Confirmed reservation | Booking confirmation linked through a valid measurement process | Incremental lift without further analysis |
| Booking revenue | Attributed value after deduplication and agreed adjustments | Profit or uncancelled stay revenue automatically |

Choose primary goals deliberately. Direction requests and outbound clicks should not silently become booking conversions. Verify the correct call action, call duration rule, phone source and reporting; [call conversion guidance](https://support.google.com/google-ads/answer/6100664?hl=en).

For an external chain booking engine, coordinate with its owner/provider for permitted tags, cross-domain attribution, click identifiers, deduplication, purchase value and cancellation handling. Never assume a hotel can install tags on a chain's domain. Keep guest-level information private and follow applicable consent requirements. Until purchases are verified, report them as unverified—not zero bookings and not successful bookings.

## 7. Capture every meaningful step and verify after saving

Use the [launch checklist and evidence manifest](../templates/LAUNCH-CHECKLIST.md). Capture the configured screen before continuing and capture the saved state again. Inspect the image you saved: transitions can produce stale or incomplete screenshots.

Keep the originals in a private dated folder. Use names such as `07-keywords.png`; add a caption explaining the property, setting, timestamp/time zone and whether the view is a draft, preview or saved state. Public examples must be sanitized and approved. Avoid filming logins, payment details and unrelated tabs.

After any save or toggle, refresh/reopen the panel. Confirmation dialogs can leave a setting unchanged if not completed. Verify budget, bid limit, geography, schedule, start date, goals, final URL and asset inheritance. The final saved state takes precedence over earlier wizard screens.

## 8. Publish, distinguish review from delivery, and hand off

Publish only with the owner's authority and the agreed spending boundary. If remaining checks require a pause or future start date, explicitly state that decision and record when the hotel can begin serving. Never report “running” because a campaign was merely created.

| State | Evidence to save | Appropriate statement |
| --- | --- | --- |
| Draft | Saved draft | Prepared, not published |
| Published / scheduled | Status + start date | Created; scheduled to start |
| Under review | Policy status | Awaiting Google approval |
| Eligible / enabled | Current policy and campaign status | Eligible to serve; no placement guarantee |
| Delivered | Dated impressions/clicks or valid placement evidence | Delivery observed for that period |

Use Google's [Ad Preview and Diagnosis tool](https://support.google.com/google-ads/answer/148778?hl=en) with the intended location, language and device. A single incognito search cannot prove universal delivery or failure. Do not click your own paid ad to test it. An organic Maps listing is not paid-ad evidence, and a generic chain ad is not necessarily this campaign.

Prepare a concise client/team recap: what changed, budget boundary, current status and time, confirmed evidence, limitations, next action and owner. Send only to authorized recipients.

## 9. Optimize against bookings, not vanity metrics

First week: inspect policy status, spend, landing page functionality, irrelevant queries and missed calls daily. After 7–14 days, review the [weekly report](../templates/WEEKLY-REVIEW.md), acknowledging a tiny budget may still have too little data to judge.

- Irrelevant searches: tighten terms and add appropriate negatives.
- Relevant clicks but few inquiries: inspect mobile booking friction, availability and message alignment.
- Calls but few bookings: review qualification, rate/availability and response handling.
- Low impressions: check eligibility, search demand and bid competitiveness before expanding.
- Apparent overspend: compare date/time zone, budget history, other campaigns and final billing adjustments.

Change one major hypothesis at a time and record before/after periods. Do not chase every optimization-score recommendation. Agree acquisition economics with the owner before scaling; review cancellations and attribution limitations.

## 10. Separate Search, Maps and Google Hotels

Search targets search intent. Eligible location assets can support local discovery; they do not buy organic Maps rank. Hotel Center rate/availability feeds and linked Ads accounts support Hotel campaigns and eligible travel-feed formats. A normal Search launch does not establish this connection. [Hotel Center linking](https://support.google.com/google-ads/answer/7663773?hl=en).

Ask the chain/connectivity provider whether the correct property's direct rates and free booking links are connected, whether paid campaigns already exist, and who controls the feed. Verify price accuracy and bookability before adding paid Hotel inventory. Avoid duplicate competition with an existing brand program.

## Sources

Sources are linked beside the relevant guidance. Budget and Hotel Center pages were checked September 9, 2026; other links are an operator reference set and should be reopened before each launch. Recommendations are our operating judgment, not Google guarantees. The Gallatin setup lessons in [LESSONS.md](LESSONS.md) are historical observations rather than live reporting.
