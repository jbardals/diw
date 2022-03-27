

# Maquetación con Bootstrap
## 1. Contenedores
https://getbootstrap.com/docs/5.1/layout/containers/

Un contenedor es el “padre” de todos los elementos de nuestra página web. Es una etiqueta que. como regla general, va a contener todas las otras etiquetas del contenido de nuestra página.

### Tipos de contenedores

BootStrap 5 nos ofrece 3 tipos de contenedores:

-   **container**  : Ocupará diferentes anchos dependiendo del tamaño de la pantalla. Puede ocupar todas la pantalla o dejar unos márgenes a izquierda a derecha aunque, en este caso, siempre estará centrado.

```
<body>

<div class="container">

</div>

</body>

```

-   **container-fluid**: Ocupará todo el ancho (100%) de lo que podemos ver en el navegador.

```
<body>

  <div class="container-fluid">

  </div>

</body>

```
-   **responsive containers**: permite especificar una clase que ocupa una anchura del 100% hasta alcanzar el breakpoint especificado

```
```html
<div class="container-sm">100% wide until small breakpoint</div>
<div class="container-md">100% wide until medium breakpoint</div>
<div class="container-lg">100% wide until large breakpoint</div>
<div class="container-xl">100% wide until extra large breakpoint</div>
<div class="container-xxl">100% wide until extra extra large breakpoint</div>
```

**IMPORTANTE:**  Aunque los contenedores se pueden anidar unos dentro de otros son pocas las páginas que son tan complejas para necesitar contenedores anidados.

## 2. Breakpoints
https://getbootstrap.com/docs/5.1/layout/breakpoints/

En el mundo del diseño responsivo un **breakpoint** es un tamaño de pantalla (en pixels) donde se produce un cambio en la disposición de los elementos que conforman nuestra página web.
En Bootstrap 5 se usan los siguientes:
![breakpoints](BS5_Breakpoints)

De **especial importancia** son los prefijos CSS de las clases **.col-*** 

- 
   ` .col-`  (extra small devices - screen width less than 576px)
-   `.col-sm-`  (small devices - screen width equal to or greater than 576px)
-   `.col-md-`  (medium devices - screen width equal to or greater than 768px)
-   `.col-lg-`  (large devices - screen width equal to or greater than 992px)
-   `.col-xl-`  (xlarge devices - screen width equal to or greater than 1200px)
-   `.col-xxl-`  (xxlarge devices - screen width equal to or greater than 1400px)
> Voy a escribir el enlace a google:

que son los que nos van a permitir establecer la anchura de los diferentes elementos que compongan nuestro layout. En definitiva son esas clases las que me proporciona BootStrap 5 para poder maquetar.

## 3. Márgenes y rellenos
BootStrap  añade clases que nos van a permitir modificar los márgenes y los paddings de las columnas. Según la documentación oficial son las _Utilidades de espaciado_.
https://getbootstrap.com/docs/5.1/utilities/spacing/
**Márgenes**
Para establecer los márgenes entre las columnas usaremos la clas  _m{lado}-{tamaño}_  o si queremos distinguir según los distintos tamaños de pantalla:

-   **m{lado}-sm-{tamaño}**  Para pantallas entre 576px y 768px.
-   **m{lado}-md-{tamaño}**  Para pantallas entre 768px y 992px.
-   **m{lado}-lg-{tamaño}**  Para pantallas entre 992px y 1200px.
-   **m{lado}-xl-{tamaño}**  Para pantallas de más de 1200px.

Pudiendo ser lado:

-   **t**  para margen superior (top).
-   **b**  para margen inferior (bottom).
-   **l**  para margen izquierdo (left).
-   **r**  para margen derecho (right).
-   **x**  para los márgenes superior e inferior.
-   **y**  para los márgenes izquierdo y derecho.
-   En blanco si es para todos los lados.

Y pudiendo ser tamaño de tamaño:

-   **0 :**  No hay margen
-   **1 :**  0.25rem
-   **2 :**  0.25rem
-   **3 :**  1rem
-   **4 :**  1.25rem
-   **5 :**  3rem
-   **auto :**  Para clases que establecen una margen auto

**Márgenes**
La notación de las clases para establecer los paddings en las columnas es muy similar a la notación de las clases para establecer márgenes entre las columnas. Simplemente tenemos que cambiar la **_m_** por la **_p_**

## 4. Grid system de 12 columnas
https://getbootstrap.com/docs/5.1/layout/grid/

 Consiste en dividir la pantalla en filas, donde cada fila puede dividirse en 12 columnas o espacios.
El sistema de rejilla está pensado para ayudarnos en la disposición de los contenidos de nuestra web y su adaptación a los diferentes tamaños de pantalla de forma
automática. A continuación se detalla el funcionamiento de este sistema:

- Las columnas irán agrupadas dentro de filas (.row).
- Las filas (.row) se deben colocar dentro de una etiqueta contenedora, esto permitirá alinear las celdas y asignarles el espaciado correcto.
- El contenido se debe disponer dentro de columnas o celdas, las cuales deben de ser el único hijo posible de las filas (.row).
- Cada fila se puede dividir "hasta un máximo" de 12 columnas, pero somos nosotros los que tendremos que definir el número de columnas en el que queremos dividir cada fila y su ancho para cada tamaño de pantalla
- Si el tamaño total de las columnas de una fila excede de 12 el tamaño sobrante se colocará en la siguiente fila
- El tamaño de las columnas se especificará con clases CSS que Bootstrap define para cada tamaño de pantalla, por ejemplo .col-md-XX, donde XX es el tamaño de la columna, que podrá tomar valores entre 1 y 12

### Tamaño definido por el usuario
Podemos establecer el tamaño de cada uno de los componentes de las row o filas y además, podemos establecer distintos tamaños dependiendo del tamaño de nuestra pantallas.
Si establecemos un tamaño para un cierto tamaño de pantallas ese tamaño se va a mantener para pantallas de mayor tamaño pero para pantallas menores ese div ocupará toda la pantalla
Ejemplo:
```

  <div class="col-sm-6 col-md-4 col-xl-3">
  </div>

