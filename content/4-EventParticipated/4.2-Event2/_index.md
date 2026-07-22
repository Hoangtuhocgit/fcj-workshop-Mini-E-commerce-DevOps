---
title: "Event 2"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: "FCAJ Community Day" (2nd edition)

### Event Information

| Item | Details |
| --- | --- |
| Event name | FCAJ Community Day (2nd edition) |
| Date & time | 09:00, May 23, 2026 |
| Location | Floors 26 & 36, Bitexco Tower, 02 Hai Trieu Street, Saigon Ward, Ho Chi Minh City |
| Role | Attendee |
| Number of sessions | 6 technical sessions + opening keynote |

### Event Objectives

FCAJ Community Day (2nd edition) continued connecting the First Cloud Journey community, focusing on **AI, Cloud, and real-world experience** from industry practitioners. Based on my attendance, the event pursued these objectives:

1. **Update AI and Cloud trends:** Help students understand AI's impact on the job market and software development demand.
2. **Share practical skills:** Convey experience using AI effectively — from context engineering, AWS architecture to enterprise system deployment.
3. **Learn from real projects:** Speakers demoed products, architectures, and lessons from hackathons and internal banking projects.
4. **Encourage community participation:** Create networking space for questions and knowledge sharing among FCAJ members.

### Speakers

| No. | Speaker | Role / Organization |
| --- | --- | --- |
| 1 | Nguyễn Gia Hưng | Solutions Architect AWS Vietnam, FCAJ Founder |
| 2 | Anh Tịnh (Trương) | Platform Engineer, GothamX |
| 3 | Hải Anh | Pacific Vietnam |
| 4 | Nguyễn Tuấn Thịnh | DevOps Cloud Engineer |
| 5 | UTM Morpho Team (Uyển, Thảo, Mai) | LA Hackathon Team |
| 6 | Đức Đào | Engineer (LLM inference sharing) |
| 7 | Cát Vy | AI/Enterprise Expert (VPBank) |

### Session Contents

#### Opening Keynote — AI Trends and Job Market (Nguyễn Gia Hưng)

The speaker opened with a perspective on **the AI paradox in the job market:** as software development costs decrease thanks to AI, demand and quantity of software increase — similar to how LED bulbs save electricity but total consumption rises because people use more lighting.

**Key content:**

- AI makes software development cheaper and more efficient → software product quantity will increase dramatically.
- Anthropic Hackathon winners included non-IT professionals (lawyers, doctors) — technical barriers are lowering.
- New career trend: **vibe software engineering** — roles fixing, maintaining, and completing products built by non-technical idea holders using AI.
- Encouraged students not to be discouraged by the job market but focus on building real problem-solving capabilities.

#### Session 1 — Context Engineering: The Secret to Getting AI Right (Anh Tịnh)

Platform Engineer at GothamX shared **how to provide the right context** for AI to be truly useful at work.

**Common problems:**

- Using one chat for all topics (travel, CV, code…) → AI switches context continuously, producing wrong results.
- Overly long prompts with internet-searchable information → wastes tokens, AI misses key points.

**Proposed solutions:**

1. **Provide unique context:** Share organization-specific knowledge — internal blueprints, banking processes, team conventions.
2. **Separate working sessions:** One session per task; summarize context when starting a new session.
3. **Confident sharing and questioning:** Communication skills matter as much as technical skills.
4. **Prioritize AI-proficient developers:** Hiring managers prefer developers who use AI tools effectively and save tokens.

#### Session 2 — Amazon Q and AI Agents for Business (Hải Anh)

Speaker from Pacific Vietnam presented **Amazon Q** — AWS's AI assistant for enterprise users.

**Problems addressed:**

- Managers and executives spend significant time aggregating data and files for weekly reports.
- Need for an integrated ecosystem (like Microsoft 365, Google Workspace) via one platform for custom agent building.

**Key features:**

