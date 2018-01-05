# CLI Assignment

* Use different linux distros containers to check **curl** cli tool version.
* The 2 different linux versions are ubuntu:14.04 and centos:7.


# Answer.

## For ubuntu 14.04
* **docker container run -it --name ubuntu ubuntu:14.04 sh**
* After the image is installed and the terminal running from the  container opens up, type **apt-get update && apt-get install curl**
* After it is installed , check curl version by **curl --version**.

## For centos:7
* **docker container run -it --name centos centos:7 sh**
* After the image is installed and the terminal running from the contaienr opens up, type **yum install curl && curl --version** to install curl and get the version.

