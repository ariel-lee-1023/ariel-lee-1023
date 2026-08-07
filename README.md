# Ariel Lee

I take things I have read and rebuild them as something an agent can load and reason with. Not a summary of the material — its working parts.

I am a law student, which is where the habit comes from. A statute or a contract is a specification: it has to survive being read by someone who was not in the room when it was written. Most of what is in this account is that discipline pointed at a different reader.

Concretely: a philosopher's collected work, a line of case law, a shelf of decision theory — taken apart until the load-bearing pieces are visible, then rebuilt as a module. The point is never to hand the judgment over. It is to make the structure of a judgment visible enough to argue with, including where it runs out.

---

## What's here

**Reasoning engines.** When a problem really is a math problem, prose about it isn't enough — you need code that runs. [`dominant-circuit`](https://github.com/ariel-lee-1023/dominant-circuit) is a Python library for the mechanics of decisions: optimal stopping, multi-attribute utility, and Markov decision processes. It has a strict test suite and continuous integration, and it is built on one commitment: "there is no answer here" counts as a real answer, not a failure. Hand it a problem the math cannot solve and it will tell you so by name — `NoOptimalStoppingRuleExists`, for instance. It makes you supply the numbers explicitly, it won't guess past what those numbers support, and it hands the unresolved part back to you.

