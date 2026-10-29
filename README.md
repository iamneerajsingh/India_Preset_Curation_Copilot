# MS-4019 · A Day with Project Nexus
### Agentic demo guide: one employee, one day, every agent scheduled

| | |
|---|---|
| **Course** | MS-4019: Transform your everyday business processes with agents |
| **Featured agents** | Personal News Digest · Plan My Day · Project Delta Digest · AI Learning Advisor |
| **Supporting agents** | Prompt Coach · Analyst · Researcher · Writing Coach · SharePoint agent |
| **Key message** | Don't just *try* an agent. **Schedule it**, so it's waiting for you every day. |

---

## The story
**Arjun Mehta** is a Program Manager at **Contoso India**. He leads **Project Nexus**, the company's rollout of Microsoft 365 Copilot and agents to 2,000 employees. He has 9 meetings a day, about 200 messages and six workstream leads to chase.

Today his VP, **Priya Nair**, needs answers: *Where does Nexus stand? Why is Finance adoption falling? What do we do next?*

Arjun starts the day overwhelmed. One problem at a time, he hands the work to an agent, and after each one he **schedules** it. By evening his agents have helped him **understand, prioritise, investigate, recommend, execute, scale and grow**. Tomorrow morning, they're already waiting for him.

## Story flow
| Time | Arjun's question | Demo | Agent | MS-4019 topic | Scheduled prompt |
|---|---|---|---|---|---|
| 8:30 | *What changed that matters to me?* | 1 | **Personal News Digest** | What are agents | Morning briefing: daily 8:30 |
| 9:00 | *What matters today?* | 2 | **Plan My Day** + Prompt Coach | Prompt Coach, benefits of agents | Start my day: daily 9:00 · Wrap my day: daily 18:00 |
| 11:00 | *Why is Finance adoption dropping?* | 3 | Analyst | Analyst agent | n/a |
| 12:00 | *What should we do about it?* | 4 | Researcher + Writing Coach | Researcher, coach agents | n/a |
| 14:00 | *How do I never miss a blocker again?* | 5 | **Project Delta Digest** (Agent Builder) | Build, test, edit an agent | Daily project delta: daily 10:00 · Leadership recap: Fri 16:00 |
| 15:30 | *How does my team serve themselves?* | 6 | SharePoint agent + sharing | SharePoint agents, sharing | n/a |
| 16:30 | *What do I need to learn next?* | 7 | **AI Learning Advisor** | Who can create agents | Learning check-in: Mon 16:00 |
| 17:30 | *What's ready for tomorrow?* | 8 | Plan My Day + all schedules | Governance, review | Learners schedule 3 |

---

## Before you start
- [ ] Microsoft 365 Copilot licence, with the **Agents** experience enabled
- [ ] Agents available: **Personal News Digest, Plan My Day, Project Delta Digest, AI Learning Advisor**, Prompt Coach, Analyst, Researcher, Writing Coach
- [ ] Agent Builder and SharePoint agents allowed; web grounding allowed
- [ ] **Scheduled prompts** tested in your environment
- [ ] A SharePoint site called **Project Nexus** with the files from `Sample-Data/Project-Nexus` uploaded
- [ ] `Learner-Copy-Paste-Prompts.txt` posted in the class Teams chat

> If a template isn't available in your environment, build it in Agent Builder using the matching file in `Agent-Instructions/`.

## How to schedule a prompt
1. Run the prompt once and check the result.
2. Hover over **your prompt** → **⋯ More options** → **Schedule this prompt**.
3. Set the **name, frequency and time** → **Save**. The result arrives in Copilot at that time.
4. Edit, pause or delete schedules from the **Scheduled prompts** list.

> **Good scheduled prompts stand alone:** they state the role, the project and the timeframe ("last 24 hours"), and ask for a fixed format that can be read in 2 minutes.

---

## Demo 1 · 8:30 · Personal News Digest · UNDERSTAND
*MS-4019: What are agents (prebuilt, template and custom agents), and who can use them*

| | |
|---|---|
| **Overview** | An agent template grounded in your email, Teams and SharePoint. It turns company-wide announcements into a short digest of what matters to **your** role. |
| **Business scenario** | Arjun opens his laptop to a CEO note on AI, a policy deadline, an outage notice and dozens of newsletters. Two of them matter for today. |
| **Pain points** | Important updates get lost in the noise · required actions are missed · 30–45 minutes a day spent scanning |
| **Business benefits** | A 3-minute read instead of a 30-minute scan · no missed deadlines · faster alignment with leadership |
| **Learning objectives** | Explain prebuilt vs template vs custom agents · add an agent from a template · schedule a daily briefing |
| **Environment setup** | Personal News Digest available in the Agent Store or template gallery · announcements in your mailbox (or paste `Nexus_Sample_Announcements.md`) |

