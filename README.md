# rdkb-docker-development
rdkb-docker-development
# rdkb-dev
# Building RDKB Yocto Docker Image

Build the Docker image with:

```bash
#From outside the container
cd ~/Git/rdkb-dev/build-workspace/rdkb-workspace/rdkb-arm
repo init -u 'git+ssh://git@github.com/rdkcentral/meta-rdk-bsp-arm/' -m "manifests/rdkb-bsp-arm.xml" -b "develop"
repo sync
#From inside the container
cd rdkb-arm
source meta-rdk-bsp-arm/setup-environment
bitbake rdk-generic-broadband-image

