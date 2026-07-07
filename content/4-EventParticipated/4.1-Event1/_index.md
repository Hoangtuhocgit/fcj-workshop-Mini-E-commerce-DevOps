---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Summary Report: "FCAJ Community Day"

### Event Information

| Item | Details |
| --- | --- |
| Event name | FCAJ Community Day |
| Date & time | 09:00, May 9, 2026 |
| Location | 26th Floor, Bitexco Tower, 02 Hai Trieu Street, Saigon Ward, Ho Chi Minh City |
| Role | Attendee |
| Number of sessions | 4 sessions |

### Event Objectives

FCAJ Community Day is a recurring event organized by the First Cloud Journey (FCAJ) community, connecting members from beginners to experts in Cloud Computing. Based on my attendance, the event pursued the following objectives:

1. **Community building:** Create a space for networking and relationship-building among FCAJ members.
2. **Learning path guidance:** Help students and newcomers approach AWS/Cloud aligned with the FCAJ program.
3. **Self-learning inspiration:** Share methods, proactive learning mindsets, and ways to sustain motivation in a fast-changing tech landscape.
4. **Practical knowledge sharing:** Speakers convey real-world experience with AWS, AI, and software development beyond textbook theory.

### Speakers

| No. | Speaker | Role / Organization |
| --- | --- | --- |
| 1 | Huỳnh Hoàng Long | Admin FCAJ |
| 2 | Nguyễn Tuấn Thịnh | DevOps Cloud Engineer |
| 3 | Anh Khang | Solutions Architect, Cloud Kinetics |
| 4 | Chị Thảo | Software Developer, Vietnam International Bank (VIB) |

### Session Contents

#### Session 1 — Self-Learning Mindset in the Digital Era (Huỳnh Hoàng Long)

The speaker opened with the topic *"Addicted to Learning Like You're Addicted to Social Media"*, focusing on proactive learning methods rather than pure technical knowledge.

**Problem identified:** Many students spend more time on social media and online games than studying, despite initially intending short sessions. The cause lies in dopamine mechanisms — the brain prioritizes activities with instant rewards, curiosity stimulation, and lower energy consumption than focused study.

**Proposed solutions:**

1. **Apply reward mechanisms:** Break learning goals into small steps with immediate positive feedback.
2. **Build habit streaks:** Maintain continuous learning streaks, similar to language-learning apps.
3. **Leverage the FCAJ rank system:** Use ranking tiers (bronze → silver → gold) for long-term motivation on the FCAJ path.
4. **Shift habits:** Replace social media time with sharing AWS knowledge, new services, and technical articles in the community.
5. **Optimize the learning environment:** Prepare a clean study space that supports daily self-learning.

#### Session 2 — Prompt Engineering and AWS Architecture (Nguyễn Tuấn Thịnh)

This technical session covered effective AI communication and a demo of **Proptimizer** — a personal project deployed on AWS within the FCAJ program.

**Part 1 — Prompt writing techniques:**

| Issue | Consequence |
| --- | --- |
| Generic prompts | Non-specific, hard-to-apply outputs |
| Overly long prompts | High token costs |
| Vague instructions | Inconsistent, error-prone results |

The speaker introduced **7 components of an effective prompt:** Role, Task, Context, Input, Output Format, Example, and Constraint. Advanced techniques such as Chain of Thought, Self-consistency, and Tree of Thought were also covered, along with token cost considerations — especially for Vietnamese (often double the cost of English).

**Part 2 — Proptimizer solution architecture:**

| Layer | AWS Service | Purpose |
| --- | --- | --- |
| Frontend / CDN | S3, CloudFront | Static content storage and delivery |
| Authentication | Amazon Cognito | Sign-up, sign-in, JWT management |
| API | API Gateway | Request routing, rate limiting, authorization |
| Backend | AWS Lambda | Serverless logic processing |
| AI | Amazon Bedrock | Foundation model access, guardrails |
| Database | DynamoDB | Prompt and optimization history storage |
| Monitoring | CloudWatch | Logs and metrics (latency, error rate) |

The speaker also demoed a prompt optimization tool with a browser extension, showing how to integrate AI into daily workflows while maintaining output quality.

#### Session 3 — Career Guidance and Foundation Mindset (Anh Khang)

An interactive session with year 3–4 students addressing *"Why aren't students ready to start working?"* in the AI era.

**Key perspectives:**

