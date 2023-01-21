# Starwars 

::: {.rmdnote}

> **Which homeworlds have the greatest number of individuals with BMI’s greater than the average for each homework?**

:::

## Data

[Starwars Data](https://github.com/tidyverse/dplyr/tree/main/data-raw)

## Starwars

### Missing values by variable


| name| height| mass| homeworld| birth_year| species|
|----:|------:|----:|---------:|----------:|-------:|
|    0|      6|   28|        10|         44|       4|

### BMI summary


```r
starwars %>% select(name, height, mass, homeworld) %>% na.omit() %>% 
  mutate(BMI = mass/(height)^2*10000)
#> # A tibble: 56 × 5
#>    name               height  mass homeworld   BMI
#>    <chr>               <int> <dbl> <chr>     <dbl>
#>  1 Luke Skywalker        172    77 Tatooine   26.0
#>  2 C-3PO                 167    75 Tatooine   26.9
#>  3 R2-D2                  96    32 Naboo      34.7
#>  4 Darth Vader           202   136 Tatooine   33.3
#>  5 Leia Organa           150    49 Alderaan   21.8
#>  6 Owen Lars             178   120 Tatooine   37.9
#>  7 Beru Whitesun lars    165    75 Tatooine   27.5
#>  8 R5-D4                  97    32 Tatooine   34.0
#>  9 Biggs Darklighter     183    84 Tatooine   25.1
#> 10 Obi-Wan Kenobi        182    77 Stewjon    23.2
#> # … with 46 more rows
```



|name           | height| mass|homeworld |      BMI|
|:--------------|------:|----:|:---------|--------:|
|Luke Skywalker |    172|   77|Tatooine  | 26.02758|
|C-3PO          |    167|   75|Tatooine  | 26.89232|
|R2-D2          |     96|   32|Naboo     | 34.72222|
|Darth Vader    |    202|  136|Tatooine  | 33.33007|
|Leia Organa    |    150|   49|Alderaan  | 21.77778|
|Owen Lars      |    178|  120|Tatooine  | 37.87401|

### BMI summary


| mean_bmi| median_bmi|  max_bmi|  min_bmi|
|--------:|----------:|--------:|--------:|
| 32.01696|   24.56749| 443.4286| 12.88625|

### Top contenders...


|homeworld | count|
|:---------|-----:|
|Naboo     |     3|
|Tatooine  |     3|
|Alderaan  |     1|
|Corellia  |     1|
|Kamino    |     1|
|Kashyyyk  |     1|
|Mirial    |     1|

### And the winners are...


|homeworld | count|
|:---------|-----:|
|Naboo     |     3|
|Tatooine  |     3|
