# Inspecting Singularity Containers

### Task 01
Pull a remote container `library://marif/repo/democontainer:latest` and inspect various attributes

```bash
# Pull Container
singularity pull demo.sif library://marif/repo/democontainer:latest

# View Runscript
singularity inspect --runscript demo.sif

# View all properties
singularity inspect --all demo.sif

# View Environment
singularity inspect --environment demo.sif

# View Definition Files
singularity inspect --deffile demo.sif
```