```

En este caso ese div:

-   Ocupará la mitad de la fila para pantallas en 576px y 768px
-   Ocupará un tercio de la fila para pantallas entre 768px y 992px
-   Ocupará un cuarto para pantallas mayores de 992px
**pero**
- Ocupará toda la fila para pantallas extrapequeñas (<576px)

También es importante recordar que si, en un_row  nos pasamos de 12 columnas ese elemento que provoca que nos pasemos de las 12 columnas “pasará”  debajo de los elementos de la fila actual ocupando el tamaño establecido.

Así por ejemplo si tenemos la siguiente estructura:

```
  <div class="row">
    <div class="col-md-6">
    </div>
    <div class="col-md-4">
    </div>
    <div class="col-md-4">
    </div>
  </div>

```

El tercer div irá abajo ya que 6+4+4 = 14 que es mayor que 12.

### Tamaño auto
Usando elementos en los que no especifiquemos el número de columnas, el espacio que haya en la fila se va a distribuir de manera uniforme.

-   **col :**  Para todo tipo de pantallas
-   **col-sm :**  De pantallas pequeñas en adelante (>=576px)
-   **col-md :**  De pantallas medianas en adelante (>=768px)
-   **col-lg :**  De pantallas grande en adelante (>=992px)
-   **col-xl :**  Para pantallas de 1200px en adelante
Ejemplo:
```

<div class="row">
    <div class="col red">
    </div>
    <div class="col black">
    </div>
</div>

```

En este caso en cualquier tipo de pantallas esos dos elementos se repartirán a igual manera el ancho del contenedor principal.

```

<div class="row">
    <div class="col-md yellow"></div>
    <div class="col-md pink"></div>
    <div class="col-md yellow"></div>
    <div class="col-md pink"></div>
    <div class="col-md yellow"></div>
</div>

```

En este caso todo se divide en 5 partes para pantallas menores de 768px pero en cuanto la pantalla es más pequeña que eso, todos los elementos pasarán a ocupar todo el centro de la pantalla.

Este funcionamiento abre la puerta a  _rows_  (filas) que tengan más de 12 columnas, por ejemplo una fila con 14 componentes:

### Tamaño por contenido
Podemos también ajustar el tamaño de las columnas al contenido de las mismas usando  _col-{breakpoint}-auto_. Así por ejemplo:

```
<div class="row">
  <div class="col-md-auto">Anchura ajustada</div>
  <div class="col-md-auto">Al contenido</div>
  <div class="col-md-auto">De las celdas que contiene la columna</div> 
