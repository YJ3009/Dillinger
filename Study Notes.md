# SETUP

## To access jupyterlab
- Power shell 
    podman run --rm -d --name sds2025 -p 8888:8888 -v "$(pwd):/home/jovyan/work" jreades/sds:2025-amd start.sh jupyter lab --LabApp.password='' --ServerApp.password='' --NotebookApp.token=''
- Access this website 
    [JupyterLab](http://localhost:8888/)

# R
## 显示没有"st_read"这个函数
- 运行 sf::sf_extSoftVersion()
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
