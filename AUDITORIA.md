# Auditoria y registro de cambios

## Alcance

Revision de la tarjeta de presentacion y registro de los cambios realizados
para publicarla en GitHub Pages. Se comprobaron el HTML, CSS y JavaScript, la
configuracion de GitHub Actions y la respuesta HTTP del sitio publicado. No se
ejecutaron pruebas automatizadas ni una auditoria de seguridad especializada.

## Cambios realizados

- Se agregaron `index.html`, `styles.css` y `script.js` para la tarjeta de
  presentacion.
- Se agrego la ilustracion de perfil `foto.png` y se enlazo desde `index.html`.
- Se agrego este informe de auditoria.
- Se cambio el nombre visible de Ana Torres a Cielo Vizcaino en el encabezado,
  el texto alternativo del retrato y el pie de pagina.
- Se agrego `.github/workflows/deploy-pages.yml` para desplegar el sitio
  estatico en GitHub Pages con cada push a `main` y manualmente desde Actions.
- Se habilito GitHub Pages como destino del workflow y se retiro el intento
  automatico de habilitar Pages, que no tenia permisos suficientes.
- Los archivos y actualizaciones se publicaron en la rama `main` del
  repositorio `Cielo201356/Semena_1`.

## Hallazgos pendientes

1. **El estado del control de habilidades no se comunica.** El boton permite
   mostrar u ocultar la lista, pero no actualiza `aria-expanded` ni indica el
   estado actual a las tecnologias de asistencia.
2. **Quedo un mensaje de depuracion.** `script.js` imprime en la consola la
   cantidad de habilidades. No impide el funcionamiento y se puede retirar si
   ya no se necesita.
3. **El correo de contacto conserva el valor anterior.** El pie de pagina
   todavia muestra `ana.torres@correo.com`.

## Verificacion

- El documento usa elementos semanticos, declara `lang="es"` y enlaza la hoja
  de estilos y el script.
- El script actualiza el ano y alterna la visibilidad de la lista de
  habilidades.
- El workflow de GitHub Actions completo con exito en su segunda ejecucion:
  [ejecucion 2](https://github.com/Cielo201356/Semena_1/actions/runs/37668499613).
  La primera ejecucion fallo porque Pages aun no estaba habilitado; tras
  habilitar Pages se ajusto el workflow y el despliegue termino correctamente.
- El sitio publicado respondio HTTP 200 al comprobarlo:
  https://cielo201356.github.io/Semena_1/
