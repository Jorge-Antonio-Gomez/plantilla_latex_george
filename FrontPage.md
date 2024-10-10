# Documentación de `\FrontPage`

## Descripción

El comando `\FrontPage` está diseñado para simplificar la creación de una página de título personalizada en tus documentos LaTeX. Este comando incluye el título, autor, fecha, un resumen opcional y una tabla de contenido estilizada dentro de una caja de color.

## Definición del Comando \FrontPage

El comando está definido en el preámbulo del documento, de la siguiente manera:

```{LaTeX}
% Definir el comando \FrontPage con dos parámetros
\newcommand*{\FrontPage}[2]{%

  % Título
  \maketitle

  % Resumen
  \setstretch{1}
  \ifnum#1=1
      \renewcommand{\abstractname}{\color{main}Resumen}
      \begin{abstract}
          #2
      \end{abstract}
  \fi

  % División
  \HRuleGray

  # Índice
  \begin{tcolorbox}[%
      colback=main!5!white, 
      colframe=main!75!black, 
      title=\textbf{Tabla de Contenido}, 
      toptitle=1.5mm, 
      bottomtitle=1.5mm, 
      breakable]
      \renewcommand{\contentsname}{}
      \setlength{\cftbeforetoctitleskip}{-1cm}
      \setlength{\cftaftertoctitleskip}{1cm}
      \tableofcontents
  \end{tcolorbox}
}
```


## Parámetros

El comando `\FrontPage` acepta dos parámetros:

1. **Incluir Resumen (`1` o `0`)**
   - `1`: Incluye el resumen en la portada.
   - `0`: Omite el resumen.

2. **Contenido del Resumen**
   - Si el primer parámetro es `1`, este segundo parámetro debe contener el texto del resumen.
   - Si el primer parámetro es `0`, este parámetro puede dejarse vacío `{}`.

## Cómo Utilizar `\FrontPage`

Después de definir el color y el comando, puedes utilizar `\FrontPage` en tu documento de la siguiente manera:

### Con Resumen

Para incluir un resumen en la portada, establece el primer parámetro en `1` y proporciona el texto del resumen en el segundo parámetro.

```LaTeX
  \FrontPage{1}{Este es el resumen de mi documento, donde se describen los principales puntos y objetivos del trabajo.}
```

### Sin Resumen

Si no deseas incluir un resumen, establece el primer parámetro en `0` y deja el segundo parámetro vacío.

```LaTeX
  \FrontPage{0}{}
```

## Consideraciones

- **Definir Título, Autor y Fecha**: Antes de llamar a `\FrontPage`, asegúrate de definir los comandos `{ \title{}`, `{ \author{}`, y `{ \date{}`.

- **Personalización del Color**: Puedes cambiar el color principal ajustando los valores RGB en la definición de `main`.

- **Resumen Opcional**: Utiliza el primer parámetro para decidir si incluir o no un resumen en la portada.

- **Estilo de la Tabla de Contenido**: La tabla de contenido está dentro de un `tcolorbox` con colores personalizados. Puedes ajustar las opciones del entorno `tcolorbox` según tus preferencias.

## Resumen de Uso

1. **Establecer Título, Autor y Fecha**:
 
 ```LaTeX
     \title{Título del Documento}
     \author{Autor del Documento}
     \date{\today}
  ```

2. **Llamar a `\FrontPage` en el Documento**:
   - **Con Resumen**:
     { \FrontPage{1}{Este es el resumen de mi documento.} }

   - **Sin Resumen**:
     { \FrontPage{0}{} }

3. **Agregar el Contenido del Documento**:
   Continúa con las secciones y el contenido habitual de tu documento.

---

Esta documentación te proporciona una guía rápida para implementar y utilizar el comando `\FrontPage` en tus documentos LaTeX, permitiéndote crear portadas profesionales y personalizadas de manera eficiente.
