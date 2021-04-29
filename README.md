# mispriced-diamonds
mydata <- read.csv(file.choose())

library(ggplot2)

ggplot(mydata[mydata$carat<2.5,], 
       aes(carat, price, color = clarity)) +
  geom_point(alpha = 0.1) +
  geom_smooth()

ggplot(mydata, 
       aes(carat, price, color = clarity)) +
  geom_point(alpha = 0.1) +
  geom_smooth()
