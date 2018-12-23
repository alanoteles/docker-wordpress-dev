# docker-wordpress-dev
**Containerized Wordpress Development environment**

This docker-compose file creates a local development environment to Wordpress projects, including an phpMyAdmin installation to help you manage your MariaDB/MySQL database. You can access the login screen on 8080 port. (http://localhost:8080). User and password for root user is “root”.

Is important to remember :

* On `db` service, in ` - volumes` , if you set your local volume with only  “your-data-folder-name", your volume will be created on your Docker volumes folder. Something like `/var/lib/docker/volumes/your-data-folder-name/_data`. If you are on a Linux environment you’ll not have any difficulty to find and access this folder. But if you are on a Mac or Windows, since Docker runs in a layer of virtualization on  Mac or Windows computers, is a bit more complicated to get access to volumes folder.
To create your data folder on your current folder just inform `./your-folder-name`. 

* The database name you define on `environment : MYSQL_DATABASE: your-database-name` will be used to automatically create your database. Name it as you wish. But if it already exists, you’ll need to empty your data folder  before run you compose file.

As we not inform the docker-compose file version, it is a “version: ‘2’”. 
