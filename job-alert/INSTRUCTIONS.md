# Daily Job Alert — Run Instructions

The 7 AM scheduled task reads this file on each run. To change what it searches for, edit this
file. The next morning's run uses the new version.

## Who this is for

Robert (Rob) Griego, Austin TX area. 10 years in production planning and manufacturing
(Feniex Industries, Thermon). Last role: Director of Manufacturing (Dec 2024 – Oct 2026), now
deliberately moving to **individual-contributor** roles.

- ERP/MRP: **Acumatica** (MRP config, Import Scenarios, multi-warehouse, work order automation),
  Microsoft Dynamics AX2012, Fishbowl MRP
- Tools: advanced Excel, Velixo NX, Microsoft Project
- Domains: production scheduling, capacity/demand planning, forecasting, inventory management,
  labor analytics, root cause analysis, KPI reporting; Lean, 5S, Kanban, ISO 9001/14001
- Products: discrete electro-mechanical assemblies and engineered-to-order industrial equipment
- Education: CS coursework at UTSA, **no completed bachelor's degree**

## Hard requirements (exclude if any fail)

1. **Salary ≥ $80,000.** Exclude if the posted range tops out below $80K. If no salary is
   posted, include it and say "not listed".
2. **Full-time, W-2, salaried.** Exclude contract, 1099, hourly, part-time, temp, and gig work.
   Exclude AI-training/evaluation gigs that use planning titles, like Mercor.
3. **No direct reports.** Exclude roles that say "manage a team", "direct reports", "hire and
   develop", "performance management", or "supervise planners/buyers". A "Manager" title is
   **not** automatically excluded. Judge by the responsibilities, and flag it in concerns.
4. **Location** must be one of:
   - Fully remote, US
   - Austin–San Antonio corridor, TX (Austin, Round Rock, Georgetown, Cedar Park, Pflugerville,
     Kyle, San Marcos, New Braunfels, San Antonio, etc.)
   - Anywhere in Colorado
   - Anywhere in Montana
   - Chicago, IL metro area

## Target titles (search terms)

Material Planner · Senior Production Planner · Production Planning Analyst · Inventory Planning
Analyst · Supply Chain Planner · Demand Planner · Supply/Demand Planning Analyst · Master
Scheduler · MRP Analyst · Acumatica Consultant · ERP Consultant · ERP Systems Analyst · ERP
Business Analyst · ERP Implementation Consultant

## Where to search

1. **Indeed** (`search_jobs`, job_type `fulltime`), **ZipRecruiter** (`search_jobs`,
   `salary_min: 80000`, `employment_types: ["FULL_TIME"]`, `max_posted_minutes_ago: 4320`), and
   **Dice** (`search_jobs`, `posted_date: "THREE"`, `employment_types: ["FULLTIME"]`).
   Run the target titles across the locations: `remote`, `Austin, TX`, `San Antonio, TX`,
   `Denver, CO`, `Colorado Springs, CO`, `Montana`, `Chicago, IL`. You don't need every
   combination every day. Cover every location and the higher-value titles first: Material
   Planner, Production Planner, Supply Chain Planner, Demand Planner, Acumatica/ERP Consultant.
   Aim for about 25–40 searches.
2. **Acumatica partner (VAR) career pages.** These are the best-documented IC lane. Check with
   web fetch/search: Protelo, Crestwood Associates, SWK Technologies, Net at Work, NexTec,
   DSD Business Systems. Also search the web for "Acumatica consultant" remote job postings.
3. **ATS boards** for watchlist companies if reachable (Greenhouse
   `https://boards-api.greenhouse.io/v1/boards/{slug}/jobs`, Lever
   `https://api.lever.co/v0/postings/{slug}?mode=json`, Ashby
   `https://api.ashbyhq.com/posting-api/job-board/{slug}`). Watchlist: Base Power, Tesla, Sierra
   Space, plus Austin-area manufacturers. Skip any that fail. Don't spend long on them.

For promising results whose title is ambiguous, pull the full description (`get_job_details`)
to check management duties, employment type, and salary before including it.

## Dedupe

`job-alert/seen_jobs.json` lists jobs already sent or reviewed. The key is
`company | title | location`, lowercased. **Skip anything already in it.** The same job often
appears on several boards, so merge duplicates within today's run too.

## Soft preferences (use for ranking and the "why" line, not for excluding)

- Acumatica-specific roles rank highest, then other ERP/MRP planning roles.
- Discrete or electro-mechanical manufacturing ranks above process or pharma.
- Postings that accept "or equivalent experience" rank above degree-required ones. Note when a
  degree is required.
- Note startup risk or known high-turnover employers in concerns instead of excluding them.
- Remote ranks above relocation.

## Output — the email

Your **final message is emailed to Rob**, so it must be the digest itself, with no
process narration. Format:

```
Job Alert — <Weekday, Month D>  ·  <N> new matches

1. <Job Title> — <Company>
   <Location> · <Salary or "salary not listed"> · <Source board>
   Link: <URL>
   What it is: <one sentence>
   Why it fits: <one sentence tied to Rob's experience>
   Concerns: <management hints / degree required / startup / salary near floor — or "none">

2. ...
```

- Rank best fit first. Cap at 15. If there are more, add one line: "+ N more lower-fit matches
  skipped".
- Keep the full URLs exactly as returned. Don't shorten or strip parameters.
- If there are no new matches, the whole message is: `Job Alert — <date>: no new matches today.`
- End with one line: `Searched: Indeed, ZipRecruiter, Dice, Acumatica partners` (list whichever
  sources actually worked, and name any that failed).

## Before finishing

Add every job you emailed **and** every job you looked at closely and rejected to
`seen_jobs.json`, using today's date and `sent` or `rejected`. Then commit and push to the
`job-alert` branch:

```
git add job-alert/seen_jobs.json
git commit -m "job-alert: seen jobs <YYYY-MM-DD>"
git push -u origin job-alert
```

If the push fails, still send the digest. Mention the failure in the last line.
