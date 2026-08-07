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

**Genius that Relocates.** These architectures are rebuilt not to deposit information, but to subject the inquiring agent to examination. You do not bring them a claim seeking verification; you bring them a difficulty. They refuse the modern impulse to absorb that difficulty into a totalizing system—a move that would merely leave you exactly where you stand, comforted by explanation. Instead, they relocate the friction. The conceptual frame holding the problem captive is loosened, the discomfort is shifted to a terrain where human judgment can actually gain purchase, and what is returned to you is a fundamentally altered question. It is a question from which a genuine decision remains possible.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner)
stays with the difficulty until the words that were holding it in place come loose, and the
picture that made it look deep is seen for what it was — then declines to hand you a new
foundation to stand on.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor)
listens to the language you cannot stop using, and answers from the form of life those words
already inhabit — so that the difficulty you brought is met by the one that was already waiting
there for a single individual. Though these two remain the most central to my own practice, the others—arrayed by birth: Plutarch, Tocqueville, Schumpeter, Polanyi, Feynman, Liu Zhongjing, and others—hold their ground by the same methodological discipline. What binds them together is not a unified doctrine, but a shared refusal. An institutional field survives by enforcing convergence; an independent mind proves its vitality by declining it. Finally, these are structural reconstructions of thought, not theatrical impersonations. None will manufacture a quotation or attribute an invented claim to a historical personage, a boundary each explicitly declares in its opening terms.

**Field colleagues/Domain advisors.** The same method aimed at a practice rather than a person. Here you
do bring a claim, and it gets checked against a standard the practice already holds.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor)
sorts a legal argument into four load-bearing moves — factual, classificatory,
precedent-application, policy — to find the joint the conclusion actually turns on.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert)
does the same for a literature rather than a taxonomy: ten sources distilled into one
router plus a reference file each, built to name the mechanism or say it cannot, and to
find the manipulation on which two accounts of one finding diverge. Every reference file
records what was dropped and why, and the router says to name the gap and search rather
than stretch an adjacent chapter over it. Others cover labor-dispute defense, personal
finance, translation, and color matching.

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
