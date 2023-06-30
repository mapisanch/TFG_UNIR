# MLOps platform designed to include several services usefull for DataScientists

## Services available
1. Postgres database
2. MLFlow
3. Minio
4. Jupyter

## Preparing the environment

In order to be ready to use this platform, Docker and docker-compose are required in your machine. 

Install [Docker](https://docs.docker.com/engine/) and [docker-compose](https://docs.docker.com/compose/install/)

## Run the platform at your local machine

1. First, clone this repository in a folder in your machine, then go to the cloned folder.

```
Here the git clone
Here the cd
```

2. Run docker-compose up to download all services images by docker engine by layers, and then deploy all services inside the same network. Probably you need to sudo it!

```shell
docker-compose up
```
   
3. In case you want to have several requirements in your jupyter environment, you can install them directly.

```shell
pip install pandas
```

4. To stop docker-compose, just press ctrl + c (cmd + c in mac).

5. To remove containers, just do:
```shell
docker-compose down
```

## See deployed services online

1. Jupyter
Copy the token generated for your Jupyter app from the logs generated when `docker-compose` was run.
Now you need to open `localhost:8888` and everything stored under `work` folder will be persisted in your machine, under `data/jupyter` folder. This possibility has been set up by creating volumes in docker-compose definition.

2. Minio
Go to `localhost:9000` in order to open Minio interface.

3. MLFlow
Go to `localhost:4000` to open MLFlow server web app.

4. Postgres database
There is no default web view deployed with docker-compose, but you can always download [PgAdmin](https://www.pgadmin.org/download/) app and configure it using service parameters defined in docker-compose.yaml file.
