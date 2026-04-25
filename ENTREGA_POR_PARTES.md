# Entrega por partes - Switch Admin Platform

Este proyecto fue dividido en tres ZIP para evitar errores de descarga.

## Partes
1. `01_backend_api.zip`: backend FastAPI + PostgreSQL + usuarios, roles y permisos.
2. `02_frontend_element_plus_admin.zip`: frontend migrado a Vue Element Plus Admin.
3. `03_deploy_docker_docs.zip`: Docker Compose, README, MkDocs y documentación.

## Instalación rápida
Descomprimir las tres partes dentro de `/opt/switch-admin-platform` y ejecutar:

```bash
cd /opt/switch-admin-platform
docker compose down
docker compose build --no-cache
docker compose up -d
docker exec -it switch-backend python create_admin.py
```

Usuario inicial:

```txt
admin
Admin123*
```

## Correcciones incluidas
- `backend/app/core/config.py` usa `from pydantic_settings import BaseSettings`.
- `backend/requirements.txt` incluye `pydantic-settings` y `bcrypt==4.0.1`.
- Se agregaron módulos de usuarios, roles y permisos.
