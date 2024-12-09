
# Ejemplo del código de un Archivo ".svg"
```
<svg
   width="198mm"
   height="166mm"
   viewBox="0 0 198 166"
   version="1.1"
   xmlns="http://www.w3.org/2000/svg">
  <g transform="matrix(2.2373964,0,0,2.2374086,-1351.9834,-2209.4334)">
    <path
       style="fill:#fb9c08"
       d="m 647.75482,988.4343 -14.19848,24.169 h 6e-5 l -6.8e-4,17.3938 h -10.21745 l -18.15292,30.901 h -10e-5 l 42.56957,10e-5 z" />
    <path
       style="fill:#653097"
       d="m 623.33811,1012.6033 v 17.3938 l 10.21823,-17.3938 z" />
    <path
       style="fill:#653097"
       d="m 663.88003,1012.6033 v 17.3938 h 10.21813 l 18.15101,30.9009 h -42.5676 v -72.4637 z" />
    <path
       style="fill:#fb9c08"
       d="m 674.0981,1012.6033 v 17.3938 l -10.21825,-17.3938 z" />
  </g>
</svg>

```
# Explicación


- **SVG principal**: `<svg>` define el área de dibujo y sus dimensiones.
- **Agrupación**: `<g>` agrupa elementos para aplicar transformaciones como la escala y la traslación.
- **Figuras**: `<path>` define los contornos de las formas usando comandos de coordenadas y estilos de relleno.


#### 1. `<svg>`
La etiqueta `<svg>` es la raíz de un documento SVG (Scalable Vector Graphics), que se utiliza para dibujar gráficos vectoriales. 

Este SVG contiene una transformación y cuatro figuras dibujadas con diferentes colores, y las formas están definidas por caminos (`path`) que siguen coordenadas precisas. Estas propiedades definen el ancho y alto del lienzo
- **`viewBox`**: Define el área de dibujo, estableciendo las coordenadas mínimas y máximas del gráfico en un sistema de referencia. Aquí, el área de dibujo va de 0 a 198 unidades de ancho y de 0 a 166 unidades de alto.
- **`version`**: Indica la versión del SVG, en este caso es la 1.1, que es una versión comúnmente utilizada.
- **`xmlns`**: Especifica el espacio de nombres para el SVG. Básicamente, le dice al navegador que esto es un documento SVG.

#### 2. `<g>`
La etiqueta `<g>` agrupa varios elementos juntos. Esto permite aplicar transformaciones (como traslaciones o escalados) a todos los elementos del grupo de una sola vez.

### Atributos:
- **`transform`**: Este atributo aplica una transformación al grupo completo. En este caso, hay una matriz de transformación que escala y traslada el gráfico.

#### 3. `<path>`
La etiqueta `<path>` es la que define las formas o figuras en un SVG a través de coordenadas y comandos que crean líneas, curvas o cualquier otro contorno.

#### Atributos:
- **`style`**: Este atributo define el estilo de la figura, en este caso, se usa para aplicar un color de relleno. Por ejemplo, `fill:#fb9c08` significa que la forma se llenará con un color naranja (#fb9c08) y `fill:#653097` corresponde a un color morado (#653097).
- **`d`**: Este es el atributo más importante del `<path>`, ya que describe el camino que va a seguir la figura usando comandos y coordenadas. Por ejemplo, `m 647.75482,988.4343` es un comando que mueve el punto inicial de la figura a las coordenadas (647.75, 988.43), y los comandos subsiguientes indican cómo dibujar la figura.