### Demo walkthrough
1. In Copilot Chat, go to **Agents → Get agents**, search for **Personal News Digest** and select **Add**.
2. Point out the conversation starters: *"It's a template. Microsoft wrote the instructions, so you just use it."*
3. Run the briefing prompt:
```
Goal: Give me a morning briefing of what changed that matters to my work.
Context: I'm a Program Manager leading our Microsoft 365 Copilot and agents rollout (Project Nexus).
Source: Company-wide announcements from my email, Teams and SharePoint news in the last 24 hours.
Expectations: Top 5 only, as a table: Priority (Critical/Important/FYI) | Headline | Why it matters to me | Action & deadline.
```
4. Ask the follow-up:
```
Which one item should I raise with my VP today, and why?
```
*Expected:* the CEO's message asking every team to adopt agent workflows, plus the notice that new agent templates are live for everyone **except Finance**.

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Morning briefing | Daily | 8:30 AM | The briefing prompt above |

**Teaching moment:** *Search asks "what happened?" This agent asks "what happened **that matters to me**?"*

> **➡ Story:** *"Finance is falling behind, and the CEO is watching. But Arjun's calendar is already full. What actually matters today?"*


---

## Demo 2 · 9:00 · Plan My Day + Prompt Coach · PRIORITIZE
*MS-4019: Prompt Coach agent, and the benefits of using agents*

| | |
|---|---|
| **Overview** | Plan My Day combines meetings, email, Teams and tasks into one time-blocked plan, and **re-plans** when things change. Prompt Coach improves the prompt before it's scheduled. |
| **Business scenario** | 9 meetings, a status report to prepare, a stuck workstream, and 30 minutes of learning to protect. Then Priya asks for a Finance deep-dive **today**. |
| **Pain points** | No single view of the day · urgent work pushes out important work · re-planning by hand after every interruption |
| **Business benefits** | ~20 minutes saved every day · focus time protected · a clear start and end to every day |
| **Learning objectives** | Improve a prompt with Prompt Coach · plan and re-plan with an agent · schedule start-of-day and end-of-day prompts |
| **Environment setup** | Plan My Day and Prompt Coach available · a real calendar with meetings today |

### Demo walkthrough
1. Open **Prompt Coach** and improve Arjun's first attempt:
```
Improve this prompt for a Program Manager using Goal, Context, Source and Expectations: "plan my day"
```
2. Open **Plan My Day** and run the improved prompt:
```
Goal: Create a realistic, focused plan for today.
Context: I'm a Program Manager. Today I must update leadership on Project Nexus, unblock a delayed workstream, attend my meetings, and keep 30 minutes for learning.
Source: My calendar, recent email and Teams messages, and tasks.
Expectations: Table: Time | Activity | Priority | Why now. Then my top 3 outcomes and what I can postpone.
```
3. **Plot twist:** a message arrives from Priya.
```
My VP needs a deep-dive on falling Finance adoption today, with a recommendation. Re-plan my day, protect my top 3 outcomes, and tell me what to decline or delegate.
```

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Start my day | Daily | 9:00 AM | The plan prompt from step 2 |
| Wrap my day | Daily | 6:00 PM | `Wrap my day: what I completed, what slipped, decisions I owe, and tomorrow's top 3 priorities.` |

**Teaching moment:** *Making a plan is useful. **Re-planning when things change** is where an agent earns its place.*

> **➡ Story:** *"The deep-dive is now at 11:00. Arjun has the adoption data, but no time to analyse it."*


---

## Demo 3 · 11:00 · Analyst · INVESTIGATE
*MS-4019: Analyst agent*

| | |
|---|---|
| **Overview** | Analyst reasons step by step over your data files and runs Python, and you can see and check its code. |
| **Business scenario** | Arjun needs to show Priya **why** Finance adoption is falling, with evidence. |
| **Pain points** | No analyst available · pivots and charts take hours · hard to tell a trend from noise |
| **Business benefits** | Data-backed answers in minutes · transparent, checkable reasoning · charts ready for leadership |
| **Learning objectives** | Analyse a file with natural language · review Analyst's reasoning and code · turn findings into an insight |
| **Environment setup** | Analyst available · `Nexus_Adoption_Data.xlsx` saved to OneDrive |

