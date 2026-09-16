# Hoja de Sesión Exploratoria

## INFORMACIÓN DE LA SESIÓN
* **CHARTER (Misión):** Explorar las operaciones POST/PUT/GET de la API Swagger Petstore para validar persistencia y tipos de datos.
* **ÁREAS / AMBIENTE:** API REST (https://petstore.swagger.io/v2/swagger.json) | Navegador Chrome / Thunder Client.
* **INICIO:** 2026-09-16 19:30 | **DURACIÓN:** 45 Minutos
* **TESTER:** Rocío Sánchez/ QA Engineer
## DESGLOSE DE TAREAS (%)
* Setup y Swagger: 20%
* Pruebas en API: 60%
* Documentación: 20%

## ARCHIVOS Y DATOS DE PRUEBA UTILIZADOS
* `swagger.json`
* Payloads JSON con IDs negativos (`-1`) y texto en campos numéricos (`"id": "abc"`)

## NOTAS DE PRUEBA (Log de Exploración)
* **GET /pet/1:** Responde `200 OK` con la mascota correcta.
* **GET /pet/999999:** Responde `404 Not Found` (correcto).
* **POST /pet:** Envié `"id": -5` y respondió `200 OK`. Debería rechazarlo.
* **PUT /pet:** Al actualizar sin enviar el campo `name`, borra el nombre anterior sin avisar.

## LISTA DE RIESGOS IDENTIFICADOS
* Entradas de datos no validadas en el backend.

## DEFECTOS (BUGS)
* **BUG-01:** `POST /pet` permite crear mascotas con IDs negativos (retorna `200 OK` en vez de `400 Bad Request`).

## INCIDENTES Y PREGUNTAS (ISSUES)
* ¿Cuál es el límite máximo de caracteres permitido para el nombre de la mascota?