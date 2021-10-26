# Crunchy Data Container Suite

Crunchy provide a set of containers that we can use to try out various tools.

At the root, the docker-compose.yml creates a:
    - db container running Crunchy's Postgres image
    - admin container running Crunchy's pgAdmin4 image. 
    - postgres_default network for all containers to communicate through.

Run the command <i>docker-compose up</i> to start the db and admin containers.

You can access the admin container at localhost:5050 and access credentials are available in the environment section of the docker-compose.yml file. 

All subdirectories represent postgres tools and contain respective README.MDs explaining how to run them. To get started quickly and run with default values, just <i>cd</i> into a tool directory and run <i>docker-compose up</i>.

Uncomment the PGBACKREST env var in the root docker-compose.yml file to initiliaser the postgres container with pgBackR
est