# Job Search Rules

> If editing **HARD DISQUALIFY** or **FIT RATINGS** below, also update `scan-filters.md`.

## Search Targets

### Track 1: Federal Contracting (VA Ecosystem)
Target companies with React/JS needs on VA contracts:
- GovCIO, Reefpoint Group, Prometheus Federal Services, Aptive Resources
- ECS Federal, Nava PBC, Ad Hoc, Guidehouse
- Any T4NG2 primes (see `va-consulting-contractors` research doc)
- Flag roles at VA T4NG2 primes specifically — highest fit given BID background

### Track 2: Private Sector
- React + Ruby on Rails stacks preferred
- Fully remote required
- Salary range: $150–220k

## Soft Preferences
- **No startups** — prefer established companies, mid-size consultancies, or large orgs; avoid seed/Series A/B startups
- **Slow-paced environments are fine** — enterprise, government, regulated industries all acceptable; "fast-paced startup" is not a selling point
- **East coast hours are fine** — not a negative signal
- **Ruby/Rails is not required** — JS/TS-only stacks are fully acceptable; treat the resume as a superset of skills
- Remote-first culture preferred (not just "remote allowed")

## Fit Criteria

### Strong Fit (prioritize)
- React (primary signal) + TypeScript
- Full-stack JS/TS (Node, Next.js, etc.)
- Tech lead / senior engineer titles
- Federal/government consulting experience valued
- Established company (not startup)
- Remote-first orgs

### Acceptable
- GraphQL/Apollo (nice to have, not required)
- Rails stack (still a fit, just not required)
- Node.js, Python, or other backend stacks if React is on the frontend
- Contract/contract-to-hire for federal roles
- East coast hours
- Slow-paced or regulated environments

### Disqualify
- On-site or hybrid — remote only, no exceptions
- Under $150k unless federal GS equivalent or unusual upside
- No React/frontend at all — pure backend, DevOps, or data engineering roles
- Startups (seed through Series B unless exceptional circumstances)
- Requires fewer than 7 years of experience — signals a mid/junior role regardless of title; senior/lead roles should require 7–10+ years. **Exception:** roles with a 5+ year floor are acceptable if the compensation floor is $185k or greater — high salary compensates for the lower experience signal.
- **Ethical domain objections** — the following are hard disqualifiers regardless of stack or salary:
  - Social media platforms (Facebook/Meta, Twitter/X, TikTok, Snap, etc.)
  - Crypto / blockchain / Web3 / DeFi (Coinbase, Circle, etc.)
  - Defense, military, intelligence, or homeland security contractors (ManTech, GDIT, CACI, Palantir, Anduril, etc.)
  - Surveillance, ad-tech, or data broker products
  - Men's health / hormone optimization / testosterone therapy products
- **Domain preferences (disqualify)** — personal industry preferences; apply regardless of stack or salary:
  - Restaurant tech (Toast, Owner.com, Slice, etc.)
  - Consumer health, wellness, and fitness — mental health apps, telehealth platforms, wellness/fitness products; excludes enterprise healthcare data/analytics/B2B SaaS (Veeva, Arcadia, etc.)
  - Sports and sports-adjacent platforms — sports betting, fantasy sports, sports analytics, sports-first ticketing (FanDuel, DraftKings, SeatGeek, etc.)
- **USDS / 18F / TTS** — both disqualified: USDS requires DC onsite; both agencies significantly RIF'd under DOGE (2025–2026)

## Search Queries (run on Dice + Indeed)
1. "senior software engineer React Ruby on Rails remote"
2. "tech lead React federal government remote"
3. "senior software engineer React GraphQL full-stack remote"
4. "senior software engineer React TypeScript remote"
5. Federal track: search by company name at target orgs

## Where to Search by Track

