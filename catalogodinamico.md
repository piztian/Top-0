# 📱 Catálogo Celucenter - Generación Dinámica con Google Sheets y GitHub

Este archivo HTML genera automáticamente un catálogo visual de productos usando datos cargados desde una hoja de Google Sheets y las imágenes almacenadas en GitHub.

---

## 🧩 ¿Cómo funciona?

1. **Google Sheets como fuente de datos**

   El HTML consume datos desde esta hoja de cálculo pública:
   
   👉 [Top Equipos - Google Sheet](https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM/edit#gid=1821912591)

   El archivo es accedido vía JSON usando el servicio gratuito `opensheet.elk.sh`:

https://opensheet.elk.sh/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM/Top%20Equipos 


2. **Estructura esperada del Sheet**

La hoja debe contener las siguientes columnas exactas:

- `archivo` → nombre del archivo de la imagen (`Blu G74.jpg`)
- `url_imagen` → enlace directo a la imagen (por ejemplo desde GitHub)
- `Precio` → texto del precio a mostrar (ej: `$2,990`)
- `Caracteristicas` → descripción breve del producto

3. **Imágenes desde GitHub**

Las imágenes están alojadas públicamente en este repositorio:

👉 [Repositorio GitHub: Top-0](https://github.com/piztian/Top-0/tree/main/pics)

Los links a imágenes se colocan directamente en la columna `url_imagen`.

---

## 🖥 Código principal

El script de JavaScript usa `fetch()` para obtener los datos del sheet y renderiza cada producto en una tarjeta `.card` con:

- imagen
- precio
- marca (extraída del nombre del archivo)
- modelo (nombre sin extensión)
- características

---

## ✅ Ventajas

- No necesitas actualizar el HTML manualmente.
- Basta con modificar los datos en la hoja de cálculo.
- Las imágenes se mantienen centralizadas en GitHub.

---

## 🔐 Requisitos

- La hoja debe estar **publicada en la web** (`Archivo → Compartir → Publicar en la Web`) para que `opensheet.elk.sh` pueda leerla.
- Las imágenes deben estar disponibles vía enlace directo.

---

## 🚀 Personalización

Puedes cambiar estilos en el `<style>` o modificar qué columnas se muestran desde el JavaScript.

---

## 🧠 Recursos

- [opensheet.elk.sh](https://opensheet.elk.sh/)
- [Google Sheets Docs](https://support.google.com/docs)
- [GitHub: piztian/Top-0](https://github.com/piztian/Top-0)

