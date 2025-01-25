all:
	pdflatex thesis.tex
	biber thesis
	pdflatex thesis.tex

clean:
	latexmk -CA thesis.tex
	rm *.aux *.fls *.log *.nls *.nlo *.bbl *.blg *.fdb_latexmk *.run.xml *.lof *.lot *.glo *.bcf *.out *.toc
