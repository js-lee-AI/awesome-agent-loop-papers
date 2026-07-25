# Contributing

Contributions that add a relevant, verifiable paper are welcome.

## How to add a paper

Add an entry to the section that matches **where the paper enters the loop**, matching the existing format:

```markdown
- [Full Paper Title](https://arxiv.org/abs/XXXX.XXXXX) - First-Author Surname et al. Year
```

Then open a pull request.

## Requirements

- A working **arXiv or DOI link** is mandatory. Prefer the arXiv abstract page over the PDF.
- One line per paper, and one paper per line.
- Put the paper in the section matching its **role in the loop**, not the venue it appeared in. A reinforcement-learning paper that folds control into the weights belongs in *Trained Loops*, not *Loop Paradigms*, even if the abstract talks about planning.
- Do not add a paper twice. If it spans two sections, pick the one where its main contribution lands.

## A note on the generated README

`README.md` is **generated**, not hand-written. It is built from the survey's `references.bib` plus a curated supplement, so an edit made directly to `README.md` will be overwritten the next time it is regenerated.

That does not mean your PR is unwelcome. Open it against `README.md` as normal: the maintainer folds accepted entries into the source that generates the file, which is what makes the change stick.

## Sibling list

For the field-wide map of LLM agents rather than the loop itself, see [Awesome LLM Agent Papers](https://github.com/js-lee-AI/awesome-llm-agent-papers). A paper about agent memory, applications, or multi-agent systems in general probably belongs there instead. Papers that are canonical for both lists appear in both, deliberately.
