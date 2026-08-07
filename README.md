# Ariel Lee

I take things I have read and rebuild them as something an agent can load and reason with. Not a summary of the material — its working parts.

I am a law student, which is where the habit comes from. A statute or a contract is a specification: it has to survive being read by someone who was not in the room when it was written. Most of what is in this account is that discipline pointed at a different reader.

Concretely: a philosopher's collected work, a line of case law, a shelf of decision theory — taken apart until the load-bearing pieces are visible, then rebuilt as a module. The point is never to hand the judgment over. It is to make the structure of a judgment visible enough to argue with, including where it runs out.

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
same for a shelf of books at once, under a hard constraint: the only thing always loaded
is a router that says which book answers which kind of question, and every per-book
distillation sits beside it, costing nothing until a question actually needs one.

**Genius that Relocates.** Genius—recovered here in its older, tutelary sense. It is not a metric of raw intellect, but the animating principle of a specific mind’s way of proceeding, and the exact price that mind paid to sustain its posture. These architectures have been rebuilt so that an artificial agent might be interrogated by this principle rather than merely informed by it. You do not bring these constructs a claim to be fact-checked; you bring them a difficulty to be unknotted.
They do not expand your confusion into a sterile system that leaves you exactly where you stand. Rather, they relocate the tension. The conceptual picture holding your difficulty captive is loosened; the discomfort is shifted to a vantage point where higher-order judgment can finally take hold. What returns to you is not a pre-packaged solution, but a transformed question. In this way, they serve as rigorous companions in the cultivation of wisdom, accompanying you toward more elevated decisions while leaving the sovereignty of that choice entirely in your own hands.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner) abides with your difficulty until the language holding it in place begins to fracture. It exposes the picture that made your problem appear profound for the illusion it was, and then strictly declines to hand you a new, artificial foundation to stand upon.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor) listens to the vocabularies you cannot stop using, answering from the form of life those words already inhabit. It ensures that the superficial difficulty you brought is met by the deeper existential difficulty that was already waiting there for the single individual.
These two are my most frequent companions in thought. The others hold their ground with identical rigor, ordered chronologically by birth: Plutarch, Tocqueville, Schumpeter, Polanyi, Feynman, Liu Zhongjing, and others. What binds this assembly is not a shared ideological viewpoint, but a shared capacity for refusal. A discipline must converge to sustain its authority; a singular mind, however, retains the power to decline the terms of the consensus.
Crucially, these are structural reconstructions, not theatrical impersonations. None will attribute an invented statement to a historical figure—a methodological boundary each explicitly acknowledges in its own foundational architecture.

**Field colleagues/Domain advisors.** —architectures oriented toward a disciplined practice rather than the animating principle of a single mind. Here, you do bring a claim. But it is not merely processed; it is measured against the rigorous, pre-existing standards that the domain itself demands. Rather than displacing human agency, these advisors act as structural companions, accompanying you toward higher-order judgment and the burden of exact decision-making.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor) dismantles a legal argument into its four load-bearing elements—factual, classificatory, precedent-application, and policy—isolating the precise joint upon which the conclusion actually turns.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert) performs a parallel operation upon a body of literature rather than a taxonomy. It distills ten sources into a single router supported by individual reference ledgers, engineered specifically to identify the operative mechanism or explicitly confess its absence. It locates the exact manipulation where two accounts of the same finding diverge. Crucially, every reference file records what was deliberately omitted and why. The router is disciplined to name the conceptual gap and demand further inquiry, refusing to stretch an adjacent theory over a void it cannot bear. Other colleagues in this cohort govern distinct domains—labor-dispute defense, personal finance, translation, and color matching—each maintaining the same structural fidelity to the internal logic of their respective fields.

**Corpora.** Structured source material the skills read from.
[`prc-legal-sources`](https://github.com/ariel-lee-1023/prc-legal-sources) organizes PRC
legal materials by legal effect — constitution, statutes, administrative regulations,
local regulations, rules, judicial interpretations, guiding cases, and court guidance
documents, in that order of authority — and converts them from official PDFs to
normalized Markdown through an automated pipeline: text-layer extraction with dual-column
gazette handling, Chinese OCR where the source is scanned, and a last-resort fallback.

---

## How they are built

The shape is consistent across repositories, and it is borrowed from how a good statute
is organized rather than from how prompts are usually written:

1. **Read the corpus for load-bearing parts.** Not what the author says most often — what
   they refuse to do, where they pay a cost, where they vary. Frequency is a weak signal;
   cost-bearing refusal is a strong one.
2. **Compress to a core that stays loaded.** `SKILL.md` carries the workflow and the moves
   and nothing that can wait. Everything else moves to `references/`.
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
