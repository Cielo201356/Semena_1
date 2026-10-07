# Semena_1

Tarjeta de presentación web personal, construida con HTML, CSS y JavaScript y
publicada mediante GitHub Pages.

## Sitio publicado

https://cielo201356.github.io/Semena_1/

## Archivos del proyecto

- `index.html`: contenido y estructura semántica de la página.
- `styles.css`: estilos visuales y presentación adaptable.
- `script.js`: actualización automática del año y control para mostrar u ocultar
  la lista de habilidades.
- `AUDITORIA.md`: registro de cambios, comprobaciones y hallazgos pendientes.
- `.github/workflows/deploy-pages.yml`: publicación automática en GitHub Pages.

## Publicación

GitHub Actions despliega el sitio cuando se envían cambios a la rama `main`.
También se puede iniciar manualmente desde la pestaña **Actions**, ejecutando
el workflow **Deploy static site to GitHub Pages**.

La última publicación verificada finalizó correctamente y el sitio respondió
HTTP 200. [Ver ejecuciones del workflow](https://github.com/Cielo201356/Semena_1/actions).

## Pendientes conocidos

- La página hace referencia a `foto.jpg`, pero la imagen aún no está incluida
  en el repositorio.
- El control de habilidades no anuncia su estado expandido o contraído a las
  tecnologías de asistencia.
- El script conserva un mensaje de depuración en la consola.
- El correo mostrado en la página todavía es `ana.torres@correo.com`.

Consulta [AUDITORIA.md](./AUDITORIA.md) para más detalles.
