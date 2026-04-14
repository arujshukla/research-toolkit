# Beamer Template

A warm-toned Beamer template for seminars, conference talks, lectures, and workshop presentations.

It keeps the clean structure of `metropolis` but shifts the visual language toward a softer academic style.

## Included files

- `main.tex`: starter deck
- `arujbeamer.sty`: shared theme and visual system
- `Makefile`: build commands
- `sample-deck.pdf`: rendered sample output

## Features

- `16:9` layout
- warm cream background instead of stark white
- `Alegreya Sans` typography
- crimson, plum, and gold accents
- automatic section-divider slides
- auto-fit helper for oversized tables copied from papers
- a sample deck ready to adapt

## Suggested workflow

1. Copy these files into a new talk directory.
2. Update the title block and metadata in `main.tex`.
3. Replace the example slides with your content.
4. Compile locally with `make`.

The visual system lives in `arujbeamer.sty`, which keeps the deck content easy to edit while preserving a consistent style.

## Large tables

For tables that come from papers or regression exports, wrap the tabular content in `fittable` so it shrinks to fit the slide width and available height automatically:

```tex
\begin{table}
  \caption{Main Results}
  \begin{fittable}
    \input{tables/main-results.tex}
  \end{fittable}
\end{table}
```

This follows the same idea as the Beamer resizing pattern from Patrick Baylis: constrain both width and height so oversized tables scale down without hand-tuning each slide.
