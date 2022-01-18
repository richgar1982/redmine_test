# Clone el repositorio

Clone el repositorio usando el siguiente comando: 
```console
$ git clone https://github.com/richgar1982/redmine_test.git
```

Modifica el archivo 

```yml
services:
...
  redmine:
    environment:
      REDMINE_DB_MYSQL: db 
      REDMINE_DB_PASSWORD: example # Cambia el password
      REDMINE_SECRET_KEY_BASE: supersecretkey # Cambia la clave secreta 
...
  db:
    environment:
      MYSQL_ROOT_PASSWORD: example # El password debe coincidir con el del Redmine
      MYSQL_DATABASE: redmine # Nombre de la BD a crear 
```

# Configuración de Redmine
 
 Entre a la carpeta donde se encuentra el archivo `docker-compose.yml`. Allí corra el siguiente comando: 

 ```console
$ docker-compose up
 ```

 Al terminar se tendrán dos contenedores: 
  
  - El del redmine en el puerto 80. Se puede acceder con http://localhost
  - El mysql en el puerto 3306. Se puede acceder mediante un cliente SQL 