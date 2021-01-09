# docker-compose-postgres-and-pgadmin
A docker-compose file to fast install and run PostGres and Pgadmin locally.

# How to install (steps)

1) Install docker

2) Install docker-compose

3) Clone or Download the repo and run the command: docker-compose up -d

4) After the docker downloads the images and installs the containers, you can test pgadmin in the browser:

4.1) localhost: 5430 (or another port you have chosen)

4.2) username and password you set in docker-compose.yml

5) Pgadmin:

5.1) Once inside pgadmin, create a new server using the side menu: server->create server

5.2) In the General tab, define a Name, for example: postgres-local 

5.3) In the Connection tab, find out your *local* IP of the postgres container using the command: docker exec local-postgres-compose [or any other name of the container] cat /etc/hosts, example: 172.18.0.2

5.4) username: postgres and password defined in the docker-compose.yml

Notes:

If your system does not have Postgres and PgAdmin images, they will be downloaded automatically.

The PostGres version can be easily changed within the file on the line (example):
image: postgres: 12.4 to postgres: latest
