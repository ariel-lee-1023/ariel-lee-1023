# Ariel Lee

I read something, take it apart until the load-bearing pieces are visible, and rebuild those pieces as a module an agent can load and reason from. A philosopher's collected work. A line of case law. A shelf of decision theory. What comes out is not a summary. A summary is the part of a book that has stopped doing any work.

The test I use is whether a sentence still does work. That sounds like a low standard. It is not — most sentences fail it. A sentence keeps a grave face long after it has stopped lifting anything, and at that point it is not a claim any more, it is a piece of ideology. So a module has to be executable: loaded, run, tested, and able to report that it has failed. If I cannot say what would count as this module getting something wrong, I have not built a module. I have written an essay with a filename.

The habit comes from law. A statute is a specification — it has to survive being read by someone who was not in the room when it was drafted, sometimes by someone with an interest in reading it badly. But the part worth borrowing is not the drafting technique. It is where the technique came from. Nobody designed it. It settled out of centuries of argument in manor courts and parish vestries, one dispute at a time, and the order came first: the wealth came afterwards and because of it, not the other way round. None of the people in those rooms was holding the theory. Each of them was holding a case.

This is also why there are many small repositories here and no framework. The demand for grain is a fixed quantity — a person eats what a person eats. The demand for cherry pie is not. There are ten thousand cherry pies, and each exists because someone wanted a slightly different thing from one: a status, a memory, a particular Sunday. Niches divide without end, the way language-games divide without end. A single general engine for judgment would not be a more ambitious version of this work. It would be a refusal to look at how finely the real demands divide.

The world is locked tighter than it looks. Concrete survival constraints and the path already taken hold most of it in place, and the room that is left is not distributed evenly — it sits at nodes. At a node the choice matters more than any account of what the choice means, because one wrong turn commits me to a long series of turns I will not get to reconsider. Sensitivity to initial conditions is amplified, not damped. Past the node the path is locked, and the path decides the outcome. This is why refusing to answer is a first-class output in what I build rather than a failure mode. A tool that reports that the stated assumptions admit no solution has done its work. One that returns a plausible number instead has not, because a plausible number at a node is how the wrong path gets taken.

The easiest thing available to me is the excitement of a vocabulary I have not held before. Set the reality I know against an ideal I have only read about and I feel sharper immediately — at no cost, on no ground. I have done this. What it leaves once the novelty wears off is boredom and a directory of files that impressed me on the day I wrote them. So the rule I hold myself to is a narrow one: no word goes into a skill unless I can say what it does. Where I have broken it the file is worse, and I can usually tell, because the tests are thin.

There is no law here yet. New technology is prospector's country — whoever finds the seam first keeps it, and the arrangements that will eventually govern any of this are not written. I notice that I am standing in that country with a law degree in progress, and that both of those facts are doing something. I am not neutral about it, and I do not think the interval lasts.

Telling true from false is not a capacity I can acquire by having a model. It gets paid for the way anything gets paid for: specific effort, on specific material, with the ache that goes along with it. What is scarce is not knowing a great many things. It is picking out, from an unlimited supply of material, the few threads that carry weight. Everything here is built for that and for nothing beyond it — to make the structure of a judgment visible enough to argue with, including the place where it runs out.

---

## What's here

**Reasoning engines.** When a problem really is a math problem, prose about it isn't enough — you need code that runs. [`dominant-circuit`](https://github.com/ariel-lee-1023/dominant-circuit) is a Python library for the mechanics of decisions: optimal stopping, multi-attribute utility, and Markov decision processes. It has a strict test suite and continuous integration, and it is built on one commitment: "there is no answer here" counts as a real answer, not a failure. Hand it a problem the math cannot solve and it will tell you so by name — `NoOptimalStoppingRuleExists`, for instance. It makes you supply the numbers explicitly, it won't guess past what those numbers support, and it hands the unresolved part back to you.

