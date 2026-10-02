# Bryan Wudarsky

Financial Analysis · Business Analysis · Operations

Tampa Bay, FL | bryanwudarsky@gmail.com | [linkedin.com/in/bryanwudarsky](https://www.linkedin.com/in/bryanwudarsky)
Portfolio: [bryanwudarsky-lab.github.io](https://bryanwudarsky-lab.github.io)

I'm a Tampa-raised USF business graduate (B.S. Personal Financial Planning and B.S. Marketing),
back home in Tampa Bay and looking for a company to grow with for the long haul, in financial
analysis, business analysis, or operations. I turn messy numbers into clear decisions, in English
or Spanish. My experience: relationship banking at Truist (115%+ of performance goals, $1M+ in
deposits), a business and finance program I led for 150+ participants a year (100% certification
pass rate two years running, against a 66% national average), service operations at Geek Squad
(a 25% productivity gain and repair turnaround cut by a day), and a resale business I ran to
$35K+ in revenue at ~50% margins across 1,000+ transactions.

My finance and market analysis, including a Florida grocery market-entry study and two costed
Florida policy briefs, lives on my portfolio. This GitHub holds the technical side: process
write-ups for software tools I design, build, and test myself, with AI coding assistance for
implementation.

## What the write-ups show

Each repository documents one system: what it does, how I built it, what broke, and what changed
because of it. They show the habits I bring to analysis work. I define requirements in writing,
measure results instead of assuming them, and keep a dated record of every decision. The "what
broke" sections are the ones I would read first.

The August 2026 documentation snapshot records about 13,800 lines of TypeScript, 31 API routes,
and 17 SQLite tables for my self-hosted job dashboard, Agentic OS. The game-engineering notes
record 52,267 lines of Luau and 764 headless tests on one project, 2,814 assertions across 79 spec files on one prototype and 7,991 assertions across 173 test
files on a third. The two games in my portfolio are private development prototypes; version counts describe
development and test builds.

## How I work

The same loop runs every project, whether the output is a model, a report, or software:

1. A written specification comes first. Decisions made mid-project land in a dated decision log,
   so any number in the result traces back to the ruling that set it.
2. The plan is phased. Each phase delivers something that works end to end, and I verify it
   before the next phase begins.
3. Parallel work runs under a disjoint ownership map, so no two tracks touch the same files.
4. An automated test gate runs on every release. On one game that gate is a 45-step script,
   and 34 of the steps are tripwires, each pinned to a type of error that actually occurred.
5. A separate review pass hunts the errors the tests cannot see. One pre-build review returned
   19 amendments and 2 blocking defects against a spec I had considered ready; the post-build
   review caught 4 more blocking defects that 17 passing spec files had missed.
6. Deliver, then measure. Agentic OS writes every run into a permanent outcome ledger, 20 runs at
   a 60 percent success rate in the August 2026 snapshot. I use those measurements to decide
   where the process needs work.

Step 5 exists because I paid for the lesson: an earlier project reached 540 of 540 passing tests
and still produced a broken build. A passing suite proves the checks I thought to write. The
review pass exists for everything I did not think to check.

## The four repositories

### [agent-orchestration-platform](https://github.com/bryanwudarsky-lab/agent-orchestration-platform)

Agentic OS: a scheduling and monitoring dashboard for my own automated jobs (Next.js, React,
TypeScript, SQLite), deployed with Docker on a TrueNAS server I administer. It shows what ran,
what failed, and what needs another attempt, and every run keeps its own record, so a retry never
erases the first failure. Read it for the outcome ledger design and the four-hour failure that
reshaped how I structure large builds.

### [multiplayer-game-engineering](https://github.com/bryanwudarsky-lab/multiplayer-game-engineering)

Engineering notes from three Roblox projects: an economy game and two private development
prototypes, a round-based team game with asymmetric roles and a progression-based simulator. I wrote the
requirements and the automated test gates. Read it for the four-rung verification ladder and for
the review that caught a balance simulation pricing progression at about 1.8x the real price
table, a compounding error that had inverted the analysis conclusion.

### [ai-video-automation](https://github.com/bryanwudarsky-lab/ai-video-automation)

A local pipeline that turns multi-hour recordings into captioned vertical clips with no per-clip
fee, a shared caption workspace, and a procedural Blender scene built from a written spec. Read it
for measurement overruling the plan: the planned selection threshold selected nothing on real
audio, so the shipped rule derives its threshold from the data itself.

It also covers my patched fork of [OpenMontage](https://github.com/bryanwudarsky-lab/OpenMontage),
an open-source project by [calesthio](https://github.com/calesthio/OpenMontage), with a black-render
fix I verified by frame luma, 22 to 26 after against 0.0 before.

### [content-production-systems](https://github.com/bryanwudarsky-lab/content-production-systems)

A recurring writing workflow run like a production line: a quality gate that scans every draft
against 15 named writing faults and fails the run the way a failing test fails a build, a weekly
batch job, a retrospective loop that turns lessons into dated rules, and decision gates that
revise strategy on measurements instead of mood.

Where source stays private, each page says why: the dashboard is wired into my personal data, and
the games' server code carries anti-exploit logic I keep unpublished. What transfers is public
above: the process, the numbers, what broke, and what changed.

## Contact

bryanwudarsky@gmail.com | [linkedin.com/in/bryanwudarsky](https://www.linkedin.com/in/bryanwudarsky)
Portfolio: [bryanwudarsky-lab.github.io](https://bryanwudarsky-lab.github.io)

Ask me to walk through any number on this page or the four behind it. Each one has a written
record: the schema, the gate scripts, the incident notes, and the design decisions.
