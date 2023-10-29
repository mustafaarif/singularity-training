# Bind Mounts and Encrypted Containers

### Task 01

Create a local directory 'mysoftware 'on your host machine.

Bind mount this directory in an Ubuntu 20.04 container at /hostsoftware path.

```bash
cd $HOME/singularity23/exercises/09
mkdir ./mysoftware
singularity pull ubuntu2004.sif docker://ubuntu:20.04
singularity shell --bind ./mysoftware:/hostsoftware ubuntu2004.sif
ls /hostsoftware
```

### Task 02

Create an Encrypted Ubuntu 22.04 Container and Run it after decryption

```bash
cd $HOME/singularity23/exercises/09
singularity build --passphrase myencryptedcotnainer.sif encrypted-container.def
```

Run the encrypted container
```bash
singularity shell --passphrase myencryptedcotnainer.sif
```

View your secure code inside the container
```bash
Singularity> cat /opt/mysecureapp
```

