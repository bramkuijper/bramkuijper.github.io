---
layout: default
---

# Book reading group McElreath and Boyd 
You can find the complete book **online** at UExeter's library [here](http://encore.exeter.ac.uk/iii/encore/record/C__Rb3552240?lang=eng) (click on the Dawsonera link).

## Questions
Email Bram at `a dot l dot w dot kuijper at exeter dot ac uk`.

## Sessions
We meet online using [Microsoft Teams](https://products.office.com/en-gb/microsoft-teams/download-app). By now, you should have received a link to the meeting, but let me know if you haven't received it / still want to join.

If you do not know how to use the chat function and the whiteboard, please read the manual on [Microsoft Teams](https://www.exeter.ac.uk/it/teams/). You might want to mute your microphone when joining the session. 



### Session dates and times:
1. Thu April 16 1200 - 1300: chapter 1 - 1.4. 
2. Wed April 22: 1200 - 1400, chapter 1.5 - chapter 1 end (page 36) + 2 exercises
3. Wed April 29: 1200 - 1300, chapter 2 reading

At the end of each session, we'll choose the date of the next session, which will appear here.


## Session content and links
* Session 1 Thu April 16. 
    - [Haploid population genetics worksheet]({{ site.baseurl }}{% link mcelreath_boyd/ch1_14.html%})
    - Additional reading: interesting article by Wimsatt on philosophy of modeling [here](http://mechanism.ucsd.edu/teaching/models/Wimsatt.falsemodels.pdf) and another article by Paul Smaldino [here](http://smaldino.com/wp/wp-content/uploads/2017/01/Smaldino2017-ModelsAreStupid.pdf)

* Session 2 Wed Apr 22.
    - Equilibrium analysis and cobweb plots of the haploid selection model: [jupyter workbook in html]({{ site.baseurl }}{% link mcelreath_boyd/ch1_14_end.html%}), [original jupyter workbook]({{ site.baseurl }}{% link mcelreath_boyd/ch1_14_end.ipynb%}), [mathematica sheet]({{ site.baseurl }}{% link mcelreath_boyd/ch1_14_end.nb%})
    - Answers to exercises 1-5: Most derivations are given in the jupyter worksheets, either in [html format]({{ site.baseurl }}{% link mcelreath_boyd/ch1_exercises_answers.html%}) or the [original jupyter workbook]({{ site.baseurl }}{% link mcelreath_boyd/ch1_exercises_answers.ipynb%}). There is also a  [compact mathematica sheet]({{ site.baseurl }}{% link mcelreath_boyd/ch1_exercises_answers.nb%}) with the computational methods (no derivations) to arrive at the answers.
    - Interested in plotting ternary plots (where three instead of two alleles kick around)? See the [egtplot](https://github.com/mirzaevinom/egtplot) package (thanks to Arthur Newbury for the link).


## Tools needed: a computer algebra system
Most exercises can be completed using pen and paper, but this gets tedious when plotting functions and numerically solving things. Below are three possible options for programs that do numerical calculations for us. At a minimum, solutions will be provided using the first option, a [jupyter notebook](https://jupyter.org/), which will be published in .html format as well. In the longer term, we hope to provide answers to problems using more than one tool.

1. [Sympy](https://www.sympy.org/en/index.html). Open source symbolic algebra package for [Python](https://www.python.org/). Sympy is particularly handy when used in a [jupyter notebook](https://jupyter.org/). Installation instructions for Sympy [here](https://docs.sympy.org/latest/install.html) and for jupyter [here](https://jupyter.readthedocs.io/en/latest/install.html). Some features may be experimental and unreliable, so our mileage may vary. 

2. [Mathematica](https://www.wolfram.com/mathematica/) : non-free and expensive, but reliable and extremely well [documented](https://reference.wolfram.com/language/). Note: [UExeter has a license](https://www.exeter.ac.uk/it/new/softwarecatalogue/mathematica/). If you want to have the least fuss, use this. However, if you prefer something affordable which you will also be able to use when not employed/studying here, check out other tools. If you want a readable introduction to Mathematica, read the book Torrence & Torrence (2019) The Student's introduction to Mathematica, which UExeter's library has [online](http://encore.exeter.ac.uk/iii/encore/record/C__Rb4003689?lang=eng).

3. [R](https://cran.r-project.org/) and [Ryacas](https://cran.r-project.org/web/packages/Ryacas/index.html). While R is excellent to graph functions and numerically iterate over systems of recursion equations, it is less than ideal when it comes to solving equations algebraically. However, the package Ryacas (based on the program [Yacas](http://www.yacas.org)) tries to change this, with varying success. 


