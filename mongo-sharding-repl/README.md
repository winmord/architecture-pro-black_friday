# mongo-sharding

## Как запустить

```shell
docker compose up -d
```

Инициализация шардирования

```shell
./scripts/mongo-sharding-init.sh
```

## Проверка

```shell
docker exec -it shard11 mongosh --port 27018
> use somedb;
> db.helloDoc.countDocuments();
> exit(); 

docker exec -it shard21 mongosh --port 27021
> use somedb;
> db.helloDoc.countDocuments();
> exit(); 
```

Суммарно должно быть ≥ 1000 документов