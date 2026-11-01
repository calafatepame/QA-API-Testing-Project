# Hallazgos de la API – Users

## 1. Contexto

Durante la ejecución de los casos de prueba sobre el recurso `/users` de JSONPlaceholder se observaron diferencias entre los resultados esperados y las respuestas obtenidas.

Los siguientes hallazgos documentan el comportamiento observado durante la ejecución automatizada con Postman y Newman.

## 2. Hallazgos identificados

### H-01 – Aceptación de solicitudes sin email

- **Caso relacionado:** TC10
- **Método:** POST
- **Resultado esperado:** HTTP 400 y rechazo de la solicitud.
- **Resultado obtenido:** HTTP 201 Created.
- **Comportamiento observado:** La API aceptó la solicitud sin el campo email y devolvió un identificador.

### H-02 – Aceptación de body vacío

- **Caso relacionado:** TC11
- **Método:** POST
- **Resultado esperado:** HTTP 400 y rechazo de la solicitud.
- **Resultado obtenido:** HTTP 201 Created.
- **Comportamiento observado:** La API aceptó la solicitud con body vacío y devolvió un identificador.

### H-03 – Aceptación de email con tipo de dato numérico

- **Caso relacionado:** TC12
- **Método:** POST
- **Resultado esperado:** El campo email debería ser de tipo string.
- **Resultado obtenido:** HTTP 201 Created.
- **Comportamiento observado:** La respuesta conservó el valor numérico enviado en el campo email.

### H-04 – Aceptación de email con formato inválido

- **Caso relacionado:** TC13
- **Método:** POST
- **Resultado esperado:** Rechazo de la solicitud.
- **Resultado obtenido:** HTTP 201 Created.
- **Comportamiento observado:** La API aceptó la solicitud con un email de formato inválido.

### H-05 – Error interno ante JSON malformado

- **Caso relacionado:** TC14
- **Método:** POST
- **Resultado esperado:** HTTP 400 o 422.
- **Resultado obtenido:** HTTP 500 Internal Server Error.
- **Comportamiento observado:** La API respondió con un error interno del servidor ante el JSON malformado.

## 3. Análisis

Los resultados muestran que, durante la ejecución, la API aceptó diferentes solicitudes con datos incompletos o formatos no convencionales.

También se observó una respuesta HTTP 500 ante una solicitud con JSON malformado.

Estos resultados permiten identificar diferencias entre las expectativas de validación definidas para el ejercicio y el comportamiento de la API evaluada.

## 4. Limitaciones

JSONPlaceholder es una API pública de prueba. Por lo tanto, estos hallazgos describen su comportamiento observado y no constit