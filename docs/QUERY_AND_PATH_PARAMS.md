# Estándar de query params y path params

Este documento define cómo estructurar y nombrar los parámetros en URL.

## Path params

- Usar nombres claros y en singular cuando se refiera a un recurso concreto.
- Ejemplo: `/api/v1/products/{productId}`

## Query params

- Usar `camelCase` y nombres descriptivos.
- Usar la convención de paginación estándar cuando aplique:
  - `page`, `size`, `sort`, `order`.

### Ejemplo de URL con query params

```http
GET /api/v1/products?page=1&size=10&sort=price&order=asc
```
