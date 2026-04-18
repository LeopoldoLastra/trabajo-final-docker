# Usamos la imagen base de Alpine Linux
FROM node:18-alpine

# Establecemos el directorio de trabajo
WORKDIR /app

# Copiamos solo dependencias
COPY package.json yarn.lock ./

# Instalamos las dependencias del proyecto
RUN yarn install

# Copiamos los archivos del proyecto al contenedor
COPY . .

# Exponemos el puerto de la aplicación
EXPOSE 3000

# Comando por defecto para ejecutar la aplicación
CMD ["node", "src/index.js"]