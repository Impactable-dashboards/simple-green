# simple-green

Static client intelligence hub for **Simple Green (Sunshine Makers, Inc.)**, deployed on Vercel.
One Vercel project serves the whole suite — every report is a self-contained HTML file at the
project root, linked from `index.html`.

## Pages

| File | Report | Notes |
|---|---|---|
| `index.html` | Client Intelligence Hub | Landing page — featured card + supporting report cards |
| `impact-report.html` | Q3 2026 Impact Report | Quarterly intelligence room, 6 tabs |
| `abm-engagement.html` | ABM Account Engagement Dashboard | |
| `audience-segment.html` | Audience Segment Diagnostic | |
| `message-creative.html` | Messaging & Creative Diagnostic | |
| `targeting.html` | Targeting Worksheet | |

Two links live outside the repo and are linked from the hub: the Competitive White Space
Google Doc, and the prior 90-Day Impact Review Gamma deck.

## Shareable links

`https://<project>.vercel.app/impact-report.html`

The impact report is tabbed and each tab is deep-linkable via the URL fragment, so a single
tab can be shared directly:

- `#summary` · `#audience` · `#messaging` · `#pipeline` · `#penfreq` · `#next90`

e.g. `…/impact-report.html#pipeline` opens straight to the Pipeline tab.

## Adding a report

1. Drop the `.html` file at the repo root (kebab-case filename).
2. Paste the hub back-nav block from the top of any existing report page just after `<body>`,
   and change the report name in it.
3. Copy the template card at the bottom of the card grid in `index.html`, then swap the
   `href`, number, title, description, and date.

## Adding the next impact report

`impact-report.html` is the stable "current quarter" link — the one to share and re-share.
When the next quarter's report is ready:

1. Rename the outgoing file to its period (`impact-report-q3-2026.html`) so the old link and
   its data stay intact, and add it to the card grid as an archive card.
2. Write the new quarter to `impact-report.html` and update the featured card's title,
   reporting period, and dates.

That keeps one shareable link always pointing at the newest report, with every prior quarter
still reachable.
