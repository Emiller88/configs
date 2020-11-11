# nf-core/configs: UTD Europa Configuration

All nf-core pipelines have been successfully configured for use on the Europa HTC cluster at the [The Univeristy of Texas at Dallas](https://www.utdallas.edu/).

To use, run the pipeline with `-profile utd_europa`. This will download and launch the [`utd_europa.config`](../conf/utd_europa.config) which has been pre-configured with a setup suitable for the Europa HTC cluster. Using this profile, a docker image containing all of the required software will be downloaded, and converted to a Singularity image before execution of the pipeline.

Before running the pipeline you will need to load Singularity using the environment module system on Europa. You can do this by issuing the commands below:

```bash
## Singularity environment modules
module purge
module load singularity
```

All of the intermediate files required to run the pipeline will be stored in the `work/` directory. It is recommended to delete this directory after the pipeline has finished successfully because it can get quite large, and all of the main output files will be saved in the `results/` directory anyway.

> NB: You will need an account to use the HTC cluster on Europa in order to run the pipeline. If in doubt contact OIT.
> NB: Nextflow will need to submit the jobs via SLURM to the HTC cluster and as such the commands above will have to be executed on one of the login nodes. If in doubt contact OIT.
