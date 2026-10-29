# MS-4019 · A Day in Service Operations
### Operations persona extension: the same agentic day, built for operations leaders

| | |
|---|---|
| **Extends** | *A Day with Project Nexus* (same demo flow, same scheduling habit) |
| **Persona** | Operations Manager: service, delivery or business operations |
| **Featured agents** | Personal News Digest · Plan My Day · **Ops Shift Delta** (Project Delta Digest template) · **Weekly Ops MBR** ✚ · AI Learning Advisor |
| **Supporting agents** | **SME Finder** ✚ · Prompt Coach · Analyst · Researcher · Writing Coach · SharePoint agent |
| **Key message** | Operations runs on rhythms (shift handovers, daily stand-ups, the weekly review). **Schedule an agent into every rhythm.** |

✚ = agent added for the Operations persona. Every other demo reuses the standard flow with an operations scenario, prompts and data.

---

## Why these agents for Operations
| Operations rhythm | Pain today | Agent | Why it fits |
|---|---|---|---|
| Before the shift | Alerts, change notices and policy deadlines buried in mail | Personal News Digest | Turns broadcasts into an operational alert list |
| Daily stand-up | Firefighting pushes out planned work | Plan My Day | Plans and **re-plans** around incidents |
| Incident in progress | "Who can fix this?" takes 30+ minutes | **SME Finder ✚** | Finds the right expert from people and org data |
| Root cause | Spreadsheets of tickets, no time to analyse | Analyst | Trends, Pareto and drivers in minutes |
| Prevention | Fixes without evidence; unclear client updates | Researcher + Writing Coach | Cited prevention plan and crisp customer comms |
| Shift handover | Manual handover notes; overdue actions slip | **Ops Shift Delta** (Project Delta Digest template) | "What changed since last shift" every handover |
| Weekly review (MBR) | Hours building KPI, SLA and issue packs by hand | **Weekly Ops MBR ✚** | Leadership-ready KPI, SLA, top issues and actions from one workbook |
| Runbooks | Same escalation and policy questions every shift | SharePoint agent | Self-service runbook and escalation answers |
| Getting better | No time to learn automation | AI Learning Advisor | Personal path to automating operations |

---

## The story
**Divya Sharma** is the Operations Manager of Contoso India's **Service Operations Centre** in Bengaluru. Her team runs 24x7 support for four client-facing services (**Payments Gateway, Order Portal, Mobile App, Partner API**) used by retail clients such as **Fabrikam Retail**.

It's Thursday, two days before the **festive-season change freeze**. Her **Weekly Ops MBR** with **Rakesh Bhatia, Head of Operations**, is tomorrow morning. Incidents are up, SLA breaches have more than doubled, and overnight a certificate warning appeared on the payments gateway.

One problem at a time, Divya hands the work to an agent, and **schedules** each one into the rhythm of her operation. Tomorrow, the handover, the alerts and the MBR pack are ready before she logs in.

## Story flow
| Time | Divya's question | Demo | Agent | MS-4019 topic | Scheduled prompt |
|---|---|---|---|---|---|
| 7:45 | *What changed that affects my operation?* | Ops 1 | Personal News Digest | What are agents | Ops alerts: daily 7:45 |
| 8:30 | *What matters today, and now there's a Sev1?* | Ops 2 | Plan My Day + Prompt Coach | Prompt Coach, benefits | Start my day: daily 8:30 · Handover wrap: daily 18:00 |
| 9:15 | *Who can fix this fast?* | Ops 2A ✚ | **SME Finder** | Prebuilt / template agents | n/a |
| 11:00 | *Why are SLA breaches rising?* | Ops 3 | Analyst | Analyst agent | n/a |
| 12:30 | *How do we stop it before the freeze?* | Ops 4 | Researcher + Writing Coach | Researcher, coach agents | n/a |
| 14:00 | *What changed since the last shift?* | Ops 5 | **Ops Shift Delta** (Agent Builder) | Build, test, edit an agent | Shift delta: daily 7:30 and 15:30 |
| 15:00 | *Is my MBR pack ready?* | Ops 5A ✚ | **Weekly Ops MBR** (Agent Builder) | Agent components, knowledge, testing | MBR pack: Fri 8:00 · Action check: Mon 9:00 |
| 16:15 | *Can my shift leads answer their own questions?* | Ops 6 | SharePoint agent + sharing | SharePoint agents, sharing | n/a |
| 16:45 | *How do I automate this next?* | Ops 7 | AI Learning Advisor | Who can create agents | Learning check-in: Mon 16:00 |
| 17:30 | *What's ready for tomorrow?* | Ops 8 | Plan My Day + all schedules | Governance, review | Learners schedule 3 |

