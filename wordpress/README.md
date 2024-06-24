# Installation
Install mysql database in your local

## MYSQL
Log into your MySQL database, and open the configuration file with the command:
```sh
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```
In that file, look for the line:
```sh
bind-address = 127.0.0.1
```
Change that line to:
```sh
bind-address = 0.0.0.0
```
Save and close the file.

Restart the MySQL service with:
```sh
sudo systemctl restart mysql
```

create your username and database 
```sh
sudo mysql
```

```mysql
CREATE USER 'wordpress'@'%' IDENTIFIED WITH mysql_native_password BY 'wordpress';
GRANT ALL PRIVILEGES ON *.* TO 'wordpress'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

## Usage

Create an .env file and complete this with your database information
```txt
WORDPRESS_DB_HOST=
WORDPRESS_DB_USER=
WORDPRESS_DB_PASSWORD=
WORDPRESS_DB_NAME=
```

and start it 
```sh
docker compose up -d
```
your wordpress run at http://localhost:8080 now

