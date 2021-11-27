1. Start the container with config as in the file
       docker-compose up
2. Backup and restore specific db fom cmd line:
      docker exec 5df534aedf90 pg_dump -U admin -d mydb > backup.sql   ### data stored where the command run
      docker exec -i 5df534aedf90 psql -U admin -d mydb < backup.sql   ### data stored where the command run
3. Backup and restore all db's fom cmd line:
      docker exec 5df534aedf90 pg_dumpall -U admin > backup.sql   ### data stored where the command run
      docker exec -i 5df534aedf90 psql -U admin < backup.sql     ### data stored where the command run
4. Stop container:
      docker-compose stop
5. Delete container: (Optional)
      docker rm container_id
