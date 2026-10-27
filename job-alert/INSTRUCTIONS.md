# Daily Job Alert — Run Instructions

The 7 AM scheduled task reads this file on each run. To change what it searches for, edit this
file. The next morning's run uses the new version.

## Who this is for

Robert (Rob) Griego, Austin TX area. 10 years in production planning and manufacturing
(Feniex Industries, Thermon). Last role: Director of Manufacturing (Dec 2024 – Oct 2026), now
deliberately moving to **individual-contributor** roles.

- ERP/MRP: **Acumatica** (MRP config, Import Scenarios, multi-warehouse, work order automation),
  **Microsoft Dynamics 365 (D365)** and Dynamics AX 2012 (both at Thermon; Rob was the SME for
  Thermon's AX 2012-to-D365 transition and worked in both). D365 roles count as a strong ERP match.
- Tools: advanced Excel, Velixo NX, Microsoft Project
- Planning: master production scheduling (MPS), net requirements/MRP, MTO, CTO and MTS items,
  production scheduling, capacity/demand planning, forecasting, inventory management
- Manufacturing data: BOM maintenance, routings and operations, labor tracking
- Also: labor analytics, root cause analysis, KPI reporting; Lean, 5S, Kanban, ISO 9001/14001
- Results: Feniex — MTO/MTS lead times cut from 2–4 weeks to 5–10 days. Thermon — CTO lead times
  cut from 12–13 weeks to 4–5 weeks; late orders cut from a peak of 800+ to 5.
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
   - Quad Cities (Moline, Rock Island, East Moline, Silvis IL; Davenport, Bettendorf IA)
   - Bloomington–Normal, IL
5. **No required SQL, Python or other programming.** Rob has no SQL or Python experience.
   Exclude jobs that list SQL, Python, R or another programming language as a requirement
   ("required", "must have", "proficiency in", or among the minimum qualifications). If it's
   only "preferred", "a plus" or "nice to have", the job can stay, but say so in Concerns
   (e.g. "SQL preferred"). Excel, Power BI, ERP report writers and Velixo don't count as
   programming.

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
   `Denver, CO`, `Colorado Springs, CO`, `Montana`, `Chicago, IL`,
   `Moline, IL`, `Davenport, IA`, `Bloomington, IL`. You don't need every
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

## Read the full posting (required)

Before a job goes in the digest, **read its full posting.** Search-result snippets don't count.
- Indeed: `get_job_details` with the job ID.
- Dice: `get_job_details` with the job's `guid`.
- ZipRecruiter and everything else: fetch the posting URL with WebFetch. If the redirect page
  doesn't show the description, search the web for the company's own posting and fetch that.

From the full posting, confirm: direct reports or supervision duties, degree requirement
(and whether "or equivalent experience" is accepted), employment type, salary, on-site,
hybrid or remote status, and the ERP/MRP systems named. Apply the hard requirements to what
the posting actually says.

If the full posting can't be opened after two tries, the job can still go in the digest, but
its Concerns line must start with "Couldn't open full posting —". Don't write "I did not read
the full description" for a posting you could have opened.

To keep the run a reasonable length, screen the search results by title, location and
salary first, then read full postings only for the jobs that survive that first pass. That's
usually 10–25 postings.

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

## Step order (important)

1. Search and screen.
2. Update `seen_jobs.json`. Add every job you will email **and** every job you looked at
   closely and rejected, using today's date and `sent` or `rejected`. Then commit and push to
   the `job-alert` branch:
   ```
   git add job-alert/seen_jobs.json
   git commit -m "job-alert: seen jobs <YYYY-MM-DD>"
   git push -u origin job-alert
   ```
   Try the push once. If it fails, move on and note it in the digest's last line.
3. **Write the digest as your very last message, then stop.** Make no tool calls after it, no
   push retries, no notifications, and no follow-up message. Only the final message is
   emailed, so anything after the digest replaces it.

## Output — the email

The final message is emailed to Rob, so it must be the digest itself, with no process
narration. Format:

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
  sources actually worked, and name any that failed, including a failed push).
