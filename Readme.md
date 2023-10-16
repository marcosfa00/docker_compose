# Instrucciones para ejecutar Apache en Docker

Este README proporciona instrucciones para ejecutar múltiples contenedores de Apache en Docker utilizando Docker Compose.

## Composición de Docker

### Archivo docker-compose.yml

El archivo `docker-compose.yml` define dos servicios de Apache, `apache` y `apache2`, que se ejecutarán en contenedores separados.

#### Servicio `apache`

- Nombre del servidor: `apache`
- Imagen: `httpd:2.4`
- Puertos mapeados: `8080:80`
- Volumen: Mapea el directorio local `./htdocs` al directorio `/usr/local/apache2/htdocs` en el contenedor.
- Nombre del contenedor: `dam_web1`

#### Servicio `apache2`

- Nombre del servidor: `apache2`
- Imagen: `httpd:2.4`
- Puertos mapeados: `9080:80`
- Volumen: Mapea el directorio local `./htdocs` al directorio `/usr/local/apache2/htdocs` en el contenedor.
- Nombre del contenedor: `dam_web2`

## Ejecución en la Terminal

Para ejecutar estos servicios en Docker, sigue estos pasos en la terminal:

1. Asegúrate de que Docker Compose esté instalado en tu sistema.

2. Navega al directorio donde se encuentra tu archivo `docker-compose.yml`.

3. Ejecuta el siguiente comando para iniciar los contenedores en segundo plano:

   ```bash
   docker compose up -d
