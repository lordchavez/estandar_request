# Estándares de solicitud para la API de Tienda

## Descripción general
Este documento describe los estándares para el diseño de los endpoints de la API y las estructuras de solicitud del proyecto `api_tienda`. El cumplimiento de estos estándares garantiza la coherencia, la claridad y la facilidad de uso para los consumidores de la API.

## Diseño de endpoints

### URL base (base path)
Todos los endpoints de la API tendrán el prefijo `/api/v1`. Por ejemplo:

``` http://localhost:8080/api/v1/products```

### Nomenclatura de recursos

- Utilice sustantivos en plural para los nombres de los recursos (p. ej., `/products`, `/orders`).
- Utilice minúsculas y separe las palabras con guiones (p. ej., `/product-categories`).

### Métodos HTTP
- **GET**: Recuperar recursos.
- **POST**: Crear un nuevo recurso.
- **PUT**: Actualizar un recurso existente.
- **DELETE**: Eliminar un recurso.

### Ejemplos de endpoints
- `GET /api/v1/products`: Recuperar una lista de productos.
- `GET /api/v1/products/{id}`: Recuperar un producto específico por su ID.
- `POST /api/v1/products`: Crear un nuevo producto.
- `PUT /api/v1/products/{id}`: Actualizar un producto existente.
- `DELETE /api/v1/products/{id}`: Eliminar un producto.

## Estructura de la solicitud

### Encabezados
- **Content-Type**: Debe establecerse en `application/json` para solicitudes JSON.

- **Accept**: Debe establecerse en `application/json` para especificar el formato de respuesta.

### Cuerpo de la solicitud
```json
{
  "name": "Product Name",
  "description": "Product Description",
  "price": 99.99,
  "quantity": 10
}
```

### Query Params
Utilice query Params para filtrar, ordenar y paginar. Por ejemplo:

- `GET /api/v1/products?sort=price&order=asc&page=1&size=10`

## Validación
- Valide los datos de las solicitudes entrantes mediante anotaciones (p. ej., `@NotNull`, `@Size`) en las clases DTO.

- Devuelva respuestas de error adecuadas para las solicitudes no válidas.

## Control de versiones
- Incluya el versionado de la API en la URL (p. ej., `/api/v1/`).
- Incremente el número de versión para los cambios que rompen la compatibilidad.

## Conclusión
Seguir estos estándares de solicitud ayudará a mantener una API limpia y fácil de usar para el proyecto `api_tienda`, lo que facilitará a los desarrolladores la integración y el uso de los servicios proporcionados.