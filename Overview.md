[![](http://r-proto.googlecode.com/files/prototree.gif)](http://r-proto.googlecode.com/files/prototree.R)
(click for source code)

# The R proto package #

## What is proto? ##

proto is an R package which facilitates a style of programming known as prototype programming. Prototype programming is a type of object oriented programming in which classes are not a primitive notion though it sufficiently powerful to encompass them. proto is simple yet retains the object oriented features of delegation (the prototype counterpart to inheritance) and object oriented dispatch.

proto can be used to organize data and procedures without the overhead of defining classes while still providing convenient access to an object oriented style of programming. Furthermore, it can be used in a class-based style, as well, so that incremental design can begin with defining the concrete objects and later transition to abstract classes, once the general case is understood.

proto includes facilities for automatic generation of visual documentation on the object relationships in a system such as the diagram shown above. In that diagram there is an object R with children c and a. c has children d and b and the upper case objects are children of b.

Because proto objects are just environments with different semantics, proto also has a number of uses outside of object oriented programming. proto can enable the use of pass-by-reference (as opposed to pass-by-value) and can faciliate the use of environments within R as shown in some of the examples on this page.

The key goals of the package are to integrate into R while providing nothing more than a thin layer on top of it.

## Prerequisites ##

proto runs under  R, a freely available system for statistical computation and graphics.  Certain functionality uses
packages graph and Rgraphviz from Bioconductor. proto can run without these if the graphical representation of object diagrams is not required.
Operating systems: All operating systems on which R can be installed: Linux, Windows, Mac, UNIX

## Installation ##
proto can be installed directly from the internet within R either via the menu (on Windows) or via the R command line:

```
     > install.packages("proto",  dependencies = TRUE)
```

The source code is from CRAN in **.tar.gz format and precompiled binaries for Windows in**.zip format.   The development source is avalable at the svn repository at the Source tab above.

## Documentation ##

Extensive documentation (help files, tutorial and reference card) is part of the installed package or available directly:

  * online help documentation of the proto package (functions, examples): http://cran.r-project.org/doc/packages/proto.pdf

  * In R, enter this to get a list of the documentation items that come with proto:

```
     > library(proto)
     > package?proto 
```

  * tutorial (with many examples): http://cran.r-project.org/doc/vignettes/proto/proto.pdf

  * reference card: http://cran.r-project.org/doc/vignettes/proto/protoref.pdf

  * background on prototype-based programming:
    * Kates and Petzoldt (2004). Prototype-based programming in statistical computation.  Manuscript describing prototype-based programming, in general, in a way that is accessible to users of R: http://r-proto.googlecode.com/files/prototype_approaches.pdf
    * Henry Lieberman (1986). Using Prototypical Objects to Implement Shared Behavior in Object Oriented Systems. http://citeseer.ist.psu.edu/lieberman86using.html
    * Antero Taivalsaari (1996). Classes vs. Prototypes Some Philosophical and Historical Observations. http://citeseer.ist.psu.edu/taivalsaari96classes.html
    * Wikipedia on prototype-based programming.  http://en.wikipedia.org/wiki/Prototype-based_programming


## Examples ##

proto can be used for object-oriented programming (last two examples below) as well as a number of situations not related to object oriented programming (first two examples below). The following examples are, in part, collected from the [r-help
https://stat.ethz.ch/mailman/listinfo/r-help mailing list] and therefore represent real problems that users of `R` have encountered that could be addressed by `proto`. The third example is pedagogical but larger similar examples of its type can be found in the [http://cran.r-project.org/doc/vignettes/proto/proto.pdf](tutorial.md) .

1. Facilitate the use of references rather than passing by value: For example, create a `proto` object, `p`, with a matrix component, `mat`. We can now update it in place using function `incr` which references and updates mat in place in the `proto` object so that it need not be physically copied back and forth.

```
     library(proto)
     p <- proto(mat = matrix(1:25, 5))
     incr <- function(x) with(x, mat[,1] <- mat[,1] + 1)
     incr(p)
     p$mat # mat has been updated
```

2. Implicitly reset the enviornment of a function.  Here `ll` has free parameters `x` and `y` which would not be found when mle calls it since `ll`'s parent is the global environment and `x` and `y` are not located there; however, when `ll` is passed to `fit.mle` in formal argument `FUN` we can place `FUN` into a `proto` object which will implicitly reset its parent to that object and since the `proto` object is defined in `fit.mle` its parent will be the environment in `fit.mle` and so it will find the `x` and `y` arguments that are known within `fit.mle`:

```
     library(proto)
     library(stats4)
     ll <- function(ymax=15, xhalf=6) 
                   -sum(stats::dpois(y, lambda=ymax/(1+x/xhalf), log=TRUE))
     fit.mle <- function(FUN, x, y)
                   mle(proto(FUN = match.fun(FUN))[["FUN"]], method="L-BFGS-B", lower=c(0, 0))
     fit.mle("ll", x=0:10, y=c(26, 17, 13, 12, 20, 5, 9, 8, 5, 4, 8))
```

3. Manipulating formula environments: This can be tricky in `R` and `proto` can help sort it out. In this example, `update` must be able to find `v`; however, by default `update` looks only in the environment of formula `f` so a `v` created in the `nonadd` function would not be found. To address this we add a `data` argument to `update` which specifies a `proto` object containing `v`. The parent of the `proto` object is defined to be the environment of `f`. That way `v` is found in the `proto` object itself and the other components of the formula are found in the `proto` object's parent.

```
     library(proto)
     nonadd <- function(formula) {
       f <- lm(formula)
       g <- update(f, . ~ . + v, 
              data = proto(environment(formula), v = f$fitted.values^2))
       anova(f, g)
     }
     set.seed(1)
     x <- rnorm(20)
     y <- rnorm(20)
     nonadd(y ~ x)
```

4. Delegation/inheritance: In this example we define a parent object, `timera`, with two components: a method, `run` which runs a timing operation, and a variable, `x`, which is used in the timing. We execute the method and then create a child object, `timerb`, overriding the variable `x` and inheriting the method `run`. We execute the `run` method which is inherited and acts on the child `x`.

```
     library(proto)
     # time the table function
     timera <- proto(run = function(.) system.time(table(.$x)),
	         x = sample(letters, 10000, rep = TRUE))
     timera$run()# time it using different data
     timerb <- timera$proto(x = rep(letters, length = 5000))
     timerb$run()
```

5. gWidgets: The [gWidgets](http://wiener.math.csi.cuny.edu/pmg/gWidgets) R package for user interfaces can be used in conjunction with `proto` as seen from the examples [here](http://wiener.math.csi.cuny.edu/pmg/gWidgets/Examples/ProtoExample-ex.html) and [here](http://wiener.math.csi.cuny.edu/pmg/gWidgets/Examples/ScopingIssues-ex.html). Also see [this r-devel post](https://stat.ethz.ch/pipermail/r-devel/2007-September/046888.html).


## Team ##

We wish you a lot of fun with the exciting world of proto objects.

  * Gabor Grothendieck (maintainer)

  * Louis Kates

  * Thomas Petzoldt