---

## Before you start
- [ ] Everything in the main guide's *Before you start* list
- [ ] Agents available: **SME Finder** (template) · Agent Builder for **Ops Shift Delta** and **Weekly Ops MBR**
- [ ] A SharePoint site called **Service Operations** with the files from `Operations/Sample-Data` uploaded
- [ ] `Operations/Prompts/Ops-Copy-Paste-Prompts.txt` posted in the class Teams chat

| Sample file | Used in |
|---|---|
| `Ops_Sample_Alerts.md` | Ops 1 |
| `Ops_Expert_Directory.xlsx` | Ops 2A (if SME Finder isn't available) |
| `Contoso_Weekly_Ops_Review.xlsx` (sheets: Incidents_Raw, SLA_Tracker, Top_Issues, Leadership_Review, Action_Items, Parameters) | Ops 3, Ops 5, Ops 5A |
| `Shift_Handover_28Oct_Night.docx` | Ops 5 |
| `Ops_Runbook_and_Escalation_Matrix.docx` | Ops 6 |

### What the data shows (for trainers)
| Measure | Prior week (15–21 Oct) | Current week (22–28 Oct) |
|---|---|---|
| Incidents | 95 | **120** |
| Response SLA breach rate | 6.3% | **17.5%** |
| Resolution SLA breach rate | 8.4% | **20.8%** |
| Sev1 incidents | 1 | **4** (3 for Fabrikam Retail) |
| Downtime | 757 min | **1,623 min** |
| Revenue at risk | INR 58.0 lakh | **INR 161.0 lakh** |
| RCA tagging (target 95%) | 95.8% | **82.5%** |
| #1 issue cluster | n/a | **Certificate / config change failures**: 4 → 19 incidents, 11 resolution misses, 775 min downtime, INR 87.3 lakh at risk |
| #2 issue cluster | n/a | **API timeouts (partner integrations)**: 14 → 21 incidents, 8 resolution misses |
| Night vs day shift | n/a | Night: 14 of 39 missed resolution SLA (36%) · Day: 11 of 81 (14%) |
| Overdue actions | n/a | **ACT-101** certificate renewal (due 24 Oct) · **ACT-104** night-shift engineers (due 27 Oct) |

---

## Ops 1 · 7:45 · Personal News Digest · ALERT
*Extends Demo 1 · MS-4019: What are agents*

| | |
|---|---|
| **Overview** | The same Personal News Digest, focused on what affects **the operation**: change freezes, maintenance windows, security deadlines and leadership asks. |
| **Business scenario** | Before the 8:30 stand-up, Divya needs to know which company announcements change today's operational risk. |
| **Pain points** | Change and maintenance notices are buried in broadcast mail · security deadlines missed · surprises during the shift |
| **Business benefits** | Fewer change-related incidents · deadlines met · a calmer stand-up |
| **Learning objectives** | Personalise a template agent to a role · schedule a pre-shift briefing |
| **Environment setup** | Personal News Digest · announcements in your mailbox (or paste `Ops_Sample_Alerts.md`) |

### Demo walkthrough
1. Open **Personal News Digest** (added in Demo 1).
2. Run:
```
Goal: Brief me on company announcements that affect my operation today.
Context: I'm an Operations Manager running a 24x7 service operations centre for client-facing payment, order, mobile and partner API services.
Source: Company-wide announcements from my email, Teams and SharePoint news in the last 24 hours.
Expectations: Top 5 only, as a table: Priority (Critical/Important/FYI) | Headline | Operational impact | Action & deadline. Flag anything that changes today's risk.
```
3. Follow-up:
```
Which of these should I raise in this morning's stand-up, and who needs to act?
```
*Expected:* festive change freeze from 1 Nov (CAB approval by 31 Oct), gateway maintenance tonight, certificates to be renewed by 31 Oct, and the COO's festive-readiness ask.

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Ops alerts | Daily | 7:45 AM | The briefing prompt above |

> **➡ Story:** *"Certificates must be renewed by Friday, and one is already throwing warnings. Divya plans her day."*

---

## Ops 2 · 8:30 · Plan My Day + Prompt Coach · PRIORITIZE
*Extends Demo 2 · MS-4019: Prompt Coach, benefits of agents*

| | |
|---|---|
| **Overview** | Plan My Day builds the shift plan and **re-plans when an incident lands**. Prompt Coach improves the prompt first. |
| **Business scenario** | Stand-up, handover review, MBR preparation, CAB approvals and the Fabrikam service call at 16:00. At 9:10 a **Sev1 hits the Payments Gateway for Fabrikam Retail**. |
| **Pain points** | Firefighting replaces planned work · the MBR is prepared late at night · approvals missed before the freeze |
| **Business benefits** | Planned work protected · incident time absorbed without chaos · deadlines kept |
| **Learning objectives** | Improve a prompt with Prompt Coach · plan and re-plan around an incident · schedule start-of-day and handover wrap prompts |
| **Environment setup** | Plan My Day · Prompt Coach · a real calendar |

### Demo walkthrough
1. **Prompt Coach:**
```
Improve this prompt for an Operations Manager using Goal, Context, Source and Expectations: "plan my shift"
```
2. **Plan My Day:**
```
Goal: Create a realistic plan for my day in operations.
Context: I'm an Operations Manager. Today: stand-up at 8:30, review the night handover, get pending changes approved before the change freeze, prepare tomorrow's Weekly Ops MBR, and a client service call at 16:00.
Source: My calendar, recent email and Teams messages, and tasks.
Expectations: Table: Time | Activity | Priority | Why now. Then my top 3 outcomes and what I can delegate to shift leads.
```
3. **Plot twist:**
```
A Sev1 just hit our Payments Gateway for our biggest retail client. I need about 2 hours on incident command. Re-plan my day, protect my top 3 outcomes, and tell me what to delegate.
```

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Start my day | Daily | 8:30 AM | The plan prompt from step 2 |
| Handover wrap | Daily | 6:00 PM | `Wrap my day as a shift handover: incidents handled, what is still open, decisions I owe, overdue actions, and tomorrow's top 3 priorities.` |

> **➡ Story:** *"The gateway certificate on the secondary node has expired. Divya needs the right expert, now."*

---

## Ops 2A ✚ · 9:15 · SME Finder · MOBILIZE
*New for Operations · MS-4019: prebuilt and template agents*

| | |
|---|---|
| **Overview** | An agent template that finds **subject-matter experts** using people and organisation data: profiles, roles and the work people have done. |
| **Business scenario** | The incident bridge needs someone who knows gateway certificates **and** someone who can automate expiry alerts so it never happens again. |
| **Pain points** | 30+ minutes spent asking around during an outage · the same few people always pulled in · knowledge locked in individuals |
| **Business benefits** | Faster mean time to engage the right expert · less dependency on heroes · better use of org knowledge |
| **Learning objectives** | Use a template agent grounded in people data · ask for experts with evidence · understand permission-trimmed results |
| **Environment setup** | SME Finder template enabled · people/profile data in the tenant · *if unavailable:* attach `Ops_Expert_Directory.xlsx` in Copilot Chat or build it with `Operations/Agent-Instructions/SME-Finder_Instructions.md` |

### Demo walkthrough
1. Add and open **SME Finder**.
2. Run:
```
Find 3 people in my organisation with hands-on expertise in payment gateway TLS certificates and certificate-expiry automation. For each: name, team, why they're relevant (recent work or documents), and how to reach them. Rank by relevance to an active Sev1.
```
3. Follow-up:
```
Draft a short Teams message inviting the top 2 to the incident bridge now, with the incident summary in 2 lines.
```
*Expected (with the directory file):* **Ravi Menon** (Payments Platform, gateway certificates) and **Sneha Kulkarni** (Security Engineering, certificate-expiry automation).

**Teaching moment:** *In an incident, minutes matter. Finding the right person is often the slowest step.*

> **➡ Story:** *"The gateway is back by 10:40. Rakesh will ask tomorrow: is this a one-off, or a pattern?"*

---

## Ops 3 · 11:00 · Analyst · DIAGNOSE
*Extends Demo 3 · MS-4019: Analyst agent*

| | |
|---|---|
| **Overview** | Analyst reasons over the ops workbook, runs Python and shows its work. |
| **Business scenario** | Divya needs to know **what's driving** the SLA breach increase before the MBR. |
| **Pain points** | Thousands of ticket rows · Pareto and trend analysis take hours · gut feel instead of evidence |
| **Business benefits** | Root-cause signals in minutes · a defensible story for leadership · charts ready for the MBR |
| **Learning objectives** | Analyse operational data in natural language · build a Pareto · validate the reasoning |
| **Environment setup** | Analyst · `Contoso_Weekly_Ops_Review.xlsx` in OneDrive |

### Demo walkthrough
1. Open **Analyst** and attach `Contoso_Weekly_Ops_Review.xlsx`.
2. Trend:
```
Using Incidents_Raw, compare the current week with the prior week: incident volume, response and resolution SLA breach rates, Sev1 count, downtime and revenue at risk. Show a table with the week-over-week change.
```
3. Drivers:
```
Which issue clusters and which shift drive the resolution SLA breaches this week? Show a Pareto chart and the top 3 drivers with evidence.
```
4. Expand the **reasoning / code** panel.

*Expected:* incidents 95 → 120 · resolution breach rate 8.4% → 20.8% · **Certificate / config change failures** 4 → 19 incidents with 11 resolution misses · night shift 36% breach rate vs 14% for day shift.

> **➡ Story:** *"It's a pattern: certificate and config changes, made worse by a short-staffed night shift. With the freeze two days away, Divya needs a prevention plan, and Fabrikam needs an update."*

---

## Ops 4 · 12:30 · Researcher + Writing Coach · PREVENT
*Extends Demo 4 · MS-4019: Researcher, Writing Coach*

| | |
|---|---|
| **Overview** | Researcher builds a cited prevention plan from internal and external sources. Writing Coach shapes the client update. |
| **Business scenario** | Divya must propose how to stop certificate and config failures before the festive peak, and send Fabrikam a clear Sev1 update. |
| **Pain points** | Prevention ideas without evidence · RCA reports late · client communication that's too technical |
| **Business benefits** | An evidence-based plan in about 15 minutes · trust kept with key clients · faster RCA closure |
| **Learning objectives** | Run a cited research report · adapt tone for an external audience with Writing Coach |
| **Environment setup** | Researcher · Writing Coach · ops files accessible · web grounding allowed |

### Demo walkthrough
1. **Researcher:**
```
Goal: Recommend how to prevent certificate and configuration-change incidents on our payments gateway before a festive-season change freeze.
Context: Certificate/config change failures went from 4 to 19 incidents in a week, with 11 resolution SLA misses. The night shift is short-staffed and RCA tagging has dropped to 82.5%.
Source: Our ops workbook, runbook and handover notes, plus credible external guidance on certificate lifecycle management and change management.
Expectations: 1 page: 3 preventive actions (effort, impact, owner), what to do before the freeze, and how to measure success. Cite sources.
```
2. **Writing Coach:**
```
Rewrite this as an update to our retail client after a Sev1 on the payments gateway. Calm, clear, non-technical, under 120 words: what happened, impact, what we fixed, what we're doing to prevent recurrence, and when they'll get the full RCA. [paste notes]
```

> **➡ Story:** *"Prevention is planned. But the certificate warning sat in the night handover for hours. Divya decides no handover item will ever slip again."*

---

## Ops 5 · 14:00 · Ops Shift Delta (Project Delta Digest template) · HANDOVER
*Extends Demo 5 · MS-4019: Create an agent in Copilot Chat, components, test and edit*

| | |
|---|---|
| **Overview** | The Project Delta Digest template, tailored for operations: **what changed since the last shift** (new Sev1/Sev2, SLA breaches, open items, overdue actions). |
| **Business scenario** | Handovers are manual notes. The certificate warning (ACT-101) and night-shift staffing (ACT-104) were both overdue and nobody flagged them. |
| **Pain points** | Inconsistent handovers · overdue actions invisible · incoming shift starts blind |
| **Business benefits** | A consistent handover in 2 minutes · overdue actions flagged automatically · fewer repeat incidents |
| **Learning objectives** | Re-purpose a template for a new role · edit instructions and knowledge · test with edge cases · schedule at handover times |
| **Environment setup** | Agent Builder · Project Delta Digest template (or `Operations/Agent-Instructions/Ops-Shift-Delta_Instructions.md`) · Service Operations site with `Shift_Handover_28Oct_Night.docx` and `Contoso_Weekly_Ops_Review.xlsx` |

### Demo walkthrough: build
1. **New agent** → template gallery → **Project Delta Digest**.
2. **Describe:**
```
Tailor this agent for a 24x7 service operations centre. Instead of project items, report incidents, SLA breaches, handover notes and action items. Group by service and include owners.
```
3. **Configure:** name `Ops Shift Delta` · add to instructions: `Flag any action past its due date as OVERDUE and any open Sev1/Sev2 at the top. Never invent incidents or figures.` · knowledge: the **Service Operations** site · starter prompts: *Shift handover* · *Overdue actions* · *Open Sev1/Sev2*.

### Demo walkthrough: test and edit
4. Handover test:
```
Give me the shift handover: TL;DR, new Sev1/Sev2 incidents, open items by service with owner, SLA breaches, and overdue actions. Cite sources.
```
*Expected:* open Sev2 on Partner API (INC-4301), certificate warning on the secondary node (INC-4302), **OVERDUE: ACT-101 and ACT-104**.
5. Edge case: `What is the headcount cost of the night shift?` → should say it's not in the sources.

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Shift delta (morning) | Daily | 7:30 AM | The handover prompt from step 4 |
| Shift delta (afternoon) | Daily | 3:30 PM | The handover prompt from step 4 |

> **➡ Story:** *"Daily handovers are covered. Now the biggest weekly job: the MBR pack Rakesh expects tomorrow."*

---

## Ops 5A ✚ · 15:00 · Weekly Ops MBR · REPORT
*New for Operations · MS-4019: components of an agent, knowledge sources, test and edit*

| | |
|---|---|
| **Overview** | A declarative agent that creates an **executive-ready weekly operations review** from one Excel workbook: KPIs with week-over-week deltas, SLA breaches, top issue clusters, aging backlog, leadership talking points and actions. |
| **Business scenario** | Divya normally spends 3–4 hours every Thursday night building the MBR pack. Tomorrow's pack has to explain a bad week clearly. |
| **Pain points** | Manual KPI and SLA calculations · inconsistent formats week to week · insights missed under time pressure |
| **Business benefits** | MBR pack prepared in minutes · consistent, comparable reporting · leadership sees risks and asks clearly |
| **Learning objectives** | Build an agent with **structured instructions** (rules, steps, output formats, self-check) · ground it on a single workbook · test for accuracy and **guardrails** · schedule a weekly pack |
| **Environment setup** | Agent Builder · `Contoso_Weekly_Ops_Review.xlsx` on the Service Operations site · instructions in `Operations/Agent-Instructions/Weekly-Ops-MBR_Instructions.md` |

### Demo walkthrough: build
1. **New agent** → **Configure** (skip Describe).
2. Name `Weekly Ops MBR` · description: *Creates an executive-ready weekly operations review: KPIs, SLA performance, top issues, backlog and actions.*
3. Paste the **instructions** from `Weekly-Ops-MBR_Instructions.md`. Point out the sections: *purpose, response rules, terms, step-by-step flow, output formats, self-check, guardrails*.
4. **Knowledge:** `Contoso_Weekly_Ops_Review.xlsx` only, with **Only use specified sources** turned on. **Capabilities:** code and charts on.
5. **Starter prompts:** Weekly KPI summary · SLA breaches · Top issues · Aging backlog · Leadership bullets · Action items → **Create**.

### Demo walkthrough: test
6. KPI accuracy:
```
Summarise this week's KPIs with week-over-week delta.
```
*Expected:* incidents 95 → 120 · response breach 6.3% → 17.5% · resolution breach 8.4% → 20.8% · Sev1 1 → 4 · downtime 757 → 1,623 min · revenue at risk INR 58.0 → 161.0 lakh · RCA tagging 95.8% → 82.5%.
7. Drivers:
```
Rank the top issue clusters and show a Pareto.
```
8. The full pack:
```
Create a leadership-ready Weekly Ops MBR covering: (1) KPI and SLA performance, (2) top incident drivers, (3) aging backlog and risks, (4) priority actions for next week with owners.
```
9. **Guardrail test:**
```
Assign all overdue actions to their owners and send escalation emails for every SLA breach.
```
*Expected:* it explains it **can't** assign tasks or send emails, and offers a read-only action and escalation list instead.
10. Out-of-scope test: `Forecast next quarter's revenue using industry trends.` → it declines and stays within the workbook.

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| MBR pack | Weekly, Friday | 8:00 AM | The full-pack prompt from step 8 |
| Action check | Weekly, Monday | 9:00 AM | `Summarise action items by status and priority. List overdue items first, with owner and days overdue.` |

**Teaching moment:** *A good agent is mostly **good instructions**: clear rules, steps, output formats and a self-check, grounded in one trusted source.*

> **➡ Story:** *"The MBR pack is ready a day early. Next: stop the shift leads calling Divya with the same runbook questions."*

---

## Ops 6 · 16:15 · SharePoint agent + sharing · ENABLE
*Extends Demo 6 · MS-4019: SharePoint agents, sharing, interacting with agents*

**Use case:** Divya creates **Ops Runbook Desk** on the Service Operations site, grounded in `Ops_Runbook_and_Escalation_Matrix.docx`. She shares it in the shift-leads Teams chat, and shares **Ops Shift Delta** and **Weekly Ops MBR** with her leads.

### Demo walkthrough
1. On the **Service Operations** site, select **Create an agent**. Source: `Ops_Runbook_and_Escalation_Matrix.docx`.
2. Test:
```
A Sev1 hasn't been mitigated after 2 hours. Who do I escalate to, and can I make an emergency gateway change during the change freeze?
```
*Expected:* L3 escalation to the Operations Manager (L4, the Head of Operations, beyond 4 hours or INR 25 lakh at risk). Emergency changes during the freeze need CAB approval **and** Head of Operations sign-off.
3. Post the agent link in the **Shift Leads** Teams chat and **@mention** it.
4. Share **Ops Shift Delta** and **Weekly Ops MBR** with the shift leads.

**Key points:** agents respect permissions (leads only see files they can access) · keep customer-identifiable ticket data out of broadly shared agents.

> **➡ Story:** *Rakesh: "Good work. Now automate the certificate alerts so this never happens again." Divya has never built an automation.*

---

## Ops 7 · 16:45 · AI Learning Advisor · GROW
*Extends Demo 7 · MS-4019: who can create agents (business user to maker)*

| | |
|---|---|
| **Overview** | A personalised learning path from Microsoft Learn, focused on **automating operations**. |
| **Business scenario** | Divya wants to automate certificate-expiry alerts and incident summaries, but doesn't know where to start. |
| **Pain points** | Automation feels like an IT-only skill · no time to explore · unclear which tool to use |
| **Business benefits** | A clear path from agent user to maker · less dependency on IT for simple automations |
| **Learning objectives** | Build a role-specific learning plan · compare automation options · schedule a weekly check-in |
| **Environment setup** | AI Learning Advisor (or `Agent-Instructions/AI-Learning-Advisor_Instructions.md`) |

### Demo walkthrough
```
Goal: Help me learn to automate operational alerts and reports with Microsoft tools.
Context: I'm an Operations Manager. I use Copilot and agents daily. I want to automate certificate-expiry alerts, daily incident summaries and escalation reminders. I have 3 hours a week for 4 weeks.
Source: Microsoft Learn.
Expectations: Table: Week | Skill | Learning (link) | Hands-on with my ops data | How I'll know I've learned it.
```
**Follow-up:**
```
When should I use a scheduled prompt, a Power Automate flow, or a Copilot Studio agent for operations alerts? Give me a comparison table.
```

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Learning check-in | Weekly, Monday | 4:00 PM | `I'm an Operations Manager learning to automate operations. Give me this week's one skill, a 20-minute Microsoft Learn activity with a link, and one question on last week's topic.` |

> **➡ Story:** *"It's 5:30. Let's look at what Divya's operation looks like tomorrow."*

---

## Ops 8 · 17:30 · Handover wrap · SUSTAIN
*Extends Demo 8 · MS-4019: governance, interacting with agents, review*

### Demo walkthrough
1. **Plan My Day:**
```
Wrap my day as a shift handover: incidents handled, what is still open, decisions I owe, overdue actions, and tomorrow's top 3 priorities.
```
2. Show Divya's **operational rhythm**, now scheduled:

| Time | Agent | Scheduled prompt | Frequency |
|---|---|---|---|
| 7:30 | Ops Shift Delta | Shift delta (morning) | Daily |
| 7:45 | Personal News Digest | Ops alerts | Daily |
| 8:30 | Plan My Day | Start my day | Daily |
| 15:30 | Ops Shift Delta | Shift delta (afternoon) | Daily |
| 18:00 | Plan My Day | Handover wrap | Daily |
| Fri 8:00 | Weekly Ops MBR | MBR pack | Weekly |
| Mon 9:00 | Weekly Ops MBR | Action check | Weekly |
| Mon 16:00 | AI Learning Advisor | Learning check-in | Weekly |

> *"Every rhythm of the operation (handover, stand-up, weekly review) now has an agent scheduled into it."*

3. **Governance for operations:**
   - Agents only see data the user can access.
   - Declarative agents **report and recommend; they don't act**, as the guardrail test showed.
   - Keep customer-identifiable ticket data in properly permissioned sites.
   - Review schedules monthly.

### 🔁 Your turn: Schedule 3
Pick 3 from the Ops prompt pack below (at least 2 daily), personalise them, run each once and **schedule** it.

### Epilogue: Friday morning
> *7:30. The shift delta is waiting: overnight was quiet, ACT-101 is closed. 7:45: the freeze starts Monday. 8:00: the MBR pack is ready, with the certificate cluster as the headline and the night-shift ask for Rakesh. Divya walks into the review prepared. **Her agents ran the rhythm for her.***

---

## Ops prompt pack: scheduled prompts
| # | Agent | Name | When | Prompt |
|---|---|---|---|---|
| OD1 | Ops Shift Delta | Shift delta | Daily 7:30 & 15:30 | `Shift handover for [operation]: TL;DR, new Sev1/Sev2, open items by service with owner, SLA breaches, and overdue actions since the last shift. Cite sources.` |
| OD2 | Personal News Digest | Ops alerts | Daily 7:45 | `I'm an Operations Manager for [operation]. Top 5 announcements from the last 24 hours that affect my operation: Priority – Headline – Operational impact – Action & deadline.` |
| OD3 | Plan My Day | Start my day | Daily 8:30 | `Plan my day around my calendar, open incidents, approvals and tasks: Time – Activity – Priority – Why now. Top 3 outcomes and what to delegate to shift leads.` |
| OD4 | Plan My Day | Handover wrap | Daily 18:00 | `Wrap my day as a shift handover: incidents handled, still open, decisions I owe, overdue actions, tomorrow's top 3.` |
| OW1 | Weekly Ops MBR | MBR pack | Fri 8:00 | `Create a leadership-ready Weekly Ops MBR: KPI and SLA performance with week-over-week delta, top incident drivers, aging backlog and risks, and priority actions with owners.` |
| OW2 | Weekly Ops MBR | Action check | Mon 9:00 | `Summarise action items by status and priority. Overdue first, with owner and days overdue.` |
| OW3 | AI Learning Advisor | Learning check-in | Mon 16:00 | `I'm an Operations Manager learning to automate operations. This week's one skill, a 20-minute Microsoft Learn activity with a link, and one question on last week's topic.` |

**Suggested picks:** Operations managers: OD1 + OD3 + OW1 · Shift leads: OD1 + OD2 + OD4 · Ops analysts: OD1 + OW1 + OW2

*Contoso, its clients and every person named here are fictitious.*
