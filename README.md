# MySQL Docker Compose Setup

Este proyecto permite levantar rápida y cómodamente un contenedor MySQL utilizando **Docker Compose**.

---

## Puesta en marcha

Para iniciar el servicio en segundo plano:

```bash
docker compose up -d
```

Esto descargará la imagen de MySQL (si no está ya en tu máquina) y levantará el contenedor con la configuración definida en `docker-compose.yml`.

---

## Acceder a MySQL desde el contenedor

Para entrar al cliente MySQL de forma interactiva dentro del contenedor:

```bash
docker exec -it mysql-container mysql -u root -p
```

Se te pedirá la contraseña configurada en la variable `MYSQL_ROOT_PASSWORD`.
Se podrá realizar acciones desde el cliente de terminal de mySQL

---

## Estructura

```
.
└── docker-compose.yml
```

---

## Notas

* Puedes modificar las variables de entorno del servicio MySQL según tus necesidades.
* El volumen `mysql-data` asegura que los datos persistan aunque el contenedor se elimine.
