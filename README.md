# FirmSignal

FirmSignal is a law-firm prospecting dashboard that uses public signals to identify firms that may benefit from front-desk, intake, scheduling, and CRM automation.

## What it does

- Finds nearby law firms through OpenStreetMap and Nominatim.
- Inspects public website markup for scheduling, client portal, chat, SMS, and intake-form signals.
- Identifies common public email infrastructure through Google DNS-over-HTTPS.
- Produces a transparent opportunity score with evidence for every lead.
- Supports filtering, saved leads, evidence review, and CSV export.

## Responsible-use boundary

Scores are directional research aids. A missing public signal does not prove that a firm lacks an internal system. Internal CRM usage, staff workflows, lobby kiosks, call routing, private portals, and unlinked systems are not reliably detectable and should be verified before outreach.

## Development

The application is a dependency-free Cloudflare Worker ES module.

```bash
bash scripts/build.sh
node scripts/validate-artifact.mjs
```

The worker source is in `worker/index.js`. The build output is generated under `dist/`.

## Data sources

- OpenStreetMap / Overpass API
- Nominatim geocoding
- Public law-firm website HTML
- Google DNS-over-HTTPS

Built for AISimplify Solutions.

