# Dashboard de Producción y Logística

Dashboard interactivo para seguimiento de producción y despachos, construido en HTML/JS puro sin dependencias externas.

🔗 **[Ver dashboard en vivo](https://carloszabaleta.github.io/dashboard-produccion/)**

---

## ¿Qué hace?

El dashboard tiene dos pestañas principales:

### 📦 Producción
Conectado en tiempo real al Google Sheet **APP-ARCHIVO GENERAL**, muestra:
- KPIs del mes: cajas producidas, kilos, productos activos
- Producción diaria (barras por día)
- Mix de productos (donut)
- Ranking de clientes (barras horizontales)
- Evolución semanal (línea)
- Últimos remitos despachados

### 🚚 Logística
Visualización de datos de la hoja SALIDAS / SALIDAS HEADER:
- Cajas despachadas por día
- Mix de productos despachados (donut)
- Top clientes (barras horizontales)
- Transportes utilizados (torta)
- Evolución semanal de despachos (línea)
- Heatmap días × semana (paleta rojo-naranja-amarillo)
- Cajas por cliente × mes (barras agrupadas)
- Tabla de últimos remitos

---

## Tecnología

- **HTML + CSS + JavaScript puro** — sin librerías externas (Chart.js, D3, etc.)
- **Canvas 2D API** — todos los gráficos dibujados a mano con coordenadas lógicas y DPR scaling
- **Tooltips interactivos** — hit zones registradas por canvas; tooltip aparece al pasar el mouse sobre cada barra
- **Google Sheets** como fuente de datos (via gviz/tq endpoint)
- **GitHub Pages** para hosting estático

---

## Estructura del repo

```
index.html          → Dashboard principal (producción + logística)
README.md           → Este archivo
README-dashboard.md → Notas técnicas de la primera versión
```

---

## Cómo actualizar

Los datos de producción se leen en vivo desde Google Sheets — no hay que tocar nada. Para actualizar el código:

1. Editá `index.html` localmente
2. Subí el archivo en **[github.com/carloszabaleta/dashboard-produccion](https://github.com/carloszabaleta/dashboard-produccion)** → _Add file → Upload files_
3. GitHub Pages publica el cambio en ~1 minuto

---

*Construido con Claude (Cowork) — Junio 2026*
