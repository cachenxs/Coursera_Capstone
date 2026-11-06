# How Tech Startups (Seed to Growth, non-AI-lab) Use Agile Sprints / Scrum, 2024–2026

> **Method note for the report writer:** In this session WebFetch failed with DNS/allowlist errors on every host tried (linear.app, businesswire.com, parabol.co, builtin.com, dev.to). Findings below come from **WebSearch result snippets and search-engine summaries**, not from full-page reads. Treat precise figures accordingly. Where a claim comes from a vendor or low-quality aggregator, that is flagged. Source type is shown in [brackets].

## 1. What share of startups and software teams use Scrum or sprints?

### Takeaway
No survey isolates *startups*. The large surveys skew toward enterprises: Digital.ai's State of Agile respondents are mostly coaches and consultants at large companies. They show agile as near-universal and Scrum as the dominant named framework, with growing use of hybrid or homegrown models. Tooling data (Jira at ~57.5% of Stack Overflow 2024 respondents) is the best proxy for sprint-tool usage, and Linear is gaining among practitioner-skewed audiences.

### Cited Findings
- **17th State of Agile (Digital.ai, released Jan 2024):** headline "71% use Agile in their SDLC". Small organizations report strong business benefits, while medium and large companies keep hitting barriers to scaling agile. — [Business Wire press release, official/PR](https://businesswire.com/news/home/20240116199385/en/17th-State-of-Agile-Report-71-Use-Agile-in-their-SDLC-Small-Organizations-Report-Strong-Business-Benefits-Medium-and-Larger-Sized-Companies-Continue-to-Experience-Barriers-in-Successfully-Scaling-Agile) (headline only; the page itself could not be fetched)
- One secondary source puts SAFe as the leading *enterprise* scaling framework at 26% in the 2024 report. — [StarAgile blog, secondary](https://staragile.com/blog/state-of-agile)
- **Scrum share figures conflict across secondary sources.** One claims ~87% of State of Agile respondents used Scrum in the 16th report (2022/23), up from 58% in 2021. Another says 66% of agile teams used Scrum in 2023. These are aggregator figures and likely use different bases ("Scrum" vs "Scrum or Scrum hybrids"); verify against the primary PDF. — [Parabol blog](https://www.parabol.co/blog/how-many-companies-use-scrum/); [Echometer Scrum statistics 2026](https://echometerapp.com/en/scrum-statistics-2026/); [Breeze agile statistics](https://www.breeze.pm/articles/agile-statistics) (all secondary blogs)
- **18th State of Agile (Digital.ai, Oct 2025):**
  - 74% use "hybrid, blended, or homegrown" models.
  - AI use in agile delivery rose from 68% to 84%, and 41% coordinate AI tools across teams.
  - Only 49% have AI governance guardrails.
  - 41% increased agile spending over two years, and 76% report rising pressure to prove ROI.
  - The sample is about 350 respondents, mostly coaches and consultants at large enterprises, so it is **not representative of startups**.
  - Sources: [Digital.ai press release, official](https://digital.ai/press-releases/digital-ais-18th-state-of-agile-report-marks-the-start-of-the-fourth-wave-of-software-delivery/); [Report PDF, official](https://info.digital.ai/rs/981-LQX-968/images/Digital-ai-18th-State-of-Agile.pdf); [IntelligentCIO coverage, news](https://www.intelligentcio.com/north-america/2025/10/28/digital-ais-18th-state-of-agile-report-marks-the-start-of-the-fourth-wave-of-software-delivery/)
- Three more 18th-report figures appear only in a Scrum.org summary: SAFe usage "rebounded to 44%", 63% see declining software quality, and only 15% of business leaders participate meaningfully in agile practices. — [Scrum.org blog, secondary/practitioner org](https://www.scrum.org/resources/blog/18th-state-agile-report)
- **Stack Overflow Developer Survey 2024:** Jira is the most-used asynchronous/collaboration tool for the third year running. It rose from 52.37% (2023) to 57.5% (2024), with Confluence at 35.3%. Linear and Shortcut "have not gained a significant share just yet", which is qualitative; no Linear percentage was found. — [getint.io blog, secondary](https://www.getint.io/blog/stack-overflow-developer-survey-2024-jira-leads-the-way); [RDEL Substack analysis, newsletter](https://rdel.substack.com/p/rdel-56-analyzing-the-2024-stack); [Stack Overflow survey 2024, official](https://survey.stackoverflow.co/2024/)
- **Pragmatic Engineer 2025 reader survey (~3,000 responses):** Jira and Linear together account for close to 75% of project-management tooling mentions. The audience skews toward tech companies and startups, so it is not comparable to Stack Overflow. — [Pragmatic Engineer newsletter, newsletter](https://newsletter.pragmaticengineer.com/p/the-pragmatic-engineer-2025-survey-part-2)
- **Pragmatic Engineer 2021 survey (100+ responses; OLDER, flagged):** Big Tech teams generally don't use Scrum; engineers lead projects and team process varies. Scrum is "common for large, non-tech companies, non-venture funded companies and consultancies". Shape Up appears at a few venture-funded companies. — [Pragmatic Engineer, "How Big Tech Runs Tech Projects and the Curious Absence of Scrum", newsletter, Sept 2021](https://newsletter.pragmaticengineer.com/p/project-management-in-tech); [HN discussion](https://news.ycombinator.com/item?id=31705526)
- **"59% of teams still run two-week sprints, declining every year since 2022":** this claim, attributed to State of Agile, appeared only in a low-quality pages.dev blog. **Unverified; do not use without checking the primary report.** — [maail-io pages.dev blog, low-quality](https://maail-io.pages.dev/blog/the-age-of-sprints-in-tech-is-dead)

### Inferences
- "Agile" is close to universal, but the strongest recent signal is the move to *hybrid/homegrown* processes (74%). That fits the practitioner view that startups run "Scrum-inspired" processes rather than by-the-book Scrum.
- Jira's ~57% share shows sprint-capable tooling is ubiquitous, but tool use does not prove Scrum use: many teams run Kanban boards in Jira.
- VC-backed startups appear less likely than enterprises or consultancies to run formal Scrum, per Pragmatic Engineer's 2021 data, though that data is dated.

### Gaps
- No survey found that segments Scrum or sprint adoption by *startup stage* (seed, Series A, growth).
- The 17th and 18th State of Agile Scrum-specific percentages could not be verified from the primary PDF because fetches were blocked.
- The Stack Overflow 2024 or 2025 Linear percentage was not found.
- No data was found on sprint length distribution (1 vs 2 vs 3+ weeks) from a reliable survey.

## 2. How do startups modify sprints?

### Takeaway
The common pattern is "agile-ish": keep a short cadence (1–2 weeks) and a lightweight sync. Teams drop or minimise story points, formal velocity tracking and heavy ceremonies. They often move to Kanban/"Scrumban", async Slack standups, or longer appetite-based cycles (Shape Up's 6+2 weeks). A 2025–26 wave of opinion pieces argues AI coding agents are further eroding the fixed two-week sprint, but the evidence is weak.

### Cited Findings
- **Default cadence:** Atlassian's official Jira docs recommend "a fixed two-week duration for each sprint" for teams new to sprints. Its sprint-cadence guide calls two weeks the most common Scrum duration and advises starting there and adjusting. — [Atlassian, "What is a sprint?", official](https://support.atlassian.com/jira-software-cloud/docs/what-is-a-sprint); [Atlassian sprint cadence guide, official](https://www.atlassian.com/agile/project-management/sprint-cadence)
- Atlassian-derived material says the daily standup should be ≤15 minutes and is "not a full status meeting". No Atlassian page prescribing standup frequency was found. — [Atlassian Jira Server docs, official](https://confluence.atlassian.com/jirasoftwareserver102/planning-your-sprint-1473872311.html) (via search snippet)
- **Linear "cycles" as a lighter sprint:**
  - Linear's docs describe cycles as "a practice to keep up your team's momentum, similar to commonly used agile-flavored sprints" that "can last anywhere from 1-8 weeks".
  - Unfinished issues roll over automatically rather than counting as failures.
  - Cycles are not tied to release goals.
  - Source: [Linear docs, Use cycles, official](https://linear.app/docs/use-cycles.md); [Linear Method docs, official](https://linear.app/docs/linear-method)
- **Linear estimation is optional:** capacity is computed from the previous three completed cycles, using either issue count or estimate points. — [Linear docs, official](https://linear.app/docs/use-cycles.md) (via search snippet). The claim that "Linear PMs avoid story points / estimation is a poor use of time" comes only from a third-party blog. — [ideaplan.io, "How a PM ships at Linear", secondary blog](https://www.ideaplan.io/blog/how-a-pm-ships-at-linear). Other Linear-using teams do use points, e.g. one handbook targets ~50 points per cycle. — [engbook pages.dev, practitioner handbook](https://engbook.pages.dev/culture-&-workflow/linear-cycles)
- **Example of a startup using Linear-style cycles:** Plus (plusdocs.com) describes running engineering "cycles". — [Plus blog, company blog](https://www.plusdocs.com/blog/how-we-use-engineering-cycles)
- **Shape Up (Basecamp) as the alternative:**
  - The method uses 6-week build cycles plus a 2-week cool-down, with no backlog and no story points.
  - Scope varies to fit a fixed time "appetite".
  - Adopters include Babylist ("cycles instead of sprints"), Beam Dental (engineer's perspective on switching from Scrum), and a manager.dev write-up of a year without sprints.
  - Sources: [Babylist on Built In, company profile](https://builtin.com/articles/why-engineers-at-Babylist-work-cycles-instead-of-sprints); [Beam Dental on Medium, Medium](https://medium.com/beamdental/an-engineers-perspective-on-switching-from-scrum-to-shape-up-cc9ff6d83f3); [manager.dev, newsletter](https://managerdotdev.beehiiv.com/p/dropping-sprints-a-year-with-shape-up); [Marmelab, Sept 2024, blog](https://marmelab.com/blog/2024/09/26/shape-up.html)
  - No adoption statistics were found.
- **Kanban/Scrumban migrations:** Spendesk documents moving "from a scrum-based Agile methodology to Kanban". — [Spendesk engineering blog, company blog](https://engineering.spendesk.com/posts/our-migration-from-sprints-to-kanban/). An Atlassian Community article describes a team adopting Scrumban instead of dropping Scrum entirely. — [Atlassian Community, "How Scrum became a burden and what we did about it", community post](https://community.atlassian.com/forums/App-Central-articles/How-Scrum-became-a-burden-and-what-we-did-about-it/ba-p/3133342)
- **Dropping story points:**
  - Doctolib published "Why Scrum and Story Points Are Not for Everyone". — [Doctolib Engineering on Medium, Medium/company](https://medium.com/doctolib/why-scrum-and-story-points-are-not-for-everyone-ff0ecb7ddd64)
  - Wealize wrote about why it "ditched story points to be more feature-oriented". — [dev.to, blog](https://dev.to/wealize/why-we-ditched-story-points-to-be-more-feature-oriented-3i1i)
  - thoughtbot notes that story points are "not a requirement to effectively prioritize features". — [thoughtbot blog, consultancy blog](https://thoughtbot.com/blog/the-real-story-behind-story-points.md)
- **Async standups:**
  - Geekbot, a Slack standup bot built in 2015 by a 7-person remote team, claims the standup takes "5 mins or less" in Slack.
  - Customer stories cite Zapier and GitHub's Services Programs team.
  - **Vendor claims, not independent evidence.**
  - Sources: [Geekbot, agile distributed teams, vendor blog](https://geekbot.com/blog/agile-distributed-teams); [Geekbot Zapier customer story, vendor](https://geekbot.com/customer-story/zapier-keeps-the-work-flowing-with-geekbots-asynchronous-stand-ups/); [Geekbot GitHub customer story, vendor](https://geekbot.com/customer-story/why-githubs-distributed-team-prefers-slack-based-standups/)
  - Alternatives include Dailybot, Standuply and Pulses. — [standup bot comparison, pages.dev aggregator, Mar 2026](https://remote-work-tools.pages.dev/standup-bot-comparison-for-remote-engineering-teams)
- **AI-era pressure on two-week sprints (2025–26):**
  - Opinion pieces argue that AI coding agents shift the bottleneck from writing code to review and validation, which undermines fixed two-week cadences.
  - Others argue the two-week window stays, with multiple generate/review loops inside it.
  - All are opinion with weak or no data.
  - Sources: [HackerNoon, "AI coding agents are breaking the two-week sprint", blog](https://hackernoon.com/ai-coding-agents-are-breaking-the-two-week-sprint); ["The death of the two-week sprint", Invide Labs blog](https://hn.jakechampion.name/reader/https://blog.invidelabs.com/the-death-of-the-two-week-sprint); ["The 1-Day Sprint", personal site](https://sites.google.com/medeis.ai/berndschoner/articles/the-1-day-sprint)

### Inferences
- Startup adaptations cluster on three axes. **Cadence:** 1–2 week cycles, or 6-week Shape Up. **Estimation:** none, issue-count, or T-shirt sizing instead of story points. **Ceremony weight:** async or short standups, merged planning and retro, no dedicated Scrum Master.
- Tools encode these choices: Linear's auto-rollover and optional estimates make the "lightweight sprint" the default for teams that adopt it.

### Gaps
- No quantitative data on the share of startups using 1-week vs 2-week sprints, async vs sync standups, or no estimation.
- Linear's own "Linear Method" principles text could not be fetched (linear.app was blocked). Only docs snippets are available.

## 3. Concrete company and organisation examples

### Takeaway
Primary examples include YC's own guidance (Michael Seibel's two-week product cycle at Socialcam; "agile-ish" advice), Linear's cycles, Atlassian's two-week default, and Shape Up adopters (Basecamp, Babylist, Beam Dental). The Spotify model, often copied by startups, was debunked by a former Spotify PM in 2020, an older but still widely cited critique.

### Cited Findings
- **YC / Michael Seibel, "Product Development Cycle Fundamentals" (2016; OLDER, flagged):**
  - Cycle length should follow the product; at Socialcam (iOS) a **two-week cycle** left room for App Store testing.
  - Each cycle opened with a product meeting choosing one focus goal (e.g. new users, retention).
  - Ideas were sorted easy/medium/hard and prioritised by impact, then written up as specs.
  - Engineers then built quietly on pre-specified work, and the last ~3 days were for testing.
  - Arguing, skipping written specs, or long cycles are called mistakes.
  - Source: [YC blog, official](https://www.ycombinator.com/blog/product-development-cycle-fundamentals)
- **YC, "How to build product as a small startup" (Seibel, Dec 2019; OLDER):** — [YC blog, official](https://blog.ycombinator.com/how-to-build-product-as-a-small-startup/)
- **YC's essential advice:** the most important early tasks are to "write code and talk to users". — [YC Essential Startup Advice, official](https://www.ycombinator.com/blog/ycs-essential-startup-advice/)
- A summary of YC's "Tips for technical startup founders" Startup School talk advises an "agile-ish" approach: take the elements that work and evolve process as complexity grows. — [summify.io summary, secondary, unverified wording](https://summify.io/discover/tips-for-technical-startup-founders-startup-school-rP7bpY)
- **Spotify model critique:**
  - Jeremiah Lee (ex-Spotify PM, later Stripe) wrote "Failed #SquadGoals: Spotify doesn't use 'the Spotify model' and neither should you" (Apr 2020; OLDER, flagged). He argues the squads/tribes model was aspirational, never fully implemented, and had matrix-management problems.
  - Simon Willison summarised it as "cross-functional teams with too much autonomy and a poor management structure".
  - Lee later discussed it on DX's Engineering Enablement podcast.
  - Deloitte Poland's agile podcast counters that Spotify keeps evolving the model.
  - Sources: [jeremiahlee.com, personal blog](https://www.jeremiahlee.com/posts/failed-squad-goals/); [Simon Willison's weblog, blog](https://blog.simonwillison.net/2020/Apr/24/); [Engineering Enablement podcast, podcast](https://engineering-enablement.transistor.fm/episodes/spotify-s-failed-squadgoals-jeremiah-lee-spotify-stripe); [Business of Software, blog](https://businessofsoftware.org/2020/06/lessons-critique-spotifys-failed-squad-model/); [Arguing Agile podcast ep. 246, podcast](https://www.buzzsprout.com/1781319/episodes/18582039-aa246-the-spotify-model-the-viral-org-design-that-never-existed)
- **Linear, Atlassian, Shape Up adopters (Babylist, Beam Dental), Spendesk and Doctolib:** see Section 2 for citations.
- **Gergely Orosz at Skype (via the 2021 Pragmatic Engineer piece):** the team "stopped caring about sprints, and dropped most rituals". The argument is that teams shipping more often than their sprint length tend to drop Scrum. — [Pragmatic Engineer, newsletter](https://newsletter.pragmaticengineer.com/p/project-management-in-tech)

### Inferences
- YC's canonical guidance is essentially a lightweight, goal-driven two-week cycle (one focus goal, written specs, testing buffer) rather than formal Scrum. It is older (2016) but remains the reference point YC still publishes.
- The Spotify critique is a common warning against startups copying org-design frameworks wholesale.

### Gaps
- No 2024–26 primary YC post specifically about sprints was found.
- No primary 2024–26 engineering-blog post from a named seed or Series A startup describing its exact sprint ceremonies was found, apart from Plus. Most examples are 2019–2023 or undated.

## 4. Practitioner complaints and praise (Reddit, Medium, LinkedIn, YouTube)

### Takeaway
Practitioner sentiment leans skeptical of full Scrum for small startup teams. Common complaints are ceremony overhead, story-point theatre, and sprints clashing with founders changing priorities. The pragmatic consensus is "use the parts that help": standups, refinement, short cycles, Kanban flow. Defenders say Scrum works when the team is engaged, building a product, and facing competing requests.

### Cited Findings
- **Reddit (via a mirror, since reddit.com was not reached directly), 2026 threads:**
  - One commenter runs "Scranban": keeps dailies and refinements but drops sprints, saying "Sprints are garbage".
  - Another says small, aligned teams can replace ceremony with clear goals, and process mostly exists to coordinate communication as orgs grow.
  - A third says most teams run a "scrum inspired custom tailored process", not real Scrum, and that sprints only make sense if the whole team is engaged and the output is a product.
  - Source: [reddit.sentinel-team.org snapshot, Mar 2026, Reddit mirror](https://reddit.sentinel-team.org/posts/1rq16fl/snapshots/2026-03-11T15%3A10%3A00.908203Z); [snapshot, Feb 2026](https://reddit.sentinel-team.org/posts/1raz8zq/snapshots/2026-02-23T18%3A54%3A29.104875Z); [snapshot, Feb 2026](https://reddit.sentinel-team.org/posts/1rdpw0g/snapshots/2026-02-26T07%3A51%3A49.201817Z)
  - Exact subreddits could not be confirmed from snippets.
- **Counterpoint on Reddit:** one commenter says Scrum worked well for a small product team inside a big company with autonomy and budget. Another says Scrum "promotes a high level of collaboration and communication", which is useful for small teams. — [Reddit mirror snapshot](https://reddit.sentinel-team.org/posts/1s87p0k/snapshots/2026-03-31T05%3A04%3A24.228137Z); [Xebia blog](https://xebia.com/blog/how-to-use-scrum-for-small-development-teams/)
- **dev.to posts:**
  - A two-week sprint-planning ceremony is overhead when a founder can change priorities mid-day. — [dev.to, "Does Scrum even make sense for small startup teams?", blog](https://dev.to/michaeljauk/does-scrum-even-make-sense-for-small-startup-teams-388c)
  - "Agile works for startups, agile ceremonies don't". — [dev.to, blog](https://dev.to/khalfankm7/agile-works-for-startups-agile-ceremonies-dont-heres-the-difference-5b00)
  - "Why Scrum fails in small teams". — [dev.to, blog](https://dev.to/jurijtokarski/why-scrum-fails-in-small-teams-25a6)
- **Story-point criticism:**
  - Sprints plus story points "breed mediocrity" because nobody wants to carry stories over between sprints.
  - One engineering manager says points are a waste for teams under ~20 engineers.
  - Sources: [kilabit.info, "Story points: what is the point", 2022, blog](https://kilabit.info/journal/2022/story_points_what_is_the_point); [dev.to criticism of Scrum, blog](https://dev.to/ragnarkon/a-criticism-of-scrum-21al)
  - The <20 engineers attribution came via a search summary; the exact source page is unclear.
- **Hacker News:** the discussion of Orosz's "curious absence of Scrum" piece includes commenters saying Scrum implementations range from "lightweight and team-driven" to "heavyweight and dysfunctional", so labelling Scrum heavyweight is unfair. — [HN thread, forum](https://news.ycombinator.com/item?id=31705526); [End of Line blog, "Big Tech uses neither Agile nor Waterfall", blog](https://www.endoflineblog.com/big-tech-uses-neither-agile-nor-waterfall)
- **YouTube:** "Big Tech No Scrum" video. — [YouTube](https://www.youtube.com/watch?v=VXwIW4DSUhA) (content not reviewed)
- **Linear vs Jira sentiment (2025–26 comparison blogs, low authority):** Linear is recommended for startups valuing speed and developer experience over deep configuration. Jira sprints offer planning, burndown and velocity, but feel heavier. Switching costs include replacing Confluence and integrations. — [eesel.ai, vendor blog](https://www.eesel.ai/blog/linear-vs-jira); [Everhour, vendor blog](https://everhour.com/blog/linear-vs-jira/); [Dustin Diaz, "Leveling up Engineering Productivity with Linear", newsletter](https://culture-of-eng.dustindiaz.com/p/engineering-productivity-linear)

### Inferences
- The dominant complaint is overhead relative to team size and how fast priorities change. The dominant praise is predictability and a forced shared rhythm.
- The "Scrum-inspired custom process" description in Reddit threads matches the State of Agile's 74% hybrid/homegrown figure.

### Gaps
- reddit.com, LinkedIn and YouTube content could not be accessed directly. The Reddit evidence comes from a mirror site, and subreddit attribution (r/startups vs r/ExperiencedDevs vs r/scrum) is unconfirmed.
- No LinkedIn posts with verifiable content were found.
- No systematic sentiment analysis exists; everything here is anecdotal.
