# Auditoria de la pagina

## Alcance

Revision del HTML, CSS y JavaScript de la tarjeta de presentacion. Se revisaron
la estructura, los recursos referenciados, la interaccion y aspectos basicos de
accesibilidad. No se ejecutaron pruebas automatizadas ni se hizo una auditoria
de seguridad especializada.

## Hallazgos

1. **La imagen de perfil no esta incluida.** `index.html` referencia
   `foto.jpg`, pero ese archivo no esta entre los archivos disponibles. El
   navegador mostrara una imagen rota hasta que se agregue el recurso o se
   actualice la ruta.
2. **El estado del control de habilidades no se comunica.** El boton permite
   mostrar u ocultar la lista, pero no actualiza `aria-expanded` ni un texto
   que indique el estado actual. Esto puede hacer menos clara la interaccion
   para usuarios de tecnologias de asistencia.
3. **Hay un mensaje de depuracion en la consola.** `script.js` imprime la
   cantidad de habilidades. No impide el funcionamiento, pero conviene
   retirarlo si no se necesita para depuracion.

## Comprobaciones

- El documento usa elementos semanticos y declara el idioma espanol.
- La hoja de estilos y el script estan enlazados desde el HTML.
- El script actualiza el ano y alterna la clase que oculta la lista.
- No se modificaron los archivos de la pagina durante esta auditoria.
