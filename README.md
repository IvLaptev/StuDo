# StuDo

## Requirements

* [.Net Core 3.1](https://dotnet.microsoft.com/download)
* [Node.JS 12+](https://nodejs.org/en/)

## Run from docker hub images

#### Pull images
```bash
docker-compose pull
```

#### Start containers
```bash
docker-composer up -d
```

## Build

Use [Nuke](https://nuke.build/) to build all parts of application

### Build all
#### On Windows machine
```bash
./build.ps1
```
#### On Linux machine
```bash
./build.sh
```

### Build docker images
```bash
docker-compose build
```

### Start docker containers
```bash
docker-compose up -d
```

## Deploy

### Create ".env" file
### Fill it with the next content:
```env
POSTGRES_CONNECTION_STRING=your postgres connection string
LOGSOPTIONS__SECRETKEY=random_super_puper

DB_FIRSTNAME=default user firstname
DB_SURNAME=default user surname
DB_EMAIL=default user email
DB_PASSWORD=default user password

JWT_SECRET=secret key for jwt
JWT_AUDIENCE=audience for jwt
JWT_ISSUER=issuer for jwt
```

### Run this command to generate docker swarm stack file:
```bash
# powershell
.\generateStackYml.ps1
```
