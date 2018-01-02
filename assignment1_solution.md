# Assignment 1

## To create 3 processes.
* mysql process to run on default port and the environment option of random password set to true. Also find this password in logs.
* Login to mysql and execute a sql command.
* Create a http apache server to run on port 8080 of the host and 80 port in the container. (Test whether it works.)
* create a nginx server to run on port 80 of the host and 80 port in the container. (Test whether it works.)
* View all the active process.
* Stop the mysql and apache container and remove them.
* Remove the nginx container.


# Solution.

* sudo docker container run --publish 3306:3306 -e MYSQL_RANDOM_GENERATED_PASSWORD=yes --name mysql -d mysql
* sudo docker container run --publish 8080:80 --name apache -d httpd
* sudo docker container run --publish 80:80 --name nginx -d nginx
* sudo docker container ls 
* sudo docker container stop <all container ids>
* sudo docker container logs <Container id>
