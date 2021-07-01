## To check PSQL service is running or not in linux
- service postgresql status

## To connect with PSQL
- sudo -i -u postgres
- psql

## To list all database 
- \l (short hand)
- SELECT datname FROM pg_database;

## To create new db
- CREATE DATABASE _DB_NAME_;

## To drop any db
- DROP DATABASE _DB_NAME_;

## To connect any db 
- \c _DB_NAME_;

## To restore db from .sql file (WINDOW Machine)
- psql -h localhost -d _DB_NAME_ -U postgres
- pg_restore -U postgres --dbname=_DB_NAME_ --verbose <_FILE_PATH_>.sql

## To dump db 
- psql -h localhost -d _DB_NAME_ -U postgres
- pg_dump -h localhost -U postgres _DB_NAME_ > _FILE_PATH_.sql

## To import any table's data store in text file 
- COPY public.__TABLE_NAME__(id, , , , ) FROM '_TEXT_FILE_PATH_';

## To setup new instance of psql (different port)
- initdb -D _NEW_DIR_NAME_ -U postgres -W
(prompts for password)

- pg_ctl register -N _SERVICE_NAME_ -D _NEW_DIR_NAME_ -o "-p _NEW_PORT_"

- pg_ctl start -D _NEW_DIR_NAME_ -o "-p _NEW_PORT_"

