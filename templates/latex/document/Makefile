LATEXMK := latexmk
MAIN := note.tex
PDF := $(MAIN:.tex=.pdf)

.PHONY: all watch clean

all:
	$(LATEXMK) -pdf $(MAIN)

watch:
	$(LATEXMK) -pvc -pdf $(MAIN)

clean:
	$(LATEXMK) -C
	rm -f $(PDF)
