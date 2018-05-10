# Mongo-connector sync to elasticsearh5

Referencies: https://github.com/mongodb-labs/mongo-connector

Build:

```
git clone ...
cd ...
docker build -t mongo-connector .
```

Usage (Rancher):
```
docker run -itd --name mongo-connector mongo-connector:0.1 /usr/local/bin/mongo-connector -m mongo-server-address:27017 -t 'elastic-user@:elastic-password@elastic-address:9200' -d elastic2_doc_manager --continue-on-error -x 'db.exclude_collection'
```

Use with Rancher, add the option in command line:
```
--label io.rancher.container.network=true
```

