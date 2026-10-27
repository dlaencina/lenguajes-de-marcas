Parte B: Refactorización

La página original (tabla de inventario de la UD anterior) no usaba atributos style, sino una etiqueta <style> en el <head>. He trasladado esas reglas a estilos.css y las he enlazado con <link>.

- Agrupación de selectores: th, td
- Agrupación de reglas en un mismo elemento: th, td tiene border y padding en la misma regla
