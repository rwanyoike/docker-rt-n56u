# docker-rt-n56u

Containerized version of [padavan/rt-n56u](https://bitbucket.org/padavan/rt-n56u), an alternative firmware for Asus RT WiFi routers (N56U, N65U, N14U etc.)

## Usage

This will pull an image with padavan/rt-n56u and a built MIPSel toolchain:

    $ docker run -it rwanyoike/rt-n56u

## Manual build

Clone and enter the repo, and execute `docker build`:

    $ git clone https://github.com/rwanyoike/docker-rt-n56u
    $ docker build -t rt-n56u:latest .

The build will clone the padavan/rt-n56u repo and build the MIPSel toolchain. Building the toolchain can take some time depending on your hardware. It took ~20 minutes on a [Standard A2 (2 cores, 3.5 GB memory)](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-windows-sizes/#a-series) VM on Azure:

    $ docker images

    REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
    rt-n56u             latest              3bcb41f57f24        14 hours ago        3.703 GB
    debian              jessie              ddf73f48a05d        2 weeks ago         123 MB