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

- **Colores Personalizables**: Los colores principales (`main`, `secondary`, `tertiary`) son fáciles de modificar según las preferencias del usuario. La plantilla incluye una paleta de colores agradables ya definidos, como `blue`, `red`, `green`, entre otros.

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
