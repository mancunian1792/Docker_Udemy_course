# Docker_Udemy_course

## Docker Editions
1.There is a community edition and enterprise edition.(using Docker CE)
2.Docker editions at store.docker.com
3.Docker moves fast, it matters how you install it.

* ### CE VS EE
1. EE = Support + extra products.
2. Docker CE(free).

* ### Stable vs Edge
1. Edge (beta) released monthly, stable quarterly.

## Docker installation.
* Use the automated docker script curl -sSL https://get.docker.com/ | sh (to get the edge version)
* Use this link for Documentation. [Documentation]https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#set-up-the-repository
* Other ways to install -> [Store]store.docker.com (Each distribution has a way to install as the distribution name changes.)
* May not work for unlisted distributions (Amazon Linux etc).
	
## Docker compose and machine
* Docker machine and compose doesnt get bundled into the docker build
* Check the latest version from this [Docker Compose] https://github.com/docker/compose/releases and install the appropriate command that you find in that page.
* curl -L https://github.com/docker/compose/releases/download/<latest-release-version>/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose (Use sudo if any error related to permission)
* Do the same for [Docker Machine] https://github.com/docker/machine/releases
* Check if both are installed fine by checking their version. docker-machine version , docker-compose version.
* docker info - Shows most of the configuration values of the docker engine.


