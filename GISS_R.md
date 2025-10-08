# **GISS/R**
---
---
### `Before delve into practice`
- Check all ==package ticked==?  [//]: # (error load fuction)
- ==No capital== on the function code!
- File path ==delimier==: / (adjust copies from path)

[link](https://www.example.com/my%20great%20page)
[link](https://www.example.com/my great page)

![The San Juan Mountains are beautiful!](https://wallpaperaccess.com/baby-cats "San Juan Mountains")

## 显示没有"st_read"或者某个函数
- install and load package first
```sh
install.packages(c("sf", "tmap", "tmaptools", "RSQLite", "tidyverse"), 
                 repos = "https://www.stats.bris.ac.uk/R/")
```
- 或者运行 sf::sf_extSoftVersion()
- 然后重试


## .shp
#### Load 
```sh
library(sf)
shape <- st_read("C:/Users/he/Documents/CASA/GISS/Week1/homework/statsnz-territorial-authority-2018-generalised-SHP/territorial-authority-2018-generalised.shp")
```
####  Summary(shape)
```sh
Summary(shape)
```
#### Merge
```sh
shape2 <- shape%>%
  merge(.,
        mycsv,
        by.x="GSS_CODE", 
        by.y="Row Labels")
```

#### Draw all the attribute
```sh
plot(shape)
```
####  Draw outline
```sh
library(sf)
shape %>% 
  st_geometry() %>%
  plot()
  ```

#### Read CSV
```sh
library(tidyverse)
mycsv <-  read_csv("C:/Users/he/Documents/CASA/GISS/W1/HM/Statistical Area 1 dataset for Census 2018-total-New Zealand_updated_4-11-21/2018paidemployee.csv")  
```

#### View CSV
```sh
mycsv 
```


# Read shapefile
library(sf)
shape<-st_read("C:/Users/he/Documents/CASA/GISS/W2/HW/Washington_Counties_with_Natural_Shoreline___washsh_area/Washington_Counties_with_Natural_Shoreline___washsh_area.shp")

# ATTENTION: NO CAPITAL!!!! 
summary(shape)

plot(shape)

# Function enquiry
??summary.function

# Outline
library(sf)
shape %>% 
  st_geometry() %>%
  plot()

# Read CSV
library(tidyverse)
#this needs to be your file path again
mycsv <-  read_csv("C:/Users/he/Documents/CASA/GISS/W2/HW/Report_Card_Assessment_Data_2018-19_School_Year_20251007.csv")

[John gurber]



[//]: # (Links saved here. 
Note: When exported as PDF file, !!!Chinese letters do not show!!!
)

 [John gurber]: <http://daringfireball.net>