# The Self-Contained Harness

*One theme, one folder, one living note.*

**The Self-Contained Harness** is a framework manuscript about keeping personal and
professional context usable in the age of AI agents. It addresses two problems: the
information explosion that generative AI has made worse (material now grows faster than
anyone can read it, and it is scattered across notes apps, drives and chat histories),
and the churn of AI tool choices, where every change of model, engine or subscription
turns into a migration. Its core idea: keep **one self-contained folder per theme**, around
one living note, in plain portable files. The person arranges the folders as they think;
agents distill, recycle and prune what is captured in them.
**The structure is personal; the distillation is not.**

> **Status: draft, work in progress, feedback welcome.**
> This is a complete draft, not a finished work. Sections will change, and the dated
> parts (Part IV and section 3.7) are meant to be revised as tools and benchmarks move.

> **Thesis.** Agentic AI is both the cause of the information explosion and,
> paradoxically, its cure: one self-contained folder per theme around one living note,
> arranged by you and distilled by agents, so that you and they rely on the same context,
> in portable formats that outlive any tool.

**Read it:** [the-self-contained-harness.md](the-self-contained-harness.md).

**Simon Kreis & Claude.** Made with AI, mainly Claude (Anthropic), which contributed in part or in whole to the work. Simon Kreis is responsible for the result. From an original idea by Simon Kreis.

Draft, updated October 2026.

---

## What the manuscript proposes

The names below are the ones used in the manuscript.

**One problem, two victims.** Context is produced faster than ever and scattered across
more places than ever. The agent pays in results: it cannot use context it cannot find,
and works worse when handed too much. The person pays in attention: open loops, noise,
reconstruction. One complete, current, distilled description of each piece of work, in one
place, answers both.

**The unit.** *One theme = one folder = one living note = one self-contained data
system.* A theme is anything you think about as a whole: a career, your health, a
manuscript, a trip. It has one folder, named with one short name: at its centre a **note**
that holds everything alive (actions, context, ideas, incoming drafts), as complete as it
can be, and beside it `files/` for resources kept as they are. One note per theme, never
two. "Self-contained" means
self-contained per **domain**, not per **capability**: what is common to all themes lives
once, at the root.

**Your real harness is the folder.** The program that runs a model is an interchangeable
*engine*; the part worth designing is the folder, with its entry file, rules, skills and
distilled notes. The manuscript's ordering: context and skills matter more than the
engine, and the engine matters more than the model.

**You arrange, the agent distills.** The division of labour follows the line between what
is personal and what is not. **The human does four things: capture, arrange, decide,
delete.** How a life is cut into themes, and where those themes sit, is a map of how one
person thinks: the person creates, moves, regroups and prunes folders as often as they
like. The agent never moves anything on its own; it treats every arrangement as
intentional, finds each note by name wherever it now is, and keeps its own picture of the
tree current. **The agent does the rest: distill, recycle, deduplicate, verify**, through
one loop: capture, qualify, home, propagate, prune, verify.

**Pruning as a first-class operation.** Text is cut, not copied: whatever the human wrote
leaves a note only after a script has found it, word for word, in one `trash.md` for the
whole root. Files leave whole for the trash; the agent deletes only proven duplicates and
text files verified word for word in a note, and the human empties the trash. **Verify, do not journal**: no manifests, no run logs, but a
check before every removal and a counter-check before any backup is deleted. Large or
sensitive distillations are reviewed by a fresh agent, by sampling when they are very
large. Two properties make the result checkable:
**traceability** (every source can be followed to its destination) and **convergence**
(running the same pass twice produces nothing the second time).

**Compounding, portability and longevity.** Work is produced inside the theme and feeds back
into its context, and everything is an ordinary file, so changing tools becomes a pointer
change rather than a migration.

**A third generation of the second brain.** The method is offered as a contribution to the
lineage of David Allen's *Getting Things Done* and Tiago Forte's *Building a Second Brain*, with
its PARA structure (Projects, Areas, Resources, Archives), not a break with it:
every earlier idea survives, and what changes is who carries it out. From PARA it keeps
filing by actionability, but **status is a property of the note, never a place**
(active, area, archived): where a theme folder sits is the person's choice, nothing an
agent relies on is encoded in a path, and the method declutters instead of accumulating.

**Architecture (Part III).**

