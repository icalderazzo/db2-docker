# DB2 Docker
Este repositorio contiene manifiestos de IBM DB2 `docker-compose` para Windows, Mac y Linux.

Para configurar DB2 ejecutar desde la raiz
```
docker compose -f ./db2/<archivo-correspondiente> up -d
```

Una vez se complete la instalación, podrás acceder al contenedor ejecutando el siguiente comando desde una terminal
```
docker exec -ti db2 bash -c "su db2inst1"
```

### Recursos creados
* Base de datos `TESTDB`
* Usuario `db2inst1` - Password: `password`

## Backup
El deploy de DB2 permite cargar backups desde su máquina host. Para ello, es necesario crear un directorio `/backups` en la raiz del repositorio y se montará el volumen (y sus archivos) dentro del contenedor en el directorio `/home/db2inst1/backups`
