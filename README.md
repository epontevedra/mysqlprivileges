**Starting with MySQL 8 you no longer can (implicitly) create a user using the GRANT command. Use CREATE USER instead, followed by the GRANT statement:**

USE mysql;
CREATE USER 'user'@'localhost' IDENTIFIED BY 'Thanos123!';
GRANT ALL ON *.* TO 'user'@'%';
FLUSH PRIVILEGES;
