_Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away._  — [Antoine de Saint Exupéry](http://en.wikipedia.org/wiki/Antoine_de_Saint-Exup%C3%A9ry)

_Inside every large program there is a small program trying to get out._  — [CAR Hoare](http://en.wikipedia.org/wiki/C._A._R._Hoare)

_Less is more._ - [Ludwig Mies van der Rohe](http://en.wikipedia.org/wiki/Ludwig_Mies_van_der_Rohe)

_Make the irreducible basic elements as simple and as few as possible without having to surrender the adequate representation of a single datum of experience._ - [Albert Einstein](http://en.wikipedia.org/wiki/Albert_Einstein)

_Simple can be harder than complex: You have to work hard to get your thinking clean to make it simple. But it's worth it in the end because once you get there, you can move mountains."_ [Steve Jobs, BusinessWeek interview, May 1998](http://www.bbc.co.uk/news/mobile/world-us-canada-15195448)

**Latest News**  June 14, 2013.  proto among the **top 10** downloaded packages out of all packages on CRAN.  See [list](http://www.r-statistics.com/2013/06/top-100-r-packages-for-2013-jan-may/).

Discussion of proto (and my other packages) is now available on the [sqldf discussion group](https://groups.google.com/forum/?fromgroups#!forum/sqldf).

Below on this page are sections on:

## Introduction ##

[proto](http://cran.r-project.org/web/packages/proto/index.html) (google code name `r-proto`) is an R package which facilitates a style of programming known as prototype-based programming. Prototype-based programming is a type of object oriented (OO) programming in which classes and objects are unified into a single concept, prototypes.  This makes `proto` and prototye programming simpler than the usual OO model yet it retains the OO features of inheritance (known as delegation in the prototype model) and OO dispatch.  Applications, News, Additional Information sources, Proto Bugs and Avoiding R Bugs sections are given below while associated Links are in the [links page](http://code.google.com/p/r-proto/wiki/Links).

## Applications ##

There are

  * 13 CRAN packages that directly refer to proto via their Depends, Enhances, Imports or Suggests lines in their DESCRIPTION files.   (Packages not on CRAN would be in addition to that.)
  * 84 packages on CRAN that directly refer to proto or to another CRAN package that in turn directly refers to proto suggesting that packages that use proto are themselves used by many other packages.
  * 2,128 packages on CRAN (over half of CRAN) that have any direct or indirect dependency on proto, i.e. refer directly to proto or to a package which indirectly refers to proto recursively to any depth.

(The above statistics were gathered on September 26, 2011.)

Here are some packages that directly refer to proto or are typically used with proto:

  * The R [gsubfn](http://gsubfn.googlecode.com) package provides a generalization of the R function `gsub` for which the replacement string can be a function.  The replacement string can also be a `proto` object which holds the function as well as state information which can be carried from one function invocation to the next.

  * [pmg](http://cran.r-project.org/package=pmg) is an R package that provides a GUI interface to R that uses `proto` internally.

  * The [gWidgets](http://cran.r-project.org/package=gWidgets) R package for user interface construction can be used in conjunction with `proto` as seen from [this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-September/046888.html).

  * [gWidgetsWWW](http://cran.r-project.org/package=gWidgetsWWW) package is an implementation of `gWidgets` for the web that works with [RApache](http://biostat.mc.vanderbilt.edu/rapache/) on Mac and Linux (and under Windows using a virtual Linux machine). `gWidgetsWWW` uses `proto` internally.

  * The [sqldf](http://sqldf.googlecode.com) package allows R users to manipulate R data frames using SQL.  It uses `proto` internally.

  * [DescribeDisplay](http://cran.r-project.org/packages=DescribeDisplay) produces publication quality graphics from the output of the describe display plugin of [GGobi](http://www.ggobi.org/).

  * [traitr](http://cran.r-project.org/package=traitr) is an R package for creating GUIs using the model/view/controller (MVC) paradigm.

  * [benchmark](http://cran.r-project.org/package=benchmark) is an R package for benchmarking experiments.  See `as.dataset` in the package.

  * [nls2](http://cran.r-project.org/package=nls2) is an R package for nonlinear regression.  The `as.lm.nls` method of `as.lm` uses `proto`.

  * [MetaQC](http://cran.r-project.org/package=MetaQC) is an R package for quality control of microarray data.  The `MetaQC` function returns a `proto` object containing the data and methods.

  * [R2STATS](http://yvonnick.noel.free.fr/r2stats/) (also see [R2STATS on CRAN](http://cran.r-project.org/package=R2STATS)) is a GUI for GLM and GLMM models.  proto is used for [structuring the GUI](http://permalink.gmane.org/gmane.comp.lang.r.gui/706).

  * [AtelieR](http://cran.r-project.org/package=AtelieR).  A collection of statistical simulation and computation tools with a GTK GUI.  proto is used for structuring the GUI.

  * [directlabels](http://cran.r-project.org/package=directlabels) [home page](http://directlabels.r-forge.r-project.org/).  Easily add direct labels to plots.

  * [ggplot2](http://cran.r-project.org/package=ggplot2) uses proto as the container to represent geoms.  Related packages [bams](http://cran.r-project.org/package=bams), [ggmap](http://cran.r-project.org/package=ggmap), [ggsubplot](http://cran.r-project.org/package=ggsubplot), [ggtern](http://cran.r-project.org/package=ggtern), [ggthemes](http://cran.r-project.org/package=ggthemes) use proto in a similar way.

  * others. argparse, benchmark, DTR, ggHorizon, multilevelPSA, PKgraph, Rcell, coefplot, ggmap, ggsubplot, ggtern, ggthemes, bams, extracat, HistData - TODO. Add some info on these or maybe the list is just getting too large to describe every one.


## News ##

March 29, 2012.  The D language adds free methods: http://drdobbs.com/blogs/cpp/232700394  proto has had them all along!

March 19, 2011. proto 0.3-9.1 has been uploaded to CRAN.  It addresses a minor issue in R CMD check.  There is no functional difference from the prior version.

March 11, 2011.  proto 0.3-9 has been uploaded to CRAN.  It fixes the minor known bugs and has been changed to be compatible with the upcoming R 2.13.  (It should still work on earlier versions of R as well.)

September 19, 2010.  Added "Less is more" quote at top.

August 13, 2010.  Michael Bedward of the Last Resort Software blog has written an [article](http://lastresortsoftware.blogspot.com/2010/08/fun-with-proto-package-building-mcmc.html) on MCMC sampling for Bayesian regression using proto.

July 18, 2010.  Added Einstein quote near top of this page and on the [links page](http://code.google.com/p/r-proto/wiki/Links) added a link to Secrets of Simplicity presentation.

June 20, 2010.  Added reference to the [benchmark](http://cran.r-project.org/web/packages/benchmark/index.html) package above.

March 12, 2010.  The Appendix of [this document on AlgoTrader](http://code.google.com/p/algotrader/source/browse/trunk/current/inst/doc/AlgoTrader.Rnw) contains an introduction to proto that could be of interest to anyone wishing to use proto even if the Algotrader package is not applicable to their area. (This may have been there for some time but I just noticed it.)

March 2, 2010.  An [example](https://stat.ethz.ch/pipermail/r-help/2010-March/230353.html) of a stack in proto was posted on r-help.

February 27, 2010.  Recently Duncan Murdoch [discussed](http://pages.citebite.com/i2o1i8m6k6mgs) one aspect of R that he would prefer worked differently; namely, that objects were not ultimately looked up in the global environment.  If you are using proto you can emulate it.  The following are three different variations:
```
p <- proto(as.environment(2), ...) # searches loaded core and user packages but not globalenv()
p <- proto(as.environment("package:Stats"), ...) # searches core packages but not user packages nor globalenv()
p <- proto(baseenv(), ...) # searches baseenv() but not other core packages nor user packages nor globalenv()
```
Note the following R command which shows the R search path:
```
search()
```
The first example starts at the second entry in the search list (which is why it omits the global environment).  The next example starts at the Stats entry in the search list and moves forward.  The last example starts right at the end of the search list thereby skipping over the rest of it and was suggested by Peter Daneberg in the same thread as appropriate in certain  circumstances.

For example, one could define a function like this:
```
f <- proto(as.environment(2), f = function(this, x) x)$f
f(3)
```
or like this:
```
f <- with(proto(as.environment(2), f = function(x) x), f)
f(3)
```
In this case `environment(f)` will be the proto object and it parent will be the second package on the search list.

Jan 18/10.  An example of using proto to work with views on matrices can be found [here](https://stat.ethz.ch/pipermail/r-help/attachments/20100118/e6ec1b49/attachment.pl).

Jan 15/10.  Added [traitr](http://cran.r-project.org/web/packages/traitr/index.html)  to the list of applications above that use proto.

Sep 11/09.  There is information on command line completion for proto objects [here](https://stat.ethz.ch/pipermail/r-help/2009-September/211296.html).

Sep 7/09.  Added [AlgoTrader](http://algotrader.googlecode.com) package to the list of applications above that use proto.

Sep 3/09.  Added the [Things Every Programmer Should Know](http://programmer.97things.oreilly.com/wiki/index.php/Edited_Contributions) link in the [links page](http://code.google.com/p/r-proto/wiki/Links).

Aug 28/09.  Wrote out abbreviated arguments in full in the svn to avoid build warnings.

Aug 19/09.  Added the [Dog Food](http://www.c2.com/cgi/wiki?DogFood) link in the [links page](http://code.google.com/p/r-proto/wiki/Links).

Aug 8/09.  Added the [Bad Programming](http://sites.google.com/site/yacoset/Home/signs-that-you-re-a-bad-programmer) link in the [links page](http://code.google.com/p/r-proto/wiki/Links).

Jun 5/09.  Added information (see above) on the [sqldf](http://sqldf.googlecode.com) R package which uses `proto` internally.

Apr 5/09.  Added information (see above) on the [ascii](http://cran.r-project.org/web/packages/ascii/index.html) R package which uses `proto` internally.

Oct 3/08.  Updated links to Lieberman (1986) and Taivalsaari (1996) papers in the [links page](http://code.google.com/p/r-proto/wiki/Links).

Oct 3/08.  Confirmed that the LazyLoad bug in R is still present.  See the first point in the _Avoiding R Bugs_ section below and [this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-October/047184.html).

July 5/08.  Added a fifth point in the Avoiding R Bugs section.

May 19/08.  Added quotations to top of this page.

Mar 7/08.  In the [development version](http://code.google.com/p/r-proto/source) of `proto` the `parent` argument to the `proto` function may now be a function in which case its environment is used as the parent.  This facilitates constructing proxy `proto` objects: `with(proto(f, f = f, a = 1), f)` wedges an anonymous proto object between `f` and its environment inserting `a` into the proxy so that it can be accessed as a free variable from within `f`.

Mar 7/08.  The method of `proto` proxies was illustrated in an [r-devel post](https://stat.ethz.ch/pipermail/r-devel/2008-March/048625.html).

Feb 25/08.  A `dput.proto` routine was [posted on r-devel](https://stat.ethz.ch/pipermail/r-devel/2008-February/048523.html).

Jan 26/08.  Just noticed that there was a modification to the R development source made on Jan 24, 2008, see [r44139](https://code.google.com/p/r-proto/source/detail?r=44139) in [r-devel log](http://developer.r-project.org/R.svnlog.2007), which indicates that a bug in R related to promises has been fixed.  Since proto 0.4, the current development version, depends heavily on promises this should be beneficial.  The following code, which is not dependent on proto, previously failed under R but now it works:
```
# code below previously triggered errors but now works - R 2.6.2 (2008-01-26 r44181)

f <- function(x) environment()
z <- as.list(f(7))
dput(z)
structure(list(x = 7), .Names = "x")
z[[1]] == 7  # should return TRUE
force(z[[1]]) == 7 # should return TRUE
```

Jan 09/08.  Added a second paragraph to the LazyLoad subsection of the `Avoiding R Bugs` list at the bottom based on a recent discussion on the r-devel list.  Also added a new section `Proto Bugs` below.  Note that all known bugs are fixed in the [development version](http://code.google.com/p/r-proto/source) of `proto`.

Dec 07/07.  `as.proto.data.frame` method added to the devel version of `proto`.  Its
just a synonym for `as.proto.list`.
```
as.proto.data.frame <- as.proto.list
```

Dec 06/07.  `print` bug added to bug list below.

Dec 01/07.  Added a new argument, `eval.env = parent.frame()` to the `proto` function in the devel version of `proto`.  It defines the environment in which promises in the `...` arguments are evaluated.  The default value of `eval.env` is normally what one wants; however, in the case of wrappers around `proto` one would generally want the calling frame of the wrapper rather than the frame which directly calls `proto` and this argument facilitates that. The need for this is related to the problem in R described in point #4 of _Avoiding R Bugs_ at the end of this page.

Oct 28/07.  Added a reference to [pmg](http://wiener.math.csi.cuny.edu/pmg) in the Applications section above as it uses `proto` internally.

Oct 17/07.  Added a reference to this [r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-October/047184.html) and discussion to the LazyLoad subsection of the _Avoiding R Bugs_ section at the end of this page.  (This applies to packages that have `proto` objects at top level.  Also see [ReleaseNotes.txt](http://r-proto.googlecode.com/svn/trunk/inst/ReleaseNotes.txt).)

Sep 30/07.  A workaround for the R bug where promises in lists do not get evaluated was developed.  (This never affected the released version of proto on CRAN.)   See _Avoiding R Bugs_ section below.

Sep 25/07.  Added [ReleaseNotes.txt](http://r-proto.googlecode.com/svn/trunk/inst/ReleaseNotes.txt) describing new features of the [development version](http://code.google.com/p/r-proto/source) (proto 0.4-0) also found on [Source](http://code.google.com/p/r-proto/source) tab above.  To try out, after installing from the [Source Repository](http://code.google.com/p/r-proto/source) run this (under R 2.6.2):
```
library(proto)
example(proto)
demo(proto)
demo("proto-vignette")
demo("proto-gWidgets") # needs gWidgets package to be installed
```
or to try it without installing anything (other than CRAN version of proto):
```
library(proto) # loads CRAN version of proto
source("http://r-proto.googlecode.com/svn/trunk/R/proto.R") # load changed code
demo(proto)
source("http://r-proto.googlecode.com/svn/trunk/demo/demo-vignette.R")
source("http://r-proto.googlecode.com/svn/trunk/demo/demo-gWidgets.R")
```
Sep 20/07.  John Verzani has added another proto/gWidgets user interface example [here](http://wiener.math.csi.cuny.edu/pmg/gWidgets/Examples/ProtoExample-II-ex.html).  It is in addition to his others [here](http://wiener.math.csi.cuny.edu/pmg/gWidgets/Examples/ProtoExample-ex.html) and [here](http://wiener.math.csi.cuny.edu/pmg/gWidgets/Examples/ScopingIssues-ex.html). Also see [this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-September/046888.html) for another proto/gWidgets example.

Sep 15/07.  proto 0.3-8 uploaded to CRAN.  Only changes are those needed to satisfy
R 2.6.0.

## Citation ##

To get the citation for this package use the R command:
```
citation("proto")
```

## Additional Information ##

Additional information is available at:

  * one page [overview](http://code.google.com/p/r-proto/wiki/Overview) (also accessible via the [Wiki tab](http://code.google.com/p/r-proto/w/list) above).
  * tutorial (http://cran.r-project.org/web/packages/proto/vignettes/proto.pdf)
  * reference card (http://cran.r-project.org/web/packages/proto/vignettes/protoref.pdf)
  * background paper on R and prototype programming ([Kates & Petzoldt, 2004](http://r-proto.googlecode.com/files/prototype_approaches.pdf))
  * other literature on prototype programming ([Lieberman, 1986](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.69), [Taivalsaari, 1996](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.56.4713), [Wikipedia](http://en.wikipedia.org/wiki/Prototype-based_programming))
  * release notes ([Release notes for devel version](http://r-proto.googlecode.com/svn/trunk/inst/ReleaseNotes.txt)) and [NEWS file](http://r-proto.googlecode.com/svn/trunk/inst/NEWS)
  * help pages (http://cran.r-project.org/web/packages/proto/proto.pdf)
  * svn repository containing the source code at the [Source](http://code.google.com/p/r-proto/source) tab above.
  * a queuing simulation written with proto is available [here](http://www.statisticsblog.com/2011/10/waiting-in-line-waiting-on-r/)
  * examples of using `proto` with `gWidgets` listed in Applications section above

## Proto Bugs ##

The following are bugs in the released version of `proto` on CRAN.  They are all fixed in the development version already.

1. `str.proto`.  This will not affect most users but one user was redefining `print` and that caused `name.proto` (hence `str.proto`) to break.  The call to `print` has been replaced with a call to `print.default` in `name.proto` to avoid this in the devel version of `proto`.  Here are three workarounds in the meantime:
Run this code:
```
name.proto <- proto(print.proto = print.default, f = proto::name.proto)$f
```
or, source the new version of `graph.proto.R` which is the file that contains `name.proto`:
```
source("http://r-proto.googlecode.com/svn/trunk/R/proto.R") # load changed code
```
or, ensure that your `proto` object has a `..Name` component.  For example, this works even if `print` is redefined:
```
print <- function(x, ...) 1
p <- proto(..Name = "proto object: p", x = 1)
name.proto(p)
str(p)
rm(print)
```

2. A `proto` object could not have the name `x`.

## FAQ ##

1. What is the special meaning of dot in proto?

When writing method bodies the first argument to the method should be the receiver object.  It has been conventional to use a dot (i.e. a variable name consisting only of a period) for this and the receiver object and dot are often used interchangeably when discussing the receiver object but, in fact, its no more than a convention and `self`, `this` or anything else that the developer of proto methods wishes to use to name the first argument of a method are acceptable.

2. What is the difference between a function and a proto method?

A proto method is a component of a proto object which is an ordinary R function that takes the proto object as its first argument.  When the method is run using `p$meth` syntax `meth` is looked up in proto object `p` and 'p' is also inserted into `meth`'s first argument (i.e. it is curried) so that `p$meth` has one fewer arguments than `meth`.

```
p <- proto(meth = function(., x) x)
class(p$meth) # c("instantiatedProtoMethod", "function")
p$meth(3)
```

When a function is inserted into a proto object using the syntax shown above or using this syntax:
```
p$meth <- function(., x) x
```
the environment of the function/method is changed to point to the proto object  `p`.

To _not_ have the environment reset use the `funEnvir=FALSE` argument as in `proto(..., funEnvir = FALSE)` or use `[[` syntax as in `p[["f"]] <- function() 1` . (Note that if the environment is not reset then the reserved variables `.that` and `.super` cannot be used within the function/method.)

If we agree to always reset the environment of methods and never reset the environment of functions then we can use that fact to check whether a function is a method or not:

```
p <- proto(g = function(.) 1)
# insert function into p without resetting environment
p[["f"]] <- function() 1

# nm is the name of a function or method in p
# if its environment is p then its a method and otherwise is a function
is.method <- function(p, nm)  identical(p, environment(p[[nm]]))
is.method(p, "f") # FALSE
is.method(p, "g") # TRUE
```

If we don't want to make such an agreement with ourselves but are willing to agree that the first argument of every method is a dot (`.`) then we could use this alternate strategy which checks the name of the first argument of the function/method to determine if its a dot:
```
p <- proto(f = function() 1, g = function(.) 1)
is.method2 <- function(p, nm) identical(names(formals(p[[nm]]))[1], ".")
is.method2(p, "f") # FALSE
is.method2(p, "g") # TRUE
```

3. How do I add a function to a proto object without having proto change its environment to that of the proto object?

Consider this example.  The environment of the copy of `f` inserted into `p` was changed to point to `p` so invoking `p$f()` finds the `x` in `p` and not the `x` in the global environment even though `f` was originally defined there.

```
x <- 3
f <- function(.) x
p <- proto(x = 2, f = f)
p$f() # 2 since f's envir reset to p
```

There are several ways to allow `f` to retain its original environment if that is desired.  One way is to use the `funEnvir` argument to `proto` like this:
```
# 1
p <- proto(x = 2, f = f, funEnvir = FALSE)
p$f() # 3 since f's envir not reset
```
A second way is to insert `f` into `p` using `[[...]]` like this:
```
# 2
p <- proto(x = 2)
p[["f"]] <- f
p$f() # 3 since f's envir not reset
```
A third way is to wrap it in a method (rather than defining it as a component) like this:
```
# 3
p <- proto(x = 2, f. = function(.) f(.))
p$f.() # 3 since f's envir not reset, only f.'s is
```

4. Is there a way to define proto Mixins?

Thanks to Daniel Mahler for discussions on [Mixins](http://en.wikipedia.org/wiki/Mixin):

```
# two proto objects
library(proto)
dog <- proto(species = "dog")
cat <- proto(species = "cat")

# mixins (realized using lists)
Big <- list(size = "big")
Black <- list(color = "black")

# mixin composition (= list concatenation)
Big.Black <- c(Big, Black)

# create two proto objects mixing in Big.Black
# The first is a child of proto object dog and the second is child of cat

Fido <- as.proto(Big.Black, envir = dog$proto(name = "Fido"))
Whisker <- as.proto(Big.Black, envir = cat$proto(name = "Whisker"))

# or equivalently this chaining style works
# (must use x= in as.proto for this construct to work)

Fido <- dog$proto(name = "Fido")$as.proto(x = Big.Black)
Whisker <- cat$proto(name = "Whisker")$as.proto(x = Big.Black)

# this works too

Fido <- dog$proto(name = "Fido")$as.proto(x = Big)$as.proto(x = Black)
Whsker <- cat$proto(name = "Whisker")$as.proto(x = Big)$as.proto(x = Black)
```

5. How does one export a proto object from a package.

If `p` is the proto object then add `export("p")` to your `NAMESPACE` file, add `LazyData: yes` to your `DESCRIPTION` file and create an `Rd` file which documents p as a dataset. (Note to myself: double check if this still holds given changes in R.)

6. My proto code works from a script but not when I put it in a package.

This is likely because the proto objects at top level are run at INSTALL time rather than package load time.   Put the top level proto objects in a function that generates them and then call the function at load time.  e.g.

```
# this goes in a .R file in the R directory of the package
.onLoad <- function(lib, pkg) {
    initProto()
}

initProto <- function() eval(substitute({
  p <- proto() # top level proto objects go here
}), .GlobalEnv)

```


## Avoiding R Bugs ##

Due to the fundamental nature of `proto`, it makes use of portions of R that may not be commonly accessed in other packages; therefore, it has uncovered a number of R bugs or deficencies that were not previously known or at least are less known.  Fortunately there are simple workarounds to deal with them provided you know about them.

1. LazyLoad

If a package uses lazyloading then R will erroneously change the class of all `proto` objects at top level to `"environment"`.   This [r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-October/047184.html) from the R development team confirms that it is a bug in R and that there is an intention to fix it (however, as of  R version 2.12.1  it had still not been fixed.)  See
[this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2008-October/050850.html) for details and info on how to test it.)  To avoid this bug use `LazyLoad: false` in the `DESCRIPTION` file of any package that has `proto` objects at top level.

In older versions of `R` it was possible to use `SaveImage: true` in the `DESCRIPTION` file; however, SaveImage is not available in recent versions of `R`.

One gotcha is that not specifying `LazyLoad` is not the same as `LazyLoad: false`.  As mentioned in [R News 4/2](http://cran.r-project.org/doc/Rnews/Rnews_2004-2.pdf) if LazyLoad is not specified then R will use lazy loading if there is more than 25K of R code in the package and otherwise not.  See this: [r-devel discussion](https://stat.ethz.ch/pipermail/r-devel/2007-October/047118.html).   There is some information on LazyLoad and SaveImage in [this r-devel post](http://tolstoy.newcastle.edu.au/R/devel/06/02/4025.html) and there is an article on lazy loading in [R News 4/2](http://cran.r-project.org/doc/Rnews/Rnews_2004-2.pdf).  (There was discussion that this behavior will change in R 2.9.0 where true will be the default and the odd 25K criterion will be eliminated but am not sure if that happened.)

One can test this by creating an `R` package with only two files which are (1) this `DESCRIPTION` file:

```
Package: testlazy
Version: 1.0-0
Date: 2008-10-03
Title: Test lazy loading
Author: G Grothendieck
Maintainer: G Grothendieck <ggrothendieck@gmail.com>
Description: Test lazy loading with top level objects.
Depends: proto
LazyLoad: yes
License: GPL-2
```

and (2) this `R/testlazy.R` file:

```
TopLevel <- proto()
```

We test it like this:

```
library(testlazy)
class(TopLevel)
```

If the class of `TopLevel` is just `environment` then the `proto` component of the class has been stripped by `R`.

One related problem is that if you use `LazyLoad: false` to overcome the problem above then `proto` will not be available during the package load unless it is specifically loaded so add: `require(proto)` to your code if any top level `proto` objects are created at load time.  See: [this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2008-January/047926.html) and [this related post](https://stat.ethz.ch/pipermail/r-devel/2008-January/047978.html) .

2. Promises and Lists

R is supposed to evaluate promises that are stored in lists but, in fact, it does not -- see [this thread in r-devel](https://stat.ethz.ch/pipermail/r-devel/2007-September/046930.html).  It is currently believed that this has never affected the released version of `proto` on CRAN nor does it affect the most recent devel version of `proto`.  It did affect earlier devel versions of `proto`.   Even though it seems to currently have no consequence  we are leaving this item here just in case it comes up in some new form and needs to be revisited.  (This may be fixed already in the R 2.9.0 development version.)

```
# No longer a problem but recorded here just in case.

# ensure proto 0.4-0 is installed from Source tab 
# or just load the CRAN version of proto and over top
# of it source proto.R from the repository as discussed 
# in the Sep 25th News item above
# 
# in the code below:
# - p is a proto object 
# - x a child of p created by invoking p$new
# - y is a copy of x formed by converting the
#   the proto object to a list and back to proto
#
# The problem is that although ls(y) says that gg is in y
# when we try to evaluate it, R says its not there.

p <- proto(, {
	Name <- gg <- "m" # for debugging. Can omit this line.
	new <- function(., gg) proto(., Name = "n", gg = gg)
})
# one clue is that if we
# uncomment next line and comment one after it error disappears
# x <- proto(gg = "g")
x <- p$new(gg = "g") # x is a child of p
x$Name <- "x" # for debugging.  Can omit this line.
y <- as.proto(as.list(x)) # y is a copy of x
y$Name <- "y"  # for debugging.  Can omit this line.
ls(y) # shows that gg in y
# next line gives error saying gg not found
with(y, gg)
```

3. Subclassing environments

Operating locally on an environment attribute changes its value globally which seems undesirable.

The proto class is an S3 subclass of the environment class.  Unfortunately if e is a variable holding an environment and f is a copy of it then if you set an attribute on f then e gets it too:
```
f <- e
attr(f, "abc") <- 3
```
After the above e will gain attribute abc with a value of 3 as well.  This occurs even if 3 is assigned within a function. "class" is an attribute so it also applies to the class.

4. Limitations on Use of Promises

Using pure R, there is currently no way to copy promises without evaluating them nor is there any way to discover the environment associated with a promise.    For the proto clone function it would be desirable to be able to copy promises without evaluating them while preserving their environments.  Although the preceding are not possible in pure R it is possible to do this using C.

5. `[[` Does Not Work Well with Promises

This is no longer a problem in R but is being left here in case it comes up again in some other form.

In the code below `test` fails.  Note that this code does not use `proto` and this is a general problem in R.
```
idx <- 2

# Error !!!
test <- function(pf = parent.frame()) BOD[[pf$idx]]
test()

# Returns expected result by avoiding [[
test2 <- function(pf = parent.frame()) .subset2(BOD, pf$idx)
test2()

# Also works as expected by forcing pf so its not a promise 
test3 <- function(pf = parent.frame()) { force(pf); BOD[[pf$idx]] }
test3()

# Also works as expected.  Surprisingly [[.data.frame gives different result than [[ 
# See https://stat.ethz.ch/pipermail/r-devel/2008-July/050126.html
test4 <- function(pf = parent.frame()) "[[.data.frame"(BOD, pf$idx)
test4()

```

## Tests ##

The following tests use quite a few features of `proto`:

```
library(ggplot2)

qplot(carat, price, data=diamonds, facet = color ~ clarity)
qplot(carat, price, data=diamonds, colour = interaction(color, clarity, cut))
qplot(carat, price, data=diamonds, geom=rep("point", 10))
```