### Demo walkthrough
1. Open **Analyst** and attach `Nexus_Adoption_Data.xlsx`.
2. Find the trend:
```
Show weekly active users by business unit over the last 8 weeks as a line chart. Which business unit is declining, since when, and by how much?
```
3. Find the cause:
```
For that business unit, compare training completion, survey sentiment and the pulse survey comments with the others. What are the 3 most likely reasons for the decline? Show the evidence.
```
4. Expand the **reasoning / code** panel: *"You can check its work."*

*Expected:* Finance weekly active users are down about 30% over 3 weeks. Training completion is stuck at 26%, and survey comments say "no role-relevant use cases" and "not trained on agents."

**Teaching moment:** *Ask questions of data the way you'd ask a colleague, and check the working.*

> **➡ Story:** *"Now Arjun knows **why**. Priya will ask **what we should do about it**."*


---

## Demo 4 · 12:00 · Researcher + Writing Coach · RECOMMEND
*MS-4019: Researcher agent, Writing Coach agent*

| | |
|---|---|
| **Overview** | Researcher does multi-step research across your work data and the web and returns a cited report. Writing Coach turns it into a clear executive message. |
| **Business scenario** | Arjun needs a recommendation for recovering Finance adoption, backed by internal context and proven practice, sent to Priya before lunch ends. |
| **Pain points** | Research spread across mail, files and the web · recommendations without evidence · long, unclear leadership emails |
| **Business benefits** | A sourced recommendation in about 15 minutes · better decisions · crisp communication with leadership |
| **Learning objectives** | Run a cited research report · choose between Copilot Chat and Researcher · refine a message with Writing Coach |
| **Environment setup** | Researcher and Writing Coach available · Project Nexus files accessible · web grounding allowed |

### Demo walkthrough
1. Open **Researcher** and run the prompt. Point out its clarifying questions and research plan.
```
Goal: Recommend how to recover Copilot agent adoption in our Finance business unit within 60 days.
Context: Finance weekly active users fell ~30% in 3 weeks. Training completion is 26% and users see no role-relevant use cases.
Source: My email, meetings and Project Nexus files, plus credible external adoption guidance.
Expectations: 1 page: 3 options (effort, impact, risk), a recommendation, a 30-day plan. Cite sources.
```
2. Review the **citations** in the report.
3. Open **Writing Coach**:
```
Rewrite this as a note to my VP, under 100 words, confident and clear, with one ask: [paste the recommendation]
```

*Expected recommendation:* role-based Finance workshops, Finance champions, and every attendee leaving with scheduled prompts.

**Teaching moment:** *Copilot Chat for a quick answer · **Researcher** for depth and citations · **Coaches** for better thinking and writing.*

> **➡ Story:** *Priya replies: "Approved. But why did I hear about the Finance blockers three weeks late?" Arjun decides he'll never chase status again.*


---

## Demo 5 · 14:00 · Project Delta Digest · EXECUTE
*MS-4019: Tools to create agents, components of an agent, creating an agent in Copilot Chat (Describe and Configure), testing and editing agents*

| | |
|---|---|
| **Overview** | An agent template that produces a daily or weekly digest of **what changed** on a project: completed, in progress, blockers and risks, each with a source. |
| **Business scenario** | Arjun spends 2 hours every Friday chasing six leads for status. The Finance workshop blocker sat unnoticed for 8 days. |
| **Pain points** | Manual status reporting · risks found too late · a different report format every week |
| **Business benefits** | Status work cut from 2 hours to 10 minutes · blockers flagged with owner and days stuck · a consistent leadership format |
| **Learning objectives** | Create an agent from a template · identify and edit its components · test and edit an agent · schedule a digest |
| **Environment setup** | Agent Builder available · Project Delta Digest template (or `Agent-Instructions/Project-Delta-Digest_Instructions.md`) · Project Nexus SharePoint site with the sample files |

### Demo walkthrough: build
1. In Copilot Chat, select **New agent**, open the template gallery and choose **Project Delta Digest**.
2. On the **Describe** tab:
```
Tailor this agent for Project Nexus. Group the digest by workstream and include owner names.
```
3. On the **Configure** tab, walk through the **components of an agent**:
   - **Name:** `Nexus Delta Digest`
   - **Description:** short and precise
   - **Instructions:** add `Flag items with no update for 5 or more working days as STALE. Never invent figures.`
   - **Knowledge:** the Project Nexus SharePoint site
   - **Starter prompts:** Daily digest · Blockers · Leadership recap
4. Select **Create**.

