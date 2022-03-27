# Contenidos Bootstrap 

##  Texto, tipografía y colores
https://getbootstrap.com/docs/5.1/content/typography/


## Imágenes y figuras
https://getbootstrap.com/docs/5.1/content/images/
### Imágenes

En relación a las imágenes las clases de interés son:

-   **img-fluid :**  Que nos permite convertir una imagen en responsiva. Al añadir esa clase a una imagen ésta ocupará toda la anchura de su elemento padre manteniendo sus proporciones (aspect ratio).Si hemos utilizado la etiqueta  _picture_  debemos añadir esta clase a la  _img_  que contiene y no a  _picture_.
-   **img-thumbnail :**  Para añadir un marco redondeado a la imagen. Para esto podríamos también usar las clases relativas a bordes que veremos posteriormente en el capítulo sobre utilidades.
-   **rounded .**  Si queremos que las esquinas sean redondeadas.
Se puede instalar de formas diferentes. En esta sección veremos los dos métodos más utilizados: su CDN (Content Delivery Network) y descargando el código en local. En la página web oficial de Bootstrap (getbootstrap.com) se pueden ver todas las formas de distribución.

### Figures
Una  **figura**  (etiqueta  **_figure_**) es un conjunto compuesto de una imagen (etiqueta  **_img_**) y de un texto descriptivo sobre la imagen (etiqueta  **_caption_**). Esta etiqueta es una de las novedades en HTML5.Tradicionalmente es lo que se usa en  _libros_  para hacer posteriormente un índice de figuras.

```

  <figure>
    <img src="ejemplo.png">
    <figcaption>Texto descriptivo de la imagen</figcation>
  </figure>
```
En relación a las figuras las clases de interés para dar estilos con BootStrap son:

-   **figure :**  Clase a añadir a la etiqueta  _figure_.
-   **figure-img :**  Clase a añadir a la etiqueta  _img_  que contiene la figura.
-   **figure-caption :**  Clase añadir a la etiqueta  _figcation_  que contiene la figura. El texto se podrá adicionalmente alinear de distintas maneras usando  _text-justify_,  _text-left_,  _text-right_  o  _text-center_.

**IMPORTANTE :**  Si queremos que esto siga siendo responsivo debemos añadir  _.img-fluid_  a la imagen de la figura

## Tablas
https://getbootstrap.com/docs/5.1/content/tables/

Mediante el uso de clases BootStrap  podemos dar distintos estilos a las tablas y hacerlas responsivas.

Estas clases relacionadas con tablas son muchas y en este apartado únicamente vamos a ver las más destacadas.

### Haciendo que la tabla sea tabla Bootstrap

Simplemente debemos añadir la clase  **_table_**  y adicionalmente la clase  **_table-dark_**  si queremos que se inviertan los colores de fondo y de letra.

```

  <table class="table">
      .....      
  </table>

```
### Clases para la cabecera de las tablas

Para dar estilos a las cabecera de las tablas tenemos que las clases  **_thead-light_**  o  **_thead-dark_**  a la etiquetas de las filas (_tr_) o a las etiquetas (_thead_).

```

  <thead class="thead-light">
      <tr>
        <th>...</th>
        ......
      </tr>
  </thead>

```
**IMPORTANTE :** Este estilo sólo se aplica a la etiqueta _th_ (celdas de cabecera)
### Alternado colores

Si queremos que las filas de las tablas tengan colores alternativos para poder distinguirlas mejor debemos añadir la clase  **_table-striped_**  a la etiqueta  _table_. Esto funcionará también para tablas oscuras (clase  _table-dark_).

```

  <table class="table table-striped">
      .....      
  </table>

```

### Destacar (Hover)

Si queremos que conforme pase el puntero de ratón por encima de una fila (que no sea la cabecera) esa fila de destaque cambiando ligeramente de color debo añadir las clase  **_table-hover_**  a las etiqueta  _table_.

```

  <table class="table table-hover">
      .....      
  </table>

```
### Bordes de las tablas

Por defecto en BootStrap las tablas únicamente muestran unos ligeros bordes inferiores en las filas para separar estas. Si, por el contrario, queremos que todas las celdas muestren los 4 bordes (inferior,superior, derecha e izquierda) debemos añadir la clase  **_table-bordered_**  a la etiqueta  _tabla_.

```

  <table class="table table-bordered">
      .....      
  </table>

```
### Haciendo las tablas responsivas

Existen distintas técnicas para hacer las tablas responsivas pero los desarrolladores de BootStrap han optado porque aparezca un scroll horizontal cuando sea necesario.

Para conseguir esto debemos insertar nuestra tabla dentro un div con las clase BootStrap  **_table-responsive_**

```
  <div class="table-responsive">
    <table class="table table-bordered">
        .....      
    </table>
  </div>

```

También puedo fijar el breakpoint a partir de la cual quiero que la tabla sea responsiva. En esos casos usaré:

-   **_table-responsive-sm_**
-   **_table-responsive-md_**
-   **_table-responsive-lg_**
-   **_table-responsive-xl_**

## Formularios
BootStrap proporciona una serie de clases para dar estilos a los distintos elementos de los formularios. De manera general podemos describir estas clases y la jerarquía que deben ocupar de la siguiente manera:
![Jerarquias_Clases_BS_Formularios](Jerarquias_Clases_BS_Formularios.jpg)

Además, se le añadirá al final un  _input_  de tipo  _submit_  o  _button_  con las clases correspondientes a los botones cuyos ejemplos más comunes (hay muchos más) son:

-   **btn btn-primary**
-   **btn btn-secondary**
-   **btn btn-success**
-   **btn btn-danger**
-   **btn btn-warning**

Podemos además modificar ciertos aspectos de estos componentes del formulario. Los más interesantes son los siguientes.

-   **Modificar el tamaño en altura del control**. Añadiendo clases como  **_form-control-lg_**  (grande) o  **_form-control-sm_**  (pequeños) en los  _form-control._
    
-   **Modificar el tamaño en altura de la etiqueta del control**. Usando clases como  **_col-label-lg_**  (grandes) o  **_col-label-sm_**  (pequeños).
    

-   **Hacer que todos los elementos del formulario se vean en la misma línea**  añadiendo la clase  **_form-inline_**  a la etiqueta form.

-   **Hacer que las distintas opciones para elementos  _radio_  o  _checkbox_  se vean en la misma línea**  añadiendo al div que tenía la clase  _form-check_  la clase  **_form-check-inline_**
    
-   **Añadir texto de ayuda a los diferentes elementos**  usando un etiqueta small dentro del  _form-group_  o  _form-check_  y dando a esa etiqueta las clases  **_form-text_**  y  **_text-mute_**.
    

En cuanto a su disposición, los formularios por defecto ocupan en anchura lo que ocupen el contenedor padre al que corresponden pero podemos adaptar su tamaño jugando con el grid de BootStrap añadiendo clases  **_col-X_**  (o atendiendo a distintos breakpoints) al elemento que contenga la clase  _form-group_  o  _form-check_.

Para hacer los formularios más compactos hay una nueva clase que suprime el gutter,  **_form-row_**  que debe ser usada en vez de  _row_.
