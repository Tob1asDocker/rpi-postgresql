# Dockerfile for PostgreSQL and PostGIS on Raspberry Pi
* based on the Docker official image for postgres
	* https://hub.docker.com/_/postgres/
	* https://github.com/docker-library/postgres
* and postgis:
	* https://hub.docker.com/r/mdillon/postgis/
	* https://github.com/appropriate/docker-postgis

Use:
* ``` git clone REPOSITORY && cd rpi-postgresql/ ```
* Optional: ``` mkdir -p /home/pi/.local/share/postgresql ```
* ``` docker build -t rpi-postgresql:9.4 ./9.4/ ``` 
* Use without PostGIS: ``` docker run --name pgsql -d -p 5432:5432 -v /home/pi/.local/share/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=mysecretpassword rpi-postgresql:9.4 ``` 
* Use with PostGIS:
	* ``` docker build -t rpi-postgresql-postgis:9.4-2.1 ./9.4-postgis2.1/ ``` 
	* ``` docker run --name postgis -d -p 5432:5432 -v /home/pi/.local/share/postgresql:/var/lib/postgresql/data -e POSTGRES_PASSWORD=mysecretpassword rpi-postgresql-postgis:9.4-2.1 ``` 
