# MYSQL

This dockerfile creates a  MySQL container with a store schema already deployed, making it ready for database practices!

## Configuration

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

## The store schema

The default container comes with a sample database schema, based on the one provided by [mysqltutorial.org](https://www.mysqltutorial.org/mysql-sample-database.aspx). 
The sample schema consists of the following tables:

- Customers: stores customer’s data.
- Products: stores a list of scale model cars.
- ProductLines: stores a list of product line categories.
- Orders: stores sales orders placed by customers.
- OrderDetails: stores sales order line items for each sales order.
- Payments: stores payments made by customers based on their accounts.
- Employees: stores all employee information as well as the organization structure such as who reports to whom.
- Offices: stores sales office data.
