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

> **Status: v0.1 draft, work in progress, feedback welcome.**
> This is a complete draft, not a finished work. Sections will change, and the dated
> parts (Part IV and section 3.7) are meant to be revised as tools and benchmarks move.

> **Thesis.** Agentic AI is both the cause of the information explosion and,
> paradoxically, its cure: one self-contained folder per theme, where agents distill,
> prune and compound context in portable formats that outlive any tool.

**Read it:** [the-self-contained-harness.md](the-self-contained-harness.md).

By Simon Kreis. Version 0.1, draft, September 2026.

---

## What the manuscript proposes

The names below are the ones used in the manuscript.

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

**Pruning as a first-class operation.** Integrated sources leave the working surface for a
`trash/` folder with a manifest line saying where their content now lives. The agent never
deletes; the human empties the trash. Two properties make the result checkable:
**traceability** (every source can be followed to its destination) and **convergence**
(running the same pass twice produces nothing the second time).

**Compounding, portability and longevity.** Work is produced inside the theme and feeds back
into its context, and everything is an ordinary file, so changing tools becomes a pointer
change rather than a migration.

**A third generation of the second brain.** The method is offered as a contribution to the
lineage of *Getting Things Done*, PARA and *Building a Second Brain*, not a break with it:
every earlier idea survives, and what changes is who carries it out.

**Architecture (Part III).**

- *The root layer* and *the theme folder* share the same six fixed elements: `AGENTS.md`,
  `CONTEXT.md`, `inbox/`, `work/`, `trash/` (with `MANIFEST.md`) and `.agents/skills/`.
  Sub-folders are left to the agent's judgment and recorded in the map.
- *The placement rule*: behaviour goes in `AGENTS.md`, identity and preferences in the root
  `CONTEXT.md`, domain knowledge in the theme's `CONTEXT.md`, procedures in skills.
- *Anatomy of `CONTEXT.md`*: **addressability over file count**; one anchored file per
  theme (`## §core`, `§map`, `§protocol`, content sections, `§decisions`, `§open`, `§log`),
  with reliability markers and per-section sensitivity.
- *Permissions and guarantees*: a short table of agent rights, and a ladder of guarantees
  from soft to hard (relay, inline, injection, mechanism). **Engine memory is a cache.**
- *Maintenance without drift*: a five-step pass (protect, intake, consolidate, prune,
  verify).
- *Privacy by design*: the read perimeter, what zero data retention does and does not
  cover, stored copies as the long-term risk, encryption at rest for sensitive themes.
- *Stack archetypes: pick some, leave some*: dated, optional tool examples, each chosen
  because it embodies one of the principles.

**Staying current (Part IV, dated September 2026).** Principles for choosing models and
engines without constant migration (harness weight as a dial, "the thinking room" and "the
workshop", the latest frontier model at low effort as a default), benchmarks for knowledge
work, access and data retention, prompt caching, and the triggers for updating the
framework.

**Quick start (Part V) and Appendix A.** A root `AGENTS.md`, one bootstrap prompt, two
skills (`intake`, `maintain`), five trigger prompts, and a one-page `CONTEXT.md`
specification with a fictional example.

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
  note         = {Version 0.1, draft, work in progress},
  howpublished = {\url{https://github.com/SimonKreis/self-contained-harness}}
}
```

Plain text: Kreis, S. (2026). *The Self-Contained Harness: One theme, one folder,
one agent-maintained data system* (Version 0.1, draft).
<https://github.com/SimonKreis/self-contained-harness>

GitHub also offers a "Cite this repository" button, generated from `CITATION.cff`.
