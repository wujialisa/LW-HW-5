Lisa Wu HW 5
================

    ## # A tibble: 2,018,477 × 21
    ##    application_number filing_date examiner_name_last examiner_name_first
    ##    <chr>              <date>      <chr>              <chr>              
    ##  1 08284457           2000-01-26  HOWARD             JACQUELINE         
    ##  2 08413193           2000-10-11  YILDIRIM           BEKIR              
    ##  3 08531853           2000-05-17  HAMILTON           CYNTHIA            
    ##  4 08637752           2001-07-20  MOSHER             MARY               
    ##  5 08682726           2000-04-10  BARR               MICHAEL            
    ##  6 08687412           2000-04-28  GRAY               LINDA              
    ##  7 08716371           2004-01-26  MCMILLIAN          KARA               
    ##  8 08765941           2000-06-23  FORD               VANESSA            
    ##  9 08776818           2000-02-04  STRZELECKA         TERESA             
    ## 10 08809677           2002-02-20  KIM                SUN                
    ## # ℹ 2,018,467 more rows
    ## # ℹ 17 more variables: examiner_name_middle <chr>, examiner_id <dbl>,
    ## #   examiner_art_unit <dbl>, uspc_class <chr>, uspc_subclass <chr>,
    ## #   patent_number <chr>, patent_issue_date <date>, abandon_date <date>,
    ## #   disposal_type <chr>, appl_status_code <dbl>, appl_status_date <chr>,
    ## #   tc <dbl>, gender <chr>, race <chr>, earliest_date <date>,
    ## #   latest_date <date>, tenure_days <dbl>

    ## `summarise()` has grouped output by 'id', 'art_unit'. You can override using
    ## the `.groups` argument.

    ## Adding missing grouping variables: `art_unit`
    ## `summarise()` has grouped output by 'year', 'tc'. You can override using the
    ## `.groups` argument.
    ## `summarise()` has grouped output by 'tc'. You can override using the `.groups`
    ## argument.

## A. Gender Representation Across TC

#### 1. Histogram for Across TC

    ## Warning in geom_histogram(stat = "identity", position = "stack", color =
    ## "black"): Ignoring unknown parameters: `binwidth`, `bins`, and `pad`

![](Lisa-Wu-HW-5_files/figure-gfm/histogram%20for%20gender%20distribution%20of%20tc%20over%20the%20years-1.png)<!-- -->

#### 2. Pie Chart for TC = 1600 for Analysis Purpose

![](Lisa-Wu-HW-5_files/figure-gfm/pie%20chart%20for%20tc%201600-1.png)<!-- -->

    ## Adding missing grouping variables: `art_unit`
    ## `summarise()` has grouped output by 'year', 'wg'. You can override using the
    ## `.groups` argument.
    ## `summarise()` has grouped output by 'wg'. You can override using the `.groups`
    ## argument.

## B. Gender Representation Across WGs

#### 1. Histogram Across WGs

    ## `summarise()` has grouped output by 'wg'. You can override using the `.groups`
    ## argument.

![](Lisa-Wu-HW-5_files/figure-gfm/histogram%20for%20gender%20distribution%20of%20all%20WGs%20over%20the%20years-1.png)<!-- -->

#### 2. Count Table for WG 1610 for Analysis Purpose

    ## # A tibble: 16 × 3
    ## # Groups:   wg [8]
    ##       wg gender average_count_wg
    ##    <dbl> <chr>             <dbl>
    ##  1  1600 female             3   
    ##  2  1600 male               3.2 
    ##  3  1610 female            62.7 
    ##  4  1610 male              67.7 
    ##  5  1620 female            54.7 
    ##  6  1620 male              71.6 
    ##  7  1630 female            59.6 
    ##  8  1630 male              78.5 
    ##  9  1640 female            64.5 
    ## 10  1640 male              59.1 
    ## 11  1650 female            61.6 
    ## 12  1650 male              60.6 
    ## 13  1660 female             8.94
    ## 14  1660 male               7.65
    ## 15  1670 female            20.3 
    ## 16  1670 male              23.8

#### 3. Pie Chart for wg 1610 for Analysis Purpose

    ## # A tibble: 2 × 4
    ## # Groups:   wg [1]
    ##      wg gender average_count_wg percentage_wg
    ##   <dbl> <chr>             <dbl>         <dbl>
    ## 1  1610 female             62.7          48.1
    ## 2  1610 male               67.7          51.9

![](Lisa-Wu-HW-5_files/figure-gfm/pie%20chart%20for%20gender%20distribution%20of%20workgroup%201610%20over%20the%20years-1.png)<!-- -->

    ## `summarise()` has grouped output by 'year', 'art_unit', 'gender'. You can
    ## override using the `.groups` argument.
    ## `summarise()` has grouped output by 'art_unit', 'gender'. You can override
    ## using the `.groups` argument.

## C. Gender Representation Across Art Units

#### 1. Histogram for All Art Units Under Workgroup 1610 for Analysis Purpose

![](Lisa-Wu-HW-5_files/figure-gfm/histogram%20for%20gender%20distribution%20of%20art%20units%20under%20wg%201610%20over%20the%20years-1.png)<!-- -->

#### 2. Pie Chart for Art Unit 1611 for Analysis Purpose

![](Lisa-Wu-HW-5_files/figure-gfm/pie%20chart%20for%20gender%20distribution%20of%20art%20units%20of%201611%20over%20the%20years-1.png)<!-- -->

## D. Comments on Gender Segregation and representation at TC, WG, and AU level

#### The gender ratio varies across different organizational levels. At the TC 1600 level, there is an almost equal distribution of males and females. When we narrow our focus to Workgroup (WG) 1610, the gender ratio remains close to TC 1600 but with a slightly higher proportion of females.

#### Interestingly, the gender dynamics change significantly within WG 1610 even though in 1610 level, it shows an almost equal distribution. When we examine Art Unit 1611. In AU 1611, there is a substantial majority of females (61%) compared to males (39%). This observation highlights how the gender experience can vary significantly depending on the specific AU, WG, and TC, emphasizing the importance of considering multiple organizational levels when evaluating gender ratios. This insight emphasizes that gender diversity and experiences can be influenced by the specific context and organizational structure within an institution.

## E. The Implication of Any Difference

    ## [1] 119.4287

    ## [1] 88.43166

### I want to see what workgroup 1600 sees as the average size of department verses what an art unit individual sees as the average size of workgroup 1600 using social network concept.

#### I. Process to get what an individual person sees:

##### 1. Get the total employee size in each art unit (female and male)

##### 2. Squared the number of the total employee size for each art unit and see how many views in total we have

##### 3. Sum up all squared number of total employee size and then divided it by the total employee size in the art unit to get what an individual person sees as the average employee size of workgroup 1600

#### - For this, I got the result of 118 as the average size of workgroup 1600 in the art unit level

#### II. Process to get what workgroup 16000 sees rather than in the art unit level

##### 1. Get the total employee size in each art unit (female and male)

##### 2. sum all the numbers for employee size in each art unit and then divided by 8 art units

#### - For this, I got the result of 87 as the average size of workgroup 1600 in the workgroup level

#### III. In conclusion, just like the average of class size example we used in the class. It is interesting to see how an individual at the art unit level will see the size of the workgroup 1600 differently than what a person who is in charge of workgroup 1600 sees. Perceiving the size of a department can significantly differ based on one’s organizational level. Moreover, the disparity becomes even more pronounced when considering the gender distribution across various organizational levels. These variations highlight the importance of perspective.
