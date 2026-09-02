# Coro — tu día, con calma

Una agenda diaria pensada para **no agobiar**: una sola pantalla ("Hoy"), mucho aire, y por
defecto se muestra poco. El día se *ve* de un vistazo porque cada bloque ocupa el alto de su
duración, y una línea rosa marca la hora actual.

Es una app web en un solo archivo (`index.html`). No necesita internet para funcionar una vez
cargada, y **todos tus datos se guardan solo en tu dispositivo** (en el navegador). No hay
cuentas ni servidores.

## Qué hace ahora (primer prototipo)

- **Vista Hoy** con timeline de 6:00 a 23:00 (la noche se despliega tocándola).
- **Bloques** con nombre, hora de inicio/fin y categoría (gym, trabajo, comida, descanso).
  El alto del bloque = su duración.
- **Añadir / editar / borrar** bloques: toca un hueco para crear, toca un bloque para editar.
- **Añadir rápido**: pastillas de Gym, Trabajo, Comida y Descanso.
- **Línea de "ahora"** que se mueve con la hora real.
- **3 prioridades** del día siempre visibles arriba (máximo 3, a propósito).
- **Modo claro y oscuro** (botón de la luna arriba a la derecha).
- **Instalable** como app en el móvil (PWA).

Notas, rutinas y recordatorios llegarán después.

## Abrirla en el ordenador

Haz doble clic en `index.html`. Se abre en tu navegador.

## Verla / instalarla en el móvil (con GitHub Pages, gratis)

1. Crea una cuenta en <https://github.com> si no tienes.
2. Crea un repositorio nuevo (por ejemplo `coro`) y sube estos archivos
   (`index.html`, `manifest.webmanifest`, `sw.js` y los `icon-*.png`).
3. En el repo: **Settings → Pages → Build and deployment → Source: _Deploy from a branch_**,
   rama `main`, carpeta `/root`. Guarda.
4. En un par de minutos tendrás una dirección tipo
   `https://TU-USUARIO.github.io/coro/`. Ábrela en el móvil.
5. En el navegador del móvil: menú → **"Añadir a pantalla de inicio"**. Ya la tienes como app.

### Subirlo desde el ordenador con Git

```bash
cd coro-app
git remote add origin https://github.com/TU-USUARIO/coro.git
git branch -M main
git push -u origin main
```

## Archivos

| Archivo | Para qué |
|---|---|
| `index.html` | La app entera (HTML + CSS + JS). |
| `manifest.webmanifest` | Hace que sea instalable como app. |
| `sw.js` | Service worker: permite abrirla sin conexión. |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Iconos de la app. |

## Tus datos

Todo se guarda en `localStorage` del navegador, por día. Si borras los datos del navegador o
usas otro dispositivo, empiezas de cero. (La sincronización entre dispositivos es una mejora
futura.)
