# PostgreSQL on Raspberry Pi

### Image Info
This Image based on the Docker official image for postgres
* https://hub.docker.com/_/postgres/
* https://github.com/docker-library/postgres

### How to use this image
* ``` docker pull tobi312/rpi-postgresql:9.4 ```
* Optional: ``` mkdir -p /home/pi/.local/share/postgresql ```
* ``` docker run --name pgsql -d -p 5432:5432 -v /home/pi/.local/share/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=mysecretpassword tobi312/rpi-postgresql:9.4 ``` 

or build it yourself
* ``` git clone https://github.com/TobiasH87Docker/rpi-postgresql.git && cd rpi-postgresql/ ```
* ``` docker build -t tobi312/rpi-postgresql:9.4 ./9.4/ ``` 
* Optional: ``` mkdir -p /home/pi/.local/share/postgresql ```
* ``` docker run --name pgsql -d -p 5432:5432 -v /home/pi/.local/share/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=mysecretpassword tobi312/rpi-postgresql:9.4 ``` 

### PostGIS ? , see here: 
* [DockerHub](https://hub.docker.com/r/tobi312/rpi-postgresql-postgis/)
* [GitHub](https://github.com/TobiasH87Docker/rpi-postgresql-postgis)