### Private sector
- **Dice** — best for tech roles; filter `workplace_types=Remote, employment_types=FULLTIME`
- **Indeed** — use `mcp__claude_ai_Indeed__search_jobs`; company-name searches don't work well, use keyword searches
- **LinkedIn** — user searches manually and provides screenshots; after identifying promising companies from LinkedIn results, always attempt to find the listing directly on the company's careers page (WebFetch the careers URL) to get the full job description, direct apply link, and salary details that LinkedIn may not show. Add confirmed careers page URLs to the company's entry in README.md Company Notes.
- **Hacker News "Who's Hiring"** — monthly thread; WebSearch for current month URL then WebFetch; high signal for senior engineers at established companies
- **We Work Remotely** — WebSearch only (403 on direct fetch); apply $150k+ and 7+ yr filters aggressively; many listings are international or below floor
- **Mission-aligned company direct checks** — Oddball (Greenhouse), Mozilla (mozilla.org/careers/listings), Proton (verify US remote per listing), Automattic (all-remote globally)
- **jobs.ffwd.org/jobs** — curated board for mission-aligned / civic-tech companies; check periodically for remote senior engineering roles

### Federal track
- **Target company career pages** (Indeed/Dice yield nothing for these):
  - Nava PBC: https://www.navapbc.com/careers
  - Ad Hoc: https://adhoc.team/careers/
  - GovCIO: https://govcio.com/careers
  - ECS Federal: https://www.ecstech.com/careers
  - Reefpoint Group: https://reefpointgroup.com/careers
  - Guidehouse: https://guidehouse.com/careers
  - Aptive Resources: https://www.aptiveresources.com/careers
  - Oddball: https://job-boards.greenhouse.io/oddball (employee-owned, VA-focused, React/TS, fully remote)
- **LinkedIn** — most federal contractors post there; search by company + "React" or "software engineer"
- **ClearanceJobs** — for roles requiring any clearance level (Public Trust and above)

## Federal Salary Reality Check
Federal contractor and civic tech posted salaries run well below private sector:
- GovCIO React/Redux Developer: $90k–$100k (confirmed 2026-05-03)
- Ad Hoc senior/staff bands: $125k–$137k (confirmed 2026-05-03)
- Always verify salary before investing time in a federal application — many don't post it upfront
- The $150k floor effectively rules out most federal IC/subcontractor roles; only primes with commercial-adjacent work (like Ten Mile Square) tend to clear it

## Verification Rule
Dice, Indeed, and Levels.fyi listings go stale or contain inaccurate data — roles can remain indexed weeks or months after being filled, and aggregators like Levels.fyi may show incorrect experience floors or salary ranges. After identifying any promising role via Dice, Indeed, LinkedIn, or Levels.fyi:
1. Always follow up on the company's own careers page to confirm the role is still open
2. Use the careers page listing (not the aggregator listing) as the canonical source for job description, requirements, and apply link
3. If the role is not found on the careers page, treat it as likely filled or non-existent — do not apply via the aggregator
4. **Levels.fyi specifically**: experience floors and salary ranges shown are often user-submitted and unreliable — always verify against the official JD before disqualifying or pursuing based on those numbers

## Evaluation Template
When presenting a job, include:
- Title (as a markdown hyperlink to the apply/listing URL), company, salary (if listed), location/remote status
- Stack match assessment (Strong / Partial / Weak)
- Federal track or private sector
- Any red flags

When storing results in README.md `All Listings`, use the full listing block format defined there (title as link, date, salary, source, job ID, why apply, red flags).

## User-Submitted URLs (single-URL mode in /job-scan)

When the user passes a URL directly to `/job-scan`, they have **pre-approved** the role. Always add it to To Pursue + All Promising Roles. Note any disqualifiers clearly (experience floor, salary floor, etc.) but do not route to Disqualified. The only exception: hard ethical domain objections (crypto, defense/intel, surveillance, social media, men's health) — flag those explicitly and confirm before adding.

## Davy Overrides

When Davy explicitly approves a role that has a disqualifier (e.g., overrides a startup DQ, domain preference, or salary floor), label it **Davy override** in the notes — both in the To Pursue table and in All Promising Roles. This distinguishes roles Davy chose to pursue despite a known rule violation from roles that were incorrectly judged as qualifying. Example: BeatStars was a Davy override (industry attractive despite $149k floor + 5yr exp floor). Do NOT apply "Davy override" on Claude's own initiative — only when Davy has explicitly said to pursue the role.

## Notes
- BID contract transition: 2026-05-18 — urgency is high
- Resume trims to Thanx (June 2012) onward — ignore anything earlier
- AI tooling experience (Claude Code, CoPilot, GitHub MCP) is a differentiator worth highlighting
