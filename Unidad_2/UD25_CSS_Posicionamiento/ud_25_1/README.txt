UD3.1 Ejercicio 1: Laboratorio de position

Static: el cuadro 1 no se mueve con left porque los elementos static ignoran top, left, right y bottom.

Relative: el cuadro 2 se mueve desde su sitio, pero su hueco se queda guardado y el 3 no sube.

Absolute: sin padre posicionado, el cuadro 3 va a la esquina de la página. Con position: relative en el contenedor, va a la esquina del contenedor. No deja hueco, así que el texto sube.

Z-index: el cuadro 1 solo queda encima del 2 cuando le pongo position: relative, porque z-index no funciona en elementos static.