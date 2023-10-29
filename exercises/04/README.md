# Interacting with Singularity Containers

### Task 01

Start interactive session inside container bowtie2-2.2.8.sif which was already downloaded. Identify bowtie2 version.

```bash
singularity shell bowtie2-2.2.8.sif
singularity> bowtie2 --version
```

### Task 02

Use singularity exec to print Ubuntu release information for ubuntu_1804.sif container which was downloaded earlier.
```bash
singularity <cmd_for_exec> <container_name>.sif cat /etc/lsb-release
```

### Task 03
Download container from Remote repo `library://marif/repo/democontainer:latest` and save container as demo.sif. Use singularity run to execute default runscript in this container.
```bash
singularity pull <container_name>.sif <container_library_and_name>
singularity run demo.sif
```
