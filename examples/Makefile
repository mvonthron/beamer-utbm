#
# Copyright (c) 2010 
# Manuel Vonthron - <manuel DOT vonthron AT acadis DOT org>
#
# This file may be distributed and/or modified under the terms of 
# the Do What The Fuck You Want To Public License, Version 2
#

SOURCE=example
LATEX=pdflatex

all: utbm-official utbm-internship curiosity terra clean

utbm-official:
	sed -i -e '/^\\usecolortheme/s/{.*}/{UTBMOfficial}/g' $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).utbm.official $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).utbm.official $(SOURCE).tex

utbm-internship:
	sed -i -e '/^\\usecolortheme/s/{.*}/{UTBMInternship}/g' $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).utbm.internship $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).utbm.internship $(SOURCE).tex

curiosity:
	sed -i -e '/^\\usecolortheme/s/{.*}/{Curiosity}/g' $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).curiosity $(SOURCE).tex 
	$(LATEX) -jobname $(SOURCE).curiosity $(SOURCE).tex 

terra:
	sed -i -e '/^\\usecolortheme/s/{.*}/{Terra}/g' $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).terra $(SOURCE).tex
	$(LATEX) -jobname $(SOURCE).terra $(SOURCE).tex

clean:
	rm -f *.aux *.out *.log 
	rm -f *.snm *.toc *.nav

mrproper: clean
	rm -f $(SOURCE).terra.pdf $(SOURCE).curiosity.pdf $(SOURCE).utbm.internship.pdf $(SOURCE).utbm.official.pdf
