# Inventario de Microservicios (02)

> Mantener en actualización. Toda fila sin responsable o sin URL válida se considera **incompleta**.

## Tabla Resumen

| Servicio (ID)  | Descripción breve | Repo URL | Base URL (EC2) | Swagger UI | Responsable | Estado |
|----------------|------------------|----------|----------------|------------|-------------|--------|
| conjuntos-jni   | Backend OVA Matematicas Discretas | [https://github.com/org/auth-service](https://github.com/Cristian-Daniel-Cardona-Correa/conjuntos-jni) | http://<ip>:8095 | [http://<ip>:8081/swagger-ui](http://localhost:8081/api/conjuntos-jni) | Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa) | Finalizado |
| usuario-service    | Microservicio de usuarios para la lógica del inicio de sesión y guardado en la base de datos | [https://github.com/org/ova-service](https://github.com/Cristian-Daniel-Cardona-Correa/usuario-service) | http://<ip>:8082 | [http://<ip>:8082/swagger-ui](http://localhost:8082/api/usuario-service) | Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa) | Finalizado |
| costos-jni  | OVA Costos y Presupuestos |[ https://github.com/org/asset-service](https://github.com/JuanEstebanCM/ovaCostosPresupuestos) | http://<ip>:8094 | [http://<ip>:8082/swagger-ui](http://localhost:8094/api/costos-jni) | Juan Esteban Castañeda Montaño (@JuanEstebanCM) | Finalizado |
| biseccion-service | Microservicio de Analisis Numerico | [https://github.com/org/rating-service](https://github.com/Jhon1Alexis1Gonzalez1Cardenas/biseccion_service) | http://<ip>:9090 | [http://<ip>:9090/swagger-ui ](http://localhost:9090/api/biseccion_service)| Jhon Alexis Gonzalez Cardenas (@Jhon1Alexis1Gonzalez1Cardenas) | Finalizado |

---

## Detalle por Servicio

### conjuntos-jni (OVA Matematicas Discretas)
- **Responsable:** Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa)
- **Repositorio:** [https://github.com/org/auth-service](https://github.com/Cristian-Daniel-Cardona-Correa/conjuntos-jni)
- **Base URL (EC2):** http://<ip>:8095
- **Swagger UI:** [http://<ip>:8081/swagger-ui](http://localhost:8081/api/conjuntos-jni)
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

### usuario-service
- **Responsable:** Cristian Daniel Cardona Correa (@Cristian-Daniel-Cardona-Correa)
- **Repositorio:** [https://github.com/org/ova-service](https://github.com/Cristian-Daniel-Cardona-Correa/usuario-service)
- **Base URL (EC2):** http://<ip>:8082
- **Swagger UI:** [http://<ip>:8082/swagger-ui](http://localhost:8082/api/usuario-service)
- **Entidades principales:**
    - Entidad Usuario (Long id, String nombre, String email, String password) 
- **Endpoints mínimos:**
  - `GET /api/usuario-service/usuarios`
  - `GET (Buscar por ID) /api/usuario-service/usuarios/2`
  - `POST api/usuario-service/usuarios`
  - `PUT /api/usuario-service/usuarios/4`
  - `POST /api/usuario-service/login`
  - `DELETE api/usuario-service/usuarios/4 (Por ID)`

### costos-jni
- **Responsable:** Juan Esteban Castañeda Montaño (@JuanEstebanCM)
- **Repositorio:** [https://github.com/org/asset-service](https://github.com/JuanEstebanCM/ovaCostosPresupuestos)
- **Base URL (EC2):** http://<ip>:8094
- **Swagger UI:** [http://<ip>:8082/swagger-ui](http://localhost:8094/api/costos-jni)
- - **Entidades principales:**
    - Entidad Ovacostos: cfijo, cvariable, cindirecto, unidades, margen, resultado
- **Endpoints mínimos:**
  - http://localhost:8094/api/costos-jni/calcular

### biseccion-service
- **Responsable:** Jhon Alexis Gonzalez Cardenas (@Jhon1Alexis1Gonzalez1Cardenas)
- **Repositorio:** [https://github.com/org/rating-service](https://github.com/Jhon1Alexis1Gonzalez1Cardenas/biseccion_service)
- **Base URL (EC2):** http://<ip>:9090
- **Swagger UI:** [http://<ip>:9090/swagger-ui ](http://localhost:9090/api/biseccion_service)
- **Entidades principales:**
    - Rest Controller:   ConjuntosRestController (Controlador de la API)
    - Entidades de peticiones (dto):    ConjuntosRequest (DTO que representa la petición para operaciones entre conjuntos),  ElementoEnConjuntoRequest (DTO que representa la petición para verificar si un elemento está en un conjunto)
    - Service:   ConjuntosService (La logica de negocio)
    - Carga la libreria:   JavaConjuntos (Clase que representa las funciones de la biblioteca dinamica JNI)
- **Endpoints mínimos:**
  - `POST /api/biseccion_service/Evaluar`

---

## Responsables (Vista Rápida)

| Rol | Nombre | Usuario GitHub | Observaciones |
|----|--------|----------------|--------------|
| Scrum Master | Santiago Ospina Gonzalez | @Santiago-Ospina-Gonzalez | coordinación |
| Infraestructura y DevOps | Jhon Alexis Gonzalez Cardenas | @Jhon1Alexis1Gonzalez1Cardenas | puertos y EC2 |
| Documentacion y Desarrollo | Juan Esteban Castañeda Montaño | @JuanEstebanCM | pruebas |
| Desarrollo y Front-End | Cristian Daniel Cardona Correa | @Cristian-Daniel-Cardona-Correa | Indicar servicio asignado |
| Documentacion e Infraestructura | Brahian Andres Tenorio Reina | @github | Indicar servicio asignado |

---

## Notas de la semana
- Fecha: 2025-XX-XX
- Cambios relevantes:
  - …
- Bloqueos:
  - …
