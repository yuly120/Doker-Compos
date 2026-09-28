# Práctica Docker - PostgreSQL y pgAdmin

## Descripción

Práctica de instalación y configuración de PostgreSQL y pgAdmin utilizando Docker Compose.

El proyecto utiliza dos contenedores:

- PostgreSQL 16
- pgAdmin 4

## Servicios

### PostgreSQL

- Imagen: `postgres:16`
- Contenedor: `contenedor_db_prestamos`
- Base de datos: `bd_prestamos`
- Usuario: `usuario`
- Puerto: `5433`

### pgAdmin

- Imagen: `dpage/pgadmin4`
- Contenedor: `contenedor_admin_prestamos`
- Puerto: `8081`
- Correo: `admin@ejemplo.com`

## Red

Los contenedores utilizan la red `red_prestamos`.

## Ejecución

```bash
docker compose up -d
docker ps
```

Para detener los contenedores:

```bash
docker compose down
```

## Acceso a pgAdmin

Abrir: `http://localhost:8081`

- Correo: `admin@ejemplo.com`
- Contraseña: `admin`

## Conexión a PostgreSQL desde pgAdmin

- Host: `db_prestamos`
- Puerto: `5432`
- Usuario: `usuario`
- Contraseña: `password123`
- Base de datos: `bd_prestamos`

## Base de datos

Se creó la base de datos `bd_prestamos` y una tabla llamada `prestamos`.

Columnas:

- `id_prestamo`
- `nombre_usuario`
- `libro`
- `fecha_prestamo`

## Tecnologías utilizadas

- Docker
- Docker Compose
- PostgreSQL 16
- pgAdmin 4
