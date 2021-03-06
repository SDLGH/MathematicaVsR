---
output: pdf_document
classoption: landscape
---
Mathematica Vs R
========================================================
author: Anton Antonov
date: 2015-10-21
width: 1920
height: 1200
transition: none
transition-speed: fast 
<!--- incremental: true -->


Talk plan
========================================================

### How to make a comparison breakdown
   - ... that might take too long ...

### The quick list of great R features

### How to quickly start work with R
   ... If you are an experienced *Mathematica* user.
   
   1. Data structures

   2. Libraries to use

   3. How to approach problems
 
   4. How to structure files

## Examples
   - In three groups:
      - on par
      - R is worse
      - R is better
   - This list is probably too long...


How to make the comparison?
========================================================

### Language design features
   - Is it functional, lazy, based on objects?
   - What data structures?
   - Is it easy to learn?
   
### Documentation writing capabilities
   - Does it facilitate writing technical papers?
   - Presentations?
   - Automatic reports?
   
### Projects on machine learning and data mining (since we talk about R)
   - How the codes compare?
   - What observations we would abstract into rules?
   - What the best practices?
   
### Performance
   - How it can perform faster?
   - How easy/well is to parallelize the computations?

### Extensibility   
  
More detailed breakdown: [Mind-map slide](#/MindMap) .

Mind-map
========================================================
id: MindMap

Here is a more detailed view breakdown for a comparison:

![Mind map](/Users/antonov/MathFiles/Presentations/WTC-2015/Mathematica-vs-R/Mathematica-vs-R-mind-map.png)

[Mind map link](/Users/antonov/MathFiles/Presentations/WTC-2015/Mathematica-vs-R/Mathematica-vs-R-mind-map.png)


The quick list
========================================================

Programming and working with R has four great features:
  
 1. Great IDE's support
    - [RStudio](http://www.rstudio.com)
    - [ESS](http://ess.r-project.org) for Emacs. 
    - [r4intellij](https://github.com/holgerbrandl/r4intellij) of [IntelliJ Idea](https://www.jetbrains.com/idea/).
 2. Great package system
    - The package system itself, and 
    - the amount of available packages (at [CRAN](http://cran.us.r-project.org)),
 3. Documentation integration with LaTeX, Markdown, and HTML
    - [Example of HTML report](/Users/antonov/R/Senzari/ProfileAnalysis/Reports/Hot 100 Airplay ChartReport.html) automatically generated using [knitr](https://github.com/yihui/knitr)
 4. Interactive interfaces building and deployment ([Shiny](http://shiny.rstudio.com/gallery/))
    - [ODE with seasonal term solving intercative interface](http://127.0.0.1:5413)
 
 
R as a language
========================================================

### What is R?

 - [The R Project for Statistical Computing](https://www.r-project.org)

 - [What is R?](http://www.inside-r.org/what-is-r)

 - Disclaimer on my bias
   - I have used Mathematica for 22 years, and R for 2 years.
   - But look at the [R](https://github.com/antononcube/MathematicaForPrediction/R) packages I have written.
   
### Language origins

 - LISP / Scheme refitted to look and feel like S.
 
 - Too many designers and too many of them are statisticians.
   - See the [anti-pattern (Design by a comittee)](https://en.wikipedia.org/wiki/Design_by_committee).

 
R as a language 2
========================================================

### Books (having *Mathematica* programmers in mind)

 1. [The R Inferno](http://www.burns-stat.com/pages/Tutor/R_inferno.pdf) by Patrick Burns
 
 2. [Advanced R](http://adv-r.had.co.nz) by Hadley Wickham
 
### Articles

 3. [Ihaka, Ross (2010). R: Lessons Learned, Directions for the Future (PDF). Joint Statistical Meetings 2010, Statistical Computing Section.](https://www.stat.auckland.ac.nz/%7Eihaka/downloads/JSM-2010.pdf)
 
 4. [Ihaka, Ross; Temple Lang, Duncan (25 August 2008). Back to the Future: Lisp as a Base for a Statistical Computing System (PDF). Compstat 2008.](https://www.stat.auckland.ac.nz/%7Eihaka/downloads/Compstat-2008.pdf)
 
 5. [Morandat, Frances; Hill, Brandon (2012). "Evaluating the design of the R language: objects and functions for data analysis"](http://r.cs.purdue.edu/pub/ecoop12.pdf)

### Blogs

 6. Eric Blair, ["R is slow"](http://fluff.info/blog/arch/00000172.htm) (2006)

Data structures
========================================================

### data frame
  - A list of lists that make full array

### data table
  - Kind of like Dataset
 
### list
 - Very similar to Mathematica's associations
 
### vector
 - There are no scalars 
 
### factor
 - For handling categorical variables. I avoid using it. 
 
### sparse matrix
 - Really nice!
  
### formula
  - Not a data structure but object to know and use.

### environment
  - Similar to Context` but also Association. It is used to handle scoping
     (variable values, bidings, etc.)
  


R tips for a Mathematica programmer
========================================================

### Data structures
  - Learn data frames manipulations.
  - Use named elements in vectors and lists.
  - Use named rows and columns for matrices and data frames.
  
### Functions over data
  - Study and use the packages 'plyr' and 'dplyr'.
  - The articles of [Hadley Wickham](https://en.wikipedia.org/wiki/Hadley_Wickham) are insightful for R's culture and data manipulation in general.
  
### Map, Reduce, Filter
  - Those correspond to *Mathematica* Map, Fold, Select.

### In complicated data massaging use sqldf
  - The package sqldf lets you treat your data frames as SQL tables.
  - Reasonbly fast, great for project and task transition.

R tips for a Mathematica programmer 2
========================================================

### The Extract operator
  - Similar to Part
  - Used in a fashion similar to Pick

### Intros to R for programmers
  - See look for books/blogs like this:
    [R language for programmers](http://www.johndcook.com/blog/r_language_for_programmers/)
    

Object-oriented programming
========================================================

### S3

 - Functional polymorphism.
 
 - Rudimentary, can be trivially implemented with Mathematica's pattern matching of signatures.

### S4
 
 - Very nice, based on CLOS. 


Graphics
========================================================

R has three distinct graphics systems: 
 1. the “traditional” graphics system, 
 2. the grid graphics system (the [lattice](http://www.inside-r.org/packages/cran/lattice) package based on the [Trellis graphics](http://stat.bell-labs.com/doc/trellis.user.pdf)), and 
 3. ggplot2.
 
### Overview presentation from the author of "R Graphics"
[Murrell "R Graphics"] (https://www.stat.auckland.ac.nz/~paul/Talks/CSIRO2011/rgraphics.pdf)

 - Comments
   - Interesting and insightful (for an R user), but the plots are not impressive compared to *Mathematica*.

### Links

- [CRAN Task View: Graphic Displays & Dynamic Graphics & Graphic Devices &   Visualization](https://cran.r-project.org/web/views/Graphics.html)

- [Lattice project](http://lattice.r-forge.r-project.org/documentation.php)

- [ggplot2]()

(Demo Plots3D.R for 3D graphics.)


Parallel programming
========================================================

### package 'parallel'
```
if ( TRUE ) {
  cat("\n\tParallel NN's generation with mcparallel:")
  
  cat("\n\tTotal number of cores:", detectCores() )
  cat("\n\tCores to be used:", mcCores )
  
  # We assume the rowIDs to be the item ID's we want to compute NN's for.
  cat("\n\t\tComputing overall similarity...")
  startTime <- Sys.time()
  
  rowIDToIndex <- 1:length(rowIDs)
  names(rowIDToIndex) <- rowIDs
  
  rowIDToIndexList <- Slice(
    rowIDToIndex, 
    ceiling( length(rowIDToIndex) / mcCores ) )
  
  pls <- 
    lapply( 1:length(rowIDToIndexList), function(i) {
      fname <- paste("./overallNNs", as.character(i), ".tsv", sep = "_")
      mcparallel( GenerateAndWriteNNs( rowIDToIndexList[[i]], rowIDs, fname ), as.character(i) )
    })
  print(mccollect(pls, wait=TRUE))
  
  endTime <- Sys.time()
  cat("\n\t\tParallel SIMD computing time:", difftime( endTime, startTime, units="secs" ) )
  
```


Parallel programming 2
========================================================

### package 'foreach'

```  
guessesPar <-
      foreach( parMovieInds = slicedMovieIndsList, .combine = rbind ) %dopar% {
        res <- llply( parMovieInds, function( i ) {
          mvec <- movieVecs[ i,,drop=FALSE]
          recs <- SMRRecommendationsByProfileVector( gtSMR, mvec, 30 )
          prof <- SMRProfileDF( gtSMR, itemHistory = recs[,c(1,3)] )
          prof[ gtSMR$TagTypeRanges[ nrow(gtSMR$TagTypeRanges), 1] <= prof$Index, ]
        }, .progress="time", .parallel = TRUE )
        names(res) <- movieIDs
      }
```


Efficient implementations
========================================================

Lots of people (companies) are inclined to take a subset of the R language and make efficient implementations for it.

For example $H_2O$ by 0xdata: [http://h2o.ai/product/](http://h2o.ai/product/).

<!--- The following two commands remove any previously installed H2O packages for R.
if ("package:h2o" %in% search()) { detach("package:h2o", unload=TRUE) }
if ("h2o" %in% rownames(installed.packages())) { remove.packages("h2o") }
 
# Next, we download, install and initialize the H2O package for R.
install.packages("h2o", repos=(c("http://s3.amazonaws.com/h2o-release/h2o/rel-kahan/5/R", getOption("repos"))))
--->


```r
##library(h2o)
##localH2O = h2o.init()
```

Let us run a demo to see $H_2O$ at work.

```r
##demo(h2o.glm)
```

From 

 Get started with H2O in 3 easy steps

 1. Download H2O. This is a zip file that contains everything you need to get started.

 2. From your terminal, run:

```
cd ~/Downloads
unzip h2o-3.2.0.9.zip
cd h2o-3.2.0.9
java -jar h2o.jar
```

 3. Point your browser to [http://localhost:54321](http://localhost:54321).


Examples for "on par"
========================================================

### ODE simulations interactive interface
    
### Movies recommendations engines

    - *Mathematica* interface
    - [R/Shiny interface](http://127.0.0.1:7396)
     
### Geo-spatial statistics and recommendations

### Functional parsers

### Well slideshows, reports, etc.


Examples where R is worse
========================================================

### Tiger shark migration analysis

  - I wrote this [blog post](https://antonantonov.wordpress.com/2012/05/22/tiger-shark-data-analys/) three years ago.
  - I was not able to redo the experiments in R because it was very hard to get the data. 
    - (...and I gave up).
   
### 2D and 3D quantile regression

  - See this [blog post](https://mathematicaforprediction.wordpress.com/2014/11/16/directional-quantile-envelopes-in-3d/).
  - This would be hard to implement without the computational regions technology.
  
### Finding local extrema in noisy data

  - See this [blog post](https://mathematicaforprediction.wordpress.com/2015/09/27/finding-local-extrema-in-noisy-data-using-quantile-regression/).
  - The approach would be hard to implement since R does not have differentiation and equation solving.  
     - Yes, I looked for ["automatic differentiation"](https://github.com/quantumelixir/radx) in R.
     - And yes, you can solve systems of linear equations.
 
 
Examples for future projects where R would be on par with Mathematica
========================================================
    
### GitHubData plots

### Time series conversational engine

### Most characterizing sentence extraction

### Music 

### Other examples at GitHub
- I plan to post example comparison projects at GitHub:
  [MathematicaVsR](https://github.com/antononcube/MathematicaVsR/).


Examples where R "has a package for it"
========================================================

### Mel Frequency Cepstral Coefficients
    - tuneR

### Frequent sets and associations rules mining
    - arules

### **Many others**...

On being bilingual
========================================================

- In order to know your mountain you should climb the one next to it.

- Here are *Mathematica* packages I wrote that follow R existing functionalities:
  - [MosaicPlot.m](https://mathematicaforprediction.wordpress.com/2014/03/17/mosaic-plots-for-data-visualization/comment-page-1/)
  - [QuantileRegression.m](https://github.com/antononcube/MathematicaForPrediction/blob/master/QuantileRegression.m)
  - RecordsSummary in [MathematicaForPredictionUtilities.m](https://github.com/antononcube/MathematicaForPrediction/blob/master/MathematicaForPredictionUtilities.m)
  - [RSparseMatrix.m](https://github.com/antononcube/MathematicaForPrediction/blob/master/Misc/RSparseMatrix.m)

Conclusions
========================================================

- If you know *Mathematica* well I am not sure it is worth investing learning R if you do not have some project that would motivate you.

- Having R in LaTeX or org-mode is really great!

- I mostly side with the venom toward R seen in the book "The R Inferno" by Burns.

- More constructive to learning R is the book "Advanced R" by [Hadley Wickham](https://en.wikipedia.org/wiki/Hadley_Wickham).
  - And in general it is a good idea to read H. Wickham's writings.
  
- R is slow, but keep in mind that at least half dozen fast implementations exist for some subsets of R.

- More examples at GitHub
  [MathematicaVsR](https://github.com/antononcube/MathematicaVsR/).
