codebook
================
Kerrie Stewart

``` r
library(readr)
eclsk <- read_csv("~/eclsk.csv")
```

    ## New names:
    ## Rows: 2435 Columns: 20
    ## ── Column specification
    ## ──────────────────────────────────────────────────────── Delimiter: "," chr
    ## (2): parent.ed.cat, income.cat dbl (18): ...1, schid, parent.ed, female,
    ## income, math, read, gen, minority,...
    ## ℹ Use `spec()` to retrieve the full column specification for this data. ℹ
    ## Specify the column types or set `show_col_types = FALSE` to quiet this message.
    ## • `` -> `...1`

``` r
View(eclsk)
```

## Description

This dataset comprises variables related to gender, academic
achievement, school charactersitics, and family SES.

- Dependent variable: reading score
- Independent variable: parent education
- Control variables: income, female

## Variable Descriptions

- ‘female’: Binary, categorical variable. Is the participant female or
  not? Female = 0, Male = 1

- ‘parent.ed’: What is the highest level of education for the
  participant’s parent? Parental education is an ordinal variable.

- ‘income’: What is the annual income for the participant’s household?

- ‘read’: Participant’s reading score

``` r
summary(eclsk$parent.ed)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   1.000   3.000   5.000   4.925   6.000   9.000

``` r
summary(eclsk$read)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   22.73   39.23   45.33   47.68   52.16  143.02

``` r
summary(eclsk$female)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.0000  0.0000  0.0000  0.4895  1.0000  1.0000

``` r
summary(eclsk$income)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##       0   24000   44000   53201   70000  800000
