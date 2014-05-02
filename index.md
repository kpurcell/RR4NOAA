---
title       : Software for Reproducible Research
subtitle    : applications for fishery stock assessment
author      : K.M. Purcell
job         : Postdoctoral Associate
logo        : noaa.jpg
framework   : io2012        # {io2012, html5slides, shower, dzslides, deckjs...}
hitheme     : solarized_light  # {tomorrow, solarized_light, web2.0}
widgets     : [mathjax, quiz, bootstrap]    # {mathjax, quiz, bootstrap}
mode        : selfcontained      # {standalone, draft}
license     : by
github      : 
 user       :kpurcell
 repo       :RR4NOAA

---

<!-- Limit image width and height -->
<style type='text/css'>
img {
    max-height: 560px;
    max-width: 964px;
}
</style>

<!-- Center image on slide -->
<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.min.js"></script>
<script type='text/javascript'>
$(function() {
    $("p:has(img)").addClass('centered');
});
</script>

## Reproducible Research 

1. **Justifications:**
    * creates an *open* standard
    * prevents *re-creation* -- facilitates *advancement* 
    * fosters *collaboration*
    * Required by a growning number of publications
    
2. **Fisheries is especially fitted for RR approaches because our work is**:
    * inherently open in that it is for the public good 
    * open to criticism & evaluation
    
3. **Stock assessment is also**:
    * Repetitive -- meaning that reproducibility is not only a necessity but also expedient.
    * Collaborative -- meaning a number of partners contribute to any stock assessment

--- 

## The Quant's Quandry

