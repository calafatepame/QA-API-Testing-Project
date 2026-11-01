# Casos de Prueba – Users API

## 1. Información general

Los siguientes casos de prueba corresponden al recurso `/users` de JSONPlaceholder y están organizados según los métodos HTTP GET y POST.

Los casos se ejecutaron mediante una colección de Postman y se automatizaron con Newman.

## 2. Casos de prueba – GET

| ID | Escenario | Resultado esperado | Resultado obtenido |
|---|---|---|---|
| TC01 | Consultar listado de usuarios | HTTP 200 y respuesta en formato array | Aprobado |
| TC02 | Consultar usuario con ID válido | HTTP 200 y datos del usuario | Aprobado |
| TC03 | Consultar usuario inexistente (ID 999) | HTTP 404 | Aprobado |
| TC04 | Consultar usuario con ID alfabético | HTTP 404 | Aprobado |
| TC05 | Consultar usuario con ID 0 | HTTP 404 | Aprobado |
| TC06 | Consultar usuario con ID negativo | HTTP 404 | Aprobado |
| TC07 | Consultar usuario con ID decimal | HTTP 404 | Aprobado |
| TC08 | Consultar endpoint sin ID | HTTP 200 y listado de usuarios | Aprobado |

## 3. Casos de prueba – POST

| ID | Escenario | Resultado esperado | Resultado obtenido |
|---|---|---|---|
| TC09 | Crear usuario con datos válidos | HTTP 201 y datos del usuario creado | Aprobado |
| TC10 | Crear usuario sin email | HTTP 400 y rechazo de la solicitud | HTTP 201. La API aceptó la solicitud sin email |
| TC11 | Crear usuario con body vacío | HTTP 400 y rechazo de la solicitud | HTTP 201. La API aceptó la solicitud |
| TC12 | Enviar email con tipo de dato numérico | El campo email debería ser de tipo string | HTTP 201. La respuesta conservó el valor numérico |
| TC13 | Enviar email con formato inválido | Rechazo de la solicitud y ausencia de creación | HTTP 201. La API aceptó la solicitud |
| TC14 | Enviar JSON malformado | HTTP 400 o 422 | HTTP 500 Internal Server Error |
| TC15 | Enviar campos obligatorios vacíos | La colección espera HTTP 201 y acepta el nombre vacío | HTTP 201. Se recibió el nombre vacío |
| TC16 | Enviar nombre de longitud extensa | HTTP 201 y respuesta con nombre de tipo string | HTTP 201. La solicitud fue aceptada |

## 4. Consideraciones sobre los resultados

- Los resultados corresponden a una ejecución de la colección contra JSONPlaceholder.
- Los casos TC10, TC11, TC12, TC13 y TC14 presentaron diferencias respecto de las validaciones esperadas.
- TC15 y TC16 verifican la aceptación de los datos enviados; no comprueban que la API rechace campos vacíos o nombres extensos.
- Una aserción fallida representa una diferencia entre el comportamiento observado y la expectativa definida en el script de prueba.

## 5. Trazabilidad

Los casos están implementados en la colección:

`collection/users-api-testing.postman_collection.json`

La ejecución automatizada se realiza mediante Newman.
