# **GISS/R**
---
---
## `CHECK101`
- Check all ==package installed and ticked==? 
   >Install
    
    ```sh
    install.packages(c("sf", "tmap", "tmaptools", "RSQLite", "tidyverse"), 
                 repos = "https://www.stats.bris.ac.uk/R/")`
    ```
    >Tick/Load
    
    ```sh
    library(sf)
    library(tmap)
    library(tmaptools)
    library(RSQLite)
    library(tidyverse)
    ```

- ==No capital== on the function code!
- File path ==delimier==: / (adjust copies from path)
- In doubt, use ==Function enquiry==
    ```sh
   ??summary.function
    ```
### PRACTICE 01 
 - Input data
 - plot
 - pivot
 - join
 - check
 - quick thematic mapping
 
#### Read shapefile
```sh
shape <-st_read("file path")
```
#### Check info
```sh
summary(shape)
plot(shape)
```
#### Plot outline
```sh
shape %>% 
  st_geometry() %>%
  plot()
 ```
#### Read CSV
```sh
mycsv <-read.csv("file path")
```
#### View CSV
```sh
mycsv 
```
#### [Pivot] [P]
```sh
mycsv2 <- mycsv%>%
  pivot_wider( id_cols = code, names_from = year, values_from = total_action_taken)
```
`id_cols` changed based on this variable, usually the unique code 
`names_from` The column whose values will be used as column names
`values_from` The column whose values will be used as cell values

#### Join data
```sh
shape2 <- shape%>%
  merge(.,
        mycsv2,
        by.x="GSS_CODE", 
        by.y="code")
```
practice use only, it is not recommended to use at data management due to data collapse
#### Check the new file
```sh
shape2%>%
  head(., n=10)
```
#### Mapping
```sh
tmap_mode("plot")
shape2 %>%
  qtm(.,fill = "2011-12")
  ```

















[John gurber]



[//]: # (Links saved here. 
Note: When exported as PDF file, !!!Chinese letters do not show!!!
)

 [John gurber]: <http://daringfireball.net>
 [P]:<https://www.jianshu.com/p/46a53717d964>