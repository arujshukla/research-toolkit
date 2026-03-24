# Academic Paper

A modular LaTeX paper template for drafts, seminar papers, and longer research writeups.

It is designed to keep the project structure clean: the main file stays lightweight, the preamble is centralized, and each major section lives in its own chapter file.

## Included files

- `main.tex`: the top-level paper file
- `preamble.tex`: shared packages, typography, formatting, and drafting tools
- `chapters/`: section-by-section paper content
- `bibtex/biblio.bib`: bibliography file
- `Makefile`: build commands
- `sample-paper.pdf`: compiled sample output

## Style notes

- serif body text for readable long-form writing
- sans-serif tables for cleaner tabular presentation
- stronger slate-blue links instead of bright pink
- modular chapter structure for easier drafting and revision
- built-in draft mode, todos, and coauthor comment commands

## Drafting tools

Toggle draft mode at the top of `preamble.tex`:

```latex
\drafttrue
```

Set it back to `\draftfalse` for a cleaner output with comments and todos disabled.

Included note commands:

- `\todoinline{...}` for general inline tasks
- `\AR{...}` and `\ARinline{...}` for one coauthor
- `\CO{...}` and `\COinline{...}` for a second coauthor
- `\reply{...}` for visible inline responses in the text

## Quick start

```bash
make
```

Then edit `main.tex`, `preamble.tex`, and the files in `chapters/` as needed.
