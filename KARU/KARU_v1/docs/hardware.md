# Hardware

KARU v1 está pensado como un cyberdeck portátil basado en Raspberry Pi.

La prioridad inicial es validar el funcionamiento del sistema antes de cerrar un diseño físico definitivo.

---

## Hardware base previsto

- Raspberry Pi 5
- Pantalla táctil
- Almacenamiento microSD
- Almacenamiento SSD
- Módulo RTL-SDR
- Carcasa tipo cyberdeck
- Fuente de alimentación portátil o batería

---


## Raspberry Pi

La Raspberry Pi actúa como unidad principal del sistema.

Debe ejecutar:

- interfaz web local
- navegador en modo kiosk
- visor de documentos
- mapas offline
- wiki offline
- servicios internos

## Componentes actuales

| Objeto | Precio | Descripción |
|---|---:|---|
| Maletín contenedor Peli 1150 | 62,92 € | Maletín rígido usado como carcasa principal del cyberdeck |
| Kit Raspberry Pi 5 | 144,99 € | Raspberry Pi 5 8GB, microSD 64GB, cables HDMI, adaptador de tarjeta, lector de tarjeta, cooler activo, case ABS y transformador USB-C 27W |
| Pantalla IPS 7" 1024x600 | 35,06 € | Pantalla táctil con USB táctil, cable HDMI y tornillos de montaje |

---

## Coste actual

El coste actual del hardware principal es:

```text
242,97 €
```

---

## Pantalla

La interfaz está pensada para una pantalla pequeña táctil.

El diseño actual toma como referencia una resolución aproximada de:

```text
1024x600
```

---

## Radio

La primera versión contempla recepción mediante RTL-SDR.

La transmisión no entra en el alcance inicial de KARU v1.

---

## Almacenamiento

El almacenamiento debe permitir guardar:

- sistema operativo
- interfaz
- mapas offline
- PDFs
- contenido Kiwix
- scripts y servicios

Se contempla microSD para realizar pequeñas pruebas y el SSD como base del producto final.

---

## Pendiente

- definir modelo exacto de pantalla
- definir carcasa
- definir distribución interna
- definir alimentación
- probar consumo real
- documentar montaje físico
