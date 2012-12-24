LaTeX support for Sistina URW D Normal

Requirements
============
fontinst v1.925
Sistina URW D Normal Version 1.05 in PostScript Type 1 format

Instructions
============

Obtain a copy of Sistina URW D Normal in Type 1 format. The font should come with the following files:

	s096013d.afm
	s096013d.pfb
	s096013d.pfm
	
Place these files in the `resources/` directory.

Make the `install` file executable, then run it. Enter your password when prompted. All the necessary font files will be installed in your TeX tree.

Run `pdflatex sistina.tex` to generate a type specimen. To use URW Sistina in your own document, include the `sistina.sty` file, then near the top of your LaTeX file add the lines:

	\usepackage{sistina}
	\fontfamily{usz}\fontsize{48}{56}\selectfont
	
Happy TeXing