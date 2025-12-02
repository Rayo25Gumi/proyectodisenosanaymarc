Guía de Estilo – RetroBlog

#1. Identidad Visual

Inspirada en la estética de las consolas clásicas: colores vivos, sensación de nostalgia y una presentación clara y accesible. La interfaz combina tonos azulados y elementos suaves que evocan la era de los 80 y 90.


##1.1 Paleta de Colores

-->Tema Claro


Fondo principal: #99ccff – Azul claro retro utilizado en el fondo general de la página (--fondo).

Texto principal: #002244 – Azul muy oscuro para garantizar buena legibilidad (--texto).

Tarjetas y bloques de contenido: #4da6ff – Azul medio para artículos, header, footer y aside (--tarjeta).

Enlaces: #0055cc – Azul intenso para elementos clicables (--links).

Títulos: #004080 – Azul profundo para encabezados (--titulo).

Fondo semitransparente de submenús: rgba(153, 204, 255, 0.9) – Usado en el menú desplegable de “Artículos” (--semitransparente). 

Tarjeta secundaria (artículos): #66b3ff – Color utilizado en algunos bloques de texto secundarios (--tarjeta2, cuando está definido en las variables del proyecto).



-->Tema Oscuro

Fondo principal: #0a1a33 – Azul marino muy oscuro.

Texto principal: #cce6ff – Azul claro para alto contraste sobre el fondo.

Tarjetas: #3380ff – Azul vibrante para mantener la estética retro.

Enlaces: #3366cc – Azul medio adaptado al modo oscuro.

Títulos: #154db8 – Azul brillante para destacar los encabezados.



##1.2 Tipografía

RetroBlog emplea una tipografía moderna pero sencilla que combina bien con la temática retro.

>Familia: Inter, con fallback a sans-serif.

- Tamaños:

>Texto base: 16px (párrafos).

>Texto pequeño: 14px (footer y textos secundarios).

>Texto grande: 18px (si se necesita resaltar algún párrafo).

>H1: entre 2rem y 2.5rem, usado en títulos principales (por ejemplo, “Retroblog! | El mundo de las consolas retro”). 

>H2: alrededor de 1.6rem–2rem para subtítulos.

>Altura de línea general: 1.5, definida en el body para mejorar la legibilidad.


#2. Componentes

##2.1 Header

-Fondo dependiente del tema (claro u oscuro).

-Navegación en línea mediante Flexbox.

-Logo a la izquierda.

-Enlaces principales visibles en todo momento.

-Submenú con fondo semitransparente.

-Iconos sociales alineados a la derecha.



##2.2 Menú de artículos (submenú)

-->El menú “Artículos” se implementa con una lista <ul> dentro de un contenedor .menu. 


-El submenú (.submenu) permanece oculto por defecto (display: none).

-Mediante la pseudoclase :hover sobre el <li> padre, el submenú se muestra:

>position: absolute;

>Fondo rgb(var(--semitransparente)).

>Bordes redondeados y sombra.

>Espaciado interno y transición suave. 




Cada opción del submenú enlaza a uno de los artículos:

-----NES

----Game Boy

----SEGA Mega Drive vs Super Nintendo

----PlayStation 1




##2.3 Artículos

-Dispuestos dentro de un contenedor tipo tarjeta.

-Fondo según variable --tarjeta.

-Bordes redondeados y sombra suave.

-Imagen principal grande y destacada arriba.

-Imagen secundaria dentro del contenido del artículo.

-Títulos centrados y con color definido por --titulo.




##2.4 Sidebar (Aside)

-Distribución vertical mediante flex-direction: column.

-Lista de artículos con espaciado constante.

-Fondo igual que el resto de tarjetas del tema.

-Sirve como navegación complementaria.




##2.5 Footer

-Fondo según tema seleccionado.

-Texto centrado.

-Tamaño reducido (14px).

-Espaciado interno uniforme.






#3. Layout

##3.1 Sistema Principal

-->Layout construido con Flexbox:

>Columna principal → artículos

>Columna secundaria → sidebar



##3.2 Anchuras

-Artículos centrados con anchura aproximada del 70%.

-Espaciados consistentes entre secciones.



##3.3 Responsive
Las imágenes son 100% adaptables (width: 100%).







#4. Interacciones

##4.1 Estilos de Enlaces

-Color: var(--links)

-Sin subrayado

-Hover: colores del tema + submenú semitransparente






#5.  Accesibilidad

- Uso de etiquetas semánticas: `<header>`, `<main>`, `<article>`, `<aside>`, `<footer>`.   
- Imágenes con atributo `alt` descriptivo (logo, consolas, iconos de redes).
- Contraste texto/fondo controlado mediante variables para ambos temas.
- Tamaño de fuente suficiente para lectura cómoda







#6. Convenciones de Código

##6.1 Organización SCSS

_variables.scss: colores y variables globales.

_base.scss: estilos universales y reset.

_layout.scss: estructura de página.

_components.scss: slider, tarjetas, imágenes, etc.

main.scss: importa todos los anteriores.



##6.2 Buenas Prácticas

-Código modular.

-Reutilización de variables (var(--fondo), var(--texto), etc.).

-Imágenes optimizadas.






#7. Resumen del Objetivo

Esta guía asegura que todo el sitio mantenga una estética uniforme y reconocible.
---> Facilitar futuras modificaciones o ampliaciones sin romper la identidad del blog.