| Feature | Description |
| --- | --- |
| BI Dashboard | Deep analysis from input data |
| Insights Chat | Direct chat with agent via integrated information |
| Automation Flow | Process automation (transcribe meeting → send follow-up email) |
| MCP Integration | Connect custom tools via Model Context Protocol |

**Agent concept:** LLM (brain) combined with executable functions/actions — different from text-only chatbots. Demo included meeting transcription, Excel-to-dashboard analysis, and MCP integration on AWS.

#### Session 3 — CloudFront Flat-Rate Pricing (Nguyễn Tuấn Thịnh)

The DevOps Engineer shared a **flat-rate CDN pricing/package concept** using CloudFront-related services as the discussion context. Because this appears to be event material rather than a publicly documented AWS pricing model, I treat it as a session takeaway, not an official CloudFront product announcement.

**Traditional pay-as-you-go problems:**

- CDN costs depend on traffic → hard to estimate monthly bills.
- DDoS or traffic spike risks can lead to bills of tens of thousands of USD.
- Enterprises hesitate to deploy CDN due to unpredictable costs.

**Flat-rate package concept discussed in the session:**

| Tier | Price | Characteristics |
| --- | --- | --- |
| Free | $0 | Small websites, basic protection |
| Pro | $15/month | Startups, SMBs |
| Business | $200/month | Enterprises, VPC Private Origin, WAF |
| Premium | $1,000/month | Enterprise, Origin Failover, low latency |

- Fixed monthly cost model intended to reduce billing uncertainty.
- Possible packaging of CDN, protection, DNS, and storage-related credits depending on provider design.
- One package per domain; upgrade as needs grow.

#### Session 4 — 36-Hour LA Hackathon Journey: UTM Morpho Project (Uyển, Thảo, Mai)

A team of 3 (Uyển, Thảo, Mai) shared their **LA Hackathon** experience — Vietnam's largest hackathon with 36 continuous hours to build a product.

**Product idea — UTM Morpho:**

- Problem: When using AI to generate UI, every small edit (button color, spacing) requires re-prompting from scratch → wastes time and tokens.
- Solution: Editor allowing UI generation by template with **direct on-interface editing** (drag-drop components, edit CSS).

**AI architecture (3 agents):**

| Agent | Role |
| --- | --- |
| A1 — Vision | Analyze image input, create JSON layer file |
| A2 — Engineering | Read JSON, create sizes, CSS, layout |
| A3 — Design | Apply design system, generate HTML interface code |

**Hackathon lessons:**

1. Draw inspiration from daily work rather than solving theoretical macro problems.
2. Focus on core features when time is limited (final 8–9 hours for MVP).
3. Pitch strategy: demo first, explain architecture after in 5 minutes.
4. Health management over 36 hours: schedule eating, rest; avoid overthinking and AI over-generation.

#### Session 5 — LLM Inference: Temperature and Output Consistency (Đức Đào)

Technical session on the **probabilistic nature of LLMs** and optimizing output stability in production.

**Core knowledge:**

- LLMs select next tokens based on scores (logits) — probabilistic, not deterministic.
- **Temperature** parameter controls randomness: temperature = 0 doesn't guarantee 100% identical output across runs (due to GPU inference optimization).
- Temperature = 0 can cause word repetition — use 0.1 for some models.

**Mitigation strategies:**

| Strategy | Description | Trade-off |
| --- | --- | --- |
| Multiple runs + voting | Multiple sub-agents, choose most common answer | Higher cost and latency |
| Self-host model | Full inference config control | Higher infrastructure cost |
| JSON mode | Enable structured output (OpenAI JSON mode) | Reduces format errors |
| Resilient downstream design | Services must handle varied output formats | Requires thorough testing |

**Key takeaway:** LLMs are probabilistic — always design systems to handle variation; test extensively before production.

#### Session 6 — Enterprise Multi-Agent System for Credit Assessment (Cát Vy)

Final session shifted from technical to **business mindset** — AI deployment experience at VPBank.

**Four questions when designing enterprise solutions:**

