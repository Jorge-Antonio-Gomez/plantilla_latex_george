# Plantilla LaTeX George

## Descripción del Repositorio

El repositorio `plantilla_latex_george` contiene una plantilla en LaTeX diseñada para la creación y presentación de documentos académicos del Centro de Investigación y Docencia Económicas (CIDE). Esta plantilla está especialmente pensada para estudiantes y académicos que deseen mejorar la calidad y el aspecto visual de sus entregas académicas, proporcionando una organización clara de secciones, el uso de colores estéticos y elementos visuales como cajas resaltadas que mejoran la presentación del contenido. Proporciona una estructura bien definida que facilita la organización del contenido, como la inclusión de secciones para problemas, ejemplos, notas y definiciones. Además, incluye personalizaciones que mejoran la estética del documento, como el uso de cajas resaltadas y líneas divisorias.

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

- **Interlineado Configurable**: La plantilla incluye configuración personalizable del interlineado del documento. Por defecto está configurado con `\singlespacing`, pero se puede cambiar fácilmente a `\onehalfspacing` o `\doublespacing`. Además, permite configurar el interlineado específico en cualquier parte del documento usando `\setstretch{valor}`.

- **Notas al Pie Personalizadas**: Las notas al pie están completamente personalizadas con:
  - Colores personalizados para los símbolos y texto de las notas al pie
  - Numeración arábiga en lugar de símbolos
  - Interlineado específico para las notas (`\footnotelayout`)
  - Separación y márgenes configurables

- **Mejoras en Tablas y Figuras**: 
  - **Tablas**: Se ha añadido soporte para `threeparttable`, `tabularx`, `tablefootnote` y `adjustbox` para crear tablas más profesionales. Las tablas ahora se llaman "Tabla" en lugar de "Cuadro".
  - **Figuras**: Soporte mejorado para subfiguras con `subcaption` y figuras flotantes con `wrapfig`.
  - **Leyendas**: Tamaño de fuente personalizable para todas las leyendas.

- **Definiciones Matemáticas**: Se incluyen comandos predefinidos para conjuntos matemáticos comunes:
  - `\R` para números reales
  - `\N` para números naturales  
  - `\Z` para números enteros
  - `\Q` para números racionales
  - `\C` para números complejos
  - `\E` para esperanza matemática
  - `\qed` para símbolo de fin de demostración

- **Tags de Ecuaciones Coloreados**: Las etiquetas de ecuaciones (`\tag{}`) automáticamente usan el color principal del documento.

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

- **Fórmula para cancelar símbolos**: El comando `\CancelTo` sirve para cancelar partes de ecuaciones de modo que se puedan colorear. Su sintaxis de uso es la siguiente: `\CancelTo[<color>]{<resultado>}{<expresión>}`.
  El comando toma tres argumentos: el primero (opcional) para definir el color del tachado, el segundo para especificar el resultado que aparecerá encima de la flecha que indica hacia dónde "cancelar", y el tercero es el símbolo o fórmula que se desea tachar. Un ejemplo es `\CancelTo[\color{red}]{0}{x} + 5 = 5`, el cuál cancela a cero la `x`.

## Configuración del Documento

### Personalización del Encabezado

La plantilla permite configurar fácilmente los elementos principales del documento:

```latex
% Configuración en main.tex
\newcommand{\asignatura}{Nombre de la Asignatura}
\newcommand{\titulo}{Título del Documento}
\newcommand{\autor}[1][]{Nombre del Autor\\Centro de Investigación y Docencia Económicas}

% Configuración opcional de fecha
% \date{} % Vacío usa la fecha actual
% \date{Fecha personalizada}
```

### Control del Interlineado

```latex
% En cualquier parte del documento:
\setstretch{1.2} % Configura interlineado específico

% O usando comandos predefinidos en el preámbulo:
\singlespacing    % Interlineado simple (por defecto)
\onehalfspacing   % Interlineado de 1.5
\doublespacing    % Interlineado doble
```

### Configuración de la Página Frontal

