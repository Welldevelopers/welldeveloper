# welldeveloper

install.packages("devtools")
install.packages("htmltools")
install.packages("httpuv")
install.packages("mime", dependencies=T)
install.packages("xtable", dependencies=T)
install.packages("magrittr", dependencies=T)
install.packages("crosstalk", dependencies=T)
install.packages("jsonlite", dependencies=T)
install.packages("yaml", dependencies=T)
install.packages("shiny", dependencies=T) # explorar mais
install.packages("Rcpp", dependencies=T)
install.packages("leaflet")
install.packages("dplyr")
install.packages("tidyr")

library(magrittr)
library(leaflet)
library(jsonlite)
library(devtools)
library(dplyr)
library(tidyr)


leaflet() %>% addTiles()

df <- read.csv("datatran2020.csv", sep = ";", dec = ",", encoding = "latin1", na.strings = "",head=T)
df

dfPernambuco <- df %>%
  select(uf,tipo_acidente, latitude, longitude) %>%
  filter(uf == "PE")

dfPernambuco


leaflet(dfPernambuco) %>% addTiles() %>% addMarkers(clusterOptions = markerClusterOptions(),popup=as.character(dfPernambuco$tipo_acidente),label=as.character(dfPernambuco$tipo_acidente))
