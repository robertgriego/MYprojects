# Ursa Major — Senior Supply Planner interview prep

Posting: https://ursamajor.com/careers/senior-supply-planner/
Berthoud, CO · hybrid, at least 3 days a week on-site · $90K–$121K · exempt · U.S. Person and
clearance-eligible (ITAR/EAR)

## The job in one line

Own the MPS for one propulsion segment: turn the demand plan into a capacity-feasible supply
plan, release MOs, run MRP and work its messages, keep planning parameters right, kill shortages
at the root, and feed the monthly SIOP cycle. Also forecasting, new-hardware supply plans, and
mentoring junior planners.

## Company facts worth knowing

- Propulsion and defense systems: hypersonics, solid rocket motors, satellite maneuvering
  (in-space propulsion), launch. Shifted toward defense.
- New CEO Chris Spagnoletti (Feb 2026).
- Hadley H13 engine first hot fires (Mar 2026); Draper engine flight demo with AFRL (Mar 2026).
- Opened a new Longmont, CO manufacturing facility (Aug 2026) for avionics and in-space
  propulsion.
- Going public through a SPAC merger (reported $2.3B; expected to close Q1 2027).
- Takeaway: they're moving from development into production ramp. That's when MPS discipline,
  clean parameters and shortage control matter most. Say that.

## Your 30-second pitch

"I've been a production planner for 10 years. At Thermon I managed the master schedule and net
requirements for about 60,000 meters a month of mostly make-to-order and engineered-to-order
tubing bundles, and cut late orders from over 800 to 5 and CTO lead times from 12–13 weeks to
4–5. Most recently at Feniex I led planning and scheduling hands-on: I rebuilt the MPS in
Acumatica, updated the MRP parameters and planning strategy by item, and moved shortage tracking
from Excel into MRP. That cut lead times from 2–4 weeks to 5–10 days. This role is exactly that
work, for hardware that's ramping into production."

## Match: what they ask for → your proof

| They want | Your example |
|---|---|
| Own and execute the MPS | Managed MPS + net requirements at Thermon; rebuilt the MPS in Acumatica at Feniex; built the MPS tool at Feniex 2016–2020 |
| Capacity-feasible plan, load vs. constraints | Prioritized back, current and upcoming orders against capacity at Thermon (800+ late orders → 5); quoted lead times from capacity |
| Run MRP, work reschedule/cancel/expedite messages | Rescheduled production, sales and purchase orders as dates moved; handled expedites and cancellations; moved shortage tracking into Acumatica MRP |
| Maintain planning parameters (lead times, lot sizing, safety stock, order policies) | Updated MRP parameters and MTO/MTS strategy by item; found and fixed a min/max error that caused stockouts (72% of core SKUs back to min) |
| "How bad parameters or BOMs break the plan" | The min/max story, and keeping BOMs accurate through the Smartsheet-to-Acumatica work order migration |
| Shortage root cause with Procurement / Manufacturing | Min/max root cause; live Velixo NX shortage dashboard; pulled in vendor material to protect the schedule |
| Replenishment and safety stock strategy | Ran the Kanban/replenishment system at Thermon; 3-week stock rebuild goals hit on 9 of 12 SKUs |
| ERP experience (SAP, Oracle, Odoo, Katana, Sage) | Four ERPs: Acumatica, D365, AX 2012, Fishbowl. SME for the AX-to-D365 move. Learning a new one is something you've already done several times |
| Low-volume, high-complexity, engineer-to-order | Thermon was mostly MTO/ETO, configured per order, at high volume (60,000 m/month). Feniex: discrete electro-mechanical assemblies |
| Engineering change management | Coordinated engineering changes into production lines at Thermon; maintained part numbers, BOMs, routings |
| KPIs, dashboards, data visualization | Velixo NX dashboard; KPI tracking; advanced Excel dashboards |
| Present to management | Daily production status and capacity reporting to managers and sales at Thermon |

## Likely questions and answer outlines (use STAR: situation, task, action, result)

**1. Walk me through how you build and maintain an MPS.**
Demand in (open orders, forecast, stock targets) → check against capacity → time-phase it →
release work orders → watch MRP messages and shortages daily → reset when demand or capacity
changes. Give the Thermon numbers and the Acumatica rebuild.

**2. Tell me about a time bad planning data broke the plan.**
The min/max story: recurring stockouts, traced to a min/max setup error in the ERP, fixed it,
72% of core SKUs back to minimum stock and 9 of 12 hitting 3-week rebuild goals.

**3. How do you handle a shortage that's about to stop the line?**
Find it early (MRP + the live shortage dashboard), expedite or pull in from the vendor,
resequence work so the floor stays busy, then fix the root cause so it doesn't come back.

**4. How did you get late orders from 800+ to 5?**
Prioritized back orders, current orders and upcoming orders against real capacity, kept the
MPS honest, rescheduled production, sales and purchase orders as dates moved, and told sales
and managers the truth daily. (Be ready with how long it took — you know this, I don't.)

**5. You were a Director. Why a planner role now?**
"At Feniex the part of the job I owned and was best at was planning and scheduling — I rebuilt
the MPS and MRP myself. I want that to be my whole job, not one piece of it." Keep it positive
and short.

**6. Why did you leave Feniex?**
Keep it short and neutral, and don't discuss the severance terms. Have a one-sentence answer
ready before the interview.

**7. Our ERP isn't one you've used. How fast can you get up to speed?**
Four ERPs so far, and you were the SME for a major migration (AX 2012 → D365). MRP logic is the
same everywhere: lead times, lot sizes, safety stock, order policies.

**8. Experience with S&OP / SIOP?**
Answer honestly from what you actually did. Closest examples: daily capacity and status
reporting to managers and sales at Thermon, quoting lead times from capacity, adjusting
planning strategy to market trends. Show you understand the supply review: capacity, inventory,
risk scenarios, recovery options.

**9. Forecasting from sales and market data?**
Same rule: real examples only. At Thermon you adjusted the planning strategy to market trends
and reviewed lead times with inside sales.

**10. This role mentors junior planners and may act as a lead. Comfortable with that?**
Yes to mentoring and training. Then ask what "lead or first-level supervisor" means here (see
questions below). You want to hear that it's informal.

**11. Why Ursa Major? Why aerospace/defense?**
Use your saved answer in ABOUT_ME.md (Ursa Major section), plus the production-ramp angle:
new Longmont facility, hot fires turning into production hardware.

## Questions to ask them

1. Which propulsion segment would I own, and is it in production or ramping from development?
2. What ERP do you run, and how mature is the MRP setup — are parameters trusted today?
3. What does a typical week look like between MPS, MRP messages and shortage meetings?
4. The posting mentions acting as a lead or first-level supervisor. How often does that
   happen, and do any planners report to this role?
5. Where does planning sit in the SIOP cycle, and who facilitates the supply review?
6. What's the biggest planning problem the team is fighting right now?
7. How will the SPAC listing and the new Longmont site change production volumes next year?
8. What would make someone in this role successful in the first 90 days?

## Before the interview — check these

- **U.S. Person / clearance:** required. Be ready to confirm.
- **Relocation:** the job is in Berthoud, CO, at least 3 days a week on-site. Have your answer
  ready (timing, whether you need relocation help).
- **Salary:** posted $90K–$121K. Your Indeed minimum is $100K. With 10 years, asking in the
  upper part of the range is reasonable. Decide your number before the call.
- **Degree:** the posting accepts "equivalent education and experience." Your coursework line
  is fine.
- **Supervision:** the posting says the role may act as a lead or first-level supervisor. If
  that's a problem for you, ask about it (question 4) rather than finding out later.
