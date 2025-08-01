# 📱 Catálogo Dinámico CriShop - Celucenter

Este proyecto muestra un catálogo interactivo de equipos disponibles en CriShop, utilizando HTML puro, imágenes desde GitHub y datos desde Google Sheets a través de la API de OpenSheet.

---

## 📁 Estructura del Repositorio

- `/fotos/` → Contiene las imágenes de los equipos en formato `.jpg` o `.png`.
- `catalogo.html` → Página principal del catálogo dinámico.
- `detallecrishop.html` → Página de detalle que se abre al hacer clic sobre un equipo.

---

## 🌐 Fuente de Datos

Toda la información se carga en tiempo real desde una hoja de cálculo de Google Sheets:

**Hoja: `Lista F`**  
📄 https://docs.google.com/spreadsheets/d/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM/edit#gid=1856771547  
🌍 API JSON:  
`https://opensheet.elk.sh/1YGFRcNmZ6bXe7L2hFS1w8YVkWXJVkyn46ILx0ki3uCM/Lista%20F`

### Columnas utilizadas:
- `archivo`: Nombre del archivo de imagen (sin espacio adicional).
- `url_imagen`: Link directo a la imagen en GitHub.
- `Precio`: Precio del equipo.
- `Caracteristicas`: Detalles del equipo.

---

## 📸 Imagen del producto

Las imágenes se alojan en GitHub en esta ruta base:




Se construye automáticamente el link desde la columna `archivo`.

---

## ⚙️ Funcionamiento del catálogo

1. El HTML hace un `fetch()` a la API de OpenSheet.
2. Crea dinámicamente tarjetas para cada equipo.
3. Cada imagen es un enlace que abre el detalle del producto.

---

## 🔍 Detalle de producto

La página `detallecrishop.html` se abre cuando se hace clic en un equipo.  
Usa el parámetro `modelo` en la URL para encontrar los datos y mostrar:

- Imagen del equipo
- Marca
- Modelo
- Precio
- Características

Ejemplo:



---

## 🛠️ Personalización

Puedes modificar:
- El diseño desde los estilos CSS embebidos.
- Los datos desde la hoja de Google.
- Las imágenes subiéndolas a la carpeta `/fotos`.

---

## ✅ Requisitos

- La hoja de cálculo debe estar **publicada en la web**.
- Las imágenes deben tener nombres compatibles con los datos (`archivo`).

---

## ✨ Desarrollado por

**Celucenter Tech Team**  
Integración por [ChatGPT + GitHub + Google Sheets + HTML puro]
