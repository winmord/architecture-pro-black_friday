# mongo-sharding

## Как запустить

```shell
docker compose up -d
```

Инициализация шардирования

```shell
./scripts/sharding-repl-cache-init.sh
```

## Проверка

Второй и последующие вызовы эндпоинта http://localhost:8080/helloDoc/users выполняются <100мс
