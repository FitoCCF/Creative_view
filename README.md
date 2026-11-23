# Creative Corporation · Integración de datos industriales

Landing page y brochure para ofrecer servicios de integración de datos industriales
(OPC UA, Modbus TCP/IP, IEC 61850 → historial, tableros y alertas) a plantas de proceso
del sur del Perú.

- Web: https://fitoccf.github.io/Creative_view/
- Brochure: [`brochure/creative-corporation-brochure.pdf`](brochure/creative-corporation-brochure.pdf) (A4, 2 páginas)

## Estructura

```
index.html                 Landing (HTML + CSS en un solo archivo, sin dependencias externas)
brochure/brochure.html     Fuente del brochure (A4, lista para imprimir a PDF)
brochure/creative-corporation-brochure.pdf
assets/fonts/              Archivo (variable, peso y ancho), licencia SIL OFL 1.1
assets/favicon.svg
```

## Antes de compartir: reemplaza los datos de ejemplo

Busca y reemplaza en `index.html` y `brochure/brochure.html`:

| Ejemplo                     | Reemplazar por            |
|-----------------------------|---------------------------|
| `51900000000`               | Tu número de WhatsApp con código de país, sin `+` ni espacios |
| `+51 900 000 000`           | Tu número para mostrar    |
| `contacto@tudominio.pe`     | Tu correo                 |
| `tu-perfil`                 | Tu usuario de LinkedIn    |

## Regenerar el PDF del brochure

Después de editar `brochure/brochure.html`, desde la carpeta `brochure/`:

```bash
google-chrome --headless --no-pdf-header-footer \
  --print-to-pdf=creative-corporation-brochure.pdf brochure.html
```

(También sirve abrirlo en Chrome → Imprimir → Guardar como PDF, tamaño A4,
márgenes "Ninguno" y "Gráficos de fondo" activado.)

## Publicación

GitHub Pages sirve la rama `main` desde la raíz (`/`). Cualquier push a `main`
actualiza la web en uno o dos minutos.
