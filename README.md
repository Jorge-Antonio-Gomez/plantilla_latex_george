# Plantilla LaTeX George

## Descripción del Repositorio

El repositorio `plantilla_latex_george` contiene una plantilla en LaTeX diseñada para la creación y presentación de tareas académicas. Esta plantilla está especialmente pensada para estudiantes que deseen mejorar la calidad y el aspecto visual de sus entregas académicas, proporcionando una organización clara de secciones, el uso de colores estéticos y elementos visuales como cajas resaltadas que mejoran la presentación del contenido. Proporciona una estructura bien definida que facilita la organización del contenido, como la inclusión de secciones para problemas, ejemplos, notas y definiciones. Además, incluye personalizaciones que mejoran la estética del documento, como el uso de cajas resaltadas y líneas divisorias.

La plantilla es altamente personalizable, con funcionalidades para resaltar conceptos importantes, incluir ejemplos y notas, presentando la información de manera clara y profesional. Es ideal para cursos de matemáticas, economía y otras disciplinas donde sea necesario un enfoque riguroso y estéticamente agradable.

## Contenido del Repositorio

- **`main.tex`**: Archivo principal que contiene la estructura de la plantilla. Incluye ejemplos de cómo organizar problemas, soluciones, definiciones y notas.
- **`preamble.tex`**: Archivo con la configuración inicial, incluyendo paquetes utilizados, estilos de letra, colores y definiciones de comandos personalizados.
- **`img/`**: Carpeta donde se pueden almacenar las imágenes que se quieran incluir en el documento y donde se encuentran los fondos de página.

## Características Principales

- **Uso de `tcolorbox`**: La plantilla utiliza cajas (`tcolorbox`) para resaltar definiciones, notas y ejemplos, ayudando a diferenciar claramente los distintos elementos del contenido. Las cajas son personalizables en términos de color, estilo y bordes, con tres colores principales definidos: `main`, `secondary` y `tertiary`.

  ```LaTeX
  \begin{tcolorbox}[colback=main!5!white, colframe=main!75!black, title=\textbf{Título de caja}, toptitle=1.5mm, bottomtitle=1.5mm, breakable]
    
    Esto es texto.

    \tcbsubtitle{Subtítulo de la caja}
    Más texto.

    \tcblower
    Texto final.

  \end{tcolorbox}
  ```

- **Colores Personalizables**: Los colores principales (`main`, `secondary`, `tertiary`) son fáciles de modificar según las preferencias del usuario. La plantilla incluye una paleta de colores agradables ya definidos, como `blue`, `red`, `green`, entre otros.

  Este código define macros y colores para facilitar la personalización estética de documentos en LaTeX. La idea principal es definir colores consistentes que puedan ser utilizados a lo largo del documento, asegurando una apariencia visual atractiva y profesional. A continuación, se detallan las partes más importantes del código:
  
  #### Definición de Nombres de Colores
  
  - **`\maincolorname`**: Se define el color principal del documento. En este caso, es `blue`.
  - **`\secondarycolorname`** y **`\tertiarycolorname`**: Se asigna `\maincolorname`, lo que significa que tanto el color secundario como el terciario por defecto serán iguales al color principal. Si se desea cambiar estos colores, simplemente se reemplaza el valor de la macro.
  - **`\bgcolorname`**: Define el color de fondo, que por defecto también es el color principal (`\maincolorname`). Esto permite uniformidad visual en la mayoría de los elementos del documento.
  
  #### Definición de Colores Específicos
  
  El código también define una serie de colores específicos en formato RGB mediante el comando `\definecolor`. Estos colores pueden ser usados en el documento para diferentes propósitos, tales como texto, títulos, fondos de cajas (`tcolorbox`), etc. Los colores definidos incluyen:
  
  - **`blue`**: Color azul agradable (#0072B2).
  - **`red`**: Color rojo agradable (#D55E00).
  - **`gray`**: Color gris (#808080).
  - **`orange`**: Color naranja agradable (#E69F00).
  - **`green`**: Color verde agradable (#00AAA6).
  - **`darkgreen`**: Color verde oscuro agradable (#007642).
  - **`yellow`**: Color amarillo agradable (#F0E442).
  - **`purple`**: Color morado agradable (#7100B2).
  - **`pink`**: Color rosa agradable (#CB4EBC).
  - **`brown`**: Color marrón agradable (#8C613C).
  - **`cyan`**: Color cian agradable (#44D3CB).
  
  Estos colores han sido seleccionados para ofrecer una paleta visual atractiva y que no sea agresiva para el lector, buscando una buena combinación que sea útil en entornos académicos o profesionales.
  
  El código también se puede expandir o modificar para añadir colores adicionales según las necesidades del usuario, y estos colores pueden ser referenciados en cualquier parte del documento utilizando los comandos de color de LaTeX.

- **Fondo Personalizable**: La plantilla permite establecer un fondo personalizado para cada página, utilizando imágenes específicas para diferentes colores (`bgcolor`). Esto se puede ajustar desde el preámbulo usando el comando `\setbackgroundimage`.

- **Divisiones Estéticas**: Se utilizan líneas divisorias (`\HRuleGray`) para hacer el documento más agradable y legible. Estas líneas grises ayudan a dividir las secciones de manera visualmente atractiva.

- **Formato Claro y Consistente**: Títulos, subtítulos y secciones están claramente definidos para garantizar una estructura ordenada. Se utiliza el paquete `titlesec` para personalizar el formato de los títulos, utilizando colores y líneas divisorias para mejorar la legibilidad.

- **Listas y Tablas Personalizadas**: Las listas (`itemize`, `enumerate`) y tablas están configuradas para mantener un estilo visual coherente con el resto del documento, incluyendo colores personalizados para los símbolos y líneas de tablas.

- **Cajas para Código (`lstlisting`)**: La plantilla incluye configuraciones para resaltar código fuente, utilizando el paquete `listings`. Por ejemplo, el siguiente fragmento de código R:

  ```r
  \begin{lstlisting}[style=userR]
    # Ejemplo de código R
    x <- seq(0, 10, by = 0.1)
    y <- sin(x)
    plot(x, y, type = 'l', col = 'blue', lwd = 2)
  \end{lstlisting}
  ```
# Front Page

Puede modificar la parte inicial del documento en  `\FrontPage`. Más documentación sobre el comando a continuación: [Documentación de `\FronPage`](/FrontPage.md)
