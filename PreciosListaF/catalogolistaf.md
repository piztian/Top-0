# 📦 Catálogo Dinámico Celucenter - Lista F

Esta segunda versión del catálogo usa la misma estructura HTML y las mismas imágenes de productos en GitHub, pero toma los precios y características desde una **nueva pestaña** del Google Sheets: `"Lista F"`.

---

## 🌐 Fuente de datos

Esta versión utiliza:

- 📄 **Google Sheets:**  
  [https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM](https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM)

- 📑 **Pestaña:** `"Lista F"`

- 🔗 **API JSON (opensheet):**  


---

## 🖼️ Imágenes

Las imágenes están alojadas en:

👉 [Repositorio GitHub](https://github.com/piztian/Top-0/tree/main/pics)

Cada fila del catálogo debe tener la columna `url_imagen` apuntando al enlace directo como:


---

## 🔧 Columnas esperadas en “Lista F”

| Columna       | Descripción                                |
|---------------|--------------------------------------------|
| archivo       | Nombre del archivo de imagen (ej. `Moto G24.jpg`) |
| url_imagen    | URL directa a la imagen                    |
| Precio        | Precio visible en la etiqueta              |
| Caracteristicas | Descripción corta del equipo              |

---

## 🧪 Fragmento de código JS modificado

Solo cambia el `fetch()` del HTML por este:

```js
fetch("https://opensheet.elk.sh/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM/Lista%20F")
✅ Ventajas

## Puedes cambiar precios sin tocar el HTML. ## 

Puedes generar diferentes catálogos con solo duplicar el fetch() y usar distintas pestañas del mismo Google Sheets.

Centralizas imágenes en GitHub y datos en la nube.

🧠 Tip
Puedes duplicar el mismo HTML, solo cambiando el nombre de la pestaña en el fetch, y ya tienes catálogos independientes para distintas campañas o promociones.
