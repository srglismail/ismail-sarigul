# ismail-sarigul

write something about your repo. For example, how to use it.

library(tidyverse); library(ggthemes); library(ggjoy)


ism<- mpg %>% select(hwy, cty, cyl, year, class, displ, model)

best_in_class <- ism %>% group_by(year) %>%  top_n(1, class)

library(ggrepel)

ggplot(ism, aes(displ, hwy))+ 
         geom_point(aes(colour=cty))
