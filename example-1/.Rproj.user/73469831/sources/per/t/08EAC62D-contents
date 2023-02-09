rm(list=ls())
if(require(easypackages))install.packages("easypackages")
easypackages::packages("stargazer","tidyverse")

# plot mpg vs horsepower

mtcars %>% 
  as_tibble() %>% 
  ggplot(aes(x=hp,y=mpg,color=factor(cyl)))+
  geom_point()+
  theme_light()+
  scale_color_viridis_d(end=0.9)+
  labs(x="Horsepower",y="Miles per gallon", color="Cylinders")+
  theme(legend.position="bottom")
ggsave("Figures/mpg_hp.png",device="png")

# regress mpg on horsepower and cylinders and save a regression table

mtcars %>% 
  lm(mpg~hp+cyl,data=.) %>% 
  stargazer(header=F,out = "Tables/reg1.tex")
