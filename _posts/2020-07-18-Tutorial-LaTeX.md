---
layout: single
title: Tutorial LaTeX
excerpt: "Esta semana toca un post más práctico y menos técnico, una guía para poder realizar nuestros trabajos o textos de una manera mucho más eficiente que con los procesadores de texto clásicos. Seguramente ya te lo habías imaginado pero te lo confirmo, vamos a aprender a trabajar con $\\LaTeX{}$. Veremos cómo instalar un editor de texto multilenguaje, técnicas para llevar nuestros textos al máximo nivel, control de versiones de nuestros trabajos usando Git, etc."
date: 2020-07-18
classes: wide
toc: true
toc_label: "Índice"
# toc_sticky: true
header:
  teaser: /assets/images/tutolatex/1.png
  teaser_home_page: true
categories:
  - Tutoriales
  - LaTeX
tags:
  - VSCode
  - LaTeX
  - TFG
  - Github
  - Textos
  - Figuras SVG
  - Editor
---

Esta semana toca un post más práctico y menos técnico, una guía para poder realizar nuestros trabajos o textos de una manera mucho más eficiente que con los procesadores de texto clásicos. Seguramente ya te lo habías imaginado pero te lo confirmo, vamos a aprender a trabajar con $\LaTeX{}$. Veremos cómo instalar un editor de texto multilenguaje, técnicas para llevar nuestros textos al máximo nivel, control de versiones de nuestros trabajos usando Git, etc.

![](/assets/images/tutolatex/1.png){: .align-center}

Todo el software utilizado en esta guía está disponible para 64 y 32 bits. El sistema utilizado es **Windows** pero la manera de proceder en Linux y MacOS es idéntica.
{: .notice--info}

## ¿Por qué LaTeX?

Para los que lo conocen vagamente o directamente es su primera vez leyendo sobre LaTeX, no es un editor de textos sino un lenguaje de programación enfocado a composición de textos. Podría decirse que hay casi infinidad de motivos por los que aprenderlo pero para mí estos son los más importantes:

- Te centras en el **contenido** y dejas el formateo a LaTeX (índices, numeración de tablas y figuras, etc.).
- Sistema de **citaciones** sencillo.
- Tipografía de muy alta calidad (**símbolos y ecuaciones**). 
- Open source y gratis.
- ¡Es **fácil**!

![](/assets/images/tutolatex/curva.png){: .align-center}

## Instalación

### MiKTeX

Primero necesitamos la distribución de **TeX** (TeX es el lenguaje de macros en el que está basado LaTeX), es donde vienen todas las dependencias del lenguaje necesarias para compilar nuestro texto así como algunos paquetes. Los paquetes son conjuntos de macros creados por la comunidad que nos facilitarán el manejo de nuestro querido LaTeX.

Hay diversas distribuciones: TeX Live, proTeXt, MiKTeX...Yo me decanto por MiKTeX pero cualquiera es válida.

