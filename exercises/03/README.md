# Downloading Containers from Remote Repos

**Task 01**

Download ‘bowtie2’ container with tag '2.2.8' from Biocontainers Docker Hub Repo and save as bowtie2-2.2.8.sif

Navigate to [Docker Hub](https://hub.docker.com) and in search bar type "bowtie". Identify the right tag.

```bash
singularity pull bowtie2-2.2.8.sif docker://biocontainers/bowtie2:2.2.8

```

**Task 02**

Download Tensorflow GPU container from Docker Hub and save as tensorflow-gpu.sif

Navigate to [Docker Hub](https://hub.docker.com) and in search bar type "tensorflow". Identify the right tag.

```bash
singularity pull tensorflow-gpu.sif docker://<insert_right_repo_tag>
```

**Task03**

Download 'Ubuntu 18.04' container from Singularity Library and save as ubuntu-1804.sif

Navigate to [Sylabs Cloud](https://cloud.sylabs.io/library/) and in search bar type "Ubuntu". Identify the right tag and the repo. Singularity is developed and mainted by Sylabs. The official repo by Sylabs is named 'library'

```bash
singularity pull <output_container_name>.sif library://<insert_right_repo_tag>
```

**Task 04**

Download Python3 3.8.17 container from Docker Hub and save as python3.8.17.sif

```bash
singularity pull <output_container_name>.sif <remote_repo>://<insert_right_repo_tag>
```
