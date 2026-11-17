# 🎄 Feliz Navidad ASCII

Una escena navideña interactiva dibujada con arte ASCII sobre un lienzo HTML. Todo el proyecto vive en un **único archivo HTML**: no hay dependencias, paquetes ni pasos de compilación.

**[Ver la demo](https://wulflo.github.io/FelizNavidad/)**

## Qué incluye

- **Pueblo nevado** a la izquierda: casas con tejados cubiertos de nieve, ventanas encendidas, chimeneas con humo, farolas y una capilla con campanario.
- **Pesebre de Belén** a la derecha: un haz de luz descendente desde el cielo, estrella de Belén, María, José y el niño Jesús, con figuras esbeltas y proporcionadas.
- **Árbol de Navidad** animado con luces, guirnaldas, adornos, nieve, chispas, aurora y fuegos artificiales.
- **Cuenta regresiva local**: usa la hora del dispositivo (no un servidor). Muestra días y `HH:MM:SS` hasta el 25 de diciembre.
- **Saludo navideño**: del 25 de diciembre al 6 de enero (ambos incluidos) se muestra «Feliz Navidad» en el idioma del dispositivo. A partir del 7 de enero vuelve la cuenta regresiva hacia la Navidad siguiente.
- **Idiomas**: español, inglés, portugués, francés, alemán, italiano, catalán y gallego (se detecta con `navigator.language`; si no se reconoce, se usa español).
- **Sonido**: cuatro arreglos instrumentales originales generados con Web Audio API, sin archivos externos. Cada pieza combina campanas, pads armónicos, bajo, arpegios, reverberación y (en «Trineo») percusión.

## Uso

Abre `ASCII Navidad.html` directamente en cualquier navegador moderno.

Si prefieres servirlo localmente:

```bash
python3 -m http.server 8000
```

y visita <http://localhost:8000/ASCII%20Navidad.html>.

## Controles

La barra inferior agrupa los controles:

| Control | Función |
| --- | --- |
| `♪` | Activa o silencia la música |
| **Repetir** | Reinicia la animación |
| **Música** | Selecciona entre `Campanas`, `Villancico`, `Nochebuena` y `Trineo` (al pulsarlo se muestra el nombre de la pieza siguiente) |
| **Estilo** | Cambia entre los modos de dibujo del árbol |
| **Giro / Luces / Guirnalda / Adornos / Estrella / Regalos / Nieve / Chispas / Aurora / Fuegos** | Activa o desactiva cada efecto |

También puedes **arrastrar** para girar la escena y **tocar** para crear chispas. En pantallas estrechas todos los botones siguen visibles (se distribuyen en varias filas).

## Estructura del repositorio

```
ASCII Navidad.html        Aplicación completa (HTML + CSS + JavaScript)
.github/workflows/pages.yml   Workflow de publicación en GitHub Pages
CONTRIBUTING.md           Guía para contribuir
LICENSE                   GNU General Public License v3.0
README.md                 Este archivo
```

## Publicación

El workflow `.github/workflows/pages.yml` publica el sitio automáticamente en cada `push` a `main` (y también puede ejecutarse manualmente con `workflow_dispatch`). Copia `ASCII Navidad.html` a `index.html` dentro del artefacto y lo despliega con las acciones oficiales de GitHub Pages.

Para publicarlo en otro repositorio, cambia el nombre del repositorio en el enlace de este README y habilita Pages con **GitHub Actions** como fuente.

## Contribuciones

Las contribuciones son bienvenidas: consulta [CONTRIBUTING.md](CONTRIBUTING.md) antes de abrir un issue o una pull request.

## Licencia

Este proyecto se distribuye bajo la [GNU General Public License v3.0](LICENSE): una licencia **copyleft fuerte**. Puedes usar, modificar y redistribuir el código, y si publicas una versión modificada debes compartirla bajo la misma licencia.