### Demo walkthrough: test and edit
5. Test for accuracy:
```
Give me today's Project Nexus digest: TL;DR, completed, in progress, blockers (owner, days stuck) and risks. Cite sources.
```
*Expected:* two **Blocked** Finance items (workshops, template enablement) marked STALE with their owners.
6. Test an edge case:
```
What is the budget variance for the Sales workstream?
```
*Expected:* "Not found in sources." If it guesses, tighten the instructions, update the agent and test again.
7. Test the leadership format:
```
Give me a one-page leadership digest for Project Nexus: TL;DR, milestones, top 3 risks, and the one decision I need.
```

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Daily project delta | Daily | 10:00 AM | The digest prompt from step 5 |
| Leadership recap | Weekly, Friday | 4:00 PM | The leadership prompt from step 7 |

**Teaching moment:** *Start from a template, tailor it, test it, **schedule** it. That's how business users build agents.*

> **➡ Story:** *"With the plan approved, Arjun's team is flooded with questions: How do I get a licence? Who is my champion?"*


---

## Demo 6 · 15:30 · SharePoint agent + sharing · SCALE
*MS-4019: Creating an agent in SharePoint, managing agents, sharing agents, sharing in Teams, interacting with agents*

**Use case:** Arjun creates a **Nexus Help Desk** agent on the project site so the team can answer their own questions. He also shares his Delta Digest with the workstream leads.

### Demo walkthrough
1. On the **Project Nexus** SharePoint site, select **Create an agent**. Name it `Nexus Help Desk`, with sources `Nexus_Team_FAQ.docx` and `Nexus_Rollout_Plan.docx`.
2. Test it:
```
How do I get a Copilot licence, and who is the Finance champion?
```
3. Copy the agent link, post it in the **Nexus Teams chat** and **@mention** the agent.
4. Share **Nexus Delta Digest** with specific users (the workstream leads).

**Key points:** shared agents **respect permissions**, so sharing an agent doesn't share its files · a site owner can set the site's **default agent** · your chats with agents are private to you.

> **➡ Story:** *Priya: "Great. You'll run the Finance agent workshops yourself next week." Arjun knows Copilot, but can he teach agents?*


---

## Demo 7 · 16:30 · AI Learning Advisor · GROW
*MS-4019: Who can create and use agents (from business user to maker)*

| | |
|---|---|
| **Overview** | An agent template grounded in **Microsoft Learn**. It gives personalised learning plans and trusted answers with links. |
| **Business scenario** | Arjun has to teach Finance users about agents next week. His gaps are knowledge sources, Agent Builder vs Copilot Studio, and governance. |
| **Pain points** | Too many resources and no clear path · no time to learn · the same questions sent to experts again and again |
| **Business benefits** | A focused learning plan in minutes · trusted answers with sources · continuous skill growth |
| **Learning objectives** | Build a personalised learning plan · use an adaptive knowledge check · schedule a weekly learning check-in |
| **Environment setup** | AI Learning Advisor available (or `Agent-Instructions/AI-Learning-Advisor_Instructions.md`) · web grounding allowed |

### Demo walkthrough
1. Add and open **AI Learning Advisor**.
2. Build the plan:
```
Goal: Make me confident explaining Microsoft 365 Copilot agents to finance professionals.
Context: I'm comfortable with Copilot and prompting. My gaps: knowledge sources, Agent Builder vs Copilot Studio, sharing and governance. I have 3 hours a week for 4 weeks.
Source: Microsoft Learn.
Expectations: Table: Week | Skill | Learning (link) | Hands-on | How I'll know I've learned it.
```
3. Make it adaptive:
```
Quiz me with 3 questions, one at a time, then adjust my plan.
```
4. Answer the question every audience asks:
```
What's the difference between Agent Builder and Copilot Studio, and which should a finance user start with?
```

### 🔁 Schedule it
| Name | Frequency | Time | Prompt |
|---|---|---|---|
| Learning check-in | Weekly, Monday | 4:00 PM | `I'm a Program Manager learning Copilot agents. Give me this week's one skill, a 20-minute Microsoft Learn activity with a link, and one question on last week's topic.` |

**Teaching moment:** *Content discovery gives you a list. **Personalised learning** gives you a path, and the schedule keeps you on it.*

> **➡ Story:** *"It's 5:30. Arjun's day started with 200 unread items and no plan. Let's see what he's set up for tomorrow."*


---

## Demo 8 · 17:30 · Wrap my day · SUSTAIN
*MS-4019: IT governance for agents, interacting with agents, learning path review*

### Demo walkthrough
1. In **Plan My Day**, run Arjun's end-of-day prompt:
```
Wrap my day: what I completed, what slipped, decisions I owe, and tomorrow's top 3 priorities.
```
2. Open the **Scheduled prompts** list and show Arjun's agentic day:

