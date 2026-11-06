# How AI Companies Organize Engineering/Product Work (Sprints vs. Alternatives), 2024–2026

**Method note for the report writer:** WebFetch could only reach claude.com. `newsletter.pragmaticengineer.com` and `calv.info` were blocked by this session's network allowlist, so I could not read the Pragmatic Engineer deep dives or Calvin French-Owen's essay in full. Except where a finding says "fetched," the claims below come from search-result snippets and summaries, attributed to the most relevant URL returned. Each finding is tagged:
- **[Fetched]**: I read the primary page.
- **[Snippet-primary]**: a search snippet from the primary source.
- **[Secondary]**: news coverage, aggregators, unofficial summaries or translations. Verify these before quoting.

Search snippets did not reliably say which URL each sentence came from. Where attribution is uncertain I name the likeliest source and flag it.

---

## 1. What leaders and employees of AI companies say publicly about process

### Takeaway
No source I found says a frontier lab or AI-native startup runs textbook Scrum with fixed 2-week sprints, but no source said they don't either. They do describe the same small set of practices:
- bottom-up prototyping instead of roadmaps or PRDs;
- small teams forming around prototypes that work;
- continuous shipping, internally and externally;
- heavy dogfooding;
- leaders who frame "speed" as the strategy.

Short, intense, deadline-driven pushes (for example OpenAI's "7-week sprint" to build Codex) are called "sprints" in the colloquial sense, not the Scrum one.

### Cited Findings

**OpenAI**
- Calvin French-Owen worked at OpenAI from May 2024 to June 2025 and published "Reflections on OpenAI" on July 15, 2025. In that window the company grew from about 1,000 to about 3,000 employees. [Secondary] [Entrepreneur](https://alpha.entrepreneur.com/business-news/former-openai-engineer-details-what-its-like-to-work-there/494711); [Digital Information World](https://www.digitalinformationworld.com/2025/07/openais-internal-culture-revealed.html). Original essay (not reachable here): https://calv.info/openai-reflections
- French-Owen describes a 7-week push that produced the Codex coding agent. By February 2025 several competing prototypes were circulating internally, and two teams were merged into one effort. [Secondary] [Analytics India Mag](https://analyticsindiamag.com/ai-news-updates/openai-built-codex-in-just-7-weeks-from-scratch/); [Gizmodo](https://gizmodo.com/an-engineers-diary-reveals-the-human-cost-of-building-openais-next-big-thing-2000630482)
- He says work is bottom-up: small groups built prototypes without approval, and teams formed around the promising ones. He reportedly saw 3–4 similar prototypes before Codex launched. A Japanese-language report says that when he asked about a quarterly roadmap early on, he was told none existed. [Secondary] [Xenospectrum](https://xenospectrum.com/openais-chaotic-internal-situation-former-engineer-discusses-the-light-and-shadow-of-rapid-growth/); [36Kr](https://www.36kr.com/p/3381278242564609)
- Reports also say teams could be pulled between projects at any time and that leadership is active in Slack. [Secondary, Chinese-language report] [36Kr](https://eu.36kr.com/zh/p/3382663528274305)
- The Pragmatic Engineer's "Inside OpenAI: How does ChatGPT Ship So Quickly?" interviews Evan Morikawa, the first engineering manager of the ChatGPT group. It says OpenAI had never publicly discussed its software engineering practices before, and it calls the engineering, product and design org "Applied." The rest is paywalled. [Snippet-primary] [Pragmatic Engineer](https://newsletter.pragmaticengineer.com/p/inside-openai-how-does-chatgpt-ship?open=false)
- Sulman Choudhry, head of ChatGPT engineering, was interviewed by the Engineering Leadership newsletter. The preview mentions "4 core pillars" of OpenAI's engineering culture and says most ideas come bottom-up. [Snippet-primary] [Engineering Leadership](https://newsletter.eng-leadership.com/p/inside-openais-engineering-culture)
- On the Engineering Leadership Podcast (#250), Choudhry describes OpenAI moving from siloed research to cross-functional teams. He also describes a "chaos factory" culture that encourages several independent efforts before converging on one. [Secondary, episode summary] [Metacast](https://metacast.app/podcast/the-engineering-leadership-podcast/hereHPAV/how-openai-s-engineering-org-is-reshaping-teams-roles-and-workflows-w-sulman-choudhry-250/8JeXJ6ZI)
- OpenAI's "Harness engineering: leveraging Codex in an agent-first world" was published February 11, 2026 by Ryan Lopopolo. Over five months a team built and shipped an internal beta product with "0 lines of manually-written code." Even the initial AGENTS.md file was written by Codex. [Snippet-primary] [OpenAI](https://openai.com/index/harness-engineering/)
  - Secondary write-ups say the codebase reached about 1M LOC and about 1,500 PRs.
  - They disagree on team size: 3 engineers, or 3 growing to 7.
  - [Secondary] [The Neuron](https://www.theneuron.ai/explainer-articles/openais-harness-engineering-playbook-how-to-ship-1m-lines-of-code-without-writing-any/); [Latent Space](https://latent.space/p/harness-eng)

**Anthropic (Claude Code team)**
- "How Anthropic teams use Claude Code," dated July 24, 2025. [Fetched] [Claude blog](https://claude.com/blog/how-anthropic-teams-use-claude-code)
  - Product Engineering calls Claude Code its "first stop" for any programming task.
  - Product Design feeds Figma files to Claude Code and sets up autonomous loops that write code, run tests and iterate. Humans review the results.
  - Security Engineering changed its cycle from "design doc → janky code → refactor → give up on tests" to pseudocode first, TDD, and periodic check-ins.
  - The post says agentic coding is "dissolving the boundary between technical and non-technical work."
- The Pragmatic Engineer's "How Claude Code is built" (2025). [Snippet-primary] [Pragmatic Engineer](https://newsletter.pragmaticengineer.com/p/how-claude-code-is-built)
  - A dogfooding-ready version shipped in November 2024, two months after the first prototype.
  - By day five, 50% of Anthropic Engineering was using it.
  - The team grew from 1 engineer to about 10.
  - PR throughput rose 67% while Anthropic's headcount doubled.
- A secondary summary of the same article says the team makes about 60–100 internal releases a day, with a new internal npm package per change. [Secondary] [Pixel Pioneers blog](https://thepixelpioneers.blogspot.com/2025/09/how-claude-code-is-built.html)
- Pragmatic Engineer podcast "Building Claude Code with Boris Cherny" (March 2026): prototypes replaced PRDs. Instead of writing specs, the team builds many working prototypes before shipping a feature. [Snippet-primary] [Pragmatic Engineer](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny)
- A 36Kr report quotes Cherny: "Our culture is that we don't write much. We just show." It says the team doesn't write PRDs and prototypes in code instead. [Secondary] [36Kr](https://eu.36kr.com/en/p/3727086198963080)
- Lenny's Podcast episodes:
  - Boris Cherny, "Head of Claude Code: What happens after coding is solved" (around February 19, 2026). [Snippet-primary] [Audible listing](https://www.audible.com.au/podcast/Head-of-Claude-Code-What-happens-after-coding-is-solved-Boris-Cherny/B0GP7MGTT8)
  - Cat Wu, "How Anthropic's product team moves faster than anyone else" (Claude Code product lead). [Snippet-primary] [Rosetta listing](https://rosetta.to/u/lennyspodcast/how-anthropic-s-product-team-moves-faster-than-anyone-else-cat-wu-head-of-product-claude-code)
  - An unofficial summary of Cat Wu's material says the team delegates research, code prototypes, *draft PRDs* and competitive teardowns to Claude, then audits the output. That partly contradicts the "no PRDs" framing. [Secondary] [PM archive](https://the-pm-archive.vercel.app/articles/2026-04-28-how-anthropics-product-team-ships-in-days-not-months-cat-wus-playbook-for-pms-in-the-ai-era)
- A dev.to post claims a "two-engineer team" rule at Anthropic. It looks AI-rewritten and cites no source. Treat as unverified. [Secondary] [dev.to](https://dev.to/gentic_news/inside-anthropic-how-claude-code-engineers-ship-with-2-engineer-teams-and-4kh5)

**Cursor (Anysphere)**
- A Cursor product job posting says product at Cursor is not a traditional PM org. It relies on product-minded engineers, has "no roadmap committee," and prefers people who ship "the high-leverage thing now" over months of exploration. The team builds in person. [Snippet-primary, job posting; exact URL uncertain] [Anysphere careers](https://anysphere.inc/careers/enterprise_product_engineer)
- Separate Cursor PM listings exist, for example a PM who partners with customers, sales and TAMs, so the PM role is not absent. [Secondary] [ResumeGeni](https://resumegeni.com/jobs/product-manager-at-anysphere-san-francisco)
- Anysphere's stated mission is to automate coding through "inventive research, design, and engineering." [Snippet-primary] [Anysphere careers](https://anysphere.inc/careers/enterprise_engineering_manager)

**Perplexity**
- At UC Berkeley Haas, Aravind Srinivas described shipping products about 80% complete and iterating over the following months. [Secondary, single news-style write-up] [Particle News](https://particlenews.pages.dev/story/perplexity-ceo-aravind-srinivas-outlines-80-then-iterate-strategy-at-uc-berkeley-haas)
- Srinivas quote: "Your only strategy is speed. You must innovate faster than anyone else. It's like running a marathon in full sprint." [Secondary] [dev.to](https://dev.to/maybe_ai/the-survival-code-of-perplexitys-ceo-how-to-break-through-the-siege-of-ai-giants-1g60)
- Reports say he treats speed and urgency as non-negotiable and as a moat against Big Tech. He gives feedback "as a user" rather than as the CEO, and prefers Slack over meetings. [Secondary] [Benzinga](https://www.benzinga.com/news/topics/25/08/46815754/i-dont-do-anything-other-than-working-says-perplexity-ceo-aravind-srinivas-as-his-14-billion-ai-start); [New India Abroad](https://www.newindiaabroad.com/news/perplexity-ceo-shares-key-lessons-for-startup-founders)

**Replit**
- About 65 employees in March 2025, after Amjad Masad cut the team roughly in half in "founder mode." He says this previews firms built around generalists who direct AI agents rather than specialist teams. [Secondary] [TBPN digest](https://tbpn-digest.vercel.app/story/2025-03-24/replit-ceo-amjad-masad-agents-drove-500-metric-gains-net-dollar-retention-above-100-on-consumer-plan)
- At SaaStr AI 2026, Masad described an internal nightly agent that reads user traces, generates PRs with prompt changes, and ships them as A/B tests. In effect, part of the improvement loop runs continuously without humans scheduling it. [Snippet-primary-ish, SaaStr's own write-up] [SaaStr](https://www.saastr.com/amjad-masad-and-me-at-saastr-ai-2026-the-agents-we-actually-built-and-what-replits-founder-thinks-comes-next/)

**Hugging Face**
- Hugging Face is described as remote-first and async-first, works in public on GitHub, and has an unclear career ladder. Sources are review sites, job boards and profile pieces. I found no primary statement on sprints or planning, and nothing supporting a "no managers" claim. [Secondary] [Bridged reviews](https://www.getbridged.co/company-reviews/hugging-face); [Press Farm](https://press.farm/the-anti-hustle-billionaire-clem-delangues-unconventional-life-outside-hugging-face/)

### Inferences
- The recurring operating model is roughly: prototype-led discovery, then small team convergence, then dogfooding, then fast ship. This looks closer to Kanban or continuous flow with occasional deadline-driven pushes than to Scrum. Inference: no source explicitly says "we don't use sprints."
- "Prototypes instead of PRDs" (Anthropic) and "no roadmap committee" (Cursor) suggest that when building is cheap, written specs and planning ceremonies lose value and working software becomes the spec.
- Several of these practices predate heavy AI coding at OpenAI (bottom-up work, merging competing efforts), so they are partly startup and research-lab culture, not only an effect of AI tools.

### Gaps
- **Google DeepMind, Mistral, Vercel v0, Scale AI:** I found no sources in my tool budget. These need dedicated searches, for example DeepMind "Gemini team planning" or Vercel's Guillermo Rauch on v0 shipping cadence.
- **Missing primary text:** Full Pragmatic Engineer articles (paywall and network block) and Calvin French-Owen's original essay are blocked. Exact quotes on whether OpenAI or Anthropic use sprints or OKRs are unverified.
- **Cursor:** No primary interview from Michael Truell or the Cursor team describing process in their own words.

---

## 2. Why sprints fit ML research poorly, and what ML teams use instead

### Takeaway
Practitioners agree that fixed-scope timeboxes clash with ML's exploratory, non-linear work:
- effort is hard to estimate;
- training runs take days or weeks;
- results force pivots;
- output is often insight rather than a shippable increment.

The usual replacements are Kanban, CRISP-DM-style iterative lifecycles, research or discovery spikes, and longer cycles such as Shape Up. Evidence is mostly practitioner opinion, not controlled study.

### Cited Findings
- Practitioners report that data science tasks are hard to express as user stories and hard to estimate. A model can take days or months depending on feature selection. One author compares Scrum on DS to "managing researchers in a university department and having them switch their research subject at random every two weeks." [Secondary, practitioner blogs] [Medium/Amethix](https://medium.com/amethix/why-is-scrum-a-terrible-idea-for-machine-learning-2325826f3104); [Medium/Product Popcorn](https://medium.com/product-popcorn/how-does-agile-work-for-data-science-teams-a230fc7781f)
- Training a complex model can take days or weeks, which can derail a sprint that expects continuous progress. Much DS work is research, not product increments. [Secondary, practitioner] [LinkedIn mirror: Why Scrum Struggles with AI Projects](https://meilu1.jpshuntong.com/url-68747470733a2f2f7777772e6c696e6b6564696e2e636f6d/pulse/why-scrum-struggles-ai-projects-rethinking-agile-machine-alex-alieja-3p8cf); [IIA: Don't make data scientists do Scrum](https://iianalytics.com/community/blog/dont-make-data-scientists-do-scrum)
- Case report: a company adopted Scrum because it had many experienced Scrum practitioners, found it didn't work for model development, and moved to Kanban (2025 blog). [Secondary] [ML Project and Scrum](https://chezo-uno.pages.dev/blog/2025-05-02-ml-project-and-scrum); see also [Chang Hsin Lee, "Agile in Data Science: Why My Scrum Doesn't Work?"](https://changhsinlee.github.io/agile-ds-scrum-kanban/)
- Shape Up (6-week cycles plus cool-down) is proposed as closer to DS needs than Scrum, though still imperfect for research-heavy projects. [Practitioner blog] [Eric J. Ma, Oct 2023](https://ericmjl.github.io/blog/2023/10/5/shape-up-and-data-science-a-match-closer-to-agile-than-you-think)

### Inferences
- Frontier-lab research (pretraining and RL runs lasting weeks) is likely managed by milestones: compute allocation, evals and model releases. Two-week sprints are unlikely. This is inference only; I found no primary lab source describing research-team planning.
- The OpenAI pattern of parallel competing prototypes converging later resembles portfolio-style research management more than a sprint backlog. Also inference.

### Gaps
- No primary source from OpenAI, Anthropic, DeepMind or Mistral research teams on how research planning works (milestones, experiment trackers such as W&B, compute-allocation cycles).
- No Reddit r/MachineLearning or r/ExperiencedDevs threads were retrieved within budget.

---

## 3. How AI coding tools are changing agile ("is the sprint dead?")

### Takeaway
2025–2026 commentary argues that AI coding agents shrink implementation time from weeks to days or hours. That undermines the two-week sprint's planning assumptions and ceremonies such as story-point estimation and sprint planning. Most writers conclude the sprint is being reshaped, not killed. Commentators and survey data still affirm agile values, while the ceremony-heavy versions take most of the criticism. Much of this content is opinion on Medium, dev.to, Hackernoon and blogs.

### Cited Findings
- **InfoQ, February 2026:** reports a debate over an "AI agile manifesto." A commenter argues bureaucracy killed agile before AI agents arrived. [Snippet, trade press] [InfoQ](https://www.infoq.com/news/2026/02/ai-agile-manifesto-debate)
- **Hackernoon:** "AI coding agents are breaking the two-week sprint." It argues an AI-native workflow can ship a feature before sprint planning ends. [Opinion] [Hackernoon](https://hackernoon.com/ai-coding-agents-are-breaking-the-two-week-sprint)
- **"The death of the two-week sprint"** (Invide Labs blog). [Opinion] [Invide Labs via HN reader](https://hn.jakechampion.name/reader/https://blog.invidelabs.com/the-death-of-the-two-week-sprint)
- **Dataconomy, November 14, 2025, "Waterfall 2.0":** argues AI brings back more structured, spec-first development, with sprint planning reduced to approving AI-generated task breakdowns. [Opinion, trade press] [Dataconomy](https://dataconomy.com/2025/11/14/waterfall-2-0-ai-brings-back-structured-software-development)
- **StickyMinds, "Is Agile Dead?":** argues agile and craftsmanship are "far from dead." [Opinion] [StickyMinds](https://www.stickyminds.com/article/agile-dead-how-ai-coding-transforming-software-development)
- **"The End of Process Theater":** the ceremony-heavy version of agile is becoming irrelevant, not agile itself. [Opinion blog] [sawinyh.com](https://sawinyh.com/blog/end-of-process-theater)
- **dev.to, "The Agentic Manifesto: Why Agile is breaking in the age of AI agents."** [Opinion] [dev.to](https://dev.to/crywolfe/the-agentic-manifesto-why-agile-is-breaking-in-the-age-of-ai-agents-1939)
- **P3 Group consulting whitepaper (September 2025), "From Sprints to Swarms."** [Consulting whitepaper, not read in full] [P3 Group PDF](https://www.p3-group.com/wp-content/uploads/2025/09/From_Sprints_to_Swarms.pdf)
- **"AI Is Breaking and Remaking Software Teams."** [Opinion blog] [sysid](https://sysid.github.io/ai-is-breaking-and-remaking-software-teams)
- **Practice examples from AI companies:**
  - Anthropic's Claude Code team does 60–100 internal releases a day. [Secondary] [Pixel Pioneers](https://thepixelpioneers.blogspot.com/2025/09/how-claude-code-is-built.html)
  - Replit runs a nightly agent that opens PRs and A/B tests. [SaaStr](https://www.saastr.com/amjad-masad-and-me-at-saastr-ai-2026-the-agents-we-actually-built-and-what-replits-founder-thinks-comes-next/)
  - OpenAI's "harness engineering" recasts engineers as designers of environments, intent specs and feedback loops for agents. [OpenAI](https://openai.com/index/harness-engineering/)
  - Together these are concrete examples of cadence decoupled from sprint boundaries.

### Inferences
- **Bottleneck shift:** the constraint moves from writing code to specifying intent, reviewing output and validating it with evals. This favours continuous flow (Kanban-like WIP limits on review) and spec-first work over velocity-based sprint planning. The Dataconomy "Waterfall 2.0" and OpenAI "harness engineering" framings both point here.
- **Cadence:** the fixed "sprint" unit may survive mainly as a stakeholder and alignment cadence rather than a delivery unit.

### Gaps
- No quantitative study found measuring sprint-length changes at AI-adopting companies.
- No Reddit r/agile or r/ExperiencedDevs threads were retrieved.
- Kent Beck's "augmented coding" writing appeared in results but was not retrieved in detail.

---

## 4. Surveys on AI/ML team methodologies

### Takeaway
The surveys that exist are small and dated. In a Data Science Process Alliance poll (n=109), CRISP-DM was the most-used approach (about 49%), ahead of Scrum (about 18%) and Kanban (about 12%). A 2022 academic survey found only 25% of participants used any formal DS methodology.

On AI tool adoption, Anthropic's internal study (December 2025) is the most specific company-level data. Respondents reported using Claude in about 59–60% of their work, up from 28% a year earlier, with about 50% self-reported productivity gains.

### Cited Findings
- **Data Science Process Alliance poll (n=109):**
  - Nearly half most commonly use CRISP-DM, followed by Scrum, Kanban and "My Own." [Snippet-primary] [datascience-pm.com](https://www.datascience-pm.com/crisp-dm-still-most-popular/)
  - A citing paper gives CRISP-DM 49%, Scrum 18%, Kanban 12% and individual approaches 12%. [Secondary] [ojs.udb.ac.id](https://ojs.udb.ac.id/Senatib/article/download/3015/2576/7299)
  - The authors note the sample likely skews toward process-interested readers, and that CRISP-DM is a workflow model while Scrum and Kanban are collaboration frameworks.
- **2022 academic survey, "A survey study of success factors in data science projects":** Agile DS Lifecycle was the most-used framework, followed by CRISP-DM and Microsoft TDSP. Only 25% of participants used any DS project methodology. This conflicts with the DSPA ranking. [Snippet-primary, arXiv] [arXiv 2201.06310](https://arxiv.org/pdf/2201.06310)
- **Anthropic, "How AI is transforming work at Anthropic"** (December 2, 2025). [Snippet-primary] [Anthropic](https://www.anthropic.com/research/how-ai-is-transforming-work-at-anthropic)
  - Method: survey of 132 engineers and researchers, 53 interviews, and Claude Code usage data, collected August 2025.
  - Usage: Claude used in about 59–60% of work with about 50% productivity gains, versus 28% and 20% a year earlier.
  - Delegation: most respondents could "fully delegate" only 0–20% of their work.
  - New work: 27% of Claude-assisted work wouldn't have been done otherwise.
  - Concerns about skill erosion and mentorship.
  - Anthropic itself cautions that the results may not generalize.
  - Feature implementation rose from 14% to 37% of usage, per secondary coverage. [Secondary] [Interview Query](https://www.interviewquery.com/p/anthropic-ai-skill-erosion-report)
- **Forrester 2025 State of Agile:** a search summary says 95% of professionals affirm agile's critical relevance. I could not tie this to a specific primary URL, so treat it as unverified.

### Inferences
- In small surveys, ML and DS teams pick a lifecycle model (CRISP-DM) more often than a team-cadence framework (Scrum). That is consistent with sprints fitting research work poorly.

### Gaps
- No survey specifically of frontier-lab or AI-startup engineering methodology (sprints vs. Kanban vs. other) was found.
- I did not check whether the Stack Overflow 2024/2025 Developer Survey or the Digital.ai State of Agile report break out AI/ML teams.
- Forrester figure: primary source not located.
