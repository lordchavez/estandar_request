# Estándar de headers y autenticación

Este documento define los headers mínimos que deben enviarse en las
peticiones de los microservicios.

## Headers requeridos

- `Content-Type: application/json; charset=utf-8`
- `Accept: application/json`
- `Authorization: Bearer <token>` (cuando aplique)
- `X-Correlation-Id: <uuid>` (opcional pero recomendado)

## Ejemplo

```http
POST /api/v1/products HTTP/1.1
Host: api.miempresa.com
Content-Type: application/json; charset=utf-8
Accept: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
X-Correlation-Id: 8f14e45f-ea9c-4f28-8bb2-123456789abc
```
