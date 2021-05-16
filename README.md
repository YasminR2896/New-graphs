---
title: "New graph"
author: "Yasmin Roustaei"
date: "16 May 2021"
output: html_document
---
library(readxl)
Lizard_data <- read_excel("~/Lizard data.xlsx")
View(Lizard_data)
plot(Lizard_data$Elevation,Lizard_data$AR,col='blue')
plot(Lizard_data$Elevation,Lizard_data$AR, xlab='Elevation',ylab='AR',main='relationship between elevation and AR',col='blue')
abline(lm(Lizard_data$Elevation,Lizard_data$AR))
abline(Lizard_data$Elevation,Lizard_data$AR)
mymodel<-lm(Lizard_data$Elevation,Lizard_data$AR)
mymodel<-lm(Ho~Hs,data=Lizard_data)
summary(mymodel)
abline(mymodel)
plot(Lizard_data$Elevation,Lizard_data$Ho, xlab='Elevation',ylab='Ho',main='relationship between elevation and Ho',col='blue')
abline(Lizard_data$Elevation,Lizard_data$Ho)
