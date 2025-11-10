```
title: "Latex template"
author: icanccwhite
output:
  html_document: default
date: "18/Mar./2025"
```



**This is a latex template I had modified for my paper publication:**

1. [main.tex](/blog/Latex/main.tex)

2. [sample.bib ](/blog/Latex/sample.bib) BibTex

3. [jabbrv.sty](/blog/Latex/jabbrv.sty)  About Automatic Journal Title Abbreviation Package for LaTeX

4. [wlscirep.cls](/blog/Latex/wlscirep.cls) This included in  "Template for submissions to Scientific Reports [(Nature Publishing Group)](http://www.nature.com/srep/index.html)" was  downloaded from Overleaf.

5. other files pls check Overleaf "Templates" or DIY

   

**The functions I have added in the template:**

1. Table format

2. Figure layout format

3. Watermarker

4. ORCID

5. Linenumbers

6. Optional: page layout with red frame

7. ...

   

**The suggested cmds (double check) for running above latex scripts:**



```
latexmk -C

bibtex main
pdflatex main
bibtex main
pdflatex main 

latexmk -f -pdf main.tex
```

---

<div align="center">

[🏠 Home](/) | [📁 Archives](/archives) | [📧 Contact](mailto:icanccwhite@icloud.com)

</div>

---

<div align="center">
<p><em>✨ Life is a journey of continuous learning and discovery ✨<em><p>

</div>