</div>
```

**IMPORTANTE:**  Debemos tener mucho cuidado cuando mezclemos tamaños automáticos junto tamaños, definidos por el usuario porque cuanto no quepan las columnas (y puede que no sumen 12) pasarán a la siguiente fila y se repartirán el espacio de la siguiente fila -> **column wrapping**

## 4. Columnas
https://getbootstrap.com/docs/5.1/layout/columns/
### Saltos de línea
Si mientras estamos construyendo nuestro grid y queremos que haya un salto de línea podemos forzarlo de la siguiente manera:
```

<div class="row">

  <!-- Ocupamos 5/12 de la fila -->
  <div class="col-md-3"></div>
  <div class="col-md-2"></div>

  <!-- Forzamos el salto de línea -->
  <div class="w-100"></div>

  <!-- Ocupamos otra vez 5/12 pero en una nueva línea -->
  <div class="col-md-3"></div>
  <div class="col-md-2"></div>


</div>

```
### Alineación horizontal y vertical
BootStrap utiliza contenedores flex. Las *filas* serán **flex containers** y las *columnas* **flex items** 

Podremos añadir una nueva clase al contenedor  _row_  para cada tipo de alineación.

-   Alineación horizontal de los elementos de la fila con -> **justify-content**
- Alineación vertical de los elementos de la fila con -> **align-items**

añadiendo una nueva clase al contenedor  _row_  o fila.

### Desplazamiento -> offset
Hemos visto en apartados anteriores cómo podemos dar diferentes tamaños a los distintos componentes o columnas de una  _row_  o fila.

Adicionalmente podemos establecer no sólo el tamaño de la columna si no también la posición a partir de la cuál se va a posicionar.

Para conseguir eso debemos añadir la clase  _offset-X_  donde X es el número de columnas a la izquierda que desplazaremos el elemento que queremos posicionar.
Este desplazamiento puede ser también establecido de manera diferente para cada tamaño de pantalla:

-   **offset-sm-X :**  Para desplazamientos para pantallas entre 576px y 768px.
-   **offset-md-X :**  Para desplazamientos para pantallas entre 768px y 992px.
-   **offset-lg-X :**  Para desplazamientos para pantallas entre 992 y 1200px.
-   **offset-xl-X :**  Para desplazamientos para pantallas mayores de 1200px.
Ejemplo:

```

<div class="container-fluid">
  <div class="row">
    <div class="col-sm-4 offset-md-1 red"></div>
    <div class="col-sm-4 offset-sm-4 offset-md-2 blue"></div>
  </div>
</div>

```

En este ejemplo para pantallas mayores de 768px el primer div está desplazado una columna a la izquierda y ambos bloques se separan dos columnas mediante el uso de un desplazamiento de dos columnas en el segundo bloque.

Además para pantallas entre 576px y 768px no hay desplazamiento para el primer bloque y hay un desplazamiento de 4 columnas para el segundo bloque consiguiendo, de esta forma que ese bloque quede totalmente pegado a la derecha.

### Ordenación
Usa `.order-` clases para controlar el **orden visual** de las columnas. Estas clases son responsive, así que permiten el uso de breakpoint (e.g., `.order-1.order-md-2`).

### Espaciado -> Gutter
BootStrap introduce separación entre el contenido de las columnas mediante _paddings_ y márgenes a derecha e izquierda. Es lo que se denomina *gutter*.
Podemos evitarlo añadiendo al elemento que tenga la clase  *row*  la clase *no-gutters* .Así las columnas o elementos de la fila no tendrán ese padding con la posibilidad de que el contenido de la misma queden pegados.
Un ejemplo sería:

```

<div class="container">
  <div class="row">
    <div class="col-md-6"><h3>Elemento con Gutter</h3></div>
    <div class="col-md-6"><h3>Elemento con Gutter</h3></div>
  </div>

  <div class="row no-gutters">
    <div class="col-md-6"><h3>Elemento sin gutter</h3></div>
    <div class="col-md-6"><h3>Segundo Elemento</h3></div>
  </div>

</div>
```

 1. kkkk
 2. jjhjhjh
 3. 
ghjgghjhjgjgh
# h1
## h2
### h3
> [enlace a google](www.google.es)
> 
 4. List item




<dl>

<dt>elefono</dt>

<dd>9999999</dd>

<dt>email</dt>

<dd>pepito@gmail.com</dd>

</dl>
`
