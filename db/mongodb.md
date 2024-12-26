# MongoDB

## dump/restore
```
mongodump -d opea -o opea.json  -u root -p xxxroot --authenticationDatabase admin

mongodump -o opea.json   --uri "mongodb://root:passwdxxx@127.0.0.1:27017/xx_db"


cp -r opea.json xxx/opea.json
mongorestore -d opea ./opea.json/opea/ --drop  -u root -p xxxroot --authenticationDatabase admin
```
