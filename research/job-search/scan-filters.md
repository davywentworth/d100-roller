# Job Scan Filter Rules

Agents reference this file for filter rules and return format. If editing **HARD DISQUALIFY** or **FIT RATINGS** in `rules.md`, also update this file.

---

## Filter Rules

Apply to every candidate:

### Hard Disqualify (no exceptions)
- On-site or hybrid — remote only
- Salary under $150k (unless federal GS equivalent)
- No React/frontend — pure backend, DevOps, or data roles
- Startups (seed through Series B)
- Experience floor fewer than 7 years (exception: 5+ yr floor acceptable if salary ≥ $185k)
- Social media platforms (Facebook/Meta, Twitter/X, TikTok, Snap)
- Crypto / blockchain / Web3 / DeFi
- Defense, military, intelligence, homeland security (ManTech, GDIT, CACI, Palantir, Anduril)
- Surveillance, ad-tech, data broker products
- Men's health / hormone optimization / testosterone therapy
- Restaurant tech (Toast, Owner.com, Slice)
- Consumer health/wellness/fitness apps (excludes enterprise healthcare B2B SaaS)
- Sports betting, fantasy sports, sports analytics platforms
- USDS / 18F / TTS (USDS requires DC onsite; both agencies heavily RIF'd)

### Strong Fit (prioritize)
- React + TypeScript, full-stack JS/TS, Tech lead / senior engineer titles
- Federal/government consulting, established company, remote-first

### Acceptable
- GraphQL/Apollo, Rails stack, Node/Python backend if React is frontend
- Contract/contract-to-hire for federal roles, east coast hours, regulated environments

### Fit Ratings
- **"Perfect"** — strong fit on all axes (React/TS, senior/lead title, remote-first, established co, $185k+)
- **"Strong"** — meets all criteria, one minor gap
- **"Possible"** — meets core criteria, notable caveat (salary unconfirmed, partial stack, etc.)
- **"Exception"** — has a hard disqualifier but compensating factors; surface for user approval, do NOT auto-add to To Pursue

---

## Return Format

JSON array. Each element:

```json
{
  "title": "...",
  "company": "...",
  "url": "...",
  "salary": "...",
  "track": "IC | Manager | Unknown",
  "fit": "Perfect | Strong | Possible | Exception",
  "notes": "...",
  "red_flags": "...",
  "source": "...",
  "job_id": "..."
}
```

Return `[]` if no qualifying roles found. Do not write to any files unless instructed.

---

## Listing Block Format

For appending to `listings.md`:

```
### [Title](url) — Company
**Date found:** YYYY-MM-DD | **Salary:** $ | **Track:** | **Stack fit:**
**Source:** | **Job ID:** <id>

> <1–2 sentence description>

**Why apply:** <stack match, salary, remote, experience fit, standout factors>

**Red flags:** <any concerns>
```
