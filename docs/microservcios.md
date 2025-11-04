# Inventario de Microservicios (02)

> Mantener en actualización. Toda fila sin responsable o sin URL válida se considera **incompleta**.

## Tabla Resumen

| Servicio (ID)  | Descripción breve | Repo URL | Base URL (EC2) | Swagger UI | Responsable | Estado |
|----------------|------------------|----------|----------------|------------|-------------|--------|
| auth-service   | Manejo de login y tokens JWT | https://github.com/org/auth-service | http://<ip>:8081 | http://<ip>:8081/swagger-ui | Nombre Apellido (@github) | En progreso |
| ova-service    | CRUD OVA, módulos, lecciones | https://github.com/org/ova-service | http://<ip>:8082 | http://<ip>:8082/swagger-ui | Nombre Apellido (@github) | En progreso |
| asset-service  | Gestión de archivos (img/pdf/video-url) | https://github.com/org/asset-service | http://<ip>:8083 | http://<ip>:8083/swagger-ui | Nombre Apellido (@github) | Pendiente |
| rating-service | Comentarios / calificaciones | https://github.com/org/rating-service | http://<ip>:8084 | http://<ip>:8084/swagger-ui | Nombre Apellido (@github) | Pendiente |

---

## Detalle por Servicio

### auth-service
- **Responsable:** Nombre Apellido (@github)
- **Repositorio:** https://github.com/org/auth-service
- **Base URL (EC2):** http://<ip>:8081
- **Swagger UI:** http://<ip>:8081/swagger-ui
- **Entidades principales:** Usuario (id, nombre, email, passwordHash, rol)
- **Endpoints mínimos:**
  - `POST /auth/login`
  - `POST /auth/refresh`
- **Checklist:**
  - [ ] Compila local
  - [ ] Health UP
  - [ ] Swagger operativo
  - [ ] Commits diarios

### ova-service
- **Responsable:** Nombre Apellido (@github)
- **Repositorio:** https://github.com/org/ova-service
- **Entidades principales:** OVA, Módulo, Lección
- **Endpoints mínimos:**
  - `POST /api/ova`
  - `GET /api/ova`
  - `GET /api/ova/{id}`
  - `PUT /api/ova/{id}`
  - `DELETE /api/ova/{id}`

### asset-service
- **Responsable:** Nombre Apellido (@github)
- **Repositorio:** https://github.com/org/asset-service

### rating-service
- **Responsable:** Nombre Apellido (@github)
- **Repositorio:** https://github.com/org/rating-service

---

## Responsables (Vista Rápida)

| Rol | Nombre | Usuario GitHub | Observaciones |
|----|--------|----------------|--------------|
| Scrum Master | Nombre | @github | coordinación |
| DevOps | Nombre | @github | puertos y EC2 |
| QA | Nombre | @github | pruebas |
| Servicios | Nombre | @github | Indicar servicio asignado |

---

## Notas de la semana
- Fecha: 2025-XX-XX
- Cambios relevantes:
  - …
- Bloqueos:
  - …
