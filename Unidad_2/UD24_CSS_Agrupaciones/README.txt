UD24_1

¿inline-block o flex?

Me quedo con flex. Con inline-block tuve que ponerme a hacer cuentas y bajar el ancho de las tarjetas para que entraran las tres, y aun así queda un hueco raro entre ellas por los espacios del HTML. Con flex basta con poner display: flex en .contenido y las tarjetas se colocan en fila solas, sin huecos raros y sin tener que calcular nada.


1. ¿Qué diferencia hay entre margin y padding?
El padding es el espacio de dentro de la caja, entre el texto y el borde. El margin es el espacio de fuera, el que separa una caja de las que tiene alrededor. Si le pones fondo a una caja, el padding se pinta de ese color y el margin no.

2. ¿Por qué saltaba la tercera tarjeta de línea?
Porque el width solo mide el contenido, y luego se le suman el padding, el borde y el margin de los dos lados. Cada tarjeta ocupaba en realidad 220 + 30 + 4 + 20 = 274px, y las tres juntas 822px, que no caben en los 800px de la página. Encima, con inline-block el navegador mete un pequeño espacio entre tarjeta y tarjeta. Lo arreglé bajando el width a 200px: 254 × 3 = 762px, y ya caben.

3. ¿Qué propiedades ignoraba el span y por qué?
Ignoraba el width, el height y el margin de arriba y abajo (el de los lados sí lo respetaba). Es porque un span es un elemento en línea: va metido dentro del texto como si fuera una palabra más, así que su tamaño lo marca lo que lleva dentro. Al ponerle display: inline-block sigue yendo en la línea, pero ya se comporta como una caja y respeta todo.

4. ¿Qué hace display: none con el espacio que ocupaba la caja?
Lo quita del todo. La tercera tarjeta desaparece como si no estuviera en el HTML y no deja hueco: las demás se recolocan y ocupan su sitio.