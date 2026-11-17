# Guía de contribución

Gracias por interesarte en mejorar **Feliz Navidad ASCII**. Este documento explica cómo participar de forma sencilla y ordenada.

## Antes de empezar

- Respeta a todas las personas que participan. Mantén un tono cordial y constructivo.
- Busca si tu idea o error ya está reportado en la pestaña _Issues_.
- Las contribuciones se aceptan bajo la licencia [GNU GPL v3.0](LICENSE) del proyecto.

## Reportar un problema

Abre un _issue_ e incluye:

1. Qué esperabas que ocurriera y qué ocurrió realmente.
2. Navegador, sistema operativo y tamaño de pantalla.
3. Pasos para reproducirlo (por ejemplo, la fecha del dispositivo si afecta a la cuenta regresiva).
4. Capturas de pantalla si se trata de un problema visual.
5. Mensajes de error de la consola del navegador, si los hay.

## Proponer un cambio

1. Haz un _fork_ del repositorio `wulflo/FelizNavidad`.
2. Crea una rama con un nombre descriptivo: `git checkout -b mejorar-pesebre`.
3. Realiza los cambios y comprueba que todo sigue funcionando.
4. Haz un _commit_ con un mensaje claro en español, por ejemplo: `Ajusta la silueta de las figuras del pesebre`.
5. Envía la rama a tu fork y abre una _pull request_ contra `main`, explicando qué cambiaste y por qué.

Si tu cambio es grande, abre primero un _issue_ para comentarlo y evitar trabajo duplicado.

## Preparar el entorno

No hay dependencias ni build. Solo necesitas un navegador moderno.

```bash
git clone https://github.com/wulflo/FelizNavidad.git
cd FelizNavidad
python3 -m http.server 8000
```

Abre <http://localhost:8000/ASCII%20Navidad.html>.

## Estilo del código

- El programa es un único archivo, `ASCII Navidad.html`, con HTML, CSS y JavaScript integrados.
- Mantén el código sin dependencias externas (ni bibliotecas ni fuentes remotas).
- Usa nombres descriptivos y comentarios breves en español.
- Respeta la indentación y el estilo existente: las líneas suelen ser compactas y se agrupan por secciones (`// ---- ... ----`).
- Si añades texto visible, procura que siga siendo legible en pantallas estrechas y que respete los idiomas ya soportados.
- No añadas iconos decorativos dentro de los botones: las etiquetas deben ir solas junto a su indicador de estado.

## Comprobaciones antes de enviar

- [ ] La escena se dibuja sin errores en la consola del navegador.
- [ ] La cuenta regresiva usa la hora local y muestra días, horas, minutos y segundos.
- [ ] El saludo aparece del 25 de diciembre al 6 de enero y vuelve la cuenta regresiva el 7 de enero.
- [ ] El saludo se muestra en el idioma del dispositivo, con español como respaldo.
- [ ] Los diez controles de efecto y los botones principales son visibles y funcionan en una ventana de 390 px de ancho.
- [ ] El haz de luz, la estrella y las figuras del pesebre siguen proporcionados.
- [ ] El sonido sigue funcionando tras la interacción del usuario (los navegadores bloquean el audio automático).
- [ ] Las cuatro piezas musicales se pueden seleccionar desde el botón **Música** y no aparecen errores al cambiar de pieza.

## Licencia

Al enviar una contribución aceptas que se publique bajo la GNU GPL v3.0, la misma licencia del proyecto.
