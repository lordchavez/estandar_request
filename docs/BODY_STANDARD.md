# Estándar de cuerpos de request (JSON)

Este documento complementa `ESTANDAR_REQUEST.md` y define cómo deben estructurarse
los cuerpos (`body`) de las peticiones HTTP.

## Convenciones generales

- Formato JSON.
- Campos en `camelCase`.
- Evitar enviar campos nulos innecesarios.
- Mantener diferencias claras entre campos obligatorios y opcionales.

## Ejemplo de cuerpo para creación de producto

```json
{
  "name": "Laptop XYZ",
  "description": "Laptop de ejemplo para el estándar",
  "price": 19999.99,
  "currency": "MXN",
  "stock": 10,
  "categoryId": "electronics"
}
```

## Ejemplo de cuerpo para actualización parcial (PATCH)

```json
{
  "price": 18999.99,
  "stock": 8
}
```

Usa estos ejemplos como referencia cuando definas DTOs o modelos de entrada.
