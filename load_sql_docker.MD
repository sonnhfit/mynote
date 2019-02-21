- show docker container id: ```docker ps```
- docker-compose down
- show docker volume ```shell docker volume  ls ```
- remove volume sql exist with command : 
- docker volume rm <name volume>
- create docker db volume blank with command: docker-compose up -d db
  ```docker-compose up -d <db_name>``` 
- import sql file with command: ```cat <sqlfile.sql> | docker exec -i <dontainer id> psql -U postgres -d postgres```
- for example:   cat sixcents-db-2018-11-16.sql | docker exec -i e1a2a1e3ab89 psql -U postgres -d postgres
