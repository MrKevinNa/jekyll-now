Company Review Analysis
================

Data collection
---------------

잡플래닛에서 기업리뷰 데이터를 크롤링한다. 잡플래닛은 기업리뷰를 작성한 회원에게만 다른 회사의 기업리뷰를 조회할 수 있도록 한다. 즉, 로그인을 해야 한다는 것을 의미한다. 로그인을 한 상태로 크롤링하는 방법은 2가지가 있는데 하나는 쿠키를 이용하는 것이고, 다른 하나는 RSelenium을 이용하는 것이다. 우리는 쿠키를 이용하는 방법을 사용할 것이다. 단, 로그인 정보는 공개하지 않을 것이므로 이 포스팅을 따라하려면 본인의 로그인 정보를 활용하기 바란다.

웹 크롤링에 필요한 라이브러리를 먼저 불러오도록 하자!

``` r
# 필요한 라이브러리를 불러옵니다. 
library(httr)
library(rvest)
```

    ## Loading required package: xml2

    ## 
    ## Attaching package: 'rvest'

    ## The following object is masked from 'package:purrr':
    ## 
    ##     pluck

    ## The following object is masked from 'package:readr':
    ## 
    ##     guess_encoding

``` r
library(tidyverse)
```