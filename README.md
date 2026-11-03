# 🗺️ Geoportal Cartográfico ITEC 2026
### Carrera de Gestión de Riesgos — Instituto Superior Tecnológico ITEC

Aplicación web geográfica (Web GIS) responsiva, diseñada especialmente para estudiantes de la **Carrera de Gestión de Riesgos del ITEC (2026)**. Permite explorar, aislar y descargar cartografía oficial de la división territorial del Ecuador (Provincias, Cantones y Parroquias) directamente desde teléfonos inteligentes o computadoras.

---

## 📱 Acceso Web (GitHub Pages)

Una vez activado GitHub Pages en este repositorio, los estudiantes pueden acceder desde cualquier celular al siguiente enlace:
👉 **`https://<TU_USUARIO>.github.io/<NOMBRE_REPOSITORIO>/`**

---

## 🚀 Características Principales

1. **📱 100% Responsivo y Mobile-First:**
   * Diseñado para funcionar de manera fluida en cualquier smartphone (Android / iOS) sin requerir computadoras potentes ni software GIS instalado.
2. **✂️ Geoprocesos Básicos tipo QGIS (Cortar y Aislar):**
   * Selecciona cualquier Provincia, Cantón o Parroquia y pulsa **"Cortar y Aislar"** para apagar las demás capas y enfocar la entidad de estudio.
   * Visualiza divisiones internas (cantones de una provincia o parroquias de un cantón) de forma aislada.
   * Árbol de capas estilo QGIS para encender, apagar o descargar GeoJSONs de los recortes generados.
3. **📸 Exportación Cartográfica Oficial (PNG / PDF):**
   * Descarga la vista del mapa con encuadre centrado y equilibrado.
   * Incluye membrete oficial del **Instituto Tecnológico ITEC 2026 - Carrera de Gestión de Riesgos** con nombre editable del estudiante.
4. **🔍 Buscador Rápido de Entidades:**
   * Encuentra al instante cualquiera de las 24 provincias o 221 cantones del Ecuador con zoom automático.
5. **⚡ Arquitectura Zero-CORS:**
   * Funciona tanto servido en la web como abriéndolo directamente en local (`file:///`), gracias a la carga empaquetada en `data_js/`.

---

## 📂 Estructura del Repositorio

```text
├── index.html                 # Aplicación web principal del Geoportal (Leaflet 1.9.4)
├── data_js/                   # Datos geoespaciales cargados de forma instantánea (offline/CORS free)
│   ├── provincias.js          # 24 Provincias del Ecuador
│   ├── cantones.js            # 221 Cantones
│   ├── parroquias.js          # Parroquias del Ecuador
│   └── periferia.js           # Límites fronterizos
├── geojson_web_ligero/        # GeoJSONs optimizados para visualización web rápida
├── geopackage/                # Geopackages limpios para QGIS (EPSG:4326 y EPSG:32717 UTM 17S)
├── shapefile_wgs84/           # Shapefiles reparados en coordenadas geográficas WGS84
├── shapefile_utm17s/          # Shapefiles reparados en coordenadas proyectadas UTM 17S
└── README.md                  # Documentación del proyecto
```

---

## 🛠️ Activación de GitHub Pages

Para publicar el visor web gratuito en GitHub:
1. En el repositorio de GitHub, entra a **Settings** (Configuración).
2. En el menú izquierdo, busca la sección **Pages**.
3. En **Build and deployment > Source**, selecciona: **`Deploy from a branch`**.
4. En **Branch**, selecciona: **`main`** y la carpeta **`/(root)`**, luego pulsa **Save**.
5. Espera unos 60 segundos y GitHub te proporcionará el enlace público para compartir con tus estudiantes.

---

*Desarrollado con Leaflet, html2canvas y jsPDF para la práctica docente en Sistemas de Información Geográfica y Gestión del Riesgo.*

