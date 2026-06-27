# Conversor Soles Euros

PWA mobile first para convertir Soles Peruanos a Euros y Euros a Soles. Funciona con HTML, CSS y JavaScript puro, se puede instalar en iPhone y usa rutas relativas para GitHub Pages.

## Funciones

- Conversión PEN -> EUR y EUR -> PEN.
- Botón para invertir la dirección.
- Conversión automática mientras escribes.
- Tipo de cambio actualizado desde `https://open.er-api.com` sin API key.
- Guarda el último tipo de cambio en `localStorage`.
- Si la API falla o no hay internet, usa el último tipo guardado.
- Si nunca se pudo obtener un tipo online, usa el respaldo `1 EUR = S/ 4.10`.
- Service worker para abrir la app offline.

## Archivos

- `index.html`: app completa, estilos y JavaScript.
- `manifest.json`: configuración PWA.
- `service-worker.js`: cache offline.
- `icon-192.png`: icono PWA de 192 px.
- `icon-512.png`: icono PWA de 512 px.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub, por ejemplo `conversor-soles-euros`.
2. Sube estos archivos a la rama principal del repositorio.
3. En GitHub, abre `Settings` -> `Pages`.
4. En `Build and deployment`, selecciona:
   - `Source`: `Deploy from a branch`
   - `Branch`: `main`
   - Carpeta: `/root`
5. Guarda los cambios.
6. Abre la URL publicada por GitHub Pages.

## Instalar en iPhone

1. Abre la URL de GitHub Pages en Safari.
2. Toca el botón de compartir.
3. Toca `Agregar a pantalla de inicio`.
4. Abre la app desde el icono instalado.

## Nota sobre el tipo de cambio

La app solicita `EUR -> PEN` a `open.er-api.com`. Como cualquier API pública puede fallar o estar temporalmente no disponible, la app siempre mantiene un resultado usando el último valor guardado o el respaldo fijo.
