# Ejercicio Responsivo Mobile First y Flex

Este proyecto es una demostración de diseño web responsivo utilizando la técnica de "mobile first" y Flexbox. Incluye un archivo HTML y un archivo CSS que se adaptan a diferentes tamaños de pantalla, desde móviles hasta escritorio.

## Archivos

- `index.html`: Archivo HTML principal.
- `assets/css/media.css`: Archivo CSS que contiene las reglas de estilo y media queries.

## Descripción del Proyecto

El objetivo de este proyecto es mostrar cómo se puede usar CSS para crear un diseño responsivo que se adapte a diferentes tamaños de pantalla. Utilizamos media queries para definir estilos específicos para móviles, tablets y pantallas de escritorio.

### Estructura del HTML

El archivo `index.html` tiene la siguiente estructura:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="assets/css/media.css"> 
    <title>Ejercicio Responsivo Mobile First y Flex</title>
</head>
<body>
    <div class="rosado col-xs-12"></div>
    <div class="verde col-xs-12"></div>
    <div class="azul col-xs-12"></div>
    <div class="rojo"></div>
    <div class="morado"></div>
    <div class="gris col-xs-12"></div>
</body>
</html>

