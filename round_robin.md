# Round Robin.

* In this test, we are going to create 2 elastic search servers with the same net alias so that whenever we hit the dns (alias name) we try to hit the 2 different servers.

* First, we need to create a network. **docker network create search**
* Then create 2 elastic search servers and attach it to the network.
* **docker container run -d --network search --net-alias esearch elasticsearch:2** Run this command twice to get 2 different servers. We are not altering the name option because it doesnt matter as of now.
* Now to test it , **docker container run --rm --net search alpine nslookup esearch** This should return the ip address of both the elastic search servers.
* Now to use curl command and get the elastic search server names, 
**docker container run --rm --net search centos:7 curl esearch:9200** several times to get different names. The --net command connects the container to the particular network.

