setwd(“C:/Users/spatt/OneDrive - McGill
University/patterson\_pouliot/inequality/inequality”)

Library, load corpus
====================

``` r
pacman::p_load(dplyr,tokenizers,readr,tidytext,tidyverse,quanteda,tidyr,stringr,text2vec)

unga_tibble <- tibble(read_csv("unga_2017_corpus_unregional.csv"))
```

    ## Warning: Missing column names filled in: 'X1' [1]

    ## Parsed with column specification:
    ## cols(
    ##   X1 = col_double(),
    ##   doc_id = col_character(),
    ##   text = col_character(),
    ##   docvar1 = col_character(),
    ##   docvar2 = col_double(),
    ##   docvar3 = col_double(),
    ##   P5 = col_double(),
    ##   NWS = col_double(),
    ##   ECOWAS = col_double(),
    ##   EU = col_double(),
    ##   UN_AFRICA = col_double(),
    ##   UN_ASIAPAC = col_double(),
    ##   UN_EASTEUROPE = col_double(),
    ##   UN_GRULAC = col_double(),
    ##   UN_WEOG = col_double(),
    ##   UN_REGION = col_character()
    ## )

Working through this tutorial:
<a href="http://text2vec.org/vectorization.html" class="uri">http://text2vec.org/vectorization.html</a>

Vectorization
=============

GloVe
=====

How the fuck do I visualize this?

Collocations
============

Hello Vincent! This is where you are supposed to look…

``` r
model <- Collocations$new(collocation_count_min = 25)
txt <- unga_tibble$text
it <- itoken(txt)
model$fit(it,n_iter = 8)
```

    ## INFO  [12:03:04.256] iteration 1 - found 17880 collocations 
    ## INFO  [12:03:23.837] iteration 2 - found 24091 collocations 
    ## INFO  [12:03:43.986] iteration 3 - found 25213 collocations 
    ## INFO  [12:04:04.450] iteration 4 - found 25340 collocations 
    ## INFO  [12:04:24.884] iteration 5 - found 25349 collocations 
    ## INFO  [12:04:45.286] iteration 6 - converged

``` r
model$collocation_stat
```

    ##                               prefix     suffix   n_i   n_j n_ij       pmi
    ##     1:                         Jigme     Singye    31    27   26 19.200630
    ##     2: Treaty_Banning_Nuclear_Weapon   Tests_in    31    32   31 19.004114
    ##     3:                  Other_Cruel, Inhuman_or    33    27   26 18.942106
    ##     4:                        Dar_es     Salaam    34    27   26 18.899037
    ##     5:                        Cruel,    Inhuman    37    36   32 18.829896
    ##    ---                                                                    
    ## 25345:                     increased assistance  3238  7486   40  5.000335
    ## 25346:                      justice.         In   946 30748   48  5.000335
    ## 25347:                            an   alliance 69076   465   53  5.000211
    ## 25348:                           us, especially  2543  5958   25  5.000202
    ## 25349:                   activities.         It   550 36367   33  5.000038
    ##             lfmd       gensim      llr iter
    ##     1: -19.81704  23173.52808 719.2236    1
    ##     2: -19.09572 101764.89315 871.7727    3
    ##     3: -19.73891  19371.74523 706.4426    2
    ##     4: -19.78198  18801.98802 703.4479    2
    ##     5: -19.58865 101932.20796 861.7282    1
    ##    ---                                     
    ## 25345: -32.77436     12.00279 200.4437    1
    ## 25346: -32.24829     15.33689 242.1306    1
    ## 25347: -31.96250     16.90813 270.6460    1
    ## 25348: -34.13063      0.00000 125.1862    1
    ## 25349: -33.32972      7.75778 166.7298    1

Distance between words
======================
