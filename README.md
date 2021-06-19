## Rails new

versions
- Ruby 3.x
- Rails 6.x
- MySQL 8.x


```sh
$ docker compose run app rails new --api . --force --database=mysql
```

config/database.yml

```rb
default: &default
  adapter: mysql2
  encoding: utf8mb4
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: user
  password: password
  host: db
```

## Run

```sh
$ docker compose build --no-cache
$ docker compose up -d
```

log

```sh
$ docker logs app
$ docker logs db
```


