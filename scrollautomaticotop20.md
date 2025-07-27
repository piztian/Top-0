# 📱 Catálogo Celucenter - Carrusel Dinámico

Este proyecto muestra un carrusel de productos actualizado dinámicamente desde una hoja de Google Sheets, ideal para mostrar un **catálogo de celulares o equipos destacados** en páginas como Bitrix24 Sites o cualquier sitio HTML.

---

## 🚀 Características

- Carrusel horizontal **automático e infinito**
- Carga de productos desde Google Sheets con [OpenSheet API](https://opensheet.elk.sh)
- Imágenes grandes, modelo, precio y características visibles
- Diseño **responsive y ligero**
- Sin dependencias externas (no necesita jQuery ni librerías pesadas)

---

## 📦 Demo

Puedes ver un ejemplo funcional aquí:  
[https://celucentershop.bitrix24.site/pruebascris](https://celucentershop.bitrix24.site/pruebascris)

---

## 📄 Estructura del archivo

```html
<body>
  <h1>📱 Catálogo Celucenter - Scroll Automático</h1>
  <div class="carousel-wrapper">
    <div class="carousel-track" id="carrusel">
      <!-- Productos dinámicos aquí -->
    </div>
  </div>

  <script>
    // Script que consume la hoja de cálculo y construye las tarjetas
  </script>
</body>
