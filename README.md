# How to build container for conference_app demo

## To run container, first build using Dockerfile:

    docker build . -t postgres-demo

Once built, create a container based on that image:

    docker create --name postgres-demo -p 5432:5432 postgres-demo:latest

Start the container

    docker start postgres-demo

Wait for the import of sql files to complete in database (1-2 minutes)

Done!