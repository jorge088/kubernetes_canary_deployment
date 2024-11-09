# Usa una imagen de servidor web como base
FROM nginx:alpine
COPY nginx.conf /etc/nginx/nginx.conf
# Copia los archivos de la aplicación a la carpeta html del servidor NGINX
COPY . /usr/share/nginx/html

# Exponer el puerto 80 para que la aplicación sea accesible
EXPOSE 5001
