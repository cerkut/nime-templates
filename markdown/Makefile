all: nime2017.pdf nime2017.html

nime2017.html: nime2017.txt references.bib
	pandoc --template=pandoc/nime.html --filter pandoc-citeproc --number-sections nime2017.txt -o nime2017.html

nime2017.pdf: nime2017.txt references.bib pandoc/nime.latex pandoc/nime.sty
	pandoc --template=pandoc/nime.latex --filter pandoc-citeproc --number-sections nime2017.txt -o nime2017.pdf

nime2017.docx: nime2017.txt references.bib
	pandoc --filter pandoc-citeproc --number-sections nime2017.txt -o nime2017.docx

nime2017x.pdf: nime2017.txt references.bib pandoc/nime.latex pandoc/nime.sty
	pandoc --template=pandoc/nime.latex --filter pandoc-citeproc --number-sections nime2017.txt --latex-engine=xelatex -o nime2017x.pdf
