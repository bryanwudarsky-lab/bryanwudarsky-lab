# Bryan Wudarsky

Tampa, FL | bryanwudarsky@gmail.com | [linkedin.com/in/bryanwudarsky](https://www.linkedin.com/in/bryanwudarsky)

I am based in Tampa, FL, with B.S. degrees in Personal Financial Planning and Marketing.
I taught business and accounting and worked in hands-on technical service at Geek Squad
from October 2020 to June 2023, then from February 2024 to June 2026. I now build and test
software systems with AI coding assistance. The four repositories below document my
requirements, implementation decisions, testing, and revisions.

## Self-taught, with receipts

I did not come through a CS program. I taught myself software engineering by building and
running real systems, and the discipline came from shipping them: written specifications,
automated test gates, adversarial review, and attended testing. The repositories on this profile are
process documentation for those systems. Each page records what the system does, how I built
it, what broke, and what changed because of it. The "what broke" sections are the ones I would
read first.

The August 2026 documentation snapshot records about 13,800 lines of TypeScript, 31 API
routes, and 17 SQLite tables for the self-hosted agent platform. The game-engineering
documentation records 52,267 lines of Luau and 764 headless tests on one project, and 7,991
assertions across 173 files on another. These are historical engineering measurements.
The two game examples in my current portfolio are private development prototypes; version
counts describe development and test builds.

## How I build

I define requirements, make implementation decisions, and review the result, with AI coding
agents assisting implementation. My workflow follows this loop:

1. A written specification comes first. Agents build against the document, and rulings made
   mid-build land in a committed decision log.
2. The build plan is phased. Each phase ships working features end to end, and I verify it in
   the running system before the next phase begins.
3. Agents build in parallel under a disjoint ownership map, so no two tracks touch the same
   files.
4. An automated test gate runs on every release. On one game that gate is a 45-step script, and
   34 of the steps are tripwires, each pinned to a bug class that actually occurred.
5. Adversarial review hunts the defects the tests cannot see. One pre-code review panel
   returned 19 amendments and 2 blocking-class defects against a spec I had considered ready;
   the post-code panel caught 4 more blocking defects that 17 green spec files had sailed past.
6. Ship, then measure. The platform writes every agent run into an immutable outcome ledger,
   20 runs at a 60 percent success rate in the August 2026 documentation snapshot. I use
   those measurements to identify where the workflow needs improvement.

Step 5 exists because I paid for the lesson: an earlier project reached 540 of 540 passing
tests and still shipped a broken build. A green suite proves the assertions I thought to
write. The review pass exists for everything I did not think to assert.

## The four repositories

### [agent-orchestration-platform](https://github.com/bryanwudarsky-lab/agent-orchestration-platform)

A self-hosted web dashboard (Next.js, React, TypeScript, SQLite) that schedules, launches, and
monitors AI agent runs, deployed with Docker on a TrueNAS server I administer. Read it for the
outcome ledger design and the four-hour multi-agent failure that forced the build structure I
still use. The same machinery runs my week across 22 tracked projects.

### [multiplayer-game-engineering](https://github.com/bryanwudarsky-lab/multiplayer-game-engineering)

Engineering notes from three Roblox projects: an economy game, an asymmetric 5v5
competitive game, and a multiplayer management sim. The portfolio examples remain private
development prototypes. Read the notes for the four-rung verification ladder and for
the ratio it produced: 24,783 lines of verification machinery against 44,890 lines of game
source on the 5v5 game. That ratio was never a target; every failure class found in review
became a permanent check.

### [ai-video-automation](https://github.com/bryanwudarsky-lab/ai-video-automation)

A local pipeline that turns multi-hour footage into finished, captioned vertical clips using local
processing without a per-clip API fee, a Remotion caption workspace, and a Blender scene built procedurally from a
prose spec I wrote to stand in for a photograph the agent could not see. The documented workflow combines automated output checks with visual review.

The one public-source item here is my patched fork of [OpenMontage](https://github.com/bryanwudarsky-lab/OpenMontage), with a black-render fix I verified by frame luma, 22 to 26 after against 0.0 before.

### [content-production-systems](https://github.com/bryanwudarsky-lab/content-production-systems)

A weekly publishing operation run as a production line: a voice gate that scans every draft
against 15 named AI anti-patterns and fails the run the way a failing test fails a build, a
Sunday batch job that drafts the coming week, a retrospective loop that turns session lessons
into dated rules, and decision gates that revise strategy on measurements instead of mood.
Writing is where I proved this workflow before pointing it at code.

Where source stays private, each page says why: the platform is wired into my personal data,
and the games' server code carries anti-exploit logic I keep unpublished. What transfers is
public above: the process, the numbers, what broke, and what changed.

## Contact

bryanwudarsky@gmail.com | [linkedin.com/in/bryanwudarsky](https://www.linkedin.com/in/bryanwudarsky)

Ask me to walk through any number on this page or the four behind it. Each one has a written
record: the schema, the gate scripts, the incident notes, the design decisions.