1. **Foundational knowledge is irreplaceable:** In a fast-changing environment, candidates should focus on foundations (infrastructure, problem-solving mindset) rather than mastering all AWS services.
2. **Real hiring expectations:** Employers don't require knowing everything; mastering about 5 AWS services deeply matters more than surface-level knowledge of many.
3. **AI in hiring assignments:** Most candidates use AI for take-home tests — what matters is explaining why a solution was chosen, not just submitting output.
4. **Experience vs. exposure:** Years of work don't equal professional maturity; diverse projects and domains can accumulate exposure beyond years of experience.

**Three recommended actions:** Ask more questions and learn to ask the right ones; prioritize long-term vision (accept lower salary for experience); work in teams rather than solo projects.

#### Session 4 — BMAD Method for Software Development (Chị Thảo)

The speaker presented the **BMAD Method** — an open-source framework for disciplined AI-assisted software development, replacing unstructured approaches (continuous prompting without quality control).

**Problems with unstructured development:**

- AI loses context during long continuous conversations.
- Generated code is difficult to deploy and maintain.
- No control when updating or modifying features.

**BMAD 3-phase process:**

| Phase | Activities | Output |
| --- | --- | --- |
| Planning | Brainstorm ideas, analyze requirements | PRD (Product Requirements Document) |
| Solutioning | Design architecture, select tech stack | Architecture document, epics, user stories |
| Implementation | Develop each story independently | Source code, updated per documentation |

Core philosophy: software quality depends on specification quality; each feature is assigned to a separate AI agent to reduce context overlap and minimize hallucination.

### Key Takeaways

Across four sessions, I consolidated the following knowledge groups:

**1. Learning mindset and personal development**

- Sustaining study habits depends on reward systems and learning environments, not willpower alone.
- Sharing knowledge in the community effectively reinforces understanding and builds professional credibility.
- Daily consistent learning yields better long-term results than cramming.

**2. AI working skills**

- Structured prompts using the 7-component framework reduce output errors and optimize token costs.
- AI is a support tool, not a replacement for thinking — understanding and explaining solutions is essential.
- Breaking tasks into small parts and separating sessions when context gets mixed is effective AI usage.

**3. Practical AWS architecture**

- A full serverless model can be deployed from frontend to AI without server management.
- Amazon Cognito shortens authentication system development time.
- CloudWatch is mandatory in production architecture, not optional.

**4. AI-assisted software development process**

- BMAD Method demonstrates combining AI agents with standard SDLC.
- Document-driven development (PRD → Architecture → Stories → Code) enables better quality control.
- Teamwork — even with AI agents playing multiple roles — is more effective than solo development.

### Application to Internship Work

Based on acquired knowledge, I identified specific application directions:

| No. | Application | Approach |
| --- | --- | --- |
| 1 | FCAJ learning path | Maintain streaks, accumulate ranks, share knowledge daily |
| 2 | Workshop project | Reference Proptimizer architecture (serverless + Bedrock) for AWS labs |
| 3 | Prompt engineering | Apply the 7-component framework when working with AI in internship projects |
| 4 | BMAD Method | Try Planning → Solutioning → Implementation for the mini e-commerce project |
| 5 | Career direction | Focus on mastering 5 core AWS services instead of surface-level learning |

### Event Experience

I attended FCAJ Community Day at Bitexco Floor 26 as an attendee. The event combined mindset guidance, technical knowledge, and career direction — distinct from pure technical workshops I had previously attended.

**Atmosphere and community connection**

The hall was well-attended, primarily by final-year students passionate about Cloud Computing. The open atmosphere encouraged questions and sharing — fitting FCAJ's learning community spirit.

**Impressions by session**

- **Huỳnh Hoàng Long's session:** Shifted my perspective on learning — focus on building environment and habits rather than just studying harder.
- **Nguyễn Tuấn Thịnh's session:** Live Proptimizer demo on AWS, clearly illustrating how to combine multiple services into a complete product.
- **Anh Khang's session:** Provided practical perspectives on hiring expectations and AI's role in interviews.
- **Chị Thảo's session:** Introduced BMAD Method — a new approach for disciplined AI-assisted software development.

**Lessons learned**

The event helped me recognize that becoming a Cloud Engineer involves not just accumulating AWS service knowledge, but also building self-learning habits, software development discipline, and solid foundational thinking. AI is a powerful tool but must be used within clear process frameworks — without process, products cannot be deployed in practice.
