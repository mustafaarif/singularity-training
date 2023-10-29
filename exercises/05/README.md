# Singularity Definition Files

### Task 01

Write a Container deinition file which builds an Ubuntu 22.04 Container from Docker Hub.

```bash
singularity build ubuntu2204.sif ubuntu2204.def

```
### Task 02

Write a Container definition file 'ubuntu-with-r.def' to install 'R' inside the container.

```bash
singularity build ubuntu-with-r.sif ubuntu-with-r.def
```

### Task 03

Copy the generated Container to Codon SLURM Cluster

If you are using Cloud VM, Login to Codon SLURM Cluster and issue following

```bash
cd ~/singularity23/exercies/05/
scp ebi@<ipaddr>:/home/ebi/singularity23/exercies/05/ubuntu-with-r.sif .
```


If you are using Local VM and currently not connected to EBI network make sure to establish a VPN Connection via Pulse Secure. Then from your local VM, issue following

```bash
scp ubuntu-with-r.sif <ebiusername>@codon-slurm-login:~/
ssh ebiusername@codon-slurm-login
cd ~/singularity23/exercies/05/
```

### Task 04

Run the container in Codon SLURM Cluster

```bash
singularity shell ubuntu-with-r.sif
R --version
```

### Task 05

Submit a SLURM job to run sample.Rscript with R present inside the container 'ubuntu-with-r.sif' and examine the output file

```bash
sbatch slurm.job
```
