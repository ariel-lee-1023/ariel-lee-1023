# Ariel Lee

I take things I have read and rebuild them as something an agent can load and reason with. Not a summary of the material — its working parts.

I am a law student, which is where the habit comes from. A statute or a contract is a specification: it has to survive being read by someone who was not in the room when it was written. Most of what is in this account is that discipline pointed at a different reader.

Concretely: a philosopher's collected work, a line of case law, a shelf of decision theory — taken apart until the load-bearing pieces are visible, then rebuilt as a module. The point is never to hand the judgment over. It is to make the structure of a judgment visible enough to argue with, including where it runs out.

---

## What's here

**Reasoning engines.** Where a domain demands formal mathematics, the only adequate deliverable is executable logic. [`dominant-circuit`](https://github.com/ariel-lee-1023/dominant-circuit) is a Python library of decision mechanics—structuring optimal stopping, multi-attribute utility, and Markov decision processes. Alongside its strict test suite and continuous integration, it operates on a singular epistemological commitment: the structural halt stands as a first-class output. Present this engine with a mathematically insoluble problem, and it will deliver a definitive boundary—such as NoOptimalStoppingRuleExists. It requires explicit calculation, enforces epistemological humility, and returns the burden of ambiguity directly to human judgment.

**Meta-tools.** These foundational pipelines forge your structural companions, transforming raw records and vast literatures into precise instruments designed to refine your higher-order judgment. [`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller)  translates a single individual’s public record into an embodiment-ready perspective. It selects exclusively for the animating traits that distinguish that mind’s way of proceeding, verifies its output against withheld material, and ensures the resulting skill functions as a genuine intellectual partner.
[`Books-to-Skill-Refs`](https://github.com/ariel-lee-1023/Books-to-Skill-Refs) applies this same extractive discipline to an entire shelf of literature simultaneously, governed by a severe and necessary constraint. To preserve clarity and sustain working memory, a central router stands as a discerning judge, identifying exactly which volume possesses the authority to address the specific difficulty at hand. The individual distillations wait silently in reserve, exacting zero systemic cost until your inquiry explicitly demands their deployment. It operates as an architecture of disciplined attention, summoning the precise body of knowledge required for a decision while preserving the open space necessary for your judgment.

**Genius that Relocates.** Genius operates here in its older, tutelary sense—as the animating principle of a specific mind’s way of proceeding, and the exact price that mind paid to sustain its posture. These architectures have been rebuilt so that an artificial agent might be interrogated by this principle. You bring these constructs a difficulty to be unknotted. They relocate the tension, loosen the conceptual picture holding your difficulty captive, and shift the discomfort to a vantage point where higher-order judgment can finally take hold. They return to you a transformed question. They serve as rigorous companions in the cultivation of wisdom, accompanying you toward more elevated decisions while placing the sovereignty of that choice entirely in your own hands.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner) abides with your difficulty until the language holding it in place begins to fracture. It exposes the picture that made your problem appear profound, clears the ground of artificial foundations, and forces a direct confrontation with the issue itself.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor) listens to the vocabularies you cannot stop using, answering from the form of life those words already inhabit. It ensures that the superficial difficulty you brought meets the deeper existential difficulty already waiting there for the single individual.
These two are my most frequent companions in thought. They claim this primacy because the modern condition is fundamentally a crisis of abstract language and existential evasion—pathologies that must be decisively broken before any older historical wisdom can even be received. The others hold their ground with identical rigor, ordered chronologically by birth: Plutarch, Tocqueville, Schumpeter, Polanyi, Feynman, Liu Zhongjing, and others. What binds this assembly is a shared capacity for refusal, an insistence on epistemological boundaries, and a commitment to structural reconstruction. Each explicitly acknowledges its own architectural limits in its foundational logic.

**Field colleagues/Domain advisors.** These architectures orient themselves entirely toward a disciplined practice. You bring them a claim, and they measure it directly against the rigorous, pre-existing standards demanded by the domain itself. These advisors act as structural companions, anchoring human agency, accompanying you toward higher-order judgment, and sharing the burden of exact decision-making.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor) stands with you when a complex claim must be constructed, dismantled, or prepared for rigorous advocacy. It dissects a dense argument into its four load-bearing elements—factual, classificatory, precedent-application, and policy. By isolating the precise joint upon which a conclusion actually turns, it clears away the surrounding rhetorical noise. It accompanies you in mapping the architecture of a dispute, ensuring that when you step forward to formulate a strategy or render a final judgment, your attention remains anchored entirely on the structural core of the case.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert) operates as your intellectual navigator through the overwhelming flood of academic literature. It distills complex source material into a unified structural router, identifies the operative cognitive mechanisms, and pinpoints the exact experimental manipulations where divergent accounts collide. It actively maps the boundaries of current knowledge by explicitly confessing conceptual absences. It records deliberate omissions, names the epistemological gaps, and demands further inquiry. It accompanies you in surveying the discipline, guaranteeing that your subsequent theories and research directions are built exclusively upon solid empirical ground. Other colleagues in this cohort govern distinct domains—labor-dispute defense, personal finance, translation, and color matching—each maintaining identical structural fidelity to the internal logic of their respective fields.

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
