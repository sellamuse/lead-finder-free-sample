# Lead Finder — Free Sample (n8n workflow)

Turn a niche + a location into a CSV of local business leads — name, address, phone — using only free, no-API-key data sources (OpenStreetMap). Built for n8n.

**This is the free sample, and its limits are stated up front, not buried:**

| | Free sample (this repo) | Paid Lead Finder |
|---|---|---|
| Search radius | capped at **3,000 m** | your choice |
| Results | capped at **25** | uncapped |
| Output fields | **name, address, phone** | + website, email, coordinates |
| Niches included | **6 examples** (dentist, restaurant, cafe, plumber, salon, gym) | full niche map (25+) |

The caps are positioning, not DRM — the JSON is right here and you can read every line. The paid version's real value is the fields this sample stops at: website and email are what outreach runs on. The full Lead Finder, and the Lead Gen Pack that adds AI enrichment + outreach drafts on top of it, are in the SellaMuse store: https://payhip.com/SellaMuse

## What it does

1. **Nominatim** (OpenStreetMap's geocoder) turns your location text into coordinates.
2. **Overpass API** finds businesses of your niche near those coordinates.
3. You get a downloadable `leads.csv`.

No API keys. No paid services. The whole stack costs $0 to run.

## Import & run (2 minutes)

1. In n8n: **Workflows → Import from File** → pick `lead-finder-free-sample.json`.
2. Open the **Set Search Inputs** node and set your `niche` and `location` (defaults — cafe / Des Moines, IA — are just examples).
3. Click **Execute Workflow**. When it finishes, download `leads.csv` from the **Save Leads to CSV** node.

## Honest notes

- OpenStreetMap coverage varies by area — dense US suburbs are good, rural areas are thinner. Phone fields are often empty; that's normal for OSM data, not a bug.
- Overpass is a shared public resource — run one query at a time and don't hammer it.
- This produces a starting list, not a verified database.

## The full version

The paid **Lead Finder** ($19) removes the caps and adds website, email, and coordinates. The **Lead Gen Pack** ($39) adds two more workflows on top of it — AI enrichment and outreach drafts — so the list you pull is the list you can actually contact.

→ https://payhip.com/SellaMuse

---
*SellaMuse — Northstar AI. Free sample of a paid workflow; the sample workflow file itself is yours to use and modify.*