1. **Who uses it?** — Identify end users.
2. **What do they use?** — Specific functions to solve.
3. **Why use it?** — Value compared to current approach.
4. **When to use it?** — Appropriate deployment timing.

**Use case: Startup credit assessment**

- Startups carry significant weight in banking but traditional credit models underfocus on them.
- Building an **enterprise-grade multi-agent system** for credit assessment workflows.

**Six enterprise system pillars:**

| Pillar | Content |
| --- | --- |
| Knowledge Transfer | Transfer domain expert knowledge into models — not just pushing data |
| Context Engineering | Index business documents, codebase; expert validation required |
| Guardrails & Compliance | Prompt injection defense, audit trail, data validation |
| Security Perimeter | VPC, Security Group, PrivateLink, network isolation |
| Reliability | Single point of failure, processing, high availability |
| Deployment Phases | Internal Testing → SIT → UAT → Pilot → Scale |

**Important message:** Enterprises evaluate **mindset** more than project depth in interviews. Software engineering knowledge (JWT, OAuth) remains mandatory to move AI from lab to production.

### Key Takeaways

**1. Industry trends and career direction**

- AI doesn't eliminate IT jobs but changes structure — creating new roles (maintaining AI-generated products).
- Developers proficient with AI will be prioritized in hiring.
- Business mindset (who, what, why, when) matters as much as technical knowledge.

**2. AI working skills**

- Context engineering: provide organization-specific context, separate sessions by task.
- LLMs are probabilistic — don't assume temperature = 0 gives fixed output; design resilient systems.
- Knowledge transfer from domain experts is critical in enterprise AI.

**3. AWS knowledge**

- A flat-rate CDN package can help control cost uncertainty for startups and SMBs, but official CloudFront pricing should still be verified before use.
- Amazon Q supports building AI agents with MCP integration for business automation.
- Serverless multi-agent architecture (vision → engineering → design) deployable for AI products.

**4. Hackathon and real project experience**

- Ideas from daily pain points outperform theoretical macro problems.
- Focus on MVP under time constraints; demo before explaining architecture.
- Enterprise AI deployment requires: Internal Test → SIT → UAT → Pilot → Scale.

### Application to Internship Work

| No. | Application | Approach |
| --- | --- | --- |
| 1 | Context engineering | Separate AI sessions by task; provide project context instead of generic prompts |
| 2 | CloudFront | Consider cost-control options and verify official CloudFront pricing before deploying CDN for workshop projects |
| 3 | Multi-agent architecture | Reference 3-agent model (vision → engineering → design) for AI labs |
| 4 | LLM production | Design downstream services to handle variable output; test many cases |
| 5 | Business thinking | Apply 4 questions (who, what, why, when) when designing solutions |

### Event Experience

I attended the 2nd FCAJ Community Day at Bitexco with large attendance across floors 26 and 36. Compared to the first Community Day (May 9, 2026), this event went deeper into **AI production techniques** and **enterprise experience**.

**Atmosphere and community connection**

Open atmosphere encouraging questions and discussion — fitting FCAJ's learning community spirit.

**Impressions by session**

- **Opening (Nguyễn Gia Hưng):** Optimistic job market perspective — AI creates long-term jobs rather than fully replacing them.
- **Anh Tịnh's session:** Practical and applicable — separating context and sessions when working with AI daily.
- **Hải Anh's session:** Live Amazon Q demo showing AI agent potential in enterprise environments.
- **Nguyễn Tuấn Thịnh's session:** CDN pricing and cost-control ideas — useful for project cost estimation.
- **UTM Morpho session (Uyển, Thảo, Mai):** Inspiring hackathon story — proving a complete product can be built in 36 hours.
- **Đức Đào's session:** Deeper understanding of LLM probabilistic nature and production-ready system design.
- **Cát Vy's session:** Shifted perspective from technical to business — clearer understanding of enterprise AI expectations.

**Lessons learned**

The event helped me recognize that the Cloud/AI Engineer journey involves not just learning AWS services but also: context engineering skills, production-ready system design thinking, and especially **business mindset** to solve real enterprise problems.


