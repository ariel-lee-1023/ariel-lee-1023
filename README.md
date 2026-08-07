# Ariel Lee

I take things I have read and rebuild them as something an agent can load and reason with. Not a summary of the material — its working parts.

I am a law student, which is where the habit comes from. A statute or a contract is a specification: it has to survive being read by someone who was not in the room when it was written. Most of what is in this account is that discipline pointed at a different reader.

Concretely: a philosopher's collected work, a line of case law, a shelf of decision theory — taken apart until the load-bearing pieces are visible, then rebuilt as a module. The point is never to hand the judgment over. It is to make the structure of a judgment visible enough to argue with, including where it runs out.

---

## What's here

**Reasoning engines.** Where a domain demands formal mathematics, the only adequate deliverable is executable logic. [`dominant-circuit`](https://github.com/ariel-lee-1023/dominant-circuit) is a Python library of decision mechanics—structuring optimal stopping, multi-attribute utility, and Markov decision processes. Alongside its strict test suite and continuous integration, it operates on a singular epistemological commitment: the structural halt stands as a first-class output. Present this engine with a mathematically insoluble problem, and it will deliver a definitive boundary—such as NoOptimalStoppingRuleExists. It requires explicit calculation, enforces epistemological humility, and returns the burden of ambiguity directly to human judgment.

**Meta-tools.** These are the pipelines that build the rest — a raw record or a shelf of literature in, an instrument out. [`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller) translates a single individual’s public record into an embodiment-ready perspective. It selects for the traits that distinguish that mind’s way of proceeding, verifies the result against material the build never saw, and drops whatever is generic enough to belong to no one.
[`Books-to-Skill-Refs`](https://github.com/ariel-lee-1023/Books-to-Skill-Refs) applies the same discipline to a whole shelf at once, under the constraint that does most of the design work: a central router decides which volume has standing to speak to the difficulty at hand, and the individual distillations cost nothing until it calls one. Ten books stay as flat in context as one.
[`repo-to-project-instructions`](https://github.com/ariel-lee-1023/repo-to-project-instructions) compiles a repository into paste-ready instructions for hosts that can neither clone nor execute it, supplying the routing layer a Gem or Project cannot derive from a link alone.

**Genius that Relocates.** Genius operates here in its older, tutelary sense — the animating principle of a specific mind’s way of proceeding, and the price that mind paid to hold its posture. Each is rebuilt so that an agent can be interrogated by that principle rather than made to imitate it. What comes back is not an answer but a relocated difficulty: the conceptual picture holding the problem in place is loosened, and the question returns in a form that can be worked on. I reach for these when I cannot yet tell what I am stuck on.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner) stays with a difficulty until the language holding it in place begins to fracture, exposing the picture that made the problem look profound and clearing the ground of foundations it never needed.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor) listens to the vocabulary I cannot stop using and answers from the form of life those words already inhabit, so that the difficulty I brought meets the one already waiting under it for the single individual.
These two are my most frequent companions in thought. They claim this primacy because the modern condition is fundamentally a crisis of abstract language and existential evasion—pathologies that must be decisively broken before any older historical wisdom can even be received. The others hold their ground with identical rigor, ordered chronologically by birth: [`Plutarch-perspective`](https://github.com/ariel-lee-1023/Plutarch-perspective) (c. 46), [`tocqueville-investigator`](https://github.com/ariel-lee-1023/tocqueville-investigator) (1805), [`schumpeter-perspective`](https://github.com/ariel-lee-1023/schumpeter-perspective) (1883), [`Polanyi-perspective`](https://github.com/ariel-lee-1023/Polanyi-perspective) (1891), [`feynman-perspective`](https://github.com/ariel-lee-1023/feynman-perspective) (1918), [`Kaplan-perspective`](https://github.com/ariel-lee-1023/Kaplan-perspective) (1952), and [`liu-zhongjing-perspective`](https://github.com/ariel-lee-1023/liu-zhongjing-perspective) (1974). What binds this assembly is a shared capacity for refusal, an insistence on epistemological boundaries, and a commitment to structural reconstruction. Each explicitly acknowledges its own architectural limits in its foundational logic.

**Field colleagues&Domain advisors.** These face a practice rather than a mind. They measure a claim against the standards the domain already enforces, which makes them worth having only where those standards are specific enough for a claim to fail against.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor) dissects a dense argument into its four load-bearing elements — factual, classificatory, precedent-application, and policy — and isolates the joint the conclusion actually turns on, which is rarely the one the briefing spends its length on. I use it before drafting, while the dispute is still an undifferentiated mass.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert) routes across ten sources to the mechanism at issue and names the experimental manipulation where competing accounts actually diverge. Its more useful habit is the confession: it records what its sources do not cover, names the gap rather than filling it with a plausible account, and says what would have to be read or run to close it.
The rest of the cohort each holds a single post and keeps the same fidelity to the internal logic of its own field. Named by what I take to them: [`TechLaw-colleague`](https://github.com/ariel-lee-1023/TechLaw-colleague) reads a product, a data flow, or a clause against the regimes that actually bind it. [`financial-planner`](https://github.com/ariel-lee-1023/financial-planner) works a household balance sheet when a decision is large enough to move it — an allocation, a tax treatment, the timing of a purchase. [`Color-Matching-Consultant`](https://github.com/ariel-lee-1023/Color-Matching-Consultant) builds a palette and diagnoses a color that is off, whether the surface is a slide deck, an outfit, a wall, or a canvas. [`soccer-analyst`](https://github.com/ariel-lee-1023/soccer-analyst) reads a match, a signing, or a wage bill with the economics attached. [`English-Chinese-translator`](https://github.com/ariel-lee-1023/English-Chinese-translator) carries Chinese↔English prose to the standard a publisher would accept rather than the one a reader would tolerate. [`transcript-proofreader`](https://github.com/ariel-lee-1023/transcript-proofreader) makes a recording readable under edited-verbatim discipline, without letting it stop being what was said. [`us-study-advisor-for-law-students`](https://github.com/ariel-lee-1023/us-study-advisor-for-law-students) handles the American application and the career it is supposed to open. [`toefl-2026-writing-speaking`](https://github.com/ariel-lee-1023/toefl-2026-writing-speaking) marks writing and speaking against the 2026 rubric and says where the score is actually lost.

**Corpora.** Structured source material the skills read from. A perspective skill carries the
way a mind proceeds; the corpus carries what it actually said. Keeping them in separate
repositories is what lets an agent be corrected by the record instead of by its own paraphrase
of the record. Each is a search-first tree: where the corpus has matching text, that text
governs, and the skill yields to it. [`prc-legal-sources`](https://github.com/ariel-lee-1023/prc-legal-sources) organizes PRC
legal materials by legal effect — constitution, statutes, administrative regulations,
local regulations, rules, judicial interpretations, guiding cases, and court guidance
documents, in that order of authority — and converts them from official PDFs to
normalized Markdown through an automated pipeline: text-layer extraction with dual-column
gazette handling, Chinese OCR where the source is scanned, and a last-resort fallback.
[`Plutarch-Thoughts`](https://github.com/ariel-lee-1023/Plutarch-Thoughts) holds the Plutarchan
corpus under `content/PT/Works/`; the original works are public domain, while the modern
editions used for conversion may remain in copyright, so the archive is non-commercial.
[`LiuZhongjing-Thoughts`](https://github.com/ariel-lee-1023/LiuZhongjing-Thoughts) holds the
Liu Zhongjing corpus (姨學思想) under `content/LZJT/`, split into writings, critiques of
historical figures, and lecture transcripts, and pairs with the perspective skill of the same
name.

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
