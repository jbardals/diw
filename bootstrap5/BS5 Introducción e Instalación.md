# Bootstrap 5
Bootstrap (http://getbootstrap.com/) es uno de los frameworks de HTML, CSS y JavaScript más populares actualmente. Gracias a este framework, desarrollado por
Twitter, podemos crear interfaces ahorrando tiempo al utilizar recursos desarrollados previamente: clases CSS, componentes JavaScript, repositorios de
tipografías y botones, etc. Bootstrap ha sido creado para ofrecer la mejor experiencia de usuario (UX) tanto en versión escritorio, como en tabletas y smartphones.
Bootstrap es responsive (permite crear páginas web adaptables a cualquier dispositivo) y compatible con los navegadores más utilizados.

## Por qué Bootstrap
**Ventajas**

-   Fácil de usar
-   Bien documentado y mantenido (ver repo en github)
-   Usado en múltiples páginas de múltiples sitios web

aunque

-   Páginas uniformes por defecto -> habrá que customizar temas para mejorar SEO.

**Bootstrap usa:**

-   Flexbox -> todos los componentes de la misma fila misma altura automáticamente
-   Preprocesador SaaS
-   Unidad de medida del tamaño de las fuentes: **rem** (ref: font-size del elemento root)
-   Nuevos componentes: cards, carrouseles,  tooltips..
-   Javascript ES6

## Tipos de instalación
Se puede instalar de formas diferentes. En esta sección veremos los dos métodos más utilizados: su CDN (Content Delivery Network) y descargando el código en local. En la página web oficial de Bootstrap (getbootstrap.com) se pueden ver todas las formas de
distribución.
### 1. Forma más rápida: utilizando CDN
La forma más sencilla de utilizar Bootstrap es utilizando su red de distribución de contenidos o **CDN** (del inglés Content Delivery Network). El inconveniente es que se necesita Internet para que funcione correctamente. Este método se suele utilizar para realizar pruebas rápidas.
Para utilizar la CDN de Bootstrap lo único que debemos hacer es copiar, en la cabecera del archivo HTML de nuestro proyecto, el código que se indica en el siguiente enlace:
https://getbootstrap.com/docs/5.1/getting-started/introduction

### 2. Descarga del código para desarrollo
Permite implementar nuestras páginas de forma local sin
necesidad de utilizar Internet

Para ello, podemos descargar el código con la opción de “CSS y JS compilado” desde https://getbootstrap.com/docs/5.1/getting-started/download/
Después de descomprimir el archivo descargado con la versión compilada de Bootstrap, verás una estructura de archivos y directorios similar a la siguiente:
bootstrap/
	|-->css/
		|-->bootstrap.css
		|-->bootstrap.min.css
		|-->bootstrap-grid.css
		|-->bootstrap-grid.min.css
    |-->js/
		|-->bootstrap.js
		|-->bootstrap.min.js

Estos archivos son la forma más sencilla de utilizar Bootstrap en cualquier proyecto web. Para cada archivo se ofrecen dos variantes: los archivos compilados (cuyo
nombre es bootstrap.*) y los archivos compilados + comprimidos (cuyo nombre es
bootstrap.min.*).
