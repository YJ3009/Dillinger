# SETUP

## To access jupyterlab
- Power shell 
    podman run --rm -d --name sds2025 -p 8888:8888 -v "$(pwd):/home/jovyan/work" jreades/sds:2025-amd start.sh jupyter lab --LabApp.password='' --ServerApp.password='' --NotebookApp.token=''
- Access this website 
    [JupyterLab](http://localhost:8888/)
