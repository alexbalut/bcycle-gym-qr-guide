# b.cycle Gym QR Guide (unofficial demo)

**QR machine-instruction app skinned for a b.cycle club demo.** Members scan a QR on a machine → bilingual (EN/FR) how-to guide. Staff manage machines, download QRs, print floor sheets, and review ROI insights.

> **Unofficial demo mockup for pitching only.** Not affiliated with b.cycle or any parent company. Does **not** use official logo image assets — text wordmark only. Brand colors (`#E91E63` / `#212121`) are approximate pitch tokens.

Seeded demo gym: **b.cycle Montreal**. `/` is the **demo-ready member product UI** — not a marketing landing page.

Sibling (generic GymQR Guide): [gym-machine-qr-guide](https://github.com/alexbalut/gym-machine-qr-guide)

## Disclaimer

This repository is an **unofficial product demo**. b.cycle® and related marks belong to their respective owners. Do not represent this app as an official b.cycle product. No official logos are bundled.

## Quick start

```bash
cd bcycle-gym-qr-guide
cp .env.example .env
npm install
npx prisma db push
npm run seed
npm run dev
```

Or one-shot setup:

```bash
npm install && npm run setup && npm run dev
```

Open [http://localhost:3000](http://localhost:3000) — member gym home for **b.cycle Montreal** (Machines / Workout / Progress / Scan).

## Demo credentials

| Field    | Value                    |
|----------|--------------------------|
| Email    | `admin@bcycle.demo`        |
| Password | `demo1234`             |
| Gym      | b.cycle Montreal                |
| Slug     | `bcycle`           |

Seed creates **10 bilingual machines**, sample view counts, and a few open/resolved issues.

## Branding notes

- Surfaces use secondary `#212121` with primary accent **`#E91E63`**
- Text wordmark **b.cycle** — no trademarked logo files
- Tagline: “Spin boutique”

## Key routes

| Route | Description |
|-------|-------------|
| `/` | Gym member home |
| `/scan` | Camera QR scan |
| `/q/[token]` | Machine guide |
| `/m/bcycle/[machineSlug]` | Friendly slug URL |
| `/admin/login` | Staff login |
| `/admin/insights` | Owner ROI dashboard |

## Caveats

- Auth is simple credential + JWT cookie — fine for demo; harden for production.
- SQLite at `prisma/dev.db` — don’t commit it.
- Member workout/progress is browser localStorage only (`bcycle-workout:v1:<slug>`).
- Unofficial branding — do not ship as an official b.cycle app.

## Photo credits

Demo photos under `public/machines/` are from Unsplash — see [CREDITS.md](./CREDITS.md). Not official b.cycle assets.

## License / affiliation

This repository is an **unofficial product demo mockup** for pitch purposes. b.cycle® and related marks belong to their respective owners. Do not represent this app as an official b.cycle product.

## Repo

https://github.com/alexbalut/bcycle-gym-qr-guide
