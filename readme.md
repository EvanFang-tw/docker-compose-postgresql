# Use docker-compose to start PostgreSQL

Start PostgreSQL with docker-compose and create table while DB is initialized.

## docker-compose
```sh
# run
docker-compose up
docker-compose up -d

# enter container
docker exec -it psqldb bash

# teardown
docker-compose down
```

## psql

Run commands below in the container.

```
# conntect to database
psql -U admin -d mydb

# show tables
\dt

# describe tables
\d products

# test insert and select
insert into products (name) values ('first name');
select * from products;
```