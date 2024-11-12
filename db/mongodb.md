# MongoDB

## dump/restore
```
mongodump -d opea -o opea.json  -u root -p xxxroot --authenticationDatabase admin
cp -r opea.json xxx/opea.json
mongorestore -d opea ./opea.json/opea/ --drop  -u root -p xxxroot --authenticationDatabase admin
```
