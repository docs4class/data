--- 
title: "A Minimal Book Example"
author: "John Doe"
date: "2023-01-06"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
# url: your book url like https://bookdown.org/yihui/bookdown
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is a minimal example of using the bookdown package to write a book.
  The HTML output format for this example is bookdown::bs4_book,
  set in the _output.yml file.
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# 12 Groups 


```r
library(datasauRus)
head(datasauRus::datasaurus_dozen, n= 50)
#>    dataset       x       y
#> 1     dino 55.3846 97.1795
#> 2     dino 51.5385 96.0256
#> 3     dino 46.1538 94.4872
#> 4     dino 42.8205 91.4103
#> 5     dino 40.7692 88.3333
#> 6     dino 38.7179 84.8718
#> 7     dino 35.6410 79.8718
#> 8     dino 33.0769 77.5641
#> 9     dino 28.9744 74.4872
#> 10    dino 26.1538 71.4103
#> 11    dino 23.0769 66.4103
#> 12    dino 22.3077 61.7949
#> 13    dino 22.3077 57.1795
#> 14    dino 23.3333 52.9487
#> 15    dino 25.8974 51.0256
#> 16    dino 29.4872 51.0256
#> 17    dino 32.8205 51.0256
#> 18    dino 35.3846 51.4103
#> 19    dino 40.2564 51.4103
#> 20    dino 44.1026 52.9487
#> 21    dino 46.6667 54.1026
#> 22    dino 50.0000 55.2564
#> 23    dino 53.0769 55.6410
#> 24    dino 56.6667 56.0256
#> 25    dino 59.2308 57.9487
#> 26    dino 61.2821 62.1795
#> 27    dino 61.5385 66.4103
#> 28    dino 61.7949 69.1026
#> 29    dino 57.4359 55.2564
#> 30    dino 54.8718 49.8718
#> 31    dino 52.5641 46.0256
#> 32    dino 48.2051 38.3333
#> 33    dino 49.4872 42.1795
#> 34    dino 51.0256 44.1026
#> 35    dino 45.3846 36.4103
#> 36    dino 42.8205 32.5641
#> 37    dino 38.7179 31.4103
#> 38    dino 35.1282 30.2564
#> 39    dino 32.5641 32.1795
#> 40    dino 30.0000 36.7949
#> 41    dino 33.5897 41.4103
#> 42    dino 36.6667 45.6410
#> 43    dino 38.2051 49.1026
#> 44    dino 29.7436 36.0256
#> 45    dino 29.7436 32.1795
#> 46    dino 30.0000 29.1026
#> 47    dino 32.0513 26.7949
#> 48    dino 35.8974 25.2564
#> 49    dino 41.0256 25.2564
#> 50    dino 44.1026 25.6410
tail(datasauRus::datasaurus_dozen, n= 50)
#>         dataset        x          y
#> 1797 wide_lines 77.06711 51.4869182
#> 1798 wide_lines 75.01714 46.6224426
#> 1799 wide_lines 76.66531 38.4402510
#> 1800 wide_lines 77.91587 45.9268434
#> 1801 wide_lines 73.74205 39.1209853
#> 1802 wide_lines 75.32982 32.8303519
#> 1803 wide_lines 63.41044 38.3777356
#> 1804 wide_lines 68.85649 43.0841472
#> 1805 wide_lines 66.33779 33.3065100
#> 1806 wide_lines 64.20372 26.6441143
#> 1807 wide_lines 64.49863 22.8635013
#> 1808 wide_lines 68.89099 27.2962057
#> 1809 wide_lines 72.37152 21.9616397
#> 1810 wide_lines 69.76542 19.9998505
#> 1811 wide_lines 68.62131 18.9156764
#> 1812 wide_lines 64.29774 20.4287497
#> 1813 wide_lines 66.69927 18.5910853
#> 1814 wide_lines 67.54453 16.4479381
#> 1815 wide_lines 63.94695 18.6928454
#> 1816 wide_lines 64.38819 15.7728123
#> 1817 wide_lines 65.57005 23.7657582
#> 1818 wide_lines 38.40284 19.0468587
#> 1819 wide_lines 37.83236 14.4694894
#> 1820 wide_lines 36.90416 13.5838158
#> 1821 wide_lines 36.28614 17.1057707
#> 1822 wide_lines 62.78663 13.9189931
#> 1823 wide_lines 66.81768 11.4124972
#> 1824 wide_lines 66.75502 18.0853051
#> 1825 wide_lines 65.41553 10.4635122
#> 1826 wide_lines 36.94633 13.5143775
#> 1827 wide_lines 37.82543  9.6010343
#> 1828 wide_lines 36.72284  9.3333021
#> 1829 wide_lines 67.07332  6.0492146
#> 1830 wide_lines 64.60182 12.0019170
#> 1831 wide_lines 65.43728 15.5453861
#> 1832 wide_lines 67.00402 15.3458266
#> 1833 wide_lines 66.72419  5.2498055
#> 1834 wide_lines 68.30762 13.2809165
#> 1835 wide_lines 68.76805 13.5214566
#> 1836 wide_lines 74.16727  5.3498809
#> 1837 wide_lines 64.90036 16.2452584
#> 1838 wide_lines 68.76343  8.7005729
#> 1839 wide_lines 66.81691 12.2732943
#> 1840 wide_lines 67.30935  0.2170063
#> 1841 wide_lines 34.73183 19.6017951
#> 1842 wide_lines 33.67444 26.0904902
#> 1843 wide_lines 75.62726 37.1287519
#> 1844 wide_lines 40.61013 89.1362399
#> 1845 wide_lines 39.11437 96.4817513
#> 1846 wide_lines 34.58383 89.5889020
```

