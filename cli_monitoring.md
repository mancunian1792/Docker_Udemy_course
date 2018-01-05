# What is going on in containers ?- A Look at CLI Process Monitoring tools.

## Requirement :
To know how to start a container.

## Commands 
* **docker container top <Name of the container / container id>** - This lists all the processes that are running inside the container.
* **docker container inspect <Name of the container / container id>** - This shows the metadata of the container. Its configuration, volumes and the networking.
* **docker container stats** - This shows a streaming data of all the active containers and their performance metrics like CPU%, Memory usage and its limit etc.. If you give a container name or id for this command the stats are shown only for that container.


# Getting a shell inside container - No Need for SSH.

* **docker container run -it -p 80:80 --name nginx nginx bash** - This command creates a container with an image of nginx and opens the port 80 of the host and 80 of the container and opens up an interactive terminal inside the container.

* If we exit inside the container then the container is stopped. By this way, we can access the container without even connecting it via an ssh. The -it option basically is -i (interactive) and -t (opens up a tty /basically like an ssh)

* **docker container start -ai <Name or container id>** -  To start a stopped container and still open up an interactive terminal inside the container.

* **docker container exec -it <Name or container id> <Additional command or program to run>** eg., docker container exec -it mysql bash --> This opens up a terminal inside the mysql container so that we can do any admininstrative stuff. When you type exit and come out of the container, the container doesnt stop as the command instructs the container to run an additional process within the container. This can be checked by typing ps aux (Lists all processes/ daemons inside any linux environment.)

# Other Linux Distributions.

* Alpine is a compressed or very tiny in size version of linux. It has its own package manager called apk to install all the packages.
