# 📦 Catálogo Dinámico Celucenter - Lista F (CriShop)

Este catálogo dinámico genera una galería visual de productos a partir de una hoja de cálculo de Google Sheets (pestaña: **Lista F**) y las imágenes públicas alojadas en GitHub.

---

## 🌐 Fuente de datos

- 📄 **Google Sheets:**  
  [https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM](https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM)

- 📑 **Pestaña usada:** `"Lista F"`

- 🔗 **API JSON (opensheet):**  

---

## 🖼️ Imágenes

Las imágenes están alojadas en el repositorio GitHub:

👉 [https://github.com/piztian/Top-0/tree/main/pics](https://github.com/piztian/Top-0/tree/main/pics)

Cada entrada debe tener su campo `url_imagen` apuntando a la ruta pública:


---

## 📋 Columnas esperadas

La hoja `"Lista F"` debe tener las siguientes columnas:

| Columna         | Uso en HTML                     |
|------------------|-------------------------------|
| archivo          | Nombre del archivo de imagen  |
| url_imagen       | Ruta de la imagen en GitHub   |
| Precio           | Texto que se muestra en la etiqueta de precio |
| Caracteristicas  | Descripción del producto       |

---

## 🧠 Funcionamiento del script

```js
fetch("https://opensheet.elk.sh/.../Lista%20F")
  .then(response => response.json())
  .then(data => {
    // Crea tarjetas HTML dinámicamente
    data.forEach(item => {
      const html = `
        <div class="card">
          <img src="${item.url_imagen}" alt="${item.archivo}">
          <div class="price">${item.Precio}</div>
          <div class="info">
            <div class="brand">${item.archivo.split(' ')[0]}</div>
            <div class="model">${item.archivo.replace('.jpg','')}</div>
            <div class="specs">${item.Caracteristicas}</div>
          </div>
        </div>
      `;
      document.getElementById("catalogo").insertAdjacentHTML("beforeend", html);
    });
  });
✅ Ventajas
Puedes actualizar precios y textos desde Google Sheets sin tocar código.

Puedes controlar el orden de aparición de productos simplemente cambiando el orden en la hoja.

Ideal para catálogos ligeros conectados a inventarios públicos.

🔐 Requisitos
La hoja debe estar publicada en la web:
Archivo → Compartir → Publicar en la web

Las imágenes deben ser accesibles públicamente desde GitHub o similar.
