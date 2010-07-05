FILE    := Paper
SRCFIGS := $(wildcard figs/*.png)
ARGS	:= -interaction=nonstopmode

all: pdf clean

pdf: $(FILE).tex *.bib
	@pdflatex $(ARGS) $(FILE).tex > /dev/null 2>&1
	@bibtex $(FILE).aux > /dev/null 2>&1
	@pdflatex $(ARGS) $(FILE).tex > /dev/null 2>&1
	@pdflatex $(ARGS) $(FILE).tex > /dev/null 2>&1
	@xdg-open $(FILE).pdf > /dev/null 2>&1

clean:
	@rm -f *.aux *.bbl *.blg *.out > /dev/null 2>&1
