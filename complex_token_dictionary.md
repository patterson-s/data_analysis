Library
=======

Load Data
=========

``` r
pacman::p_load(dplyr,tokenizers,readr,tidytext,tidyverse,quanteda,tidyr,stringr)

load("C:/Users/spatt/OneDrive - McGill University/patterson_pouliot/inequality/inequality/complex_tokenization_2.RDATA")
```

Complex Tokens
==============

``` r
pre_dtm %>% print(n = 1e2)
```

    ## # A tibble: 56 x 6
    ##    doc_id      index token                                  nlevel count code   
    ##    <chr>       <dbl> <chr>                                   <dbl> <dbl> <chr>  
    ##  1 BHS_67_201~   758 conference review progress implementa~     15     1 UN_Art~
    ##  2 GIN_61_200~  2608 conference review progress implementa~     15     1 UN_Art~
    ##  3 JAM_61_200~  3465 conference review progress implementa~     15     1 UN_Art~
    ##  4 LAO_61_200~  3849 conference review progress implementa~     15     1 UN_Art~
    ##  5 LSO_61_200~  4125 conference review progress implementa~     15     1 UN_Art~
    ##  6 NGA_67_201~  5002 conference review progress implementa~     15     1 UN_Art~
    ##  7 TGO_61_200~  6595 conference review progress implementa~     15     1 UN_Art~
    ##  8 ARG_27_197~   198 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ##  9 AUT_26_197~   345 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 10 BLR_26_197~   787 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 11 CAN_26_197~  1156 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 12 CUB_32_197~  1666 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 13 DZA_46_199~  2000 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 14 IRL_26_197~  3155 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 15 LKA_26_197~  4049 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 16 MNG_26_197~  4635 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 17 NOR_25_197~  5096 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 18 NPL_26_197~  5140 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 19 RWA_27_197~  5842 treaty prohibition emplacement nuclea~     14     1 UN_Art~
    ## 20 BHS_48_199~   739 international tribunal prosecution pe~     13     1 UN_Art~
    ## 21 DNK_48_199~  1912 international tribunal prosecution pe~     13     1 UN_Art~
    ## 22 IRN_50_199~  3225 international tribunal prosecution pe~     13     1 UN_Art~
    ## 23 SLE_49_199~  6111 international tribunal prosecution pe~     13     1 UN_Art~
    ## 24 YUG_68_201~  7402 international tribunal prosecution pe~     13     1 UN_Art~
    ## 25 COG_44_198~  1442 special session assembly devoted inte~     13     1 UN_Art~
    ## 26 GUY_44_198~  2880 special session assembly devoted inte~     13     1 UN_Art~
    ## 27 OMN_44_198~  5264 special session assembly devoted inte~     13     1 UN_Art~
    ## 28 RWA_44_198~  5859 special session assembly devoted inte~     13     1 UN_Art~
    ## 29 VEN_44_198~  7178 special session assembly devoted inte~     13     1 UN_Art~
    ## 30 FJI_60_200~  2335 convention rights child involvement c~     13     1 UN_Art~
    ## 31 MCO_55_200~  4281 convention rights child involvement c~     13     1 UN_Art~
    ## 32 PRY_55_200~  5671 convention rights child involvement c~     13     1 UN_Art~
    ## 33 SMR_59_200~  6191 convention rights child involvement c~     13     1 UN_Art~
    ## 34 BTN_27_197~  1032 declaration principles governing sea ~     12     1 UN_Art~
    ## 35 GRD_34_197~  2783 declaration principles governing sea ~     12     1 UN_Art~
    ## 36 IRQ_26_197~  3247 declaration principles governing sea ~     12     1 UN_Art~
    ## 37 ISL_26_197~  3293 declaration principles governing sea ~     12     1 UN_Art~
    ## 38 KEN_31_197~  3596 declaration principles governing sea ~     12     1 UN_Art~
    ## 39 KWT_29_197~  3773 declaration principles governing sea ~     12     1 UN_Art~
    ## 40 KWT_30_197~  3774 declaration principles governing sea ~     12     1 UN_Art~
    ## 41 LKA_26_197~  4049 declaration principles governing sea ~     12     1 UN_Art~
    ## 42 MAR_35_198~  4238 declaration principles governing sea ~     12     1 UN_Art~
    ## 43 MLT_29_197~  4540 declaration principles governing sea ~     12     1 UN_Art~
    ## 44 MYS_26_197~  4846 declaration principles governing sea ~     12     1 UN_Art~
    ## 45 SEN_28_197~  5968 declaration principles governing sea ~     12     1 UN_Art~
    ## 46 SLV_26_197~  6134 declaration principles governing sea ~     12     1 UN_Art~
    ## 47 SUR_35_198~  6279 declaration principles governing sea ~     12     1 UN_Art~
    ## 48 TTO_33_197~  6724 declaration principles governing sea ~     12     1 UN_Art~
    ## 49 URY_33_197~  7008 declaration principles governing sea ~     12     1 UN_Art~
    ## 50 URY_34_197~  7009 declaration principles governing sea ~     12     1 UN_Art~
    ## 51 ESP_50_199~  2162 mission verification human rights com~     12     1 UN_Art~
    ## 52 ESP_52_199~  2164 mission verification human rights com~     12     1 UN_Art~
    ## 53 GTM_50_199~  2843 mission verification human rights com~     12     1 UN_Art~
    ## 54 GTM_51_199~  2844 mission verification human rights com~     12     1 UN_Art~
    ## 55 GTM_51_199~  2844 mission verification human rights com~     12     1 UN_Art~
    ## 56 GTM_63_200~  2856 mission verification human rights com~     12     1 UN_Art~

