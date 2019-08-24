# GoBarber

Backend em Node de aplicação de agendamento de horários em barbearia.


# Ambiente Dev

Para executar esse projeto siga as instruções abaixo:

criar arquivo `.env` na raiz tento o seguinte formato:

```
APP_URL=http://localhost:3333
NODE_ENV=development

# Auth

APP_SECRET=f29618255c309de4469993cce24286ea

# Database

DB_HOST=localhost
DB_USER=postgres
DB_PASS=docker
DB_NAME=gobarber

# MONGO

MONGO_URL=mongodb://localhost:27020/gobarber

# Redis

REDIS_HOST=localhost
REDIS_PORT=6380

# Mail

MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USER=62bac25f963075
MAIL_PASS=62ad933d9a609c

# Sentry

SENTRY_DSN=

```


## criar instancia do postgres no docker

`docker run --name gobarber-database -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d postgres`

## criar instancia do mongo no docker

`docker run --name gobarber-mongo -e POSTGRES_PASSWORD=mysecretpassword -p 27017:27017 -d -t mongo`

## criar instancia do servidor redis no docker

`docker run --name gobarber-redis -p 6379:6379 -d -t redis:alpine`

## executar aplicação

```
yarn dev
yarn queue
```
