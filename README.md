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

