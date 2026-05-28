# 📊 Dashboard de Producción

Dashboard interactivo de producción industrial con datos en tiempo real, construido como una aplicación web de una sola página (HTML/CSS/JS).

🔗 **[Ver dashboard en vivo](https://carloszabaleta.github.io/dashboard-produccion/dashboard-produccion.html)**

---

## ¿Qué hace?

Visualiza la producción diaria de la planta en un panel tipo Power BI, conectado directamente a Google Sheets como fuente de datos. Cada vez que se abre el dashboard, consulta la hoja de cálculo y muestra los datos actualizados al momento.

## Funcionalidades

- **Resumen General** — KPIs principales: total de cajas, promedio diario, días activos y productos distintos
- **Por Producto** — Ranking de producción por línea de producto con gráficos de barra y tabla comparativa
- **Evolución Diaria** — Gráfico de producción día a día con línea de promedio y curva acumulada
- **Detalle** — Tabla completa de registros individuales, filtrable por producto y mes
- Filtros dinámicos por mes y producto
- Botón de actualización manual sin recargar la página
- Caché automático: si la fuente no está disponible, muestra los últimos datos guardados

## Fuente de datos

Los datos provienen de la hoja **EMISION ROTULO** (pestaña HISTORICO) en Google Sheets. El dashboard la consulta mediante la API pública de Google Visualization (`gviz/tq`) — no requiere autenticación ni API key, solo que la hoja esté compartida como "Cualquier persona con el enlace puede ver".

Filtros aplicados automáticamente:
- Se excluyen productos INS (insumos/materias primas)
- Se excluye marzo 2026 (datos parciales de un solo día)
- Se deduplican registros por ID para evitar doble conteo

## Tecnologías

- HTML5 / CSS3 / JavaScript vanilla (sin frameworks)
- [Chart.js 4.4.1](https://www.chartjs.org/) para gráficos
- Google Sheets como base de datos (vía endpoint CSV público)
- GitHub Pages para hosting estático gratuito

## Estructura del proyecto

```
dashboard-produccion/
└── dashboard-produccion.html   # Aplicación completa en un solo archivo
```

## Cómo actualizar los datos

No requiere ninguna acción. Basta con cargar los registros normalmente en la app de producción (Google Sheets EMISION ROTULO). El dashboard los mostrará la próxima vez que se abra o cuando se use el botón ↻ Actualizar.

## Autor

Carlos Zabaleta — [@CarlosZabaleta](https://github.com/CarlosZabaleta)