- *The root layer*: one `AGENTS.md`, `USER.md` (the person), every skill in
  `.agents/skills/`, the human's own `0-dashboard/` and `1-inbox/` (out of the agents'
  reach), theme folders grouped as the person likes (`<name>/<name>.md` and `files/`),
  and `9-trash/`.
- *The project note*: four sections (Actions, Context, Ideas, Incoming, always last) and a
  `status:` in its front matter; one living Markdown file over a body of static material,
  as complete as possible, with loose context files folded back in.
- *Reading a note in slices*: **addressability over file count**, with visible statuses
  (the human's decision, a hypothesis, an assistant's suggestion) and orientations rather
  than rules.
- *Permissions and guarantees*: a short table of agent rights, and a ladder of guarantees
  from soft to hard (relay, inline, injection, mechanism). **Engine memory is a cache.**
- *Maintenance without drift*: one `declutter` skill whose routine is to empty a note's
  Incoming section into Actions, Context and Ideas, and to catch up after the person
  rearranges the tree, with the mechanical checks left to a small script.
- *Privacy by design*: the read perimeter, what zero data retention does and does not
  cover, stored copies as the long-term risk, encryption at rest for sensitive themes.
- *Stack archetypes: pick some, leave some*: dated, optional tool examples, each chosen
  because it embodies one of the principles.

**Staying current (Part IV, dated September 2026).** Principles for choosing models and
engines without constant migration (harness weight as a dial, "the thinking room" and "the
workshop", the latest frontier model at low effort as a default), benchmarks for knowledge
work, access and data retention, prompt caching, and the triggers for updating the
framework.

**Quick start (Part V) and Appendix A.** A root `AGENTS.md`, one bootstrap prompt, one skill
(`declutter`) for the whole workflow, six trigger prompts, and a one-page project note
specification with a fictional example.

**Related approaches and limits.** Section 2.10 situates the method against entry-file
conventions, built-in assistant memories, memory servers, retrieval over embeddings and
context engineering, and says where the single-note model stops. A closing section lists
what is not yet known.

---

## How to read it

- **The argument**: Parts I and II (the problem, then the solution).
- **The specification**: Part III and Appendix A. Parts I to III and Appendix A are meant to
  change rarely.
- **The dated advice**: Part IV and section 3.7, revised when models, providers or
  benchmarks change.
- **To try it**: Part V, then Appendix A. The templates are deliberately basic; the system
  is meant to refine them from your own context. Run the bootstrap prompt on a copy first.

The manuscript distinguishes three levels of support and says which one applies where it
matters: *validated by* direct evidence on language models and agents, *consistent with*
findings from cognitive science (used as analogies), and *engineering judgment*. Sources
are given as footnotes and were last checked on 29 September 2026.

## Repository layout

```text
self-contained-harness/
├── README.md                        this page
├── the-self-contained-harness.md    the manuscript (single file, GitHub-flavoured Markdown)
├── references/bibliography.md       the sources, labelled by level of support
├── LICENSE                          CC BY 4.0 (text)
├── LICENSE-CC0                      CC0 1.0 (Appendix A and Part V templates)
└── CITATION.cff                     citation metadata
```

## Feedback

Feedback is welcome: open an issue on
[this repository](https://github.com/SimonKreis/self-contained-harness/issues).
Corrections to sources and dated facts (Part IV, section 3.7) are especially useful, as
are reports from anyone who tries the method on a real folder.

## License

- **Text**: Creative Commons Attribution 4.0 International (CC BY 4.0).
- **Appendix A and the templates, prompts and skills in Part V**: CC0 1.0 (public domain
  dedication).

See `LICENSE` and `LICENSE-CC0`.

## Citation

```bibtex
@misc{kreis2026harness,
  author       = {Kreis, Simon and Claude},
  title        = {The Self-Contained Harness: One Theme, One Folder, One Living Note},
  year         = {2026},
  note         = {Draft, work in progress. Made with AI, mainly Claude (Anthropic)},
  howpublished = {\url{https://github.com/SimonKreis/self-contained-harness}}
}
```

Plain text: Kreis, S., & Claude (2026). *The Self-Contained Harness: One theme, one folder,
one living note* (draft).
<https://github.com/SimonKreis/self-contained-harness>

GitHub also offers a "Cite this repository" button, generated from `CITATION.cff`.

Contact: Simon Kreis, M. Sc., [simon@kreisconsulting.ca](mailto:simon@kreisconsulting.ca).