**Meta-tools.** These are the tools that build the other tools. Feed in one person's writing, or a whole shelf of books; get back a working instrument.
[`persona-distiller`](https://github.com/ariel-lee-1023/persona-distiller) turns one person's published record into a perspective an agent can think from. It picks out what makes that mind's way of working recognizably its own, checks the result against writing the build never saw, and throws out anything general enough to belong to nobody in particular.
[`Books-to-Skill-Refs`](https://github.com/ariel-lee-1023/Books-to-Skill-Refs) does the same for a whole shelf at once. One constraint does most of the design work: a central router decides which book has any business speaking to the question in front of it, and the individual book summaries cost nothing until the router picks one. Ten books take up no more room in context than one.
[`repo-to-project-instructions`](https://github.com/ariel-lee-1023/repo-to-project-instructions) turns a repository into instructions you can paste into a host that can't clone it or run it — a Gem, a Project — so that host gets the routing it could never work out from a link alone.

**Geniuses that relocate the difficulty.** "Genius" here in its older sense: the guiding spirit of a particular mind — how that person proceeded, and what it cost them to keep standing there. Each of these is built so an agent gets questioned *by* that mind rather than made to imitate it.
These are geniuses of judgment and decision, not only of explanation. Each of them, when they took something apart, was on the hook for what would still be standing afterwards. They look for the edges of an order that already exists rather than inventing problems to show how clever they are, and none of them treats the world as a laboratory where concepts can be pulled apart at will — it is nearer to a fragile web that has to be kept in repair. None of them is a general assistant. Choosing which one to bring a problem to is usually the first thing I work out about the problem.
The rule leaves out a kind of mind I like reading, though some of that work has shown me things I would never have seen otherwise. He criticizes one thing to great depth and never sets it beside the alternatives — but comparison is the part judgment needs, and criticism can do without it. So he opposes what he opposes and goes over to something worse; he makes his living by taking apart, and is never exposed to the result. What gets cleared away is the middle of a society — a custom, a trade body, a local way of doing things — and what moves into the emptied space is rarely gentler than what stood there. Those who made a career of the clearing are seldom the ones who survive it.
What comes back is not an answer. It is the difficulty itself, moved — and the move is the direction. The picture that was holding the problem in place gets loosened, and the question comes back in a shape I can act on. Being shown where to stand next is worth more to me than being handed a conclusion. I reach for these when I can't yet tell what I'm stuck on.
[`later-Wittgensteinian-Thinking-Partner`](https://github.com/ariel-lee-1023/later-Wittgensteinian-Thinking-Partner) is for the question that feels deep and will not move. An argument where both sides hold the same facts and neither will give an inch. The same word doing different work in two mouths, and neither of us asking where his way of putting it came from or what problem it first answered. A quarrel I want to settle by how things are in themselves, when the only world either of us can set on the table is one already described by somebody — and there is no other kind to appeal to. A rule I can state and still cannot apply to the case in front of me. A certainty I can neither ground nor put down. He will not let me keep the sentence I came in with, and the word that goes first is always the one I was leaning on hardest. Often nothing gets answered: the question stops being a question, and I find I can go on.
[`kierkegaard-diagnostic-interlocutor`](https://github.com/ariel-lee-1023/kierkegaard-diagnostic-interlocutor) is for the trouble that has no problem in it. A correct life that feels wasted. Dread with nothing in particular to be afraid of. Wanting proof before I will commit to anything, and calling the delay rigor. When I bring him the age, the crowd, what everyone is like now, he hands me back to the singular and the complaint has nowhere left to stand. He will not give me a conclusion — appropriating it was the only part that ever mattered — but the trouble stops being weather I am under and becomes something I am doing, and a thing I am doing can be stopped. It is colder than I was hoping for, every time.
These two I reach for first, and I think it is because they work on the question rather than on the case. My own words are usually what is holding a problem shut — too abstract, or arranged so that the question never quite gets asked. Until that is dealt with, whatever the older minds have to say arrives at a question I have not managed to put properly.
The rest hold their ground just as firmly. In order of birth: [`Plutarch-perspective`](https://github.com/ariel-lee-1023/Plutarch-perspective) (c. 46), [`tocqueville-investigator`](https://github.com/ariel-lee-1023/tocqueville-investigator) (1805), [`schumpeter-perspective`](https://github.com/ariel-lee-1023/schumpeter-perspective) (1883), [`Polanyi-perspective`](https://github.com/ariel-lee-1023/Polanyi-perspective) (1891), [`feynman-perspective`](https://github.com/ariel-lee-1023/feynman-perspective) (1918), [`Kaplan-perspective`](https://github.com/ariel-lee-1023/Kaplan-perspective) (1952), and [`liu-zhongjing-perspective`](https://github.com/ariel-lee-1023/liu-zhongjing-perspective) (1974).

**Field colleagues and domain advisors.** These face a line of work rather than a mind. They check a claim against the standards the field already applies — which makes them worth having only where those standards are specific enough that a claim can actually fail against them.
[`legal-reasoning-advisor`](https://github.com/ariel-lee-1023/legal-reasoning-advisor) is for the stage where the dispute is still a shapeless pile and everything in the file looks equally important. Forty pages of briefing with no way to tell which paragraph is load-bearing. A case that can be argued either way and no account of why. It separates the factual question from the classificatory one, the precedent from the policy, and says which joint the conclusion actually hangs on — rarely the joint the brief spent its length on. I use it before drafting, not after.
[`Cognitive-Neuroscience-Expert`](https://github.com/ariel-lee-1023/Cognitive-Neuroscience-Expert) is for the claim about the brain that I cannot tell is settled or only well repeated. Two accounts that both fit the finding, with nothing visible to separate them. A popular version of a result, and the question of whether anything is under it. It names the experiment where the rival accounts actually come apart; and where the literature does not reach that far, it says so and says what would have to be read or run to close the gap, rather than handing me something plausible.
The rest each cover one job and keep the same fidelity to how their own field reasons. Listed by what I bring them: [`TechLaw-colleague`](https://github.com/ariel-lee-1023/TechLaw-colleague) reads a product, a data flow, or a contract clause against the rules that actually bind it. [`financial-planner`](https://github.com/ariel-lee-1023/financial-planner) works through a household balance sheet when a decision is big enough to move it: an allocation, a tax treatment, the timing of a purchase. [`Color-Matching-Consultant`](https://github.com/ariel-lee-1023/Color-Matching-Consultant) builds a palette and diagnoses a color that's off, whether it's a slide deck, an outfit, a wall, or a canvas. [`soccer-analyst`](https://github.com/ariel-lee-1023/soccer-analyst) reads a match, a signing, or a wage bill with the economics attached. [`English-Chinese-translator`](https://github.com/ariel-lee-1023/English-Chinese-translator) translates prose between Chinese and English to a standard a publisher would accept, not just one a reader would put up with. [`transcript-proofreader`](https://github.com/ariel-lee-1023/transcript-proofreader) makes a recording readable under edited-verbatim rules, without it stopping being what was actually said. [`us-study-advisor-for-law-students`](https://github.com/ariel-lee-1023/us-study-advisor-for-law-students) handles the American application and the career it's meant to open. [`toefl-2026-writing-speaking`](https://github.com/ariel-lee-1023/toefl-2026-writing-speaking) marks writing and speaking against the 2026 rubric and says where the points are actually going.

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
