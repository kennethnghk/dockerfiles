# Redis dockerfiles

Ref from : https://docs.docker.com/engine/examples/running_redis_service/

## Redis server

Build image
```
docker build -t <repository>/redis-server -f redis-server-dockerfile .
```

Run in background
```
docker run --name redis-server -d <repository>/redis-server
```

## Redis client

Build image
```
docker build -t <repository>/redis-client -f redis-client-dockerfile .
```

Run container
```
docker run --name redis-client --link redis-server:db -i -t <repository>/redis-client /bin/bash
```

`--link redis:db` : Docker has created some environment variables in our web application container.

```
$ env | grep DB_
```

Connect to redis-server
```
redis-cli -h $DB_PORT_6379_TCP_ADDR
```