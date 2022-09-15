# MYSQL

This dockerfile creates a  MySQL container with a store schema already deployed, making it ready for database practices!

Firstly, you have to build the image that will be used:
```bash
$ docker build -t IMAGE_NAME .
```

Then, you can create new containers from it for your lab practices. 
To start this new container you can run the following command:
```bash
$ docker run --detach --name=CONTAINER_NAME --publish 3306:3306 IMAGE_NAME
```

Once the container is created, you can connect to the MySQL instance using `localhost:3306` as  database address in any client applicaton.

In case you want to access the database locally, you can do it by connecting to the docker instance, and then accessing the mysql instance with its command line interface, as follows:

```bash
$ docker start mysql-lab # if container is not running
$ docker container exec -it CONTAINER_NAME /bin/bash
$ mysql -uroot -p # By default, password is also 'root'
```