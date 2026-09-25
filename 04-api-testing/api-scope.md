# API Testing - Alcance
## API
Swagger Petstore
## Alcance funcional
Gestión de mascotas (pet).
## Operaciones seleccionadas
| Método HTTP | Endpoint | Propósito |
|---|---|---|
| POST | /pet | Crear una nueva mascota en la tienda |
| GET | /pet/{petId} | Obtener la información de una mascota por ID |
| PUT | /pet | Actualizar los datos de una mascota existente |
| DELETE | /pet/{petId} | Eliminar una mascota por ID |
## Justificación
Se seleccionó el flujo CRUD principal del recurso `pet` para verificar el ciclo de vida completo de la entidad.
## Condiciones de prueba identificadas
- Creación de mascota con datos válidos.
- Consulta de mascota existente por ID válido.
- Consulta de mascota inexistente (manejo de error 404).
- Actualización exitosa del estado de la mascota.
- Eliminación correcta del recurso.
## Fuera de alcance
- Métodos `/pet/findByStatus` y `/pet/findByTags`.
- Módulos `store` y `user`.
- Pruebas de carga, rendimiento o seguridad.