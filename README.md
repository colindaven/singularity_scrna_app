# singularity_scrna_app
A test environment for scrna_seq_apps



## How to build using Singularity: build process command:
```
### takes ~10 minutes (uses up to 24 cores on a multicore machine!)
sudo singularity build ../scrnaseq_app.simg singularity_app_recipe.txt
```

## Run app - exits without msg
```
singularity run ../scrnaseq_app.simg

singularity exec ../scrnaseq_app.simg ls  /data/scrnaseq/

singularity shell ../scrnaseq_app.simg 
```

### Actual app to run:
```
wget https://raw.githubusercontent.com/mariusrueve/scrnaseq/marius_changes/scrnaseq_app.R
```

### Test app in container. Currently missing pbmc_2020-06-08.rds', probable reason 'No such file or directory'
```
singularity exec ../scrnaseq_app.simg     R -e "options('shiny.port'=3838,shiny.host='0.0.0.0'); shiny::runApp('/data/scrnaseq/scrnaseq_app.R')"
```


```
Tested/built on:

singularity version
-3.5.3
-Ubuntu 1604
```

### Helpful links - singularity setup and SLURM

https://njstem.wordpress.com/2018/08/02/r-script-seurat-with-a-singularity-container-using-slurm/


### Dependencies : downloaded in script
```
git clone (marius dev repo)
wget https://owncloud.gwdg.de/index.php/s/rRawkhIOVe1T5qi/download
```
