The latex template I use for my paper publication:

[draft template](/attachment/main.tex)

The suggested cmds (double check) for running above latex scripts:

```
latexmk -C

bibtex main
pdflatex main
bibtex main
pdflatex main 

latexmk -f -pdf main.tex
```