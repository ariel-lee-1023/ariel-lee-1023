# Ariel Lee

I write specifications precise enough that another party can execute expert judgment
without exercising it.

That sentence describes most of what is in this account, and it is also a description of
statutory and contract drafting — which is what I study. I am a law student (LL.B. 2027,
Macau University of Science and Technology), and the repositories here are what happens
when I take that instinct to a different reader: instead of a court or a counterparty,
the thing reading the specification is a model.

Concretely: I take a body of expertise — a philosopher's collected work, a line of case
law, a shelf of decision theory — and rebuild it as a module an agent can load and reason
from. Not a summary of the material. The working parts of it.

---

## What's here

**Reasoning engines.** Where the subject has actual mathematics, the deliverable is code
rather than prose. [`dominant-circuit`](https://github.com/ariel-lee-1023/dominant-circuit)
is a Python decision-mechanics library — optimal stopping, multi-attribute utility,
Markov decision processes — with a test suite, CI, and a design commitment that refusing
to answer is a first-class output: ask it about a problem whose stated assumptions admit
no solution and you get `NoOptimalStoppingRuleExists`, not a plausible number.

**Meta-tools.** The pipelines that produce everything else.
[`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller) turns one
person's public record into an embodiment-ready perspective skill, selecting for the
traits that actually distinguish that person rather than countable surface style, and
verifying the result against held-out material.
[`Books-to-Skill-Refs`](https://github.com/ariel-lee-1023/Books-to-Skill-Refs) does the
same for a shelf of books at once, under a hard constraint: the master router that stays
loaded is capped at roughly 2,500 tokens, and every per-book reference sits beside it,
costing nothing until a question actually needs one. It re-points the extraction engine
from [virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill) (MIT) at
a different output shape; the engine is his, the architecture is mine.

**Perspective skills.** A single thinker's method, reconstructed as a lens an agent can
think through — Wittgenstein, Feynman, Schumpeter, Polanyi, Tocqueville, Plutarch,
Kaplan, and others. These are thinking lenses, not impersonations. None of them will
attribute an invented statement to a real person, and each says so in its own frontmatter.

**Domain advisors.** The same method aimed at professional judgment rather than a person:
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor)
sorts a legal argument into four load-bearing moves — factual, classificatory,
precedent-application, policy — to find the joint the conclusion actually turns on;
[`TechLaw-colleague`](https://github.com/ariel-lee-1023/TechLaw-colleague) runs technology
regulation through institutional, efficiency-refusal, and doctrinal-mechanics passes.
Others cover labor-dispute defense, personal finance, translation, and color matching.

**Corpora.** Structured source material the skills read from.
[`prc-legal-sources`](https://github.com/ariel-lee-1023/prc-legal-sources) organizes PRC
legal materials by legal effect — constitution, statutes, administrative regulations,
local regulations, rules, judicial interpretations, guiding cases, and court guidance
documents, in that order of authority — and converts them from official PDFs to
normalized Markdown through an automated pipeline: text-layer extraction with dual-column
gazette handling, Chinese OCR where the source is scanned, and a last-resort fallback.
The hierarchy is the point; an agent that cites from it cannot silently treat a
departmental rule as a statute.

---

## How they are built

The shape is consistent across repositories, and it is borrowed from how a good statute
is organized rather than from how prompts are usually written:

1. **Read the corpus for load-bearing parts.** Not what the author says most often — what
   they refuse to do, where they pay a cost, where they vary. Frequency is a weak signal;
   cost-bearing refusal is a strong one.
2. **Compress to a core that stays loaded.** `SKILL.md` carries the workflow and the moves
   and stays under a hard size ceiling. Everything else moves to `references/`.
3. **Disclose progressively.** Reference clusters are pulled only when the current move
   needs them, so base context stays small.
4. **Verify.** Held-out projection tests, citation resolution, corpus-drift guards. Where
   there are numbers, golden oracles.
5. **Say when the material runs out.** Every skill has a way to report that the question
   falls outside what its sources cover. This is the part most worth keeping.

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
