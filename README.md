# The Self-Contained Harness

*One theme, one folder, one agent-maintained data system.*

**The Self-Contained Harness** is a framework manuscript about keeping personal and
professional context usable in the age of AI agents. It addresses two problems: the
information explosion that generative AI has made worse (material now grows faster than
anyone can read it, and it is scattered across notes apps, drives and chat histories),
and the churn of AI tool choices, where every change of model, engine or subscription
turns into a migration. Its core idea: keep **one self-contained folder per theme**, in
plain portable files, and let agents file, distill and prune that folder while the human
only captures, decides and deletes.

> **Status: v0.2 draft, work in progress, feedback welcome.**
> This is a complete draft, not a finished work. Sections will change, and the dated
> parts (Part IV and section 3.7) are meant to be revised as tools and benchmarks move.

> **Thesis.** Agentic AI is both the cause of the information explosion and,
> paradoxically, its cure: one self-contained folder per theme, where agents distill,
> prune and compound context in portable formats that outlive any tool.

**Read it:** [the-self-contained-harness.md](the-self-contained-harness.md).

By Simon Kreis. Version 0.2, draft, October 2026.

---

## What the manuscript proposes

The names below are the ones used in the manuscript.

**One problem, two victims.** Context is produced faster than ever and scattered across
more places than ever. The agent pays in results: it cannot use context it cannot find,
and works worse when handed too much. The person pays in attention: open loops, noise,
reconstruction. One complete, current, distilled description of each piece of work, in one
place, answers both.

**The unit.** *One theme = one folder = one agentic project = one self-contained data
system.* A theme is anything you think about as a whole: a career, your health, a
manuscript, a codebase. "Self-contained" means self-contained per **domain**, not per
**capability**: everything that belongs to a theme lives in its folder, and what is common
to all themes lives once, in a thin root layer.

**Your real harness is the folder.** The program that runs a model is an interchangeable
*engine*; the part worth designing is the folder, with its entry file, map, rules, skills
and distilled state. The manuscript's ordering: context and skills matter more than the
engine, and the engine matters more than the model.

**The loop: capture, qualify, home, propagate, prune, verify.** One maintenance loop runs
the system. The division of labour is deliberately lopsided: **the human does three
things: capture, decide, delete.** Filing, merging, summarizing, linking and tidying belong
to the agent.

**Pruning as a first-class operation.** Text is cut, not copied: source text moves word for
word into the theme's `TRASH.md` before it is distilled, and processed files leave for
`2-trash/` with a manifest line saying where their content now lives. The agent never
deletes; the human empties the trash. Losses are checked by **sampling**, not by rereading
everything: a fresh agent verifies the essence of a random tenth. Two properties make the
result checkable:
**traceability** (every source can be followed to its destination) and **convergence**
(running the same pass twice produces nothing the second time).

**Compounding, portability and longevity.** Work is produced inside the theme and feeds back
into its context, and everything is an ordinary file, so changing tools becomes a pointer
change rather than a migration.

**A third generation of the second brain.** The method is offered as a contribution to the
lineage of *Getting Things Done*, PARA and *Building a Second Brain*, not a break with it:
every earlier idea survives, and what changes is who carries it out. From PARA it keeps
filing by actionability, but **status belongs to the theme folder, never to the file**:
whole themes move between tiers, files never do, and the method declutters instead of
accumulating.

**Architecture (Part III).**

- *The root layer*: `AGENTS.md`, `CONTEXT.md` (the system), `USER.md` (the person), the
  shared skills, and numbered tiers (`0-system`, `1-inbox`, `2-active`, `3-backlog`,
  `4-areas`, `5-archive`, `9-trash`); a theme's tier is its status.
- *The theme folder*: four files (`AGENTS.md`, `CONTEXT.md` for what is true, `TODO.md` for
  what is open, `TRASH.md` for source text cut verbatim) and three standard folders
  (`0-assets/`, `1-ai-workspace/`, `2-trash/<run>/`); the theme's top level is its inbox.
  Classification happens in sections, not in folders.
- *The placement rule*: behaviour goes in `AGENTS.md`, the person in `USER.md`, the system in
  the root `CONTEXT.md`, domain knowledge in the theme's `CONTEXT.md` and `TODO.md`,
  procedures in skills.
- *Anatomy of `CONTEXT.md`*: **addressability over file count**; one anchored file per
  theme (`## §core`, `§map`, `§protocol`, content sections, `§decisions`, `§log`),
  with reliability markers and per-section sensitivity.
- *Permissions and guarantees*: a short table of agent rights, and a ladder of guarantees
  from soft to hard (relay, inline, injection, mechanism). **Engine memory is a cache.**
- *Maintenance without drift*: one `declutter` pass (protect, survey, structure, integrate,
  consolidate, verify by sampling, close on request), with the mechanical checks left to a
  small script.
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
(`declutter`) for the whole workflow, five trigger prompts, and a one-page `CONTEXT.md`
specification, with its companion `TODO.md`, and a fictional example.

**Related approaches and limits.** Section 2.10 situates the method against entry-file
conventions, built-in assistant memories, memory servers, retrieval over embeddings and
context engineering, and says where the single-file model stops. A closing section lists
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
  author       = {Kreis, Simon},
  title        = {The Self-Contained Harness: One Theme, One Folder, One Agent-Maintained Data System},
  year         = {2026},
  note         = {Version 0.2, draft, work in progress},
  howpublished = {\url{https://github.com/SimonKreis/self-contained-harness}}
}
```

Plain text: Kreis, S. (2026). *The Self-Contained Harness: One theme, one folder,
one agent-maintained data system* (Version 0.2, draft).
<https://github.com/SimonKreis/self-contained-harness>

GitHub also offers a "Cite this repository" button, generated from `CITATION.cff`.

Contact: Simon Kreis, M. Sc., [simon@kreisconsulting.ca](mailto:simon@kreisconsulting.ca).
