# ismail-sarigul

write something about your repo. For example, how to use it.

library(tidyverse); library(ggthemes); library(ggjoy)


ism<- mpg %>% select(hwy, cty, cyl, year, class, displ, model)

best_in_class <- ism %>% group_by(year) %>%  top_n(1, class)

library(ggrepel)

ggplot(ism, aes(displ, hwy))+ 
         geom_point(aes(colour=cty))


filter(salary_long, wage < 200)
occupation IS 
filterout Physicians
filter(salary_long, ocuupation == Physicians /
#questian mark is equal to <-
# a name connot start with a  number

filter(salary_long, ocuupation != Physicians /
```{r}
filtered1 <- filter(salaery:_long, !(occupation == "Phsycians"))
filtered <- filter(salary_long, ocuupation != "Phsycians"))
all_equal(filtered, filtered)
````

#regular expression to filter rows select "Dentists"
```{r}
filter(salary_long, str_detesc(occupation, "Dent"))
str_detect(salary_long$ocuupation, "Den")
´´´´

#Remove NA-s Filter out NA-s in hair_colour column
´´´´{r}
starwars
filter(starwars, is.na(hair_color))
filter(starwars, !is.na(hair_color))

#Remove all  rows with NA-s in any variable
´´´´{r}
filter(starwars, is.na(hair_color))

##select first four colums
starwars %>% 
select(1:4) %>% 
filter(complete.cases(.))


#summarise() or summurize()
´´´´´{r}
salary_long %>% 
summarise(mean_wage = mean(wage), SD= sd(wage), N= n(), SEM= SD/sqrt(N))
´´´´´´
