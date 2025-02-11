# Instructions for running on Alma

To run the docker image on Alma

If this was the docker command:
```
docker run --rm -it -v ./login/temp:/home \
icrsc/icr-cca \
crisprCountsAnalysis COUNTS=noClone.txt REPMAP=noClone.repmap OUT=noClone
```
This would be the sngularity command on alma if the data was stored in (relatively to where you are): ./tst
`/`:
```
singularity run -B ./tst:/home \
/data/rds/DIT/SCICOM/SCRSE/shared/singularity/icr-cca_latest.sif \
crisprCountsAnalysis COUNTS=noClone.txt REPMAP=noClone.repmap OUT=noClone

```



# Dev download the image to rds
cd /data/scratch/DCO/DIGOPS/SCIENCOM/ralcraft/support/2025_02_11_cca

export SINGULARITY_CACHEDIR=/data/rds/DIT/SCICOM/SCRSE/shared/singularity
cd /data/rds/DIT/SCICOM/SCRSE/shared/singularity/

singularity pull docker://tohsumirepare/cca
singularity pull docker://icrsc/icr-cca