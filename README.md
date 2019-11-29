# springsecurityjpawithsqlpoc
1) Install mysql locally in the computer. For my case I have mac os, so I installed the myswl from https://www.dev2qa.com/how-to-use-mysql-on-mac/ and then go to usr\local\mysql and then type ./mysql -u root -p yourpassword to connect to mysql server.

2) Some steps I used to create a dummy user :

//creating a database
     mysql> create database springsecurity;

//using the database
    mysql> use springsecurity;
//creating a table
    mysql> CREATE TABLE user (id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,password VARCHAR(120), roles VARCHAR(40),user_name    VARCHAR(40),active BOOLEAN);
 
//Inserting data in table
  mysql> INSERT INTO USER VALUES(1,'pass','ROLE_USER','user',true);

 //checking to see if i have any data;
      mysql>select * from user;
+----+----------+-----------+-----------+--------+
| id | password | roles     | user_name | active |
+----+----------+-----------+-----------+--------+
|  1 | pass     | ROLE_USER | user      |      1 |
+----+----------+-----------+-----------+--------+
1 row in set (0.01 sec)

3) Make sure to add all dependencies in pom and configure the applicatio.properties files with all info needed to connect to database.