``` r
token_remove %>%
  arrange(.,desc(defensive_15)) %>%
  print (n = 25)
```

    ## # A tibble: 7,507 x 11
    ##    doc_id index text_base text_15 defensive_15 text_14 defensive_14 text_13
    ##    <chr>  <dbl> <chr>     <chr>          <int> <chr>          <int> <chr>  
    ##  1 BHS_6~   758 printed ~ printe~          124 printe~            0 printe~
    ##  2 GIN_6~  2608 pleasure~ pleasu~          124 pleasu~            0 pleasu~
    ##  3 JAM_6~  3465 honour a~ honour~          124 honour~            0 honour~
    ##  4 LAO_6~  3849 madam co~ madam ~          124 madam ~            0 madam ~
    ##  5 LSO_6~  4125 delegati~ delega~          124 delega~            0 delega~
    ##  6 NGA_6~  5002 start co~ start ~          124 start ~            0 start ~
    ##  7 TGO_6~  6595 behalf d~ behalf~          124 behalf~            0 behalf~
    ##  8 AFG_2~     1 82 presi~ 82 pre~            0 82 pre~            0 82 pre~
    ##  9 AFG_2~     2 presiden~ presid~            0 presid~            0 presid~
    ## 10 AFG_2~     3 1 pleasu~ 1 plea~            0 1 plea~            0 1 plea~
    ## 11 AFG_2~     4 presiden~ presid~            0 presid~            0 presid~
    ## 12 AFG_3~     5 114 pres~ 114 pr~            0 114 pr~            0 114 pr~
    ## 13 AFG_3~     6 pleasure~ pleasu~            0 pleasu~            0 pleasu~
    ## 14 AFG_3~     7 212 beha~ 212 be~            0 212 be~            0 212 be~
    ## 15 AFG_3~     8 1 act ad~ 1 act ~            0 1 act ~            0 1 act ~
    ## 16 AFG_3~     9 traditio~ tradit~            0 tradit~            0 tradit~
    ## 17 AFG_3~    10 presiden~ presid~            0 presid~            0 presid~
    ## 18 AFG_3~    11 behalf d~ behalf~            0 behalf~            0 behalf~
    ## 19 AFG_3~    12 behalf d~ behalf~            0 behalf~            0 behalf~
    ## 20 AFG_3~    13 66 outse~ 66 out~            0 66 out~            0 66 out~
    ## 21 AFG_3~    14 begin st~ begin ~            0 begin ~            0 begin ~
    ## 22 AFG_4~    15 outset c~ outset~            0 outset~            0 outset~
    ## 23 AFG_4~    16 begin st~ begin ~            0 begin ~            0 begin ~
    ## 24 AFG_4~    17 behalf d~ behalf~            0 behalf~            0 behalf~
    ## 25 AFG_4~    18 pleasure~ pleasu~            0 pleasu~            0 pleasu~
    ## # ... with 7,482 more rows, and 3 more variables: defensive_13 <int>,
    ## #   text_12 <chr>, defensive_12 <int>
