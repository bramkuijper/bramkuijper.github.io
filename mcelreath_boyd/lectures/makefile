# General make file for all the lectures
.PHONY: lecture1.pdf all clean


all: lecture1_handout.pdf lecture1_for_lecture.pdf

lecture1_handout.pdf: lecture1.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make lecture1.tex


clean:
	latexmk -CA

