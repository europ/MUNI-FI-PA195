FILE=pres

# Casual build
.PHONY: make
make: clean-all
	pdflatex -draftmode $(FILE)
	pdflatex $(FILE)

# TRAVIS-CI build
.PHONY: travis-build
travis-build: clean-all
	pdflatex -halt-on-error -draftmode $(FILE)
	pdflatex -halt-on-error $(FILE)

# Remove LaTeX auxiliary files
.PHONY: clean
clean:
	@rm -fv *.aux *.log *.dvi *.ps *.bbl *.blg *.toc *.out *.lof *.snm *.nav

# Remove all excluding source files
.PHONY: clean-all
clean-all: clean
	@rm -fv *.pdf
