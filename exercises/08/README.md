# Singularity Containers with GPU

### Task 01

Download TensorFlow GPU container from Docker Hub and run MNiST code on Codon SLURM Cluster

**Step 01** Request for an allocation on on Codon Cluster to download a container. 

```bash
ssh user@codon-slurm-login.ebi.ac.uk

salloc -t 00:30:00 --ntasks=4 --mem=32GB --reservation=singularity23 --account=singularity-cpu

cd ~/singularity23/exercises/08/
singularity pull tensorflow-gpu.sif docker://tensorflow:tensorflow-gpu
exit
```

**Step 02** Submit a GPU job to run MNist Code using TensorFlow GPU Container. 

```bash
sbatch slurm-gpu.job
```
