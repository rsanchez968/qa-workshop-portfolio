# API Testing Casos de prueba

## Caso API-01
**Objetivo:** Crear una nueva mascota con datos válidos
**Operación y endpoint:** POST /pet
**Precondiciones:** Ninguna
**Datos de entrada:** 
`{"id": 889901, "name": "Rocco_Win11", "status": "available"}`
**Resultado esperado:** HTTP 200 OK, respuesta con la mascota creada y el mismo ID
**Resultado obtenido:** Pendiente de ejecución
**Evidencia:** `![API-01](evidence/API-01.png)`

## Caso API-02
**Objetivo:** Consultar la mascota recién creada por su ID
**Operación y endpoint:** GET /pet/889901
**Precondiciones:** La mascota con ID 889901 debe existir
**Datos de entrada:** `petId`: 889901
**Resultado esperado:** HTTP 200 OK con los datos de la mascota "Rocco_Win11"
**Resultado obtenido:** Pendiente de ejecución
**Evidencia:** `![API-02](evidence/API-02.png)`

## Caso API-03
**Objetivo:** Consultar una mascota no existente
**Operación y endpoint:** GET /pet/9999999999
**Precondiciones:** El ID no debe existir en la base de datos
**Datos de entrada:** `petId`: 9999999999
**Resultado esperado:** HTTP 404 Not Found
**Resultado obtenido:** Pendiente de ejecución
**Evidencia:** `![API-03](evidence/API-03.png)`

## Caso API-04
**Objetivo:** Eliminar la mascota creada por su ID
**Operación y endpoint:** DELETE /pet/889901
**Precondiciones:** La mascota con ID 889901 debe existir
**Datos de entrada:** `petId`: 889901
**Resultado esperado:** HTTP 200 OK indicando eliminación exitosa
**Resultado obtenido:** Pendiente de ejecución
**Evidencia:** `![API-04](evidence/API-04.png)`
# Conclusiones

## Resultados relevantes
Se verificó el comportamiento del ciclo CRUD básico sobre el recurso pet, confirmando la persistencia y eliminación correcta de los datos en un entorno público

## Limitaciones
Al ser un entorno público y compartido, algunos IDs pueden sobreescribirse o eliminarse por otros usuarios durante la ejecución

## Pruebas adicionales
Si se contara con más tiempo, se evaluarían validaciones de tipos de datos en el payload (ej. IDs alfanuméricos) y pruebas de carga ligeras
