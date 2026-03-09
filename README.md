# Truth Of India

A collection of documented investigative articles on BJP and RSS governance — written by **Muhammed Shafin P** (hejhdiss), from Malappuram, Kerala.

🌐 **Live site:** [https://truthofindia.hejhdiss.workers.dev/](https://truthofindia.hejhdiss.workers.dev/)

---

## Why This Exists

This is not a political pamphlet. It is not written against Hinduism, or against any Indian.

It is written in defence of the **Constitution of India** — the document that guarantees equality for every person on this soil, regardless of religion, caste, gender, or origin.

The articles in this series are based entirely on publicly verifiable sources: government data, Supreme Court records, NCRB statistics, UN reports, and internationally published journalism. Every claim can be checked. Every source is listed. Readers are encouraged to verify independently and disagree where the evidence takes them.

The author is not a professional journalist or academic. He is an educated Indian citizen who looked at the public record and could not stay quiet.

---

## How This Repo Works

`index.html` is the full site — a single-page reader that loads each `.md` article inline. All article files sit in the same directory. No framework, no build step. Deploy anywhere static hosting works (GitHub Pages, Netlify, etc.).

---

## Articles

| # | File | Title | What it covers |
|---|------|-------|----------------|
| 01 | `betrayal-of-palastenians.md` | **When Refugees Became Occupiers: The Betrayal of Palestine** | The documented history of the Nakba, who started the Iran-Israel war, and the bombing of a girls' school where 165 children were killed. |
| 02 | `south-india-vs-rss-brainwash.md` | **You Dropped Your Brain. RSS Picked It Up.** | How RSS manufactured consent through textbook revision, media capture, and social conditioning — and why South India has been more resistant to it. |
| 03 | `indias-compromised-pm.md` | **India's First Compromised Prime Minister** | Indira Gandhi made the USS Enterprise turn around. Modi asked Trump for a 30-day oil permit. The full documented record of India's surrendered sovereignty. |
| 04 | `modi-puppet-sovereignty.md` | **Is Modi Renting Out India's House?** | Three concrete tests of whether Modi can say no to Washington — on energy, Palestine, and independent foreign policy. He fails all three. Includes the documented story of Indian workers sent to replace Palestinians at Netanyahu's personal request. |
| 05 | `bjp-rss-farmers-betrayal.md` | **The Broken Promise: How BJP and RSS Betrayed India's Farmers** | 300,000 farmer suicides since 1995. The three farm laws, the year-long protest of 700,000 people, the Lakhimpur Kheri killings, and Modi's broken promise to double farmers' income by 2022. |
| 06 | `bjp-rss-children-betrayal.md` | **The Children BJP Left Behind** | India's child malnutrition crisis, POCSO failures, NCERT textbook deletions, and what the hunger index data actually shows about BJP's decade in power. |
| 07 | `bjp-rss-violence-impunity.md` | **Violence Without Consequence** | Hathras, Manipur, Bilkis Bano, bulldozer politics — a documented record of state-enabled violence against minorities, women, and Dalits, and the pattern of impunity that follows. |
| 08 | `bjp-rss-corruption-cronyism-fifa.md` | **Electoral Bonds, Adani, and the FIFA Ban** | The Electoral Bonds scheme dismantled by the Supreme Court, the Adani-Modi nexus documented by Hindenburg and OCCRP, and India's FIFA suspension over political interference in football. |
| 09 | `bjp-rss-india-tech-development.md` | **Digital India's Dark Side** | India leads the world in internet shutdowns. The gap between the Digital India brand and the reality of censorship, surveillance, and press freedom collapse. |
| 10 | `bjp-rss-truth-india.md` | **The Full Record** | A summary article tying together the series — what BJP and RSS have done to India's farmers, children, minorities, institutions, and standing in the world. |
| 11 | `bjp-rss-corruption-cronyism.md` | **The Money Trail: How Modi's Government Built a Corruption Machine** | Adani criminally indicted in the United States. Electoral Bonds declared unconstitutional — companies under ED raids donated to BJP, then investigations stopped. PM CARES Fund: ₹10,000+ crore collected in the government's name, with no RTI, no CAG audit, and Parliament not allowed to ask questions. Three structures. One architecture of corruption. |

---

## Files in This Repo

```
index.html                          ← Full site (single-page reader)
betrayal-of-palastenians.md
south-india-vs-rss-brainwash.md
indias-compromised-pm.md
modi-puppet-sovereignty.md
bjp-rss-farmers-betrayal.md
bjp-rss-children-betrayal.md
bjp-rss-violence-impunity.md
bjp-rss-corruption-cronyism-fifa.md
bjp-rss-india-tech-development.md
bjp-rss-truth-india.md
bjp-rss-corruption-cronyism.md      ← NEW: Article 11
README.md
```

---

## Author

**Muhammed Shafin P** · writing as **hejhdiss** · Malappuram, Kerala, India

- Medium: [medium.com/@hejhdiss](https://medium.com/@hejhdiss)
- Email: hejhdiss@gmail.com

> *"Everything in this series is based on documented, verifiable public records. Sources are listed at the end of every article. Check them. Disagree if the evidence takes you there. That is the whole point."*

---

## Hosting Change — Netlify → Cloudflare Workers

This project was previously hosted on **Netlify** (free tier). The Netlify deployment served the article `.md` files as static assets directly alongside `index.html` — the frontend fetched them at runtime using `fetch('filename.md')`.

The free tier bandwidth limit was hit due to reader traffic, so the site has been migrated to **Cloudflare Workers** (free tier), which has no bandwidth cap.

### What Changed for `.md` Files

On Netlify, `.md` article files (e.g. `betrayal-of-palastenians.md`, `south-india-vs-rss-brainwash.md`) were deployed as plain static files and fetched directly by the browser.

On Cloudflare Workers, static files must be explicitly bundled and served through the Worker script. Each `.md` file is included as part of the Worker's assets so the `fetch()` calls in `index.html` continue to work without any changes to the frontend code.

### Why Cloudflare

- No bandwidth limits on the free tier
- Global CDN edge delivery
- Cloudflare's free tier handles high-traffic sites without throttling or suspension
- Zero config changes needed on the `index.html` side — the `.md` fetch logic remains identical

---

© 2026 Muhammed Shafin P. Content may be shared freely with attribution.