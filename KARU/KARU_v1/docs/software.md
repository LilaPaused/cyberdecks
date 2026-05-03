# Software

KARU v1 utiliza una arquitectura sencilla basada en servicios locales.

La idea es que la Raspberry Pi ejecute la interfaz y los módulos necesarios sin depender de conexión a internet.

---

## Base del sistema

El sistema está pensado para ejecutarse sobre Raspberry Pi OS o una distribución Linux compatible con Raspberry Pi.

Componentes principales:

- navegador en modo kiosk
- servidor web local
- interfaz HTML/CSS/JavaScript
- Leaflet para mapas offline
- PDF.js para visor de documentos
- Kiwix para wiki offline
- servicios locales para futuros módulos

---

## Interfaz

La interfaz principal es web y se sirve desde la propia Raspberry Pi.

No está pensada para abrirse directamente como archivo local, ya que algunas funciones dependen de HTTP, rutas relativas y carga dinámica de archivos.

Ejemplo de ejecución:

```bash
python3 -m http.server 8000
```

Acceso:

```text
http://localhost:8000
```

---

## Servicios previstos

- servidor web local para la interfaz
- Kiwix en `localhost:8080`
- servicio para lectura de estado del sistema
- posible servicio para radio RTL-SDR
- posible servicio para asistente local

---

## Estructura prevista

```text
KARU_v1/
├── README.md
├── docs/
├── src/
│   └── web-ui/
├── media/
└── assets/
```

---

## Estado

Actualmente la parte más avanzada es la interfaz web.

Pendiente:

- definir arranque automático
- definir estructura final de servicios
- integrar información real del sistema
- documentar instalación completa en Raspberry Pi
