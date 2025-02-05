PNT-CAT (beta)
================

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->
<!-- badges: end -->

Beta-version of computer adaptive philadelphia naming test

To run, make sure these packages are installed on your local machine:

``` r
# not run
install.packages(c("here", "shiny", "tibble", "dplyr", "tidyr", "ggplot2",
                   "shinyWidgets", "htmltools", "keys", "DT", "shinyjs", "catR",
                   "bslib", "bayestestR"))
```

Then run the following:

``` r
# not run
shiny::runGitHub("rbcavanaugh/pnt")
```

Or clone the repository and run locally.

Update 5-24: Now preliminary version is on shinyapps.io:
<https://rb-cavanaugh.shinyapps.io/pnt-cat/>

## To do list

**ARE THERE ANY COPYRIGHT CONCERNS WE NEED TO ADDRESS?**

### Validation

-   ~~Check if app is choosing the same items as catpuccino~~
-   ~~validate final results in app use (bonus if automated)~~
    -   QUESTION: How does catpuccino handle ties? Testing is showing
        occasional inconsistencies in which items are being chosen, but
        its only in cases where difficulty is the same (e.g. kite:
        -0.475 and bridge: -0.475). Shouldn’t affect final ability
        estimate right?
-   ~~ensure no bias in slight differences between catR and catpuccino~~
-   ~~Redo validation script to adjust for practice slides~~ Looks good!

### For short-term use

-   ~~Add slides with practice trials~~
    -   ~~NOTE: Responses not currently logged. ok?~~
-   Add instructions, background info, and other important info ALEX
    -   just refer to MRRI vs. including info…?
-   ~~produce a results plot, norms, and any other information to
    interpret the results~~
    -   ~~QUESTION: plot distribution sd = 1.48? Also, harder to
        get &gt;3 or &lt;3 in ability… OK~~
-   ~~click sound~~
-   ~~Make it pretty~~
-   ~~indicator that response has been logged~~
-   ~~Add full PNT~~
    -   ~~QUESTION: Add option to randomize full PNT? Done~~
-   ~~Add source code~~
-   ~~Add ability estimate to full 175 PNT (random and not-random)~~
-   Incorporate PNT stop rule? (transform SEM to information?) ALEX
-   Plot: what is the bell curve? ALEX

### Small stuff & Bugs:

-   Clearer instructions for progressing through slides
-   ~~More informative error messages on non-assessment slides~~
-   ~~Spacing throughout app. make sure ipad friendly.~~ Tentatively,
    this looks better…
-   ~~Sound not working on shinyapps.io~~
-   ~~UI resizing after opening modal.~~

### Current agenda items:

-   create ability to upload previous file to prevent reuse of
    previously tested words.
    -   ~~able to upload and don’t repeat~~
    -   ~~compare performacne between administrations (hidden results
        tab only visible if fileupload exists?)~~
    -   use prior from previous adminstration?
    -   ~~download data with all previous administrations for n = 2+i’th
        upload.~~
    -   ~~added option to mute sound~~
    -   ~~removed progress bar to avoid shinyWidgets dependency~~

### Longer-term:

-   Convert to a progressive web app - very easy. see {shiny.pwa}
-   randomly select one of 2-3 best next options
-   PNT 60 item with harder items after n = 30
-   Convert to an R package. I started this, but its tricky and things
    go wrong so I reverted back. right now, there’s an r-package branch
    to be worked on…
-   make a “report” that is downloadable
    -   I think this would just be a formulaic summary paragraph at the
        top, a small table with the main results
    -   and either use DT or another method of storing the output CSV in
        the report