```latex
% Mostrar resumen (1) o no mostrarlo (0)
\FrontPage{1}{Texto del resumen aquí...}
% \FrontPage{0}{} % Sin resumen
```

# Documentación de la Página Frontal

Puede modificar la parte inicial del documento con `\FrontPage`. Más documentación sobre el comando a continuación: [Documentación de `\FrontPage`](/FrontPage.md)

## 🚀 Herramienta de Automatización: LaTeX-Here PowerShell

Para facilitar el uso de esta plantilla, se ha desarrollado una herramienta de PowerShell que permite crear nuevos proyectos LaTeX de manera instantánea desde cualquier ubicación en Windows.

### ¿Qué es LaTeX-Here PowerShell?

**LaTeX-Here PowerShell** es un comando personalizado que automatiza la creación de nuevos proyectos LaTeX utilizando esta plantilla. Con un simple comando, crea una nueva carpeta con todos los archivos necesarios para comenzar inmediatamente.

### 🎯 Características Principales

- **🌐 Clonado inteligente**: Descarga automáticamente la versión más actualizada desde GitHub
- **📱 Modo offline**: Funciona sin internet usando una plantilla local de respaldo
- **🎯 Renombrado automático**: Renombra `main.tex` con el nombre de tu proyecto
- **🧹 Limpieza automática**: Gestión inteligente de archivos temporales
- **💬 Comandos bilingües**: Disponible en inglés (`latex-here`) y español (`plantilla`)

### 📦 Instalación y Uso

La herramienta está disponible en su propio repositorio: **[LaTeX-Here PowerShell](https://github.com/Jorge-Antonio-Gomez/latex-here-powershell)**

#### Instalación Rápida

```powershell
# 1. Clona el repositorio de la herramienta
git clone https://github.com/Jorge-Antonio-Gomez/latex-here-powershell.git
cd latex-here-powershell

# 2. Ejecuta el instalador automático
.\install.ps1
```

#### Ejemplos de Uso

```powershell
# Crear plantilla con nombre por defecto
latex-here

# Crear con nombre personalizado
latex-here "Mi Tesis Doctoral"

# Usando el alias en español
plantilla "Proyecto Final de Economía"
```

### 📁 Estructura Creada

Después de ejecutar el comando, obtienes:

```
Mi Proyecto LaTeX/
├── img/                          # 📁 Carpeta para imágenes y fondos
│   └── bg/                       # Fondos predefinidos
├── Mi Proyecto LaTeX.tex         # 📄 Archivo principal (renombrado automáticamente)
├── preamble.tex                  # ⚙️ Configuración y paquetes LaTeX
└── examples.tex                  # 📝 Ejemplos y plantillas de contenido
```

### 💡 Flujo de Trabajo Recomendado

```powershell
# 1. Navegar al directorio de trabajo
cd "C:\Proyectos\Universidad\2025"

# 2. Crear nueva plantilla
latex-here "Análisis Económico - Semestre I"

# 3. Navegar a la nueva carpeta
cd "Análisis Económico - Semestre I"

# 4. Abrir en tu editor LaTeX favorito
code .                           # Para VS Code
# o
texstudio "Análisis Económico - Semestre I.tex"  # Para TeXstudio
```

### 🔗 Más Información

Para documentación completa, ejemplos detallados y casos de uso específicos, visita:
- **Repositorio**: [latex-here-powershell](https://github.com/Jorge-Antonio-Gomez/latex-here-powershell)
- **Ejemplos detallados**: [EXAMPLES.md](https://github.com/Jorge-Antonio-Gomez/latex-here-powershell/blob/main/EXAMPLES.md)

---

## Últimas Actualizaciones

**Versión modificada el 03/08/2025:**
- Actualización para documentos del CIDE
- Mejoras en el formato de tablas y figuras
- Nuevos comandos matemáticos predefinidos
- Personalización avanzada de notas al pie
- Control mejorado del interlineado
- Formato renovado del encabezado del documento
- Tags de ecuaciones con color automático
