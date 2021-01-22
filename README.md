# Globex Database Exercise

## Pre-requisites

You will need to have the following tools installed [Docker](https://www.docker.com/products/docker-desktop) and a tool to let you interact with an MS SQL database.

### Visual Studio Code Extensions

There are extensions for Visual Studio Code that let you connect to SQL database. You will need to install [SQLTools](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools) and [SQL Server (mssql)](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).

## First time setup

Ensure that docker is running on your machine by using `docker -v`.
From command line, in this directory run the startup script appropriate for your shell. (Either `startup.bat` or `startup.sh`; Powershell & `startup.bat` recommended on Windows as Git Bash will not run some of the commands).

## Connect to the database

Check that the container is running with `docker ps`, you should see something like the following:

```
CONTAINER ID   IMAGE       COMMAND                  CREATED         STATUS                   PORTS                    NAMES
<SOME_ID>      module-09   "powershell -Command…"   3 minutes ago   Up 3 minutes (healthy)   0.0.0.0:1433->1433/tcp   module-09-container
```

If it isn't, run `docker start module-09-container` to start it. If you stop the container for any reason (e.g. restarting your machine) you'll need to run this command.

Connect to the database with the following details:
Server name: `localhost`
Port Number: 1433
_Note, in SSMS you provide server name and post together using this syntax: `localhost,1433`_
Authentication: `SQL Server Authentication`
Login: `sa`
Password: `Password123!`
