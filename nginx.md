We are going to explain the fundamentals of docker by trying to create a sample nginx server.

# Difference between image and container 
* An image is the application we want to run (Binaries or web app or here in this example creating an nginx server). 
* A container is the running instance of the image.
* There can be many containers running the same image.


# Run/stop/remove containers
* docker container run --publish 80:80 nginx
What does the above step do ?
	1. Search for a image locally named 'nginx' and if it is not found then Download image 'nginx' from Docker hub.
	2. Started a new container from that image.
	3. Opened port 80 on the host IP.
	4. Routes that traffic to the container IP, port 80.
* **docker container run --publish 80:80 --detach nginx** (use this option as the container will be running but the cmd line would have been detached so that we can run more commands on that same tab.)
* --name option for us to use our own container name.. Else that name would be autogenerated like the container id.Those names are generated from adjectives and famous known hackers or computer scientist.
* **docker container ls** - Lists all running container. -a option to list all
* **docker container stop <containerId or first few digits of container id to make it unique.>**
* **docker container rm <container name/id>** . To remove containers
* If there is any active container, it cant be removed without being stopped first or being forcefully removed . use -f option to forcefully remove.


# Check container logs and processes
* **docker container logs <Container_ID/name>**

