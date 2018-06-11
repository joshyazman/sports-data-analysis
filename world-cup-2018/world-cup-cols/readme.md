# World Cup Countries
This is a color palette of all countries competing in the 2018 FIFA World Cup. Essentially, this is just a list of vectors containing the colors in each world cup country's flag. The hex codes are sourced from [schemecolor.com](http://www.schemecolor.com/poland-flag-colors.php). The country abbreviations (used to index the list) can be found [here](http://www.nationsonline.org/oneworld/country_code_list.htm).

To load the color palette, use the `load()` and `url()` functions along with the download url from the github file. Or just copy and run the code below:

```
load(url('https://github.com/joshyazman/sports-data-analysis/blob/master/world-cup-2018/world-cup-cols/world_cup_countries.Rdata?raw=true'))
```

Then each country is an index of the `world_cup_cols` object. For example, if you want to use the Panamanian flag colors in a chart, you could do that like so:

```
library(tidyverse)
data('diamonds')
ggplot(diamonds, aes(x = cut, y = mean(price), group = cut))+
  geom_col(fill = world_cup_cols$pan[1])
```
