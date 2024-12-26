# MongoDB

## dump/restore
```
In docker container:
  mongodump -d opea -o opea.json  -u root -p xxxroot --authenticationDatabase admin

In host:
  docker exec -it f0xxxxx0c  bash -c "mongodump -o /data/db/opea.json -d opea --uri mongodb://root:passwd@127.0.0.1:27017 --authenticationDatabase admin"

cp -r opea.json xxx/opea.json
mongorestore -d opea ./opea.json/opea/ --drop  -u root -p xxxroot --authenticationDatabase admin
```
