# Interfaz web

KARU v1 utiliza una interfaz web local como panel principal del dispositivo.

La interfaz está pensada para ejecutarse desde un servidor local en la propia Raspberry Pi, no abriendo directamente el archivo `index.html`.

Esto es necesario porque algunos módulos dependen de funciones del navegador que requieren servir los archivos mediante HTTP.


![Banner](imgs/UI.png)


---

## Motivo del auto-hosting

Abrir `index.html` directamente desde el sistema de archivos puede romper algunas funciones, especialmente las que usan rutas, carga dinámica de archivos o recursos locales.

Por eso, la interfaz debe ejecutarse desde un servidor local.

Ejemplo:

```bash
python3 -m http.server 8000
```

Después se accede desde el navegador:

```text
http://localhost:8000
```

---

## Funciones actuales

La interfaz actual incluye:

- pantalla principal con accesos por módulos
- barra superior fija con hora, fecha, estado online/offline y batería
- navegación interna con botón de volver
- sección de guías
- biblioteca PDF por categorías
- visor PDF integrado mediante PDF.js
- mapa offline mediante Leaflet
- integración prevista con Kiwix
- diseño adaptado a pantalla pequeña táctil

---

## Módulos visibles

Actualmente la interfaz contempla los siguientes módulos:

- Escuchar radio
- Asistente local
- Estación meteo
- Mapa offline
- Guías
- Sistema

Algunos módulos todavía están marcados como pendientes o en fase de prototipo.

---

## Mapa offline

El mapa usa Leaflet y carga tiles locales desde la carpeta del proyecto.

La ruta configurada actualmente es:

```js
maps/base/{z}/{x}/{y}.png
```

Esto permite usar mapas sin conexión siempre que los tiles estén descargados y colocados en la estructura correcta.

---

## Biblioteca PDF

La biblioteca PDF está organizada por categorías.

Cada categoría carga sus documentos mediante un archivo `index.json`.

Categorías actuales:

- Primeros auxilios
- Supervivencia
- Comunicaciones
- Meteorología
- Manuales de uso
- Otros

La interfaz lee estos índices y muestra los documentos disponibles dentro de cada carpeta.

---

## Wiki offline

La sección de wiki está preparada para cargar Kiwix desde un servicio local.

Configuración actual:

```js
http://localhost:8080
```

Esto permite mantener una enciclopedia offline accesible desde KARU.

---

## Decisión técnica

Se ha elegido una interfaz web porque permite:

- desarrollo rápido
- ejecución local
- compatibilidad con pantalla táctil
- separación entre interfaz y servicios internos
- facilidad para añadir nuevos módulos
- uso desde navegador sin entorno gráfico complejo

---

## Estado

Estado actual: en desarrollo.

La base visual y la navegación principal ya están creadas.

Pendiente:

- limpiar textos temporales
- terminar módulos incompletos
- mejorar integración con servicios reales
- preparar arranque automático del servidor local
- adaptar el modo kiosk en Raspberry Pi
