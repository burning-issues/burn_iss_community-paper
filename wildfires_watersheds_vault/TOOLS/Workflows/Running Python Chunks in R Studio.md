# Running Python Chunks in RStudio and rmarkdown

I wanted to use the package [spacyr](https://spacyr.quanteda.io/index.html)to handle plurals in text analysis.  [spacyr](https://spacyr.quanteda.io/index.html) is An R wrapper to the [spaCy](https://spacy.io/) “industrial strength natural language processing” Python library. For the package to work in [[RStudio]], you need to have a version of Python installed in your computer. It is suggested to install [miniconda](https://docs.conda.io/en/latest/miniconda.html).

Intro to [stringr](https://cran.r-project.org/web/packages/stringr/vignettes/stringr.html)

This is the process I followed (on Windows 10-64 bit):

Workflow as described at: https://spacyr.quanteda.io/index.html

1. Install [Visual Studio Express](https://visualstudio.microsoft.com/vs/express/) (required for SpaCy installation). I installed "Express 2017 for Windows Desktop". It takes about 30 mins to complete this installation. 
2. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)-Miniconda "is a small, bootstrap version of [Anaconda](https://www.anaconda.com/) that includes only conda, Python, the packages they depend on, and a small number of other useful packages, including pip, zlib and a few others." Think of Anaconda as the biggest competitor for [[RStudio]].
3. Install spaCy in a conda enviroment:  For Windows, you need to run R as an administrator to make installation work properly. To do so, right click the RStudio icon (or R desktop icon) and select “Run as administrator” when launching R. Then, on the R console (not RStudio) type:
```
library(spacyr)
spacy_install()
```

Once you try this, you may get an HTTP error in the R console. If you are using chrome, and have multiple tabs open, you may need to close all those, clean the history for the last 24 hrs, including cache and try again. I had to shut down my laptop, and after the clean up and this part of the code worked. It took about 1 hour to complete in my laptop.  

