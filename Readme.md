# Odoo server with postgres database

_Odoo server with integrated postgres database_

## This server is still under development

## Getting Started ๐

_This is a guide for the deployment of this odoo server, no support will be provided_

Check-out **Installation** for more information.


### Requirements ๐

_Needed programs_

```
docker
docker-compose
```

### Installation ๐ง

_Execute the following commands_

```
git clone https://github.com/Javiito32/odoo-server.git
cd odoo-server
docker-compose up
```
_Instead of ```docker-compose up``` you can use ```docker-compose up -d``` to start it in detached mode._

### Start โ๏ธ and Stop ๐
_After the installation you can start and stop it with ```docker-compose start``` and ```docker-compose stop```_

### Complete Deletion ๐๏ธ
_Use ```docker-compose down``` to remove the odoo server, postgres database, and docker network's_

โ ๏ธ _The use of this command to stop it and then start it back with ```docker-compose up``` is not recommended, check ***Start โ๏ธ and Stop ๐*** instead_

โ๏ธ This won't remove the addon's [addons](odoo/addons) or the data of the database [postgres](postgres).

โจ The following directories are not working, still under development [config](odoo/config) and [web](odoo/web) 

๐งน To clean the database, remove all the contents of the [postgres](postgres) folder.

## Accessing Odoo โ๏ธ

_Now the Odoo Server should be available at localhost:8069_

โก You might set up your own configuration, the name of the database can't be _postgres_ or any other reserved word.

### Database connection โ๏ธ

_The connection between Odoo and Postgres is made via the created docker's network, you can also access it with this connection string_

```
Server=localhost;Port=3306;Database=postgres;Uid=odoo;Pwd=odoo;
```
You can modify the password and database name on [docker-compose](docker-compose.yml).

## License ๐

This project is under AGPL-3.0-only - Checkout [LICENSE](LICENSE) for more detail

---
โจ๏ธ with โค๏ธ by [Javiito32](https://github.com/Javiito32) ๐
