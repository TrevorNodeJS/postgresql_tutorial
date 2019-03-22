# postgresql Tutorial

## Install Postgresql on Windows 10
- logon https://www.postgresql.org/ , 
- find Download, and for Windows, 
- https://www.postgresql.org/download/windows/ -> https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
- select version , e.g. 11.2 for Windows X86-64
- get file "postgresql-11.2-1-windows-x64.exe" on your local PC
- Execute this file directly, you will be asked for input password
## Set system environment variants for postgresql
- PATH : C:\Program Files\PostgreSQL\11\lib;C:\Program Files\PostgreSQL\11\bin
- PGDATA: C:\Program Files\PostgreSQL\11\data

## Initialize the DB directory
$initdb -D "C:\Program Files\PostgreSQL\11\data"

## Start Database server
$ pg_ctl start

## create database
$ createdb mydb

## access database
$ psql mydb

### get warning message
>WARNING: Console code page (437) differs from Windows code page (1252)
>...
>...

### change code page
- Close current Console and open it again
- execute chcp in command line
$ chcp 1252
Active code page 1252
$ pg_ctl start
$ psql mydb






