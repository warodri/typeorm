

INSTALL TYPE ORM
===================
Follow the instructions here
https://www.npmjs.com/package/typeorm


INSTALL POSTGRES
==================
I recommend Homebrew for installing and managing applications on MacOS. It is installed using the following command in the MacOS terminal:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

```
brew update
brew install postgresql
```

```
postgres --version
postgres (PostgreSQL) 11.5
```

LOGIN AS postgres USER
========================

```
sudo su postgres
```

Then enter your passsword. You will be able to run postgres commands.

```
CREATE DATABASE mydatabasename;
DROP DATABASE mydatabasename;
```

* \list - List all of your actual databases.
* \c mydatabasename - Connect to another database.
* \d - List the relations of your currently connected database.
* \d mytablename - Shows information for a specific table.


CREATE NEW USER
=================

```
createuser --interactive --pwprompt
```

1. At the Enter name of role to add: prompt, type the user's name.
2. At the Enter password for new role: prompt, type a password for the user.
3. At the Enter it again: prompt, retype the password.
4. At the Shall the new role be a superuser? prompt, type y if you want to grant superuser access. Otherwise, type n.
5. At the Shall the new role be allowed to create databases? prompt, type y if you want to allow the user to create new databases. Otherwise, type n.
6. At the Shall the new role be allowed to create more new roles? prompt, type y if you want to allow the user to create new users. Otherwise, type n.
7. PostgreSQL creates the user with the settings you specified.


CREATING POSTGRESQL DATABASES
==============================

```
createdb -O [user] [dbname]
```

Replace [user] with the user you just created and [dbname] with the name of your new database.

ADDING AN EXISTING USER TO A DATABASE
=======================================

To grant an existing user privileges to a database, follow these steps:

```
GRANT permissions ON DATABASE dbname TO username;
```

More details on GRANT: https://www.postgresql.org/docs/9.1/sql-grant.html

More info: https://www.a2hosting.co.uk/kb/developer-corner/postgresql/managing-postgresql-databases-and-users-from-the-command-line#Creating-PostgreSQL-users

INSTALL POSTICO (postgres manager for Mac)
=============================================

Download from here: https://eggerapps.at/postico/


