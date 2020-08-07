conceptmover2
================

\#library

# CMD

`ungdc_unnest` is a base form that can be used to compute CMD for any
word

Concepts: socioeconomic inequality - from Piketty urgent v. long-term
economy - Doty, Imperial Encounters

# CMD Plots: Conceptual engagement in 2 dimensions over time.

CMD is a measure for conceptual engagement at the document level.
Positive values indicate document engagement with the specified concept
based on high cosine similarity and word frequency. Values near 0
indicate orthogonality, or no conceptual engagement. Negative values
indicate document engagement with cosign distant words.

``` r
# socioeconomic x urgent ----
## Socioeconomic 
cmd1 <-  cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.urgent, colour = UN_REGION)) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Urgent by UN_REGION")

cmd1
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

``` r
# socioeconomic x long-term ----
## Africa
cmd2 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(UN_AFRICA))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by UN_AFRICA")

cmd2
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-2.png)<!-- -->

``` r
## Latin America
cmd3 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(UN_GRULAC))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by UN_GRULAC")

cmd3
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-3.png)<!-- -->

``` r
## WEOG
cmd4 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(UN_WEOG))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by UN_WEOG")

cmd4
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-4.png)<!-- -->

``` r
## NAM

cmd5 <-  cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(nam))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by NAM")

cmd5
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-5.png)<!-- -->

``` r
# socioeconomic x poverty ----
cmd6 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.poverty, colour = as.factor(UN_WEOG))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Poverty by UN_WEOG")

cmd6
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-6.png)<!-- -->

``` r
# socioeconomic x exploitation ----
cmd7 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = as.factor(UN_WEOG))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation by UN_WEOG")

cmd7
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-7.png)<!-- -->

``` r
# 

cmd8 <- cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = as.factor(UN_GRULAC))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation by UN_GRULAC")

cmd8
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-8.png)<!-- -->

``` r
# 
cmd9 <- cmd_frame[ which(cmd_frame$UN_REGION == "WEOG" | cmd_frame$UN_REGION == "GRULAC"),] %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = UN_REGION)) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation: WEOG v. GRULAC")

cmd9
```

![](cmd2_files/figure-gfm/unnamed-chunk-2-9.png)<!-- -->

# CMD Time series

``` r
# Socioeconomic Inequality by UN_REGION ----
cmd10 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = UN_REGION)) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by UN region")
cmd10
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

``` r
# Socioeconomic Inequality by NAM ----
cmd11 <- cmd_frame %>%
  group_by(nam) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(nam))) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by NAM")
cmd11
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-2.png)<!-- -->

``` r
# Socioeconomic Inequality by g77 ----
cmd12 <-  cmd_frame %>%
  group_by(g77) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(g77))) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by g77")
cmd12
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-3.png)<!-- -->

``` r
# Comparison
cmd13 <- cmd_frame %>%
  group_by(nam,g77) %>%
  ggplot() +
  geom_smooth(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(g77))) + 
  geom_smooth(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(nam))) +
  labs(title = "Comparison")
cmd13
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-4.png)<!-- -->

``` r
# Foresight ----
cmd14 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.foresight, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Foresight UN region")

cmd14
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-5.png)<!-- -->

``` r
# 

cmd15 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.foresight, colour = as.factor(nam))) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Foresight by NAM")
cmd15
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-6.png)<!-- -->

``` r
# Hindsight ----
cmd16 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.hindsight, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Hindsight UN region")
cmd16
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-7.png)<!-- -->

``` r
cmd17 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.hindsight, colour = as.factor(nam))) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Hindsight by NAM")
cmd17
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-8.png)<!-- -->

``` r
# Poverty ----
cmd18 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.poverty, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Poverty by UN region")
 cmd18
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-9.png)<!-- -->

``` r
 # Exploitation ----
cmd19 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.exploitation, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Exploitation by UN region")
cmd19
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-10.png)<!-- -->

``` r
# Modernity ----
cmd20 <- cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.modernity, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Modernity by UN region")

cmd20
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-gfm/unnamed-chunk-3-11.png)<!-- -->
