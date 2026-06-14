# Planificador de Rutas · Provefabrica

Herramienta web autocontenida para optimizar rutas de despacho por calles reales,
leyendo los puntos de entrega en vivo desde Google Sheets.

## Cómo publicarlo en GitHub Pages (paso a paso)

### 1. Crear el repositorio
1. Entra a https://github.com e inicia sesión.
2. Botón **New** (o el `+` arriba a la derecha › New repository).
3. **Repository name:** por ejemplo `planificador-rutas`.
4. Marca **Public** (GitHub Pages gratis requiere repo público).
5. Clic en **Create repository**.

### 2. Subir los archivos
1. En el repo nuevo, clic en **uploading an existing file**
   (o pestaña **Add file › Upload files**).
2. Arrastra el archivo **`index.html`** (y este README si quieres).
3. Abajo, clic en **Commit changes**.

> Importante: el archivo DEBE llamarse `index.html` para que GitHub Pages
> lo muestre como página principal.

### 3. Activar GitHub Pages
1. En el repo, ve a **Settings** (engranaje, arriba a la derecha).
2. En el menú izquierdo, **Pages**.
3. En **Branch**, elige **main** y carpeta **/ (root)**.
4. Clic en **Save**.
5. Espera 1–2 minutos. Aparecerá tu enlace:
   `https://TU-USUARIO.github.io/planificador-rutas/`

### 4. Usar la herramienta
1. Abre ese enlace `https://...` (NO el archivo local).
2. Pega la URL de tu Google Sheets y clic en **Cargar paradas**.
   - Como ahora corre en `https://`, la lectura en vivo funciona automáticamente.
3. Elige el chofer, clic en **Optimizar ruta**, y exporta a Google Maps / Waze.

## Requisitos del Google Sheets
- Compartido como **"Cualquier persona con el enlace" › Lector**.
- Columnas esperadas (el orden no importa, se detectan por nombre):
  `Marca temporal`, `Factura`, `Cliente`, `Latitud`, `Longitud`, `Chofer`, `Enlace maps`.

## Notas
- Optimización por calles reales vía OSRM (servidor público gratuito).
  Si OSRM no responde, usa cálculo geográfico de respaldo automáticamente.
- Punto de partida predeterminado: Almacén Huachipa (editable; clic derecho en el mapa para reubicar).
- Requiere conexión a internet (lee el Sheets y consulta el ruteo en vivo).
