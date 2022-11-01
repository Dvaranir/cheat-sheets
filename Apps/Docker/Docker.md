## Show docker containers
```bash
docker ps
```

## Enter docker container with bash
```bash
docker exec -it "CONTAINER_NAME or CONTAINER_ID" bash 
```

## Containers restarting with docker-compose
```bash
docker-compose down
docker-compose up
```

## Turn off docker with cache clean
```bash
docker-compose down -v
```

