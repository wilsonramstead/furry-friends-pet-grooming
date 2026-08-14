# Furry Friends Pet Grooming — demo site

Tier-1 (Clean Slate) single-page demo for **Furry Friends Pet Grooming**, a personal,
one-on-one dog groomer in St. Petersburg, FL (Pinellas County). Owner-groomer: **George**.

- Phone (matched to GBP): **(727) 522-7387** — used in all display text, tel:/sms: links, JSON-LD.
- Address: 4320 4th St N, St. Petersburg, FL 33703.
- Rating shown: **4.8 ★ across 83 Google reviews** (≥4.4 threshold met).
- Fonts: **Della Respira** (display serif) + **Gayathri** (body). Distinct from all grooming
  siblings (approved pair; no other site uses it).
- Palette: soft **sage-green** primary + warm **ivory** canvas + gentle **terracotta** accent —
  deliberately distinct from the parallel sibling Amy's Dog Dynasty (emerald/gold) and all other
  grooming folders.

## Facts / softening
- Reviews are real Google reviews, condensed, attributed as first name + last initial
  (David J., M. R., L. S., Crystal B., David W.). One closing card paraphrases the brand promise
  and shows the 4.8★/83 aggregate rather than a fabricated named review.
- Services are review-evidenced: full grooms & breed cuts, walk-in nail trims (incl. 10-week
  puppies), baths / brush-outs / de-shedding, puppy's-first-groom, calm one-on-one handling,
  spotless unhurried salon. "Not a retail assembly line" is a direct customer phrasing.
- Hours are as listed on GBP (Mon closed, Tue–Sat 7:30 AM–5:00 PM, Sun closed) — no anomaly.
- Owner George is named in body copy (owner-operator; every review names him) but there is **no
  standalone "Why George" personality section** — the feature section is framed as the boutique
  "one dog at a time" difference.
- No invented emails, prices, founding years, or licenses.

## Images — Unsplash stock (business has ~0 usable own photos)
Downloaded from images.unsplash.com, re-encoded with PIL (≤350 KB, progressive JPEG). Every image
visually verified against its alt text. IDs listed here so cross-wave dedup greps (which cover
README.md) can detect them even though the HTML references self-hosted `assets/` paths.

| File | Unsplash photo ID | Subject |
|------|-------------------|---------|
| hero.jpg + og-image.jpg | photo-1598875706250-21faaf804361 | Happy, freshly groomed golden dog smiling at camera |
| feature.jpg | photo-1625321171045-1fea4ac688e9 | Groomer gently blow-drying a small dog held in their arms |
| g1.jpg | photo-1605197161470-d0261cac6767 | Fluffy freshly washed terrier, paws up, bright and clean |
| g2.jpg | photo-1592887302112-b87aca16ad2c | Calm schnauzer wrapped snugly in a towel after a bath |
| g3.jpg | photo-1581887936036-3f4f7f0b6679 | Happy dog holding a towel in its mouth after grooming |
| g4.jpg | photo-1629030502047-b6ac6d4a78b6 | Dog wrapped in a soft white towel, licking its nose |

og-image.jpg is a 1200×630 crop of the hero (golden dog face) for the DM link-preview.

## Verify / deploy
- Verified with puppeteer-core + Edge at 390 / 1366 / 1440 px: zero horizontal overflow; hero full
  stack (eyebrow → headline → sub → CTA pair → rating chip) visible with no scroll at 1440×900 and
  1366×768. All `.reveal` motion gated behind `prefers-reduced-motion`.
- `<meta name="robots" content="noindex">` present (DEMO). Deployed to
  https://wilsoninnovations.net/furry-friends-pet-grooming/.
