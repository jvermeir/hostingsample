## Build

```
./mvnw clean package

docker build -t demo:latest .
```

## Run in compose

```
docker-compose up -d
```

## (Optional) Create database

Create only the database and run the service as a Java process

```
docker run --rm --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d postgres
```

```
docker exec -it some-postgres psql -U postgres
```

in psql:

```
create database test;
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
