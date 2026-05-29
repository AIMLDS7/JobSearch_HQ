# Job Search HQ

**A zero-dependency, single-file job search command center** — built for senior professionals targeting multi-region markets simultaneously.

![screenshot](screenshot.png)

---

## What it does

Most job searches are chaotic — 12 browser tabs open, lost bookmarks, no sense of where you applied or when. This tool replaces that chaos with a structured command center, purpose-built for senior roles across MENA, UK, and EU markets.

Open one HTML file. Everything runs locally in your browser. No server, no login, no SaaS subscription.

---

## Features

**Search Engine**
- Boolean query builder — generates `short` and `full boolean` strings ready to paste into any job board
- Filters for date range, job type, seniority level, and sector
- One-click launch across 32 platforms simultaneously

**Platform Directory**
- 32 pre-configured job boards with Smart Search links (pre-filled query) and Base Portal links
- Covers MENA (Bayt, GulfTalent, Naukri Gulf, Jadarat, NEOM, Aramco, QatarEnergy), UK/EU (LinkedIn, Indeed, Reed, Energy Jobline, IrishJobs), and Asia
- English-first filter mode highlights English-language EU platforms

**Company Intelligence**
- 32+ target companies with region tags, sector metadata, direct careers portal links, and LinkedIn shortcuts
- Filter by region or sector; search by name
- Fully editable — add, remove, or update companies in-browser

**Application Tracker**
- Kanban-style pipeline: Bookmarked → Applied → Interview → Offer → Rejected
- Add applications manually with role, company, location, salary, notes
- Sort by date, score, or company; filter by status
- Export / import tracker data as JSON

**Government Portals**
- 14 official government job portals across EU, Asia, Gulf, and visa-specific boards
- English-language availability flagged per portal
- Filter by region

**Recruiter CRM**
- Track recruiter contacts with agency, region, specialisation, and last contact date
- Status tagging: Active, Warm, Cold

**ATS Matcher**
- Paste a job description; the tool scores your CV against it and surfaces missing keywords
- Helps tailor applications before submission

**Interview Prep**
- Role-specific question banks for Cost Manager, Commercial Manager, Procurement, and Renewable Energy positions

**Timing Intelligence**
- Live widget showing optimal application time based on recruiter working hours across target time zones

---

## Architecture decision

This is a deliberate single-file architecture. Every feature — UI, state, logic, data — lives in one `.html` file.

That means:
- **Zero build tooling** — no Webpack, no Node, no `npm install`
- **Zero dependencies** — two Google Fonts and Tabler Icons (CDN, optional)
- **Instant portability** — email it, put it on a USB drive, open it offline
- **Stateless by design** — nothing persists without an explicit Export

For a personal productivity tool with a single user, this is the correct tradeoff. A React + backend stack would add complexity without adding value.

---

## Usage

```bash
# No installation required
# Just open the file in any modern browser

open DG_JobSearch_HQ_v5.0.html
```

**Keyboard shortcuts**

| Key | Action |
|-----|--------|
| `1` – `8` | Switch tabs |
| `S` | Toggle sidebar |
| `E` | Open edit mode |

---

## Customisation

Everything is editable directly in the browser via **Edit Mode** (`E`):

- Add / remove target locations
- Add / remove role categories
- Edit company list
- Edit job listings
- Modify your profile chips shown in the header

Hit **Export** to save your changes as a new `.html` file.

---

## Tech stack

| Layer | Choice |
|-------|--------|
| Structure | Semantic HTML5 |
| Styling | CSS custom properties, CSS Grid, no framework |
| Logic | Vanilla ES6+ JavaScript |
| Icons | [Tabler Icons](https://tabler.io/icons) (CDN) |
| Fonts | Syne, DM Sans, DM Mono (Google Fonts CDN) |
| Build | None |
| Dependencies | 0 |

---

## Target profile

Built around a senior profile in **EPC / Energy / Infrastructure**:

- Roles: Senior Cost Manager, Quantity Surveyor, Commercial Manager, Procurement Manager
- Sectors: EPC/EPCC, BESS / Renewable Energy, Infrastructure
- Markets: UAE · KSA · Qatar · UK · Netherlands · Ireland · Norway
- Experience: 7+ years, Samsung C&T / Gleeds / TCE background

The role categories, company list, and platform selection all reflect this context — but the tool is fully generic and reusable for any senior job search with different targets.

---

## License

MIT — fork it, adapt it, make it your own.
