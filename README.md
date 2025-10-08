<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# Ejecutar en desarrollo

1. Clonar el repositorio.
2. Ejecutar

```
yarn install
```

3. Tener Nes CLI instalado

```
nmp i -g @nestjs/cli
```

4.Levantar la base de datos

```
docker compose up -d
```
5. Clonar el archivo __.env.template__ y renombrar la copia a __.env__

6. Lenar la variables de entorno definidas en el ```.env```

7. Ejecutar la aplicación en dev:
```
yarn start:dev
```
8. Reconstruir la base de datos con la semilla
```
localhost:3000/api/v2/seed
```

## Stack utilizado

- MongoDB
- Nest

## Build
docker compose -f docker-compose.prod.yaml --env-file .env.prod up --build

## Run
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up

## Nota
Por defecto, __docker-compose__ usa el archivo ```.env```, por lo que si tienen el archivo .env y lo configuran con sus variables de entorno de producción, bastaría con
```
docker-compose -f docker-compose.prod.yaml up --build
```