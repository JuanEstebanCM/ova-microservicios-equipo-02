# Inventario de Microservicios (02)

> Mantener en actualización. Toda fila sin responsable o sin URL válida se considera **incompleta**.

## Tabla Resumen

| Servicio (ID)  | Descripción breve | Repo URL | Base URL (EC2) | Swagger UI | Responsable | Estado |
|----------------|------------------|----------|----------------|------------|-------------|--------|
| conjuntos-jni   | Backend OVA Matematicas Discretas | [https://github.com/org/auth-service](https://github.com/Cristian-Daniel-Cardona-Correa/conjuntos-jni) | http://<ip>:8095 | [http://<ip>:8081/swagger-ui](http://localhost:8081/api/conjuntos-jni) | Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa) | Finalizado |
| ova-service    | CRUD OVA, módulos, lecciones | https://github.com/org/ova-service | http://<ip>:8082 | http://<ip>:8082/swagger-ui | Nombre Apellido (@github) | En progreso |
| asset-service  | Gestión de archivos (img/pdf/video-url) | https://github.com/org/asset-service | http://<ip>:8083 | http://<ip>:8083/swagger-ui | Nombre Apellido (@github) | Pendiente |
| rating-service | Comentarios / calificaciones | https://github.com/org/rating-service | http://<ip>:8084 | http://<ip>:8084/swagger-ui | Nombre Apellido (@github) | Pendiente |

---

## Detalle por Servicio

### conjuntos-jni
- **Responsable:** Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa)
- **Repositorio:** [https://github.com/org/auth-service](https://github.com/Cristian-Daniel-Cardona-Correa/conjuntos-jni)
- **Base URL (EC2):** http://<ip>:8095
- **Swagger UI:** http://<ip>:8081/swagger-ui
- **Entidades principales:**
- Rest Controller:   ConjuntosRestController (Controlador de la API)
- Entidades de peticiones (dto):    ConjuntosRequest (DTO que representa la petición para operaciones entre conjuntos),  ElementoEnConjuntoRequest (DTO que representa la petición para verificar si un elemento está en un conjunto)
- Service:   ConjuntosService (La logica de negocio)
- Carga la libreria:   JavaConjuntos (Clase que representa las funciones de la biblioteca dinamica JNI)
- **Endpoints mínimos:**
  - `POST /api/conjuntos-jni/union`
  - `POST /api/conjuntos-jni/interseccion`
  - `POST /api/conjuntos-jni/diferencia`
  - `POST /api/conjuntos-jni/esta-en-conjunto`
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
| Scrum Master | Santiago Ospina Gonzalez | @Santiago-Ospina-Gonzalez | coordinación |
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
