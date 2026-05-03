# Mapa offline

KARU v1 incluye un módulo de mapa offline basado en Leaflet.

El objetivo es poder visualizar mapas locales sin depender de conexión a internet.

---

## Funcionamiento

El mapa carga tiles locales desde la estructura del proyecto.

Ruta configurada actualmente:

```js
maps/base/{z}/{x}/{y}.png
```

Esto significa que los tiles deben estar organizados por nivel de zoom, columna y fila.

---

## Configuración actual

La configuración base del mapa define:

- centro inicial
- zoom inicial
- zoom mínimo
- zoom máximo
- carga de tiles locales
- controles táctiles
- botones manuales de zoom

---

## Uso previsto

El usuario debe poder:

- abrir el módulo de mapa
- moverse por el mapa
- hacer zoom
- consultar mapas sin conexión
- usarlo desde pantalla táctil

---

## Motivo del servidor local

El mapa debe servirse desde HTTP local para evitar problemas con rutas y carga de recursos.

No se recomienda abrir la interfaz directamente desde `index.html`.

---

## Pendiente

- probar tiles reales
- validar rendimiento en Raspberry Pi
- mejorar zoom táctil
- definir zonas descargadas
- documentar proceso de generación de tiles
