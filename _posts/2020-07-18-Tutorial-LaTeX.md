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