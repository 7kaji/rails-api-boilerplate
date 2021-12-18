## Rails new

versions
- Ruby 3.x
- Rails 7.x
- MySQL 8.x

```sh
$ docker compose run app rails new --api . -f -d mysql
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

localhost:3000
[![Image from Gyazo](https://i.gyazo.com/66a83bf4375e336343123d0fb3655663.png)](https://gyazo.com/66a83bf4375e336343123d0fb3655663)

log

```sh
$ docker compose logs -f app
$ docker compose logs -f db
```
