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


´´´´´´{r}
n_distinct()


#group_by()

Lets calculate mean salary for each occupation:

´´´´´{r}
salary_long %>% 
group_by(occupation)


´´´´´{r}
salary_long %>% 
group_by(occupation, year)
#just attribute has changed

´´´´´{r}
salary_long_grouped %>% 
summarise(mean_wage = mean(wage), SD= sd(wage), N= n(), SEM= SD/sqrt(N))
´´´´´´



more grouping variables calculate mean "wind" variable for each status and "category"
´´´´´{r}
storms  %>% 
group_by(status, category) %>% 
summarise(mean_wind = mean(wind))



##mutate() adds ne columns and 
Lets calculate  body mass index for starwars characters:
´´´´´{r}
starwars %>%
mutate(bmi= mass/height/100) 2 %>%
select(1:3, bmi) %>%
filter(bmi > 100) 
´´´´´´
arrange(desc(bmi))
top_n(10)
geom_histogram(bins = 30)







