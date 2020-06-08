# singularity_scrna_app
A test environment for scrna_seq_apps



## How to build using Singularity: build process command:
### takes 30-60 minutes
sudo singularity build ../scrnaseq_app.simg singularity_app_recipe.txt

###faster updates, config, but sandbox chroot file system only  ?
sudo singularity build --update --sandbox ../scrnaseq_app.simg singularity_app_recipe.txt

Tested:

singularity version
3.5.3

Ubuntu 1604