![geekChoice](http://www.globalnerdy.com/wordpress/wp-content/uploads/2012/04/geeks-and-repetitive-tasks.jpg)


--- &twocol
## Tools for Reproducible Research

*** =left

1. Version control
2. Dynamic documents
   * Markdown
   * knitR
   * pandoc


*** =right
![RR](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\RR.jpg)

--- .segue .nobackground .dark

## Version Control Systems

--- &twocol

## Version control System (VCS)

*** =left

1. Origins in software development
2. Manage changes/edits to:
  * documents
  * web sites
  * computer programs
3. Advanced file versioning, and infinite undo
4. Does not interfere with current methods (backups etc.)
5. Lots of options (Subversion, Mercurial, Git)

*** =right

![vcs](http://www.phdcomics.com/comics/archive/phd101212s.gif)

--- &twocol

## Version control System (VCS)

*** =left

* with "track changes" ```accepted==gone```
* Data changes (Who? Why? When?)
* VCS maintains a full provenance:
  * date & time of change 
  * authorof changes 
  * details on exact changes
  * SSH hashes 
 
*** =right

![vcs2](http://www.phdcomics.com/comics/archive/phd101212s.gif)

--- &twocol 
## Traditional Directory Organization

*** =left

* Lots of copies
* Good organization requires complex naming scheme (means nothing to others)
* Computer file dating unreliable ("modified date") 
* No information on differences b/w files (possibly in a separate notebook)


*** =right

![files](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\numFiles.jpg)

--- &twocol

## Version control managed folder

*** =left

1. Uses traditional directories
2. Has all your files
3. And every version you have saved !
  * this directory has 92 versions of directory
4. Process is controled by the program
5. Details are saved in a hidden file in the directory

**Does not interfere with traditional backup/archiving methods**

*** =right

![gitFolder](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\gitFolder.png)

--- &twocol
## Why git?

*** =left
* Industry standard SCM/VCS
  * most common in science
* Branching & Merging
* Small & Fast
* Distributed
* Versions assurance (checksums)
* Data staging
* Free and Open source

*** =right
![gitIcon](http://2.bp.blogspot.com/-ip6Kiruk784/UypeS9wRz1I/AAAAAAAADA4/2oXVZcqpHnI/s1600/git-logo.png)

---

## git -- Branches & Merging

![gitWrkFlow](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\gitBranch.png)

---

## Distributed vs Centralized
### Centralized
![gitCent](http://git-scm.com/images/about/workflow-a@2x.png)

---

## Distributed vs Centralized
### Distributed
![gitDist](http://git-scm.com/images/about/workflow-b@2x.png)

---

## What does this look like?

![gitGUI](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\screenshot.5.png)

---

## When to commit?
![gitGUI2](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\screenshot.1.png)

---

## Detailed files changes
![gitGUI2](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\screenshot.4.png)

---

## Each commit has all the details
![gitGUI2](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\screenshot.3.png)


--- &twocol
## GitHub
*** =left



* **Git** can also operate collaboratively
* Collaboration require an **shared** server
* The most popular platform is **GitHub**


*** =right

![gitHubIcon](http://i1-news.softpedia-static.com/images/news2/Twitter-s-Original-Logo-Designer-Only-Made-3-from-It-2.jpg)

---

## GitHub 

![kpGitHub](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\kpurcellGitHub.png)

--

## Collaboration in Git

### 1. Collaboration is fueled by **Branches**
### 2. Branches can be for different authors or different methods

![gitBranch](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\gitBranch.png)

--- .segue .nobackground .dark

## How about a new Assessment

![codeReuse](http://www.phdcomics.com/comics/archive/phd031214s.gif)

---

## Starting a new assessment, 

### 1. Clone the previous repro 
### 2. START!

![gitWrkFlow](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\git-workflow.png)

--- .segue .nobackground .dark

## Dynamic Documents

---

## Dynamic Documents

>"Let us change our traditional attitude to the construction of programs: Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to humans what we want the computer to do."

>-- Donald E. Knuth, Literate Programming, 1984

Documents with code & text in one, in which tables, values, plots are dynamically created as changes to underlying structure and data occur.

## Why?

1. Increased repeatability
2. Reduced creation time 
3. Reduced transposition errors 
4. Reduced re-creation time (no repetition when data changes)

---

## Sweave

![sweaveImg](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\sweaveDiagram.png)

---

## Sweave 
```
\section{Exploratory Data Analysis}

\begin{figure}
\begin{center}

<<fig=TRUE,echo=FALSE>>=
sunflowerplot(br.gss.dat$lon, br.gss.dat$lat, main="Sampling Intensity", xlab="Lon",
              ylab="Lat")
map("state",fill=T,col="gray",add=T)
@

\caption{This is a Sunflower plot showing spatial distribution of sampling intensity}
\label{fig:sunflower}
\end{center}
\end{figure}

The spatial distribution for sampling intensity for entire Gulf Shrimp statistics dataset can be seen in the sunflower plot \ref{fig:sunflower}.  Each line is a samples and therefore more developed
petals represent positions with higher sampling.  The sampling intenstiy uniform and plenty dense. 
```

--- 

## Rmarkdown Example

![dynDocEx](http://www.rstudio.com/images/docs/markdownChunk.png)

--- &twocol
## Markdown  

*** =left 

* Created by John Gruber  
* Simplicity over LaTeX  
* Basic keyboard commands for formatting
* Faster, due to limited mouse use
* Flexible -- Allows use of LaTeX code
* Easily managed with VCS
* Standardized format for conversion

*** =right

![sweaveImg](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\mdSyntax.png)

--- &twocol

## Knitr  

*** =left

* `knitR()` is a R package for dynamic report generation  
* created by Yihui Xie (Iowa State, RStudio)
* works with other languages (*Awk*, *Lisp*, etc.)
* highly customizable (show code, hide code, etc)
![knitrCustom](http://www.rstudio.com/images/docs/markdownChunkOptions.png)
* Generates PDF (via LaTex), HTML

*** =right

![knitrBook](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\knitrBook.jpg)

---

## How does it work? 

**It takes this code:**  

![knitrE](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\knitrEx.png)

And creates the previous slide:

--- &twocol

## Knitr  

*** =left

* created by Yihui Xie (Iowa State, RStudio)
* `knitR()` is a R package for dynamic report generation  
* works with other languages (*Awk*, *Lisp*, etc.)
* highly customizable (show code, hide code, etc)
* Generates **PDF** (via LaTex), **HTML**

*** =right

![knitrBook](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\knitrBook.jpg)

--- .segue .dark

## For the MS Word hold outs!
![antiMS](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\antiMS.jpg)

--- &twocol
## Pandoc conversion utility
*** =left


* Swiss Army Knife
* Converts between  **43** formats
* Renders Lit. Cited (No need for EndNote)
* can run from within R



*** =right

![pandocCon](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\pandoc.jpg)

Inputs  | Outputs
------------- | -------------
Markdown      | **Word .docx**
HTML          | LaTex
DocBook       | LaTex Beamer
LaTex         | **PDF**
MediaWiki     | HTML 5

---

## Sources for more information

1. [Software Carpentry](http://software-carpentry.org/v4/index.html)  
2. [RStudio](https://support.rstudio.com/hc/en-us/articles/200552086-Using-R-Markdown)
3. [Try Git (quick 15 minute tutorial)](https://try.github.io/levels/1/challenges/1)
4. [GitHub Guides](https://guides.github.com/)


---

## This is the method you are looking for!

![obiOcto](C:\\Users\\Kevin.Purcell\\Documents\\GitHub\\RR4NOAA\\images\\octobiwan2.jpg)



