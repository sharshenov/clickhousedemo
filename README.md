# README

Run clickhouse container
```sh
docker run -d -p 8123:8123 -p 9000:9000 -e CLICKHOUSE_PASSWORD=clickhouse --name clickhouse --ulimit nofile=262144:262144 clickhouse/clickhouse-server
```

Check if is running
```sh
echo 'SELECT version()' | curl 'http://localhost:8123/?password=clickhouse' --data-binary @-
```