LaTeX support for Sistina URW D Normal

About
=====

Sistina is a titling face designed by Hermann Zapf in 1950. This set of serifed capitals was cut by August Rosenberger, and issued by D. Stempel AG typefoundry in 1951. It was digitized in 1995 by URW Studio.

Sistina is currently issued by URW++ and Linotype in OpenType format. The version referenced here was issued by URW++ in 1999, and may no longer be commercially available. However, it is hoped that this document can provide a useful lesson on the use of the fontinst software.

Requirements
============

* fontinst v1.925
* Sistina URW D Normal Version 1.05 in PostScript Type 1 format

Note
====

Out of the box, Sistina URW D Normal suffers from a couple of relatively minor issues that fontinst can help us remedy. The first issue is that the font offers an alternative uppercase Q which has been relegated to the _partialdiff_ slot. We will make this glyph available to TeX in an alternate font. The second, more serious issue, is that many accents are rendered slightly out of alignment when using the default fontinst commands. We will tune these diacritics with our own metrics file.

Instructions
============

The following instructions should work in Linux and Mac OS X.

Obtain a copy of Sistina URW D Normal in Type 1 format. The font includes the following files:

	s096013d.afm
	s096013d.pfb
	s096013d.pfm
	
Place these files in the `resources/` directory.

Open a Terminal in the current directory. Make the `install` file executable using the command `chmod u+x install`, then run it by typing `./install`

Enter your password when prompted. All the necessary font files will be installed in your TeX tree.

Run `pdflatex sistina.tex` to generate a type specimen. To use URW Sistina in your own document, add the following line to your premable:

	\usepackage{sistina}
	
To start setting type in Sistina, use the command:

	\fontfamily{usz}\selectfont
	
If you'd like to typeset Sistina using the alternative Q glyph, use the command:
	
	\fontfamily{usz}\fontshape{al}\selectfont
	
Happy TeXing