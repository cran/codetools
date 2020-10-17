
.SUFFIXES: .nw .tex .pdf .html .bib

.nw.tex:
	noweave -delay -index $< > $@
.tex.pdf:
	pdflatex $<
	pdflatex $<

.nw.html:
	noweave -filter l2h -index -html $< > $@

codetools.R: codetools.nw
	notangle -R$@ $< > $@

clean:
	rm -f codetools.R codetools.pdf codetools.html \
	codetools.aux codetools.log codetools.out codetools.tex
