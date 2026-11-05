# Ticketera 58 mm

Editor web para diseñar e imprimir tickets en impresoras térmicas de 58 mm (probado con una POS‑5890K).

**Úsala en línea:** se publica con GitHub Pages desde la rama `main`.

## Qué hace

- Bloques de **texto**, **filas** (producto / precio), **logos o imágenes**, **ASCII**, **separadores**, **espacios** y **QR**.
- **Galería ASCII**: emojis, kaomoji, comida, Guatemala, música y criaturas originales.
- Vista previa exacta en 1 bit a 384 px (48 mm imprimibles a 203 dpi).
- Todo se imprime como imagen, así que tildes, ñ y cualquier símbolo salen igual que en pantalla.
- Comodines `{fecha}`, `{hora}` y `{dia}`.
- Guarda y abre diseños en `.json`.

## Cómo imprimir

| Situación | Botón |
|---|---|
| Driver POS‑58 instalado (Windows) | **Imprimir**: papel 58 mm, márgenes ninguno, escala 100 % |
| Sin driver (Mac, Linux, Android con Chrome) | **USB directo** → **Imprimir directo** (ESC/POS) |
| Salen símbolos raros | Velocidad **Lenta** o modo **Compatible (ESC \*)**; apaga y prende la impresora |

La impresión directa usa WebUSB / Web Serial / Web Bluetooth: funciona en Chrome o Edge, desde `https://` (GitHub Pages) o `http://localhost`.

## Estructura

Un solo archivo, `index.html`, sin compilación. Carga fuentes de Google Fonts y la librería `qrcode-generator` desde cdnjs (sin internet se usan fuentes del sistema y el QR no se dibuja).
