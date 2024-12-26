# MongoDB

## dump/restore

In docker container:

```
  mongodump -d opea -o opea.json  -u root -p xxxroot --authenticationDatabase admin
  mongodump -d opea -o opea.json --uri mongodb://root:passwd@127.0.0.1:27017 --authenticationDatabase admin
```

In host:
```
  docker exec -it f0xxxxx0c  bash -c "mongodump -o /data/db/opea.json -d opea --uri mongodb://root:passwd@127.0.0.1:27017 --authenticationDatabase admin"
```

Restore 

In docker container:

```
mongorestore ./opea.json --drop -u root -p xxxroot --authenticationDatabase admin
mongorestore ./opea.json --drop --uri mongodb://root:passwd@127.0.0.1:27017 --authenticationDatabase admin
```
