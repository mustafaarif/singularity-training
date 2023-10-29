# Building Writable Containers

Your GTL has given you a legacy source code which needs to be run on Codon Cluster, but the HPC admin has informed you that the required dependencies can not be met on HPC system due to various technical reasons. Since you attended Introduction to Linux container course, you can easily solve this problem by installing all the requirements in a container and then port container to HPC system.


**Note:** HPC Admin can help you port the container on HPC system, but he wants you to share container definition file, so he is aware of how the container was built.

### Application Requirements
- Base OS: Ubuntu 20.04
- Packages: python3, fastaq, fastqc, seqtk, bowtie, bowtie-examples, bowtie2, bowtie2-examples

### Build File requirements
- Default runscript in the build file should run bowtie2 application
- Default runscript should also print a message "This container was built during EBI Singularity Training"

### Deliverables
- Container Definition File
