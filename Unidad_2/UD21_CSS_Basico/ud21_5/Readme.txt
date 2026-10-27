Predicciones (antes de abrir la página)

El h1 será marrón. Le afectan tres reglas: h1, .grande y #titulo. Gana #titulo porque el id es el selector más específico.

El Texto 1 será morado. Le afectan p (dos veces), .aviso y p.aviso. Gana p.aviso porque combina etiqueta y clase, y eso es más específico que la clase sola.

El Texto 2 será negro. Le afectan las mismas reglas que al Texto 1 y además #importante. El id gana a todas las demás.

El Texto 3 será naranja. Le afectan p (dos veces) y div p. Gana div p porque suma dos etiquetas y es más específico que p sola. La regla .aviso no le afecta porque no tiene esa clase.

Comprobación con el inspector (F12)

Abrí la página, hice clic derecho sobre cada elemento y elegí Inspeccionar. En el panel de Estilos, la regla ganadora aparece arriba y las que pierden salen tachadas. Los cuatro colores coinciden con mis predicciones.

Observación

Las reglas p { color: blue; } y p { color: green; } tienen la misma especificidad, así que gana la última (green). Aun así no llega a verse en ningún texto, porque siempre hay otra regla más específica que la supera.