
nip_paper.pdf: parallel_submodular.pdf
	gs -dSAFER -dNOPLATFONTS -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sPAPERSIZE=letter -dCompatibilityLevel=1.4 -dPDFSETTINGS=/printer -dCompatibilityLevel=1.4 -dMaxSubsetPct=100 -dSubsetFonts=true -dEmbedAllFonts=true -sOutputFile=nips_paper.pdf -f parallel_submodular.pdf



parallel_submodular.pdf: parallel_submodular.aux parallel_submodular.bbl
	-pdflatex -halt-on-error  parallel_submodular.tex
	pdflatex -halt-on-error  parallel_submodular.tex

parallel_submodular.bbl: parallel_submodular.aux *.bib
	-bibtex parallel_submodular

parallel_submodular.aux: *.tex *.tex *.bib
	pdflatex -halt-on-error  parallel_submodular.tex

clean:
	\rm -f *.dvi *.aux *.bbl *.log *.blg *.toc *~ *.out *.idx \

spotless: clean
	\rm -f parallel_submodular.pdf parallel_submodular.ps




