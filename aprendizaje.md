Diario de Aprendizaje — Mini Tasks

## Sesión 1 y 2: Introducción y Contexto
- **Estructura del proyecto:** Configuración inicial del entorno Spring Boot con Maven, separando correctamente las capas (Controlador, Servicio, Repositorio y Dominio).
- **Decisiones técnicas:** Uso de clases tradicionales para entidades JPA (necesarias por el constructor vacío y la mutabilidad que requiere Hibernate) frente a los records para DTOs.

## Sesión 3: Pruebas con TDD y MockMvc
- **Pruebas unitarias y de integración:** Uso de `@WebMvcTest` para aislar la capa web y comprobar los códigos de estado HTTP (`200 OK`, `201 Created`, `404 Not Found`, `400 Bad Request`).
- **Ciclo TDD aplicado a `GET /v1/tasks/{id}`:**
  - *Rojo:* Creación del test unitario llamando a un ID inexistente o existente antes de implementar la ruta, observando el fallo (`404` inesperado o excepción).
  - *Verde:* Implementación mínima en el controlador (`TaskControllerV1`) buscando en la lista en memoria y devolviendo la respuesta adecuada.
