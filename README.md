# diesel_demo

## 1. Setup

Install postgresql

```
sudo apt-get install wget ca-certificates

wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
 2045  sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ 'lsb_release -cs'-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'

sudo apt-get update

sudo apt-get install postgresql postgresql-contrib
```

Install diesel_cli

```
sudo apt install libpq-dev libmysqlclient-dev
cargo install diesel_cli --no-default-features --features postgres
diesel setup
```

## 2. Common command lines

migration

```
diesel migration generate `name`
```

new migration

```
diesel migration run
```

roll back migration

```
diesel migration redo
```

run

```
cargo run --bin `name`
```