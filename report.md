HW 1, CS 625, Fall 2021
================
Peter G. Mavronicolas
Sep 9, 2021

## Git, GitHub

1.  *What is your GitHub username?* winstreak1

2.  *What is the URL of your remote GitHub repo (created through
    Mr. Kennedy’s exercises)?*
    <https://git.cs.odu.edu/tkennedy/git-workshop.wiki.git> \#\# R

The command below will load the tidyverse package. If you have installed
R, RStudio, and the tidyverse package, it should display a list of
loaded packages and their versions.

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✓ ggplot2 3.3.5     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.3     ✓ dplyr   1.0.7
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   2.0.1     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

── Attaching packages ────────────────────────────────────── tidyverse
1.3.1 ── ✔ ggplot2 3.3.5 ✔ purrr 0.3.4 ✔ tibble 3.1.3 ✔ dplyr 1.0.7 ✔
tidyr 1.1.3 ✔ stringr 1.4.0 ✔ readr 2.0.1 ✔ forcats 0.5.1 ── Conflicts
───────────────────────────────────────── tidyverse\_conflicts() ── ✖
dplyr::filter() masks stats::filter() ✖ dplyr::lag() masks stats::lag()

## R Markdown

1.  *Create a bulleted list with at least 3 items*

### Grocery List

-   Apples
-   Oranges
-   Milk
-   Lucky Charms
-   Sugar

2.  *Write a single paragraph that demonstrates the use of italics,
    bold, bold italics, code, and includes a link. The paragraph does
    not have to make sense.*

To italicize a word simply add one *asterick* before and after the word.
I’m feeling quite **bold** today. This text is in ***bold italics***
because I used three astericks on either side of the word or expression.
My favorite website is
[D.R.O.N.E.](https://dynamicremotelyoperatednavigationequipment.com/).
To gain administration in terminal, type ‘sudo’ before the command.

3.  *Create a level 3 heading*

<h3>
This is my Heading
</h3>

## R

#### Data Visualization Exercises

1.  (Q2) \*How many rows are in mpg? How many columns?

    dim(mpg)

    234 Rows and 11 columns (Reference 5)

2.  (Q4) *Make a scatterplot of hwy vs cyl.*

    ![image](https://user-images.githubusercontent.com/17502942/131251693-a5b17bf5-0830-46bc-9d3e-111ed880e5fc.png)
    (Ref 6)

#### Workflow: basics Exercises

1.  (Q2) *Tweak each of the following R commands so that they run
    correctly (`library(tidyverse)` is correct):*

``` r
library(tidyverse)
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))

filter(mpg, cyl == 8)

filter(diamonds, carat > 3) (Ref 7)
```

## Google Colab

1.  *What are the URLs of your Google Colab notebooks (both Python and
    R)?*

    Python
    (<https://colab.research.google.com/drive/1AXOWL-KyR8YQ0K-lHqJW5rbJFXXwzsK2?usp=sharing>)
    R
    (<https://colab.research.google.com/drive/1FKMPtP376g0ZtmUrxWcnpVdZ3MRRPacH?usp=sharing>)

## Tableau

*Insert your the image of your final bar chart here*

![SalesintheEast](https://user-images.githubusercontent.com/17502942/131373403-ed569ef4-ad3e-46f6-9d80-987ddb188077.png)

1.  *What conclusions can you draw from the chart?*

    Products that showed the greatest profits were Binders in 2019 and
    Copiers in 2021. Products that showed consistent losses were
    Bookcases and Tables which may be an indicator of consumer
    preference toward digital books and a shift toward working remotely.
    Office supplies also declined in 2021 which may indicate either a
    shift away from pens, pencils and paper products in the new era of a
    remote workforce or just a reflection of budget cuts reacting to a
    COVID-19 economy.

## Observable and Vega-Lite

### A Taste of Observable

1.  *In the “New York City weather forecast” section, try replacing
    `Forecast: detailedForecast` with `Forecast: shortForecast`. Then
    press the blue play button or use Shift-Return to run your change.
    What happens?*

    Under the forecast column, the description is shortened to a bried
    description such as ‘mostly sunny’ or’haze’.

2.  *Under the scatterplot of temperature vs. name, try replacing
    `markCircle()` with `markSquare()`. Then press the blue play button
    or use Shift-Return to run your change. What happens? How about
    `markPoint()`?*

    The points on the scatter plot change from circles to squares. For
    ‘markPoint()’, the point change to open circles.

3.  *Under “Pick a location, see the weather forecast”, pick a location
    on the map. Where was the point you picked near?*

    Port Ricjey, FL (Longitude: -82.86 Latitude: 28.31)

4.  *The last visualization on this page is a “fancy” weather chart
    embedded from another notebook. Click on the 3 dots next to that
    chart and choose ‘Download PNG’. Insert the PNG into your report.*

    ![untitled](https://user-images.githubusercontent.com/17502942/132046097-f6edaabe-f89e-4a53-8fc9-ef74abe3ba11.png)

### Charting with Vega-Lite

`markCircle()`

1.  *Pass an option of `{ size: 200 }` to `markCircle()`.*9

The circles become large and overlap with one another.

3.  *Try `markSquare` instead of `markCircle`.*

The circle points become squares on the scatterplot.

5.  *Try `markPoint({ shape: 'diamond' })`.*

The points become diamonds with open insides.

`vl.x().fieldQ("Horsepower")`, …

This line of code was already included and no changes occur.

1.  *Change `Horsepower` to `Acceleration`*

The ‘X’ axis label changes to Acceleration and the points rotate about
the y -axis.

3.  *Swap what fields are displayed on the x- and y-axis*

`vl.tooltip().fieldN("Name")`

The x and y axis labels change as well as the points.

1.  *Change `Name` to `Origin`.*

    The origin of the vehicles are shown when hovering on a point.

Another example, `count()`

count included on the x axis makes a vertical line of plots.

1.  *Remove the `vl.y().fieldN("Origin")` line.*

    The scatterplot forms a straight line on the vertical axis without
    any variation in Y coordinates.

2.  *Replace `count()` with `average("Miles_per_Gallon")`.*

    The scatterplot forms a straighht, linear line that starts has a
    slope of 1/1.

## References

*Every report must list the references that you consulted while
completing the assignment. If you consulted a webpage, you must include
the URL.*

-   Insert Reference 1, <https://www.markdownguide.org/basic-syntax/>
-   Insert Reference 2,
    <https://wordpress.com/support/markdown-quick-reference/>
-   Insert Reference 3,
    <https://www.researchgate.net/figure/Bulleted-list-in-R-Markdown-input-left-and-output-right_fig1_260126796>
-   Insert Reference 4, <https://www.tidyverse.org/>
-   Insert Reference 5,
    <https://www.google.com/search?q=how+many+rows+are+in+mpg%3F&rlz=1C5CHFA_enUS864US865&oq=how+many+rows+are+in+mpg%3F&aqs=chrome>..69i57j0i512.4668j0j7&sourceid=chrome&ie=UTF-8
-   Insert Reference 6,
    <https://rstudio-pubs-static.s3.amazonaws.com/271994_11b7ddf08518406c942009d2da632982.html>
-   Insert Reference 7,
    <https://bookdown.org/yih_huynh/Guide-to-R-Book/diamonds.html>
-   Insert Reference 8,
    <https://www.earthdatascience.org/courses/earth-analytics/document-your-science/add-images-to-rmarkdown-report/>
    (add images to markdown report)
-   Insert Reference 9, <https://www.youtube.com/watch?v=ZV_Yjcs5WtM>
    (resize markCircle)
