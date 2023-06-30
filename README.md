# Plataforma MLOps diseñada para incluir varios servicios útiles para los científicos de datos

## Servicios disponibles
1. Postgres database
2. MLFlow
3. Minio
4. Jupyter

## Preparación el entorno 

Para poder utilizar esta plataforma, se requiere tener Docker y docker-compose instalados en nuestra máquina.

Instala [Docker](https://docs.docker.com/engine/) y [docker-compose](https://docs.docker.com/compose/install/)



## Ejecutar la plataforma en nuestra máquina local

1. En primer lugar, clonamos este repositorio en una carpeta de nuestra máquina y luego vamos a la carpeta clonada.

```
Aquí va el comando git clone
Aquí va el comando cd
```

2. Ejecutamos docker-compose up para descargar todas las imágenes de los servicios a través del motor de Docker en capas, y luego implementamos todos los servicios dentro de la misma red. Probablemente se necesite ejecutarlo con sudo.


```shell
docker-compose up
```
   
3. En caso de que desees tener varios requisitos en tu entorno Jupyter, puedes instalarlos directamente.

```shell
pip install pandas
```

4. Para detener docker-compose, simplemente presionamos ctrl + c (cmd + c en Mac).

5. Para eliminar los contenedores, simplemente ejecutamos:
```shell
docker-compose down
```

## See deployed services online

1. Jupyter
Copiamos el token generado para la aplicación Jupyter de los registros generados cuando se ejecutó `docker-compose`. Ahora necesitamos abrir `localhost:8888` y todo lo almacenado en la carpeta work se mantendrá en nuestra máquina, dentro de la carpeta `data/jupyter`. Esta posibilidad se ha configurado creando volúmenes en la definición de docker-compose.

2. Minio
Vamos a `localhost:9001` para abrir la interfaz de Minio.

3. MLFlow
Vamos a `localhost:5001` para abrir la aplicación web del servidor MLFlow.

4. Base de datos Postgres
No hay una vista web predeterminada implementada con docker-compose, pero siempre podemos descargar la aplicación [PgAdmin](https://www.pgadmin.org/download/) y configurarla utilizando los parámetros de servicio definidos en el archivo docker-compose.yaml.