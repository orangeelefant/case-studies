# Case study — Rastahunden

How [Rastahunden](https://rastahunden.com) became Sweden's most complete dog-friendly map. Built and maintained by [Christoffer Holmgren](https://github.com/orangeelefant) at [Webraketen](https://webraketen.se).

## The brief

Build a sole-source national directory of dog-friendly places — somewhere a dog owner can find:
- Hundrastgårdar (dog parks)
- Koppelfria zoner (off-leash zones)
- Hundbad (dog-friendly bathing spots)
- Hundvänliga caféer (dog-friendly cafés)

with one constraint: every café/restaurant must be **owner-confirmed** (not scraped).

## Numbers (live)

- **596+** verified locations
- **116** Swedish cities (Stockholm 135 · Malmö 61 · Göteborg 42 · Lund 33 · Uppsala 26 + 111 more)
- **Free** for users — no paywall, no ads
- **38%** reply rate on outreach to candidate cafés (April 2026 cohort)

## Stack

- **Next.js 16** (App Router)
- **Supabase** (Postgres + Auth + Realtime)
- **Mapbox GL JS** for interactive map
- **Netlify** for hosting + edge functions
- **Resend** for transactional outreach
- **Claude Code** in the loop for outreach copy + data hygiene

## Outreach pipeline

1. Crawl candidate cafés/restaurants from OpenStreetMap + Google Places
2. Send single-question email ("Är hundar välkomna?") via Resend
3. HMAC-signed yes/no/unsubscribe one-click links → `/api/outreach/respond`
4. Resend webhook (signed) logs delivery state to `business_outreach` table

## Live URL

→ [rastahunden.com](https://rastahunden.com)
→ Press: hej@rastahunden.com

## Related

- **Built by:** [Webraketen](https://webraketen.se)
- **Maintainer:** [github.com/orangeelefant](https://github.com/orangeelefant)
- **Webraketen portfolio:** [github.com/Webraketen/portfolio](https://github.com/Webraketen/portfolio)
