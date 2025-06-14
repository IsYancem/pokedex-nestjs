<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

<p>
  versión 09/06/2025
<p>

# Ejecutar en desarrollo

1. Clonar el repositorio
2. Ejecutar

```
yarn install
```
3. Tener Nest CLI instalado
```
npm i -g @nestjs/cli
```
4. Levantaer la base de datos
```
docker-compose up -d
```

5. Clonar el archivo __.env.template__ y renombrar kla copia a __.env__

6. Llenar las variables de entorno definidas en el __.env__

7. Ejecutar la aplicación en dev:
```
yarn start:dev
```
8. Reconstruir la base de datos con la semilla
```
http://localhost:3000/api/v2/seed
```

## Stack usado
* MongoDB
* NestJS

# Production Build
1. Crear un archivo ```.env.prod```
2. Llenar las variables de entorno de prod
3. Crear la nueva imagen
```
docker-compose -f docker-compose.prod.yaml --env-file .env.prod up --build 
```


# Notas
heroku redeploy sin cambios:
```
git commit --allow-empty -m "Tigger Heroku deploy"
git push heroku <master|main>
```
