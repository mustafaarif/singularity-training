# Installing Singularity on Cloud VM or Local VM

**Note:** This guide assumes that you are running Ubuntu 20+ and Rocky 8+ release.

Once you complete this Lab, please [answer Post Lab Questions](https://forms.gle/VLDfKq3G29trTSEu6)

## For Ubuntu

**Step 01:** Ensure repositories are up-to-date

```bash
# Ensure repositories are up-to-date
sudo apt-get update
```

**Step 02:**  Install debian packages for dependencies

```bash
sudo apt-get install -y \
   autoconf \
   automake \
   cryptsetup \
   git \
   libfuse-dev \
   libglib2.0-dev \
   libseccomp-dev \
   libtool \
   pkg-config \
   runc \
   squashfs-tools \
   squashfs-tools-ng \
   uidmap \
   wget \
   zlib1g-dev
```

## Install Go
```bash
export VERSION=1.21.0 OS=linux ARCH=amd64 && \
  wget https://dl.google.com/go/go$VERSION.$OS-$ARCH.tar.gz && \
  sudo tar -C /usr/local -xzvf go$VERSION.$OS-$ARCH.tar.gz && \
  rm go$VERSION.$OS-$ARCH.tar.gz

echo 'export PATH=/usr/local/go/bin:$PATH' >> ~/.bashrc && source ~/.bashrc 
```

## Compile and Install Singularity

```bash

sudo apt install make

export VERSION=4.0.0 && \
    wget https://github.com/sylabs/singularity/releases/download/v${VERSION}/singularity-ce-${VERSION}.tar.gz && \
    tar -xzf singularity-ce-${VERSION}.tar.gz && \
    cd singularity-ce-${VERSION}

./mconfig && \
    make -C builddir && \
    sudo make -C builddir install
```

## Verify Installation

```bash
singularity version
```

[Answer Post Lab Questions](https://forms.gle/VLDfKq3G29trTSEu6)

