# QA API Testing Project – Users Endpoint

## Descripción General

Proyecto práctico de Testing de APIs orientado a validar funcionalidades, manejo de errores y calidad de respuestas sobre el endpoint público: 

https://jsonplaceholder.typicode.com/users

El objetivo principal fue aplicar buenas prácticas de QA Testing utilizando Postman, Newman, Jira, GitHub y criterios de diseño de pruebas funcionales y negativas.

## Objetivos del Proyecto

- Validar el comportamiento funcional de endpoints REST.
- Diseñar y ejecutar casos de prueba positivos y negativos.
- Detectar defectos funcionales.
- Automatizar validaciones básicas con Postman Tests.
- Ejecutar la colección desde línea de comandos con Newman.
- Generar evidencia de ejecución profesional.
- Simular un flujo real de trabajo QA.

## Herramientas Utilizadas

- Postman
- Newman
- GitHub
- GitHub Actions
- Jira
- JSONPlaceholder API

## Alcance de Pruebas

Se realizaron validaciones sobre:

- Status Codes
- Tiempo de respuesta
- Estructura JSON
- Campos obligatorios
- Tipos de datos
- Recursos inexistentes
- Inputs inválidos
- Manejo de errores
- Escenarios negativos
- Valores límite

## Casos de Prueba Ejecutados

## ID                      Caso de Prueba

- TC01   Obtener todos los usuarios 
- TC02   Obtener usuario por ID válido 
- TC03   Obtener usuario inexistente 
- TC04   Obtener usuario con formato de ID inválido 
- TC05   Obtener usuario con valor límite ID = 0 
- TC06   Obtener usuario con ID negativo 
- TC07   Obtener usuario con ID decimal 
- TC08   Obtener usuarios sin parámetro ID 
- TC09   Crear usuario con datos válidos 
- TC10   Crear usuario sin email 
- TC11   Crear usuario con body vacío 
- TC12   Crear usuario con tipos de datos inválidos 
- TC13   Crear usuario con formato de email inválido 
- TC14   Crear usuario con body JSON mal formado 
- TC15   Crear usuario con campos requeridos vacíos 
- TC16   Crear usuario con valor de nombre muy largo 


## Defectos Detectados

## ID                        Descripción

-BUG-01                 La API acepta formato de email inválido
-BUG-02                 La API acepta body vacío
-BUG-03                 La API acepta tipos de datos incorrectos
-BUG-04                 La API acepta formato de email inválido
-BUG-05                 La API devuelve 500 en lugar de 400 Bad Request cuando se envía JSON mal formado 

Nota: Algunos comportamientos son esperables al tratarse de una Mock API.

## Automatización

Se implementaron validaciones automáticas con Postman Tests y ejecución por línea de comandos con Newman.

Validaciones automáticas incluidas:

- Status code esperado
- Tiempo de respuesta
- Campos requeridos
- Tipo de dato
- Estructura de respuesta
- Respuesta no vacía

## Ejecución Local con Newman

Para ejecutar la colección desde la terminal:

```bash
newman run "collection/Users API Testing.postman_collection.json"


## Evidencia de Ejecución

El proyecto incluye evidencia de ejecución automática con Newman en carpeta:

- /evidence
- /screenshots


## Técnicas de Testing Aplicadas

- Equivalence Partitioning
- Boundary Value Analysis
- Negative Testing
- Functional Testing
- Exploratory Testing

## Aprendizajes Obtenidos

- Testing de APIs REST con Postman.
- Automatización básica con Newman.
- Diseño profesional de casos de prueba.
- Detección y documentación de defectos.
- Validación de respuestas JSON.
- Pensamiento crítico orientado a calidad.

## Habilidades Demostradas

- API Testing
- Postman
- Newman
- Bug Reporting
- Test Case Design
- QA Analysis
- REST APIs
- JSON Validation

## Autor

Proyecto desarrollado como práctica profesional de formación en Quality Assurance orientado a posiciones QA Tester Jr / QA Analyst Jr en Argentina.