| Time | Agent | Scheduled prompt | Frequency |
|---|---|---|---|
| 8:30 | Personal News Digest | Morning briefing | Daily |
| 9:00 | Plan My Day | Start my day | Daily |
| 10:00 | Project Delta Digest | Daily project delta | Daily |
| 18:00 | Plan My Day | Wrap my day | Daily |
| Fri 16:00 | Project Delta Digest | Leadership recap | Weekly |
| Mon 16:00 | AI Learning Advisor | Learning check-in | Weekly |

> *"About five minutes of reading a day. Arjun no longer goes looking for information; it comes to him, every working day."*

3. **Governance check:**
   - Agents and scheduled prompts only use data you can already access.
   - Sensitivity labels and data loss prevention still apply.
   - Pause schedules you don't read.
   - Your organisation controls which agents are available.

### 🔁 Your turn: Schedule 3
1. Pick **3 prompts** from the prompt pack below, at least **2 of them daily**.
2. Personalise them (role, project, priorities) and run each one once.
3. **Schedule** each one, then post **"✅ 3 scheduled"** in the class chat.

### Epilogue: the next morning
> *8:30. Arjun opens Copilot. His briefing is waiting. At 9:00 his day is planned. At 10:00 the Nexus digest shows Finance training is finally scheduled. He didn't ask for any of it. **The agents came to him.***
>
> *"Tomorrow at 8:30, yours will be waiting too."*


---

## Prompt pack: scheduled prompts
Replace the **[brackets]**, run each prompt once, then schedule it.

| # | Agent | Name | When | Prompt |
|---|---|---|---|---|
| D1 | Personal News Digest | Morning briefing | Daily 8:30 | `I'm a [role] working on [area]. Top 5 company-wide updates from the last 24 hours that matter to me: Priority – Headline – Why it matters – Action & deadline.` |
| D2 | Plan My Day | Start my day | Daily 9:00 | `Create a time-blocked plan for today from my calendar, email, Teams and tasks: Time – Activity – Priority – Why now. Then my top 3 outcomes and what I can postpone.` |
| D3 | Project Delta Digest | Daily project delta | Daily 10:00 | `Today's digest for [project]: TL;DR, completed, in progress, blockers (owner, days stuck), risks from the last 24 hours, with sources.` |
| D4 | Plan My Day | Wrap my day | Daily 18:00 | `Wrap my day: what I completed, what slipped, decisions I owe, and tomorrow's top 3 priorities.` |
| W1 | Project Delta Digest | Leadership recap | Fri 16:00 | `One-page leadership digest for [project]: TL;DR, milestones, top 3 risks, and the one decision I need.` |
| W2 | AI Learning Advisor | Learning check-in | Mon 16:00 | `I'm a [role] learning [topic]. Give me this week's one skill, a 20-minute Microsoft Learn activity with a link, and one question on last week's topic.` |

**Suggested picks:** Any employee: D1 + D2 + D4 · Project or delivery managers: D2 + D3 + W1 · People building skills: D1 + D2 + W2

---

## Content pack
```
MS-4019_Project-Nexus_Demo-Pack/
├── README.md                              ← this guide
├── Demos/                                 ← one file per demo
│   ├── Demo-1_0830_Personal-News-Digest.md
│   ├── Demo-2_0900_Plan-My-Day.md
│   ├── Demo-3_1100_Analyst.md
│   ├── Demo-4_1200_Researcher-Writing-Coach.md
│   ├── Demo-5_1400_Project-Delta-Digest.md
│   ├── Demo-6_1530_SharePoint-Agent.md
│   ├── Demo-7_1630_AI-Learning-Advisor.md
│   └── Demo-8_1730_Wrap-My-Day.md
├── Prompts/
│   ├── Learner-Copy-Paste-Prompts.txt     ← post in the class Teams chat
│   └── Scheduled-Prompts.csv
├── Sample-Data/
│   ├── Nexus_Sample_Announcements.md      ← Demo 1
│   └── Project-Nexus/                     ← upload to the Project Nexus SharePoint site
│       ├── Nexus_Adoption_Data.xlsx       ← Demo 3
│       ├── Nexus_Project_Tracker.xlsx     ← Demo 5
│       ├── Nexus_Weekly_Status_W43.docx   ← Demo 5
│       ├── Nexus_Team_FAQ.docx            ← Demo 6
│       └── Nexus_Rollout_Plan.docx        ← Demo 6
└── Agent-Instructions/                    ← build an agent if its template isn't available
```
*Contoso, Project Nexus and every person named in it are fictitious.*
