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
  print (n = 20)
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
    ## # ... with 7,487 more rows, and 3 more variables: defensive_13 <int>,
    ## #   text_12 <chr>, defensive_12 <int>

``` r
token_remove %>%
  arrange(.,desc(defensive_14)) %>%
  print (n = 20)
```

    ## # A tibble: 7,507 x 11
    ##    doc_id index text_base text_15 defensive_15 text_14 defensive_14 text_13
    ##    <chr>  <dbl> <chr>     <chr>          <int> <chr>          <int> <chr>  
    ##  1 ARG_2~   198 presiden~ presid~            0 presid~          107 presid~
    ##  2 AUT_2~   345 112 pres~ 112 pr~            0 112 pr~          107 112 pr~
    ##  3 BLR_2~   787 114 cont~ 114 co~            0 114 co~          107 114 co~
    ##  4 CAN_2~  1156 48 offer~ 48 off~            0 48 off~          107 48 off~
    ##  5 CUB_3~  1666 233 pres~ 233 pr~            0 233 pr~          107 233 pr~
    ##  6 DZA_4~  2000 pleasure~ pleasu~            0 pleasu~          107 pleasu~
    ##  7 IRL_2~  3155 116 sir ~ 116 si~            0 116 si~          107 116 si~
    ##  8 LKA_2~  4049 happy op~ happy ~            0 happy ~          107 happy ~
    ##  9 MNG_2~  4635 36 presi~ 36 pre~            0 36 pre~          107 36 pre~
    ## 10 NOR_2~  5096 113 pres~ 113 pr~            0 113 pr~          107 113 pr~
    ## 11 NPL_2~  5140 68 presi~ 68 pre~            0 68 pre~          107 68 pre~
    ## 12 RWA_2~  5842 presiden~ presid~            0 presid~          107 presid~
    ## 13 AFG_2~     1 82 presi~ 82 pre~            0 82 pre~            0 82 pre~
    ## 14 AFG_2~     2 presiden~ presid~            0 presid~            0 presid~
    ## 15 AFG_2~     3 1 pleasu~ 1 plea~            0 1 plea~            0 1 plea~
    ## 16 AFG_2~     4 presiden~ presid~            0 presid~            0 presid~
    ## 17 AFG_3~     5 114 pres~ 114 pr~            0 114 pr~            0 114 pr~
    ## 18 AFG_3~     6 pleasure~ pleasu~            0 pleasu~            0 pleasu~
    ## 19 AFG_3~     7 212 beha~ 212 be~            0 212 be~            0 212 be~
    ## 20 AFG_3~     8 1 act ad~ 1 act ~            0 1 act ~            0 1 act ~
    ## # ... with 7,487 more rows, and 3 more variables: defensive_13 <int>,
    ## #   text_12 <chr>, defensive_12 <int>

