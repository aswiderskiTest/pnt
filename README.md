
<!-- README.md is generated from README.Rmd. Please edit that file -->

# pnt

<!-- badges: start -->
<!-- badges: end -->

Barebones structure for implementing a CAT naming test using shiny.

The app has now been converted to a package! (barely)

Now you can use it without worrying about package dependencies as the
app gets a little more complex

Install the package from github:

``` r
install.packages('devtools')
devtools::install_github("rbcavanaugh/pnt")
```

Then run as such:

``` r
library(pnt)
shinyPNT()
```

You can still clone the repository and run it locally. After cloning the
repository, open the Rproj file. Then run:

``` r
devtools::load_all()
shinyPNT()
```

## To do list

### Validation

-   Check if app is choosing the same items as catpuccino
-   ~~validate final results in app use (bonus if automated)~~
    -   QUESTION: How does catpuccino handle ties? Testing is showing
        occasional inconsistencies in which items are being chosen, but
        its only in cases where difficulty is the same (e.g. kite:
        -0.475 and bridge: -0.475). Shouldn’t affect final ability
        estimate right?
-   ~~ensure no bias in slight differences between catR and catpuccino~~

### For short-term use

-   ~~Add slides with practice trials~~
    -   NOTE: Responses not currently logged. ok?
-   Add instructions, background info, and other important info
-   Make it pretty
-   produce a results plot, norms, and any other information
-   make a “report” that is downloadable
-   ~~indicator that response has been logged~~

### Longer-term

-   randomly select one of 2-3 best next options
-   create ability to upload previous file to prevent reuse of
    previously tested words
