# PbR Delicias Dashboard

Dashboard estático para monitoreo de indicadores, semáforos de desempeño y auditoría de líneas de acción del municipio de Delicias. El proyecto está preparado para publicarse en GitHub Pages usando un único `index.html` y consume datos desde un CSV publicado de Google Sheets.

## Características

- KPIs generales de desempeño: total de acciones, semáforos y eficiencia PMD.
- Filtros dinámicos por eje, ODS, entidad, meta ODS, fin, propósito y componente.
- Visualizaciones con Chart.js para distribución por dependencia, estado, proyección anual y avance trimestral.
- Módulo de auditoría específica por línea de acción con expediente resumido y gráfica individual.
- Motor de recomendaciones con hallazgos automáticos a partir de los datos filtrados.
- Estructura lista para GitHub Pages sin proceso de build.

## Estructura

```text
.
├── index.html
├── README.md
└── assets/
    └── capturas/
        ├── image-2.jpg
        ├── image-3.jpg
        └── image-4.jpg
```

## Publicación en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html` al directorio raíz del repositorio.
3. Crea la carpeta `assets/capturas/` y coloca allí las imágenes de este README.
4. En **Settings > Pages**, selecciona la rama principal y la carpeta `/root`.
5. Guarda y espera a que GitHub publique el sitio.

## Dependencias externas

Este dashboard usa CDN para las librerías, por lo que requiere conexión a internet:

- Tailwind CSS
- Lucide Icons
- Chart.js
- PapaParse
- Google Fonts (Inter)

## Fuente de datos

La aplicación consume un CSV público de Google Sheets definido dentro de `APP_CONFIG.csvUrl` en `index.html`. Si cambias la hoja fuente, actualiza esa URL publicada.

## Personalización rápida

- Cambia el título del sitio en la etiqueta `<title>` y en el encabezado principal.
- Ajusta colores y sombras en el bloque `<style>`.
- Modifica los mapeos de columnas en `fieldMappings` si tu Google Sheet cambia de nombres.
- Si deseas usar un archivo local en vez de Google Sheets, reemplaza `APP_CONFIG.csvUrl` por la ruta de tu CSV.

## Capturas

### Vista general

![Vista general del dashboard](assets/capturas/image-4.jpg)

### Módulo de gráficas y auditoría

![Módulo de gráficas y auditoría](assets/capturas/image-2.jpg)

### Auditoría específica de línea de acción

![Auditoría específica de línea de acción](assets/capturas/image-3.jpg)

## Notas técnicas

- El archivo fue ajustado para funcionar como página estática en GitHub Pages.
- Se eliminó el `onclick` inline del botón de sincronización y se sustituyó por listeners en JavaScript.
- Se mejoró el comportamiento responsivo para pantallas medianas y móviles.
- Se añadió una configuración centralizada (`APP_CONFIG`) para facilitar mantenimiento.
- El tablero sigue dependiendo de que el CSV público permita acceso sin autenticación.
