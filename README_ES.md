QA API Testing Project – Users Endpoint
Descripción General
Proyecto práctico de Testing de APIs orientado a validar funcionalidades, manejo de errores y calidad de respuestas sobre el endpoint público:
https://jsonplaceholder.typicode.com/users
El objetivo principal fue aplicar buenas prácticas de QA Testing utilizando Postman, Newman y criterios de diseño de pruebas funcionales y negativas.

Objetivos del Proyecto
Validar comportamiento funcional de endpoints REST.
Diseñar casos de prueba positivos y negativos.
Detectar defectos funcionales.
Automatizar validaciones básicas.
Generar evidencia de ejecución profesional.
Simular flujo real de trabajo QA.

Herramientas Utilizadas
Postman
Newman
GitHub
Jira (reporte de bugs)
JSONPlaceholder API

Alcance de Pruebas
Se realizaron validaciones sobre:
Status Codes
Tiempo de respuesta
Estructura JSON
Campos obligatorios
Tipos de datos
Recursos inexistentes
Inputs inválidos
Manejo de errores
Escenarios negativos
Valores límite

Casos de Prueba Ejecutados
ID
Caso de Prueba
TC01
Obtener todos los usuarios
TC02
Obtener usuario por ID válido
TC03
Obtener usuario inexistente
TC04
ID con formato inválido
TC05
Valor límite ID = 0
TC06
ID negativo
TC07
ID decimal
TC08
ID vacío
TC09
Crear usuario con datos válidos
TC10
Email inválido
TC11
Body vacío
TC12
Tipos de datos inválidos


Defectos Detectados
ID
Descripción
BUG-01
La API acepta formato de email inválido
BUG-02
La API acepta body vacío
BUG-03
La API acepta tipos de datos incorrectos
BUG-04
JSON malformado devuelve éxito en lugar de error

Nota: Algunos comportamientos son esperables al tratarse de una Mock API.

Automatización
Se implementaron validaciones automáticas con Postman Tests y ejecución por línea de comandos con Newman.
Validaciones automáticas incluidas:
Status code esperado
Tiempo de respuesta
Campos requeridos
Tipo de dato
Respuesta no vacía

Evidencia de Ejecución
El proyecto incluye evidencia de ejecución automática con Newman en carpeta:
/evidence
/screenshots


Técnicas de Testing Aplicadas
Equivalence Partitioning
Boundary Value Analysis
Negative Testing
Functional Testing
Exploratory Testing

Aprendizajes Obtenidos
Testing de APIs REST con Postman.
Automatización básica con Newman.
Diseño profesional de casos de prueba.
Detección y documentación de defectos.
Validación de respuestas JSON.
Pensamiento crítico orientado a calidad.

Habilidades Demostradas
API Testing
Postman
Newman
Bug Reporting
Test Case Design
QA Analysis
REST APIs
JSON Validation

Autor
Proyecto desarrollado como práctica profesional de formación en Quality Assurance orientado a posiciones QA Tester Jr / QA Analyst Jr en Argentina.