Visitaremos este [**enlace**](https://miktex.org/download):

![](/assets/images/tutolatex/tuto1.png){: .align-center}

Para 32 bits encontrarás los binarios en el apartado *All downloads*.

Ahora simplemente procedemos con la instalación, nada nuevo bajo el sol:

![](/assets/images/tutolatex/tuto2.png){: .align-center}

Seleccionamos instalar para todos los usuarios:

![](/assets/images/tutolatex/tuto3.png){: .align-center}

Hay que marcar que instale los paquetes que faltan sobre la marcha y tamaño de papel A4:

![](/assets/images/tutolatex/tuto4.png){: .align-center}

E instalamos:

![](/assets/images/tutolatex/tuto5.png){: .align-center}

![](/assets/images/tutolatex/tuto6.png){: .align-center}

### VSCode

Este será el editor que usaremos para trabajar con LaTeX; es un editor multilenguaje, es decir, podremos tener todos nuestros proyectos (Python, C, C++, R...) en el mismo lugar. La instalación de Visual Studio Code es sencilla ([**enlace de descarga**](https://code.visualstudio.com/)), tan solo hay que pulsar **Next** hasta que finalice.

![](/assets/images/tutolatex/tuto7.png){: .align-center}

### Perl

El último requisito es **Perl**, hay algunos componentes de TeX que necesitan de este lenguaje para trabajar correctamente. En editores específicos de LaTeX como TeXstudio ya viene preconfigurado.

![](/assets/images/tutolatex/tuto8.png){: .align-center}

Pulsamos **Next** hasta el final.

## Preparación del espacio de trabajo

Entraremos en el apartado extensiones:

![](/assets/images/tutolatex/tuto9.png){: .align-center}

Buscaremos la extensión **LaTeX Workshop** y debería quedarnos así:

![](/assets/images/tutolatex/tuto10.png){: .align-center}

Una vez esté instalado iremos a los ajustes y buscaremos LaTeX.

![](/assets/images/tutolatex/tuto11.png){: .align-center}

Modificamos el parámetro **Out Dir**:

![](/assets/images/tutolatex/tuto12.png){: .align-center}

Esto hará que nuestro PDF final y los respectivos archivos necesarios para ello, queden en una carpeta independiente dentro de nuestro directorio raíz de trabajo. ¡Orden en nuestro espacio ante todo!

Ya estamos listos para trabajar con LaTeX 👏👏.

## Uso

Comenzamos con la sintaxis básica del lenguaje, los comandos de LaTeX se llaman usando una barra invertida, los argumentos principales entre llaves, las opciones adicionales de un comando entre corchetes y los comentarios se añaden con el símbolo de porcentaje. Aquí vemos un ejemplo básico de código LaTeX y su respectivo resultado:

```tex
\documentclass{article}
% preámbulo

\usepackage[utf8]{inputenc} % Para escribir tildes
\usepackage[T1]{fontenc}    % Para usar fuentes con letras acentuadas, etc.
\usepackage[spanish]{babel} % Definimos el idioma principal

\title{Hola Mundo}
\author{Escribe aquí tu nombre}

\begin{document}
% Cuerpo del documento

\maketitle

Mi primer documento en \LaTeX{}.

\end{document}
```

Si tenemos todo bien configurado debemos tener un botón llamado **TeX** y arriba a la derecha el visor PDF.

![](/assets/images/tutolatex/tuto13.png){: .align-center}

El resultado final de nuestro entorno de trabajo:

![](/assets/images/tutolatex/tuto14.png){: .align-center}

Paréntesis, corchetes y llaves coloreados son gracias al plugin *Bracket Pair Colorizer 2*.

### Crear una portada

Como hemos visto en el ejemplo anterior si definimos título, autor y fecha antes del `\begin{document}` y usamos el comando `\maketitle`, obtenemos un inicio de documento más o menos aceptable. A mi me gusta hacer la portada desde cero aunque es un tema más avanzado (podéis contactarme por privado para este tipo de cosas que se salen de la guía), pero tenemos muchísimas opciones para nuestro objetivo. 

Personalmente recomiendo esta [**web**](https://www.latextemplates.com/) de la que usaremos esta [**plantilla**](https://www.latextemplates.com/template/academic-title-page).

![](/assets/images/tutolatex/tuto15.png){: .align-center}

### Incluir dedicatorias

Creamos un nuevo entorno:

```tex
\newenvironment{dedication}
{
   \cleardoublepage
   \thispagestyle{empty}
   \vspace*{\stretch{1}}
   \hfill\begin{minipage}[t]{0.66\textwidth}
   \raggedright
}
{
   \end{minipage}
   \vspace*{\stretch{3}}
   \clearpage
}
```

Y lo añadimos en nuestro texto, quedará algo así:

![](/assets/images/tutolatex/tuto16.png){: .align-center}

### Figuras

Para incluir imágenes en nuestro texto tan solo debemos incluir el paquete `\usepackage{graphicx}`.

```tex
\begin{figure}
    \centering
    \includegraphics[scale=0.5]{img/compare.png}
    \caption{Perfiles radiales de transformada rotacional para diferentes
    conceptos de \textit{stellarators} y un \textit{tokamak}.}
    \label{fig:compare}
\end{figure}
```

![](/assets/images/tutolatex/tuto22.png){: .align-center}

Para formatear el pie de foto de esa manera:

```tex
\usepackage[labelfont=bf,labelsep=period,font={footnotesize,it}]{caption}
```

El comando `\label` es usado para darle una referencia a nuestra figura y poder nombrarla en nuestro texto:

```tex
Es obvio en la figura~\ref{fig:compare}
```

![](/assets/images/tutolatex/tuto23.png){: .align-center}

### Figuras vectoriales

Las figuras vectoriales tienen una enorme ventaja frente a los mapas de bits (JPG, PNG...): son creadas a partir de atributos matemáticos, esto es que por mucho zoom que hagamos nunca se desenfocan. Un ejemplo de figura vectorial son las fuentes tipográficas que usamos para escribir en ordenador.

![](/assets/images/tutolatex/tuto17.png){: .align-center}

Para añadir figuras vectoriales así en nuestro texto debemos incluir el paquete `\usepackage{svg}`.

```tex
\begin{figure}
    \centering
    \def\svgwidth{10cm}
    \input{svg/bindingenergy.pdf_tex}
    \caption[Energía de enlace]{Energía de enlace promedio en función del número másico.}
    \label{fig:nucleons}
\end{figure}
```

La figura está hecha con Microsoft Excel para los puntos e Inkscape para el diseño final. Este apartado se merece un artículo exclusivo porque hay que instalar algunos plugins en Inkscape y no es el punto de este tutorial.

### Ecuaciones

Podemos escribir ecuaciones dentro del texto usando los cierres con el símbolo del dólar:

```tex
Ejemplo de ecuación en línea con el texto $x^2+y^2=r^2$.
```

![](/assets/images/tutolatex/tuto18.png){: .align-center}

O podemos escribirlas en un renglón aparte:

```tex
Ejemplo de ecuación numerada
\begin{equation}
  x^2+y^2=r^2
\end{equation}
```

![](/assets/images/tutolatex/tuto19.png){: .align-center}

Si no queremos numerarla debemos incluir un asterisco en el entorno equation:

```tex
Ejemplo de ecuación numerada
\begin{equation*}
  x^2+y^2=r^2
\end{equation*}
```

### Listas

Para añadir una lista a nuestro texto podemos usar el entorno *itemize*:

```tex
\begin{itemize}
  \item Item 1
  \item Item 2
\end{itemize}
```

![](/assets/images/tutolatex/tuto20.png){: .align-center}

Si queremos una lista enumerada usaremos el entorno *enumerate*. Con el paquete `\usepackage{enumerate}` podemos variar la forma en la que se muestra nuestra etiqueta:

```tex
\begin{enumerate}[(1)]
  \item Item 1
  \item Item 2
\end{enumerate}
```

![](/assets/images/tutolatex/tuto21.png){: .align-center}

Como podréis imaginar ya que esto es LaTeX, hay infinitas posibilidades de diseño. Os animo a que juguéis con él hasta encontrar vuestro estilo.

