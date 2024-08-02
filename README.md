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
Descripción del CSS
El archivo CSS media.css contiene las siguientes secciones:

Reset de estilos por defecto: Para asegurar que todos los elementos tengan un margen y padding de 0 y que el box-sizing sea border-box.
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
Media Queries para diferentes tamaños de pantalla:

Para pantallas de hasta 500px de ancho (móviles): Definimos un sistema de grilla y estilos específicos para móviles.
@media only screen and (max-width: 500px) {
    /* Ancho de las columnas en porcentajes, simulando un grid */
    .col-xs-1 {width: 8.33%;}
    .col-xs-2 {width: 16.66%;}
    .col-xs-3 {width: 25%;}
    .col-xs-4 {width: 33.33%;}
    .col-xs-5 {width: 41.66%;}
    .col-xs-6 {width: 50%;}
    .col-xs-7 {width: 58.33%;}
    .col-xs-8 {width: 66.66%;}
    .col-xs-9 {width: 75%;}
    .col-xs-10 {width: 83.33%;}
    .col-xs-11 {width: 91.66%;}
    .col-xs-12 {width: 100%;}

    /* Mostrar ciertos divs y ocultar otros en pantallas pequeñas */
    .rosado,.verde, .azul, .gris {
        display: block;
    }
    .rojo,.morado {
        display: none;
    }

    /* Estilos específicos para divs en pantallas pequeñas */
    .rosado,.verde {
        height: 100px;
    }
    .rosado {
        background-color: #ffc0cb; /* Rosado */
    }
    .verde {
        background-color: #008000; /* Verde */
    }
    .azul {
        background-color: #0000ff; /* Azul */
        height: 55px;
    }
    .gris {
        background-color: #808080; /* Gris */
        height: 146px;
    }
}
Para pantallas entre 501px y 750px de ancho (tablets): Utilizamos Flexbox para manejar la distribución de los elementos.
@media only screen and (min-width: 501px) and (max-width: 750px) {
    /* Estilos específicos para divs en tablets */
    .rosado,.azul,.verde,.rojo {
        height: 100px;
    }
    .rosado {
        background-color: #ffc0cb; /* Rosado */
        width: 100%;
    }
    .azul {
        background-color: #0000ff; /* Azul */
    }
    .verde {
        background-color: #008000; /* Verde */
    }
    .rojo {
        background-color: #ff0000; /* Rojo */
    }
    .morado,.gris {
        height: 85px;
    }
    .morado {
        background-color: #800080; /* Morado */
    }
    .gris {
        background-color: #808080; /* Gris */
    }

    /* Configuración del contenedor (body) como flexbox y distribución de los elementos */
    body {
        display: flex;
        flex-wrap: wrap;
    }
    .verde, .azul, .rojo {
        box-sizing: border-box;
        flex: 1 0 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
    .morado {
        flex: 1 0 60%; /* Ocupa el 60% del ancho del contenedor */
    }
    .gris {
        flex: 1 0 40%; /* Ocupa el 40% del ancho del contenedor */
    }
}
Para pantallas de más de 751px de ancho (escritorio): Definimos alturas y anchos específicos, y usamos Flexbox para la distribución.
@media only screen and (min-width: 751px) {
    /* Ancho completo para ciertos divs */
    .rosado, .verde, .azul {
        width: 100%;
    }

    /* Alturas específicas y colores de fondo */
    .rosado {
        background-color: #ffc0cb; /* Rosado */
        height: 20px;
    }
    .verde {
        background-color: #008000; /* Verde */
        height: 80px;
    }
    .azul {
        background-color: #0000ff; /* Azul */
        height: 118px;
    }
    .rojo, .morado, .gris {
        height: 85px;
        width: 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
    .rojo {
        background-color: #ff0000; /* Rojo */
    }
    .morado {
        background-color: #800080; /* Morado */
    }
    .gris {
        background-color: #808080; /* Gris */
    }

    /* Configuración del contenedor (body) como flexbox y distribución de los elementos */
    body {
        display: flex;
        flex-wrap: wrap;
    }
    .rosado, .verde, .azul, .rojo, .morado, .gris {
        box-sizing: border-box;
    }
    .rojo, .morado, .gris {
        flex: 1 0 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
}
Uso
Para ver la demostración, simplemente abre el archivo index.html en un navegador web. Redimensiona la ventana del navegador para ver cómo los estilos se adaptan a diferentes tamaños de pantalla.

Tecnologías Utilizadas
HTML5
CSS3 (incluyendo Flexbox y Media Queries)

Claro, aquí tienes un archivo README.md que explica el proyecto y cómo funciona el HTML y CSS:

markdown
Copiar código
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
Descripción del CSS
El archivo CSS media.css contiene las siguientes secciones:

Reset de estilos por defecto: Para asegurar que todos los elementos tengan un margen y padding de 0 y que el box-sizing sea border-box.
css
Copiar código
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
Media Queries para diferentes tamaños de pantalla:

Para pantallas de hasta 500px de ancho (móviles): Definimos un sistema de grilla y estilos específicos para móviles.
css
Copiar código
@media only screen and (max-width: 500px) {
    /* Ancho de las columnas en porcentajes, simulando un grid */
    .col-xs-1 {width: 8.33%;}
    .col-xs-2 {width: 16.66%;}
    .col-xs-3 {width: 25%;}
    .col-xs-4 {width: 33.33%;}
    .col-xs-5 {width: 41.66%;}
    .col-xs-6 {width: 50%;}
    .col-xs-7 {width: 58.33%;}
    .col-xs-8 {width: 66.66%;}
    .col-xs-9 {width: 75%;}
    .col-xs-10 {width: 83.33%;}
    .col-xs-11 {width: 91.66%;}
    .col-xs-12 {width: 100%;}

    /* Mostrar ciertos divs y ocultar otros en pantallas pequeñas */
    .rosado,.verde, .azul, .gris {
        display: block;
    }
    .rojo,.morado {
        display: none;
    }

    /* Estilos específicos para divs en pantallas pequeñas */
    .rosado,.verde {
        height: 100px;
    }
    .rosado {
        background-color: #ffc0cb; /* Rosado */
    }
    .verde {
        background-color: #008000; /* Verde */
    }
    .azul {
        background-color: #0000ff; /* Azul */
        height: 55px;
    }
    .gris {
        background-color: #808080; /* Gris */
        height: 146px;
    }
}
Para pantallas entre 501px y 750px de ancho (tablets): Utilizamos Flexbox para manejar la distribución de los elementos.
css
Copiar código
@media only screen and (min-width: 501px) and (max-width: 750px) {
    /* Estilos específicos para divs en tablets */
    .rosado,.azul,.verde,.rojo {
        height: 100px;
    }
    .rosado {
        background-color: #ffc0cb; /* Rosado */
        width: 100%;
    }
    .azul {
        background-color: #0000ff; /* Azul */
    }
    .verde {
        background-color: #008000; /* Verde */
    }
    .rojo {
        background-color: #ff0000; /* Rojo */
    }
    .morado,.gris {
        height: 85px;
    }
    .morado {
        background-color: #800080; /* Morado */
    }
    .gris {
        background-color: #808080; /* Gris */
    }

    /* Configuración del contenedor (body) como flexbox y distribución de los elementos */
    body {
        display: flex;
        flex-wrap: wrap;
    }
    .verde, .azul, .rojo {
        box-sizing: border-box;
        flex: 1 0 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
    .morado {
        flex: 1 0 60%; /* Ocupa el 60% del ancho del contenedor */
    }
    .gris {
        flex: 1 0 40%; /* Ocupa el 40% del ancho del contenedor */
    }
}
Para pantallas de más de 751px de ancho (escritorio): Definimos alturas y anchos específicos, y usamos Flexbox para la distribución.
css
Copiar código
@media only screen and (min-width: 751px) {
    /* Ancho completo para ciertos divs */
    .rosado, .verde, .azul {
        width: 100%;
    }

    /* Alturas específicas y colores de fondo */
    .rosado {
        background-color: #ffc0cb; /* Rosado */
        height: 20px;
    }
    .verde {
        background-color: #008000; /* Verde */
        height: 80px;
    }
    .azul {
        background-color: #0000ff; /* Azul */
        height: 118px;
    }
    .rojo, .morado, .gris {
        height: 85px;
        width: 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
    .rojo {
        background-color: #ff0000; /* Rojo */
    }
    .morado {
        background-color: #800080; /* Morado */
    }
    .gris {
        background-color: #808080; /* Gris */
    }

    /* Configuración del contenedor (body) como flexbox y distribución de los elementos */
    body {
        display: flex;
        flex-wrap: wrap;
    }
    .rosado, .verde, .azul, .rojo, .morado, .gris {
        box-sizing: border-box;
    }
    .rojo, .morado, .gris {
        flex: 1 0 33.33%; /* Cada uno ocupa un tercio del ancho del contenedor */
    }
}
Uso
Para ver la demostración, simplemente abre el archivo index.html en un navegador web. Redimensiona la ventana del navegador para ver cómo los estilos se adaptan a diferentes tamaños de pantalla.

Tecnologías Utilizadas
HTML5
CSS3 (incluyendo Flexbox y Media Queries)
Autor
Tu Nombre : Carlos Vasquez

Este `README.md` proporciona una descripción completa del proyecto, incluyendo la estructura de los archivos, una explicación del CSS, y cómo utilizar el proyecto.
