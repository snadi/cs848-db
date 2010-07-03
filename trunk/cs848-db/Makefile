FILE    := Paper
SRCFIGS := $(wildcard figs/*.png)
ARGS	:= -interaction=nonstopmode

all: pdf clean

pdf: $(FILE).tex *.bib
	pdflatex $(ARGS) $(FILE).tex
	bibtex $(FILE).aux 
	pdflatex $(ARGS) $(FILE).tex 
	pdflatex $(ARGS) $(FILE).tex 

clean:
	@rm -f *.aux *.bbl *.blg *.log *.out
