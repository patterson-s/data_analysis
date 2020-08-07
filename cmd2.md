\#library

CMD
===

`ungdc_unnest` is a base form that can be used to compute CMD for any
word

Concepts: socioeconomic inequality - from Piketty urgent v. long-term
economy - Doty, Imperial Encounters

CMD Plots: Conceptual engagement in 2 dimensions over time
==========================================================

``` r
# socioeconomic x urgent ----
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.urgent, colour = UN_REGION)) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Urgent by UN_REGION")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-1.png)

``` r
# socioeconomic x long-term ----
## Africa
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(UN_AFRICA))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by UN_AFRICA")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-2.png)

``` r
## NAM
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = `cmd.long-term economy`, colour = as.factor(nam))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Long-term Economy by NAM")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-3.png)

``` r
# socioeconomic x poverty ----
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.poverty, colour = as.factor(UN_WEOG))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Poverty by UN_WEOG")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-4.png)

``` r
# socioeconomic x exploitation ----
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = as.factor(UN_WEOG))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation by UN_WEOG")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-5.png)

``` r
cmd_frame %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = as.factor(UN_GRULAC))) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation by UN_GRULAC")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-6.png)

``` r
cmd_frame[ which(cmd_frame$UN_REGION == "WEOG" | cmd_frame$UN_REGION == "GRULAC"),] %>%
  ggplot(mapping = aes(x = cmd.socioeconomic, y = cmd.exploitation, colour = UN_REGION)) +
  geom_point() +
  geom_hline(yintercept = 0) +
  geom_vline(xintercept = 0) +
  facet_wrap(vars(interval)) +
  labs(title = "CMD: Socioeconomic v. Exploitation: WEOG v. GRULAC")
```

![](cmd2_files/figure-markdown_github/unnamed-chunk-2-7.png)

CMD Time series
===============

``` r
# Socioeconomic Inequality by UN_REGION ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = UN_REGION)) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-1.png)

``` r
# Socioeconomic Inequality by NAM ----
cmd_frame %>%
  group_by(nam) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(nam))) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by NAM")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-2.png)

``` r
# Socioeconomic Inequality by g77 ----
cmd_frame %>%
  group_by(g77) %>%
  ggplot(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(g77))) +
  geom_smooth() + 
  labs(title = "Engagement w/ Socioeconomic Inequality in UNGA Floor Speeches by g77")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-3.png)

``` r
# Comparison
cmd_frame %>%
  group_by(nam,g77) %>%
  ggplot() +
  geom_smooth(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(g77))) + 
  geom_smooth(mapping = aes(x = year, y = cmd.socioeconomic, colour = as.factor(nam))) +
  labs(title = "Comparison")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'
    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-4.png)

``` r
# Foresight ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.foresight, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Foresight UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-5.png)

``` r
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.foresight, colour = as.factor(nam))) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Foresight by NAM")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-6.png)

``` r
# Hindsight ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.hindsight, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Hindsight UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-7.png)

``` r
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.hindsight, colour = as.factor(nam))) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Hindsight by NAM")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-8.png)

``` r
# Poverty ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.poverty, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Poverty by UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-9.png)

``` r
# Exploitation ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.exploitation, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Exploitation by UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-10.png)

``` r
# Modernity ----
cmd_frame %>%
  group_by(UN_REGION) %>%
  ggplot(mapping = aes(x = year, y = cmd.modernity, colour = UN_REGION)) +
  geom_smooth() + 
  geom_hline(yintercept = 0) +
  labs(title = "Engagement w/ Modernity by UN region")
```

    ## `geom_smooth()` using method = 'gam' and formula 'y ~ s(x, bs = "cs")'

![](cmd2_files/figure-markdown_github/unnamed-chunk-3-11.png)
