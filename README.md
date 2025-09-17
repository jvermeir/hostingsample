## Create database

```
docker-compose up -d db
```

## Build

```
./mvnw clean package

docker build -t demo:latest .
```

## Run in compose

```
docker-compose up -d
```

## Test

add person:

```
curl -X POST \
  http://localhost:8080/api/persons \
  -H 'Content-Type: application/json' \
  -d '{
    "firstName": "John",
    "lastName": " Doe"
  }'
```

get all persons:

```
curl -X GET http://localhost:8080/api/persons
```
