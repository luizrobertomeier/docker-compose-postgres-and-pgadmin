# docker-compose-postgres-and-pgadmin
A docker-compose file to fast install and run PostGres and Pgadmin locally.

# How to install (steps)

1) Install docker

2) Install docker-compose

3) Close or Download the repo and run the command: docker-compose up -d

If your system does not have Postgres and PgAdmin images, they will be downloaded automatically.

The PostGres version can be easily changed within the file on the line (example):
image: postgres: 12.4 to postgres: latest

