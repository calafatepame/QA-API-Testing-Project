# Plan de Pruebas – Users API

## 1. Información general

| Campo | Descripción |
|---|---|
| Proyecto | QA API Testing Project |
| API bajo prueba | JSONPlaceholder |
| Recurso | Users |
| Endpoint principal | `https://jsonplaceholder.typicode.com/users` |
| Métodos HTTP | GET y POST |
| Herramientas | Postman, Newman y GitHub Actions |
| Tipo de pruebas | Funcionales, positivas, negativas y validaciones de respuesta |

## 2. Objetivo

Verificar el comportamiento del recurso Users de la API JSONPlaceholder mediante pruebas funcionales sobre los métodos GET y POST.

Se busca validar los códigos de estado HTTP, la estructura y los tipos de datos de las respuestas, la presencia de campos y los tiempos de respuesta.

También se busca automatizar la ejecución de los casos de prueba mediante Postman y Newman, e integrar su ejecución en un flujo de CI/CD con GitHub Actions.

## 3. Alcance

### Incluido

- Consultar el listado de usuarios mediante GET.
- Consultar usuarios por identificador.
- Enviar solicitudes con identificadores inexistentes o formatos inválidos.
- Crear usuarios mediante POST.
- Enviar solicitudes con datos incompletos, vacíos o con formatos y tipos de datos no convencionales.
- Validar códigos de estado HTTP.
- Verificar estructura, propiedades y tipos de datos de las respuestas.
- Comprobar tiempos de respuesta.
- Automatizar la ejecución de las pruebas.

### Fuera del alcance

- Pruebas de autenticación y autorización.
- Pruebas de carga y rendimiento avanzado.
- Pruebas de seguridad.
- Persistencia real de los usuarios creados.
- Validaciones de interfaz de usuario.

## 4. Estrategia de pruebas

Se utilizaron las siguientes técnicas:

- **Pruebas funcionales:** verificación del comportamiento de los endpoints.
- **Pruebas positivas:** envío de solicitudes con datos válidos.
- **Pruebas negativas:** envío de identificadores o datos no válidos, incompletos o inesperados.
- **Validación de respuestas:** comprobación de códigos HTTP, estructura JSON, propiedades y tipos de datos.
- **Análisis de límites:** exploración de valores como identificadores cero, negativos y decimales.
- **Pruebas automatizadas:** ejecución de aserciones mediante scripts de Postman y Newman.

## 5. Entorno y herramientas

| Elemento | Descripción |
|---|---|
| API | JSONPlaceholder |
| Entorno | API pública de pruebas |
| Cliente HTTP | Postman |
| Ejecutor de pruebas | Newman |
| Automatización | GitHub Actions |
| Formato de intercambio | JSON |
| Protocolo | HTTP/HTTPS |

## 6. Criterios de entrada

- Disponibilidad del endpoint de la API.
- Colección de Postman configurada.
- Casos de prueba definidos.
- Newman instalado y operativo para la ejecución local.

## 7. Criterios de salida

- Ejecución de los casos de prueba definidos.
- Registro de resultados obtenidos.
- Identificación y documentación de diferencias entre resultados esperados y observados.
- Disponibilidad de evidencias de ejecución.

Los resultados se documentan independientemente de que las aserciones hayan sido aprobadas o fall