**Meta-tools.** These are the tools that build the other tools. Feed in one person's writing, or a whole shelf of books; get back a working instrument.
[`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller) turns one person's published record into a perspective an agent can think from. It picks out what makes that mind's way of working recognizably its own, checks the result against writing the build never saw, and throws out anything general enough to belong to nobody in particular.
[`Books-to-Skill-Refs`](https://github.com/ariel-lee-1023/Books-to-Skill-Refs) does the same for a whole shelf at once. One constraint does most of the design work: a central router decides which book has any business speaking to the question in front of it, and the individual book summaries cost nothing until the router picks one. Ten books take up no more room in context than one.
[`repo-to-project-instructions`](https://github.com/ariel-lee-1023/repo-to-project-instructions) turns a repository into instructions you can paste into a host that can't clone it or run it — a Gem, a Project — so that host gets the routing it could never work out from a link alone.

**Geniuses that relocate the difficulty.** "Genius" here in its older sense: the guiding spirit of a particular mind — how that person proceeded, and what it cost them to keep standing there. Each of these is built so an agent gets questioned *by* that mind rather than made to imitate it.
What comes back is not an answer. It is the same difficulty, moved: the picture that was holding the problem in place gets loosened, and the question returns in a shape you can work on. I reach for these when I can't yet tell what I'm stuck on.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner) stays with a difficulty until the language holding it together starts to come apart — showing the picture that made the problem look deep, and clearing away foundations it never needed.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor) listens for the words I keep reaching for and answers from the way of living those words already belong to, so the problem I brought runs into the one already sitting underneath it.
These two are the ones I use most. My guess at why: what I keep running into is vague abstract language and a habit of dodging the question, and I suspect that has to be dealt with before anything older has a chance of landing.
The rest hold their ground just as firmly. In order of birth: [`Plutarch-perspective`](https://github.com/ariel-lee-1023/Plutarch-perspective) (c. 46), [`tocqueville-investigator`](https://github.com/ariel-lee-1023/tocqueville-investigator) (1805), [`schumpeter-perspective`](https://github.com/ariel-lee-1023/schumpeter-perspective) (1883), [`Polanyi-perspective`](https://github.com/ariel-lee-1023/Polanyi-perspective) (1891), [`feynman-perspective`](https://github.com/ariel-lee-1023/feynman-perspective) (1918), [`Kaplan-perspective`](https://github.com/ariel-lee-1023/Kaplan-perspective) (1952), and [`liu-zhongjing-perspective`](https://github.com/ariel-lee-1023/liu-zhongjing-perspective) (1974).
What they have in common: each will refuse a question rather than answer it badly, each says where its own knowledge stops, and each rebuilds a problem instead of patching it. Each states its own limits in its own instructions.

**Field colleagues and domain advisors.** These face a line of work rather than a mind. They check a claim against the standards the field already applies — which makes them worth having only where those standards are specific enough that a claim can actually fail against them.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor) breaks a dense argument into the four parts carrying the weight — the facts, how they're classified, how precedent applies, and the policy question — and finds the joint the conclusion actually turns on. It is rarely the one the brief spends its length on. I use this before drafting, while the dispute is still a shapeless pile.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert) searches ten sources for the mechanism at issue and names the experiment where competing explanations actually come apart. Its more useful habit is admitting what it doesn't have: it records what its sources don't cover, names the gap instead of filling it with something plausible, and says what would have to be read or run to close it.
The rest each cover one job and keep the same fidelity to how their own field reasons. Listed by what I bring them:

- [`TechLaw-colleague`](https://github.com/ariel-lee-1023/TechLaw-colleague) — reads a product, a data flow, or a contract clause against the rules that actually bind it.
- [`financial-planner`](https://github.com/ariel-lee-1023/financial-planner) — works through a household balance sheet when a decision is big enough to move it: an allocation, a tax treatment, the timing of a purchase.
- [`Color-Matching-Consultant`](https://github.com/ariel-lee-1023/Color-Matching-Consultant) — builds a palette and diagnoses a color that's off, whether it's a slide deck, an outfit, a wall, or a canvas.
- [`soccer-analyst`](https://github.com/ariel-lee-1023/soccer-analyst) — reads a match, a signing, or a wage bill with the economics attached.
- [`English-Chinese-translator`](https://github.com/ariel-lee-1023/English-Chinese-translator) — translates prose between Chinese and English to a standard a publisher would accept, not just one a reader would put up with.
- [`transcript-proofreader`](https://github.com/ariel-lee-1023/transcript-proofreader) — makes a recording readable under edited-verbatim rules, without it stopping being what was actually said.
- [`us-study-advisor-for-law-students`](https://github.com/ariel-lee-1023/us-study-advisor-for-law-students) — handles the American application and the career it's meant to open.
- [`toefl-2026-writing-speaking`](https://github.com/ariel-lee-1023/toefl-2026-writing-speaking) — marks writing and speaking against the 2026 rubric and says where the points are actually going.

**Corpora.** Organized source material that the skills read from. A perspective skill carries how a mind proceeds; the corpus carries what that mind actually said. Keeping the two in separate repositories is what lets an agent be corrected by the record instead of by its own summary of the record. Each corpus is built to be searched first: where it has text that matches, that text governs and the skill gives way to it.
[`prc-legal-sources`](https://github.com/ariel-lee-1023/prc-legal-sources) organizes PRC legal materials by legal force — constitution, statutes, administrative regulations, local regulations, rules, judicial interpretations, guiding cases, and court guidance documents, in that order of authority. An automated pipeline converts them from official PDFs into clean Markdown: it pulls the text layer where there is one (handling two-column gazette layouts), runs Chinese OCR where the source is a scan, and has a last-resort fallback for the rest.
[`Plutarch-Thoughts`](https://github.com/ariel-lee-1023/Plutarch-Thoughts) holds the Plutarch corpus under `content/PT/Works/`. The original works are public domain, but the modern editions used for the conversion may still be in copyright, so the archive is non-commercial.
[`LiuZhongjing-Thoughts`](https://github.com/ariel-lee-1023/LiuZhongjing-Thoughts) holds the Liu Zhongjing corpus (姨學思想) under `content/LZJT/`, split into writings, critiques of historical figures, and lecture transcripts. It pairs with the perspective skill of the same name.

---

## How they are built

The shape is consistent across repositories, and it is borrowed from how a good statute is
organized rather than from how prompts are usually written: a short operative core that is
always in force, definitions and schedules kept out of the way until invoked, and an express
statement of scope that admits what the instrument does not reach.

1. **Read for load-bearing parts, not for themes.** What the author refuses to do, where the
   position costs them something, where they vary and on what. Frequency is a weak signal —
   an author repeats what is easy to say. A refusal that is paid for is a strong one, because
   it marks a commitment held against pressure.
2. **Compress to a core that stays loaded.** `SKILL.md` carries the workflow, the moves, and
   nothing that can wait. Anything needed only sometimes goes to `references/`. If a line does
   not change what the agent does on the next turn, it does not belong in the core.
3. **Disclose progressively.** Reference clusters load only when the current move calls for
   them, so base context stays flat whether the source is one book or a shelf of ten. The
   router decides which volume has standing to speak to the difficulty at hand.
4. **Verify against material the build never saw.** Held-out projection tests, citation
   resolution against the corpus, corpus-drift guards that fail when a reference outruns its
   source. Where there are numbers, golden oracles under continuous integration.
5. **Say when the material runs out.** Every skill can report that a question falls outside
   what its sources cover, and in the formal domains it returns a structural halt rather than
   a plausible guess. This is the part most worth keeping: a boundary stated in the output is
   what returns the judgment to the person who has to live with it.

Provenance is tracked in `NOTICE.md` and `references/provenance.md` in each repository.
Everything original is MIT-licensed; the license does not extend to the underlying source
works, which remain with their copyright holders, and no repository reproduces them beyond
short anchors kept for auditing.

---

## Using them

Any host that reads a skills directory:

```bash
git clone https://github.com/ariel-lee-1023/<repository>.git \
  ~/.claude/skills/<repository>
```

The skill is discovered from its frontmatter `name` and `description`; nothing else is
required. For Claude.ai or the API, zip the directory (or package it as a `.skill` file),
keeping the structure intact so the `references/` paths still resolve.

Issues and pull requests are welcome. The most useful ones are worked examples that expose
a failure the taxonomy does not yet catch, and corrections where a reference file overstates
a contested proposition.

---

*Not legal advice. These are reasoning aids: they are built to make the structure of a
problem visible, including where it runs out — not to tell you the answer.*
