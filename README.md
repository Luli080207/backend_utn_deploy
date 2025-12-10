Backend UTN – API REST en TypeScript

Este proyecto es una API REST desarrollada en Node.js, Express, TypeScript y MongoDB.
Incluye autenticación con JWT, validaciones con Zod, filtrado por query params, middlewares de seguridad y un sistema básico de productos y usuarios.

- Tecnologías utilizadas :

- Node.js

- Express

- TypeScript

- MongoDB + Mongoose

- Zod

- Helmet

- Morgan

- Express-rate-limit

- Nodemailer

- Estructura del proyecto :
src/
  config/
  controllers/
  interfaces/
  middleware/
  model/
  routes/
  services/
  templates/
  validators/

  Scripts de ejecución :

En package.json:

npm run dev     -> ejecutar en desarrollo con TypeScript
npm run build   -> compilar a JavaScript (carpeta dist)
npm start       -> ejecutar lo compilado en producción

- Autenticación :

Registro de usuario

Login

Generación y validación de JWT

Rutas protegidas para crear, editar o eliminar productos

- Middlewares importantes :

morgan → logging de todas las solicitudes

helmet → cabeceras de seguridad

rate-limit → aplicado solo al login y registro

zod → validación de inputs

errorMiddleware → manejo uniforme de errores

authMiddleware → rutas protegidas

- Query Params disponibles :

En productos:

categoria=

minPrice=

maxPrice=

name= (busqueda parcial)

Los filtros se aplican directamente en MongoDB.

--- Ejecución local ---

Clonar el repo

Instalar dependencias

npm install


Crear archivo .env

Ejecutar en desarrollo

npm run dev


Para producción

npm run build
npm start

deploy online:
El backend esta deployado en el siguiente link: https://backend-utn-deploy.onrender.com/

