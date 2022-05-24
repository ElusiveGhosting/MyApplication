#Postgres setup using Docker

1. install docker application
2. Pull the required images:
       docker pull postgres (Manadatory)
       docker pull thajeztah/pgadmin4 (Optional for comfortable NoCLI UI)
3. Create the docker container for both psql and UI:
       docker run --name myDB -p 5432:5432 -e POSTGRES_PASSWORD=admin -d postgres
       docker run --rm -p 5050:5050 -d thajeztah/pgadmin4
4. Test psql container (optional)
       open localhost:5050 in browser
5. Programmaticc testing of psql container:
       docker exec -it container#id bash
       psql -h localhost -p 5432 --user postgres (no password needed)
                           (or)
       psql -h localhost -p 5432 --user postgres -W (asks password)
6. Stop the container (necessary for deleting container) :
       docker stop container_id
7. Delete the container:
       docker rm container_id
8. Devops testing for created database:

       \z ###show all tables
       CREATE DATABASE mydb;
       \c mydb
       SELECT current_database();
       CREATE TABLE beer();
       DROP TABLE beer;
       \l ### list all databases
