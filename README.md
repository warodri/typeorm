

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
postgres (PostgreSQL) 11.1
```

HOW TO CREATE A PHYSICAL POSTGRESQL DATABASE
===============================================

```
initdb /usr/local/var/postgres
```

HOW TO START/STOP A POSTGRESQL DATABASE
=========================================

```
pg_ctl -D /usr/local/var/postgres start
pg_ctl -D /usr/local/var/postgres stop
```

HOW TO CREATE THE ACTUAL POSTGRESQL DATABASE
=============================================

```
createdb mydatabasename
dropdb mydatabasename
```

You can also connect to databases to execute SQL statements. Either use the psql command, or specify a database such as the default postgres database to connect:

```
psql mydatabasename
```

The command leads you to the psql shell, which you can exit by typing CTRL + d. In the psql shell, you can create and drop databases as well:

```
CREATE DATABASE mydatabasename;
DROP DATABASE mydatabasename;
```

\list - List all of your actual databases.
\c mydatabasename - Connect to another database.
\d - List the relations of your currently connected database.
\d mytablename - Shows information for a specific table.


