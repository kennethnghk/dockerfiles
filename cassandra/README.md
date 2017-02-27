# Cassandra dockerfiles

## Cassandra server

Build image
```
docker build -t <repository>/cass-server -f cassandra-server-dockerfile .
```

Run in background
```
docker run --name cass-server -d <repository>/cass-server
```

## Connect to Cassandra by `cqlsh`

```
docker run -it --link cass-server:cassandra --rm cassandra sh -c 'exec cqlsh "$CASSANDRA_PORT_9042_TCP_ADDR"'
```