``` r
token_remove %>%
  arrange(.,desc(defensive_13)) %>%
  print (n = 20)
```

    ## # A tibble: 7,507 x 11
    ##    doc_id index text_base text_15 defensive_15 text_14 defensive_14 text_13
    ##    <chr>  <dbl> <chr>     <chr>          <int> <chr>          <int> <chr>  
    ##  1 BHS_4~   739 twenty a~ twenty~            0 twenty~            0 twenty~
    ##  2 DNK_4~  1912 begin co~ begin ~            0 begin ~            0 begin ~
    ##  3 IRN_5~  3225 outset c~ outset~            0 outset~            0 outset~
    ##  4 SLE_4~  6111 pleasure~ pleasu~            0 pleasu~            0 pleasu~
    ##  5 YUG_6~  7402 honour a~ honour~            0 honour~            0 honour~
    ##  6 COG_4~  1442 drawing ~ drawin~            0 drawin~            0 drawin~
    ##  7 GUY_4~  2880 meeting ~ meetin~            0 meetin~            0 meetin~
    ##  8 OMN_4~  5264 outset o~ outset~            0 outset~            0 outset~
    ##  9 RWA_4~  5859 behalf r~ behalf~            0 behalf~            0 behalf~
    ## 10 VEN_4~  7178 presiden~ presid~            0 presid~            0 presid~
    ## 11 FJI_6~  2335 fiji ext~ fiji e~            0 fiji e~            0 fiji e~
    ## 12 MCO_5~  4281 congratu~ congra~            0 congra~            0 congra~
    ## 13 PRY_5~  5671 begin pe~ begin ~            0 begin ~            0 begin ~
    ## 14 SMR_5~  6191 outset e~ outset~            0 outset~            0 outset~
    ## 15 AFG_2~     1 82 presi~ 82 pre~            0 82 pre~            0 82 pre~
    ## 16 AFG_2~     2 presiden~ presid~            0 presid~            0 presid~
    ## 17 AFG_2~     3 1 pleasu~ 1 plea~            0 1 plea~            0 1 plea~
    ## 18 AFG_2~     4 presiden~ presid~            0 presid~            0 presid~
    ## 19 AFG_3~     5 114 pres~ 114 pr~            0 114 pr~            0 114 pr~
    ## 20 AFG_3~     6 pleasure~ pleasu~            0 pleasu~            0 pleasu~
    ## # ... with 7,487 more rows, and 3 more variables: defensive_13 <int>,
    ## #   text_12 <chr>, defensive_12 <int>

``` r
token_remove %>%
  arrange(.,desc(defensive_12)) %>%
  print (n = 20)
```

    ## # A tibble: 7,507 x 11
    ##    doc_id index text_base text_15 defensive_15 text_14 defensive_14 text_13
    ##    <chr>  <dbl> <chr>     <chr>          <int> <chr>          <int> <chr>  
    ##  1 GTM_5~  2844 congratu~ congra~            0 congra~            0 congra~
    ##  2 ESP_5~  2162 outset c~ outset~            0 outset~            0 outset~
    ##  3 ESP_5~  2164 outset i~ outset~            0 outset~            0 outset~
    ##  4 GTM_5~  2843 pleasant~ pleasa~            0 pleasa~            0 pleasa~
    ##  5 GTM_6~  2856 honour r~ honour~            0 honour~            0 honour~
    ##  6 BTN_2~  1032 behalf m~ behalf~            0 behalf~            0 behalf~
    ##  7 GRD_3~  2783 ctoday h~ ctoday~            0 ctoday~            0 ctoday~
    ##  8 IRQ_2~  3247 52 presi~ 52 pre~            0 52 pre~            0 52 pre~
    ##  9 ISL_2~  3293 80 presi~ 80 pre~            0 80 pre~            0 80 pre~
    ## 10 KEN_3~  3596 presiden~ presid~            0 presid~            0 presid~
    ## 11 KWT_2~  3773 presiden~ presid~            0 presid~            0 presid~
    ## 12 KWT_3~  3774 129 plea~ 129 pl~            0 129 pl~            0 129 pl~
    ## 13 LKA_2~  4049 happy op~ happy ~            0 happy ~          107 happy ~
    ## 14 MAR_3~  4238 presiden~ presid~            0 presid~            0 presid~
    ## 15 MLT_2~  4540 presiden~ presid~            0 presid~            0 presid~
    ## 16 MYS_2~  4846 1 presid~ 1 pres~            0 1 pres~            0 1 pres~
    ## 17 SEN_2~  5968 149 dele~ 149 de~            0 149 de~            0 149 de~
    ## 18 SLV_2~  6134 83 presi~ 83 pre~            0 83 pre~            0 83 pre~
    ## 19 SUR_3~  6279 task pre~ task p~            0 task p~            0 task p~
    ## 20 TTO_3~  6724 142 plea~ 142 pl~            0 142 pl~            0 142 pl~
    ## # ... with 7,487 more rows, and 3 more variables: defensive_13 <int>,
    ## #   text_12 <chr>, defensive_12 <int>
