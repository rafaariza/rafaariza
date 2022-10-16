---
layout: single
title: Python y ciencia
excerpt: "Aquí estamos, reunidos una semana más, esta vez con un post que me han pedido algunas personas pero que por supuesto era obligatorio tenerlo con nosotros. Manejar un lenguaje de programación como Python no puede faltar entre nuestro arsenal de científicos del siglo XXI. En este post veremos cómo instalarlo en nuestro sistema, sus características principales, la sintaxis más básica para comenzar a trabajar con él, entre otros temas. Finalmente, crearemos unas figuras muy llamativas que seguro os gustarán."
date: 2020-07-25
classes: wide
toc: true
toc_label: "Índice"
read_time: true
# toc_sticky: true
header:
  teaser: assets/images/tutopython/1.png
  teaser_home_page: true
categories:
  - Tutoriales
  - Python
tags:
  - VSCode
  - Python
  - Hydrogen-like
  - Github
  - Orbitales
  - Esféricos armónicos
  - Simulations
gallery:
  - url: /assets/images/tutopython/Armónico1.png
    image_path: /assets/images/tutopython/Armónico1.png
    title: "Armónico 0,0"
  - url: /assets/images/tutopython/Armónico2.png
    image_path: /assets/images/tutopython/Armónico2.png
    title: "Armónico 1,0"
  - url: /assets/images/tutopython/Armónico3.png
    image_path: /assets/images/tutopython/Armónico3.png
    title: "Armónico 2,0"
  - url: /assets/images/tutopython/Armónico4.png
    image_path: /assets/images/tutopython/Armónico4.png
    title: "Armónico 3,0"
  - url: /assets/images/tutopython/Armónico5.png
    image_path: /assets/images/tutopython/Armónico5.png
    title: "Armónico 3,-2"
  - url: /assets/images/tutopython/Armónico6.png
    image_path: /assets/images/tutopython/Armónico6.png
    title: "Armónico 4,-1"
  - url: /assets/images/tutopython/Armónico7.png
    image_path: /assets/images/tutopython/Armónico7.png
    title: "Armónico 5,2"
---

Aquí estamos, reunidos una semana más, esta vez con un post que me han pedido algunas personas pero que por supuesto era obligatorio tenerlo con nosotros. Manejar un lenguaje de programación como *Python* no puede faltar entre nuestro arsenal de científicos del siglo XXI. En este post veremos cómo instalarlo en nuestro sistema, sus características principales, la sintaxis más básica para comenzar a trabajar con él, entre otros temas. Finalmente, crearemos unas figuras muy llamativas que seguro os gustarán.

![](/assets/images/tutopython/1.png){: .align-center}

## Motivación

A día de hoy, hay muchos lenguajes de programación cada uno con sus ventajas e incovenientes y sus casos de uso. Si lo que buscamos es un lenguaje para trabajar en ciencia, de nuevo encontramos diversidad de ellos: *Fortran*, *MATLAB*, *R*, *C++*, *Julia*... Pero hay uno que, inconfundiblemente, es el más popular: 🐍. Su gran fama no viene de regalo, es un lenguaje con una sintaxis sencilla (se suele decir que es como si estuvieras leyendo inglés), tiene una comunidad enorme y lo más importante, open source y gratuito.

![](/assets/images/tutopython/2.jpg){: .align-center}

## Características principales

- **Tipado dinámico**. No es necesario establecer un tipo (string, integer, boolean , etc.) al declarar las variables y además puede cambiar en cualquier momento.
- **Interpretado**. La principal ventaja de un lenguaje interpretado es que es independiente de la máquina y del sistema operativo ya que no contiene instrucciones propias de un procesador sino que contiene llamadas a funciones que el interprete deberá reconocer. En contraposición, la ejecución del código es más lenta que en un lenguaje compilado como podría ser *C++*.
- **Alto nivel**. Cuando escribimos programas en *Python*, no necesitamos recordar la arquitectura del sistema, ni tampoco administrar la memoria.
- **Orientado a objetos**. La programación orientada a objetos (Object-Oriented Programming) es una forma especial de programar, más cercana a como expresaríamos las cosas en la vida real que otros tipos de programación.
- **Soporte desarrollo GUI's**. Podemos crear programas que usen interfaz gráfica con *Python*.
- **Extensible**. Podemos escribir código *Python* en lenguaje *C* o *C++* y será posible compilar ese código en *C/C++*.
- **Integrable**. Capacidad de integrarlo fácilmente con otros lenguajes.
- **Librerías**. *Python* tiene muchas librerías estándar que proporcionan un conjunto de módulos y funciones para que no tengas que escribir tu propio código para cada cosa.

## Instalación

La instalación es bastante sencilla, hay varias formas de hacerla: partiendo de la distribución oficial de *Python* ([**enlace de descarga**](https://www.python.org/downloads/)) o usando alguna distribución como [**Anaconda**](https://www.anaconda.com/products/individual). La ventaja de usar *Anaconda* es que trae consigo las librerías más utilizadas en el campo científico así como aquellas que se usan en Data Science o Machine Learning. Por el contrario, es una distribución más pesada (puede llegar a ocupar varios gigabytes en disco) de *Python*.

Elijas la que elijas no instales la versión 2.x de *Python* ya que se encuentra en estado *deprecated*. ¡Utiliza Python 3!

Yo estaré usando la distribución clásica de *Python* en sistema operativo Windows. Y sí, instalaremos la versión 32 bits ya que, por experiencia, da menos problemas (trabajar con algunos módulos, etc.).

![](/assets/images/tutopython/3.png){: .align-center}

Una cosa para tener en cuenta: durante la instalación, verás una ventana de "Setup". Asegúrate de marcar las casillas "Add Python 3.x to PATH" o "Add Python to your environment variables" y hacer click en "Install Now".

Si todo ha ido correctamente deberías ser capaz de correr comandos de Python:

![](/assets/images/tutopython/4.png){: .align-center}

Yo uso VSCode como editor e IDE de Python, pero la instalación realizada trae su propio IDE:

![](/assets/images/tutopython/5.png){: .align-center}

Para instalar VSCode os remito al tutorial que hice sobre LaTeX, [**aquí**](https://rafajurado.com/Tutorial-LaTeX/#vscode).

## Preparación del entorno de trabajo

### Python IDLE

Pulsamos arriba en *File* y después *New File*:

![](/assets/images/tutopython/6.png){: .align-center}

Se abrirá el editor por defecto de Python:

![](/assets/images/tutopython/7.png){: .align-center}

Aquí ya podemos escribir nuestro primer script de Python:

![](/assets/images/tutopython/8.png){: .align-center}

Así es la forma de decirle a Python que escriba algo por pantalla, ya os dije que era como escribir en inglés😉. Lo guardamos en *File > Save As...*:

![](/assets/images/tutopython/9.png){: .align-center}

Y el resultado:

![](/assets/images/tutopython/10.png){: .align-center}

### VSCode

Lo primero que debemos hacer es instalar la extensión de Python a través del Marketplace de VSCode:

![](/assets/images/tutopython/11.png){: .align-center}

Yo ya la tengo instalada pero simplemente hay que pulsar *Install* y después seleccionar el intérprete como véis en la imagen abajo. Os recomiendo VSCode por encima del IDLE por defecto de Python entre otras cosas porque tiene syntax highlighting y se agradece mucho a la hora de trabajar.

![](/assets/images/tutopython/12.png){: .align-center}

Para ejecutar el script, pulsamos en el botón de play arriba a la derecha:

![](/assets/images/tutopython/13.png){: .align-center}

## Uso

### Modo interactivo

Ejecutamos la orden en tiempo real en la shell de Python.

![](/assets/images/tutopython/14.png){: .align-center}

### Modo script

Escribimos un script y lo corremos en algún IDE.

![](/assets/images/tutopython/13.png){: .align-center}

Es equivalente a llamarlo desde la consola:

![](/assets/images/tutopython/15.png){: .align-center}

A medida que nuestros scripts tengan un mínimo de complejidad esta modo de trabajar es, sin lugar a dudas, mejor.

### Identificadores

Un identificador de Python es un nombre que se utiliza para identificar una variable, función, clase, módulo u otro objeto. Un identificador comienza con una letra mayúscula o minúscula o un guión bajo (_) seguido de cero o más letras, guiones bajos y dígitos (0 a 9).

Python no permite caracteres de puntuación como @, $ y % en los identificadores. Python es un lenguaje de programación sensible a mayúsculas y minúsculas. Por lo tanto, nombre y Nombre son dos identificadores diferentes en Python.

- Los nombres de las clases comienzan con una letra mayúscula. Todos los demás identificadores comienzan con una letra minúscula.
- Iniciar un identificador con un solo guión bajo indica que el identificador es privado.
- Iniciar un identificador con dos guiones bajos indica un identificador fuertemente privado.
- Si el identificador también termina con dos guiones bajos, el identificador es un nombre especial definido por el lenguaje.

### Palabras reservadas

Hay una serie de palabras que no podemos emplear como constantes o variables o como nombre identificador. Son todas en minúsculas y han sido reservadas por el lenguaje Python.

En concreto, las palabras reservadas son: and, assert, break, class, continue, def, del, elif, else, except, exec, finally, for, from, global, if, imoort, in, is, lambda, not, or, pass, print, raise, return, try, while, with, yield.

### Líneas de código

Un programa codificado con lenguaje Python está dividido en varias líneas lógicas y cada una de ellas finaliza con una nueva línea. Si la línea está en blanco, es ignorada por el intérprete de Python.

Por otra parte, las órdenes y líneas se agrupan unas dentro de otras mediante sangrado o espaciado. Y para unir dos o más líneas, se emplea la barra inclinada hacia la izquierda (\).

Otra posibilidad es que queramos realizar varias acciones o peticiones en una única línea. Para ello, podemos combinar todas las instancias empleando como separador el símbolo de punto y coma.

```python
if True:
   print "Verdadero"
else:
   print "Falso"
```

Esa estrucutura es correcta.

### Comillas

Python acepta comillas simples ('), dobles (") y triples (""") para denotar literales, siempre que el mismo tipo de comillas comience y termine la cadena.

Las comillas triples se utilizan para abarcar la cadena en varias líneas.

```python
palabra = 'palabra'
sentence = "Esta es una oración."
párrafo = """Este es un párrafo. Está
compuesto por múltiples líneas y oraciones."""
```

### Comentarios

Un signo de hash (#) que no está dentro de un literal de cadena comienza un comentario. Todos los caracteres después del # y hasta el final de la línea son parte del comentario y el intérprete de Python los ignora.

```python
# Primer comentario
print("Hola") # segundo comentario
```

### Definir funciones

Utilizamos el identificador `def`:

```python
def suma(x,y):
  resultado = x+y
  return resultado

suma1 = suma(2,3)
suma2 = suma(1,4)

print(suma1)
print(suma2)
```

El código arriba produce el siguiente resultado:

![](/assets/images/tutopython/16.png){: .align-center}

Nótense varias cosas: `return` devuelve una salida de la función, con esto podemos almacenarlo en diferentes variables `suma1`, `suma2`... Y después de declarar una función se añaden dos puntos y las líneas que la codifican van indentandas.

### Tipos de variables

Los tipos de datos básicos de Python son los booleanos (True o False), los numéricos (enteros, punto flotante y complejos) y las cadenas de caracteres.

```python
entero = -3
real = 1/2
complejo = 2+1j # Python tiene definida la unidad imaginaria por defecto como j.

print(type(entero), type(real), type(complejo))
```

![](/assets/images/tutopython/17.png){: .align-center}

Los vectores en Python se definen como listas o arrays y se llaman mediante corchetes:

```python
vector1 = [1,2,3]
for i in vector1:
  print(i)
```

![](/assets/images/tutopython/18.png){: .align-center}

De nuevo vemos que es muy similar a escribir en inglés. Por supuesto son estructuras muy simples y Python es un universo gigante, si de verdad queréis aprender a programar con él no os voy a recomendar ningún curso o tutorial simplemente os digo que os pongáis a programar, lo que sea. 

Conforme os vayan surgiendo dudas, las busquéis y resolváis, aprenderéis lo más grande.

Todo está en Internet, de verdad, todo.

### Instalar paquetes

El gestor de paquetes por defecto de Python es `pip`. Su uso es bastante simple, en la consola:

`pip install <nombre del paquete>`

Y se instalará en vuestro entorno. Os recomiendo encarecidamente que uséis entornos virtuales para no tener encontronazos entre diferentes versiones de librerías, pero esto lo dejo para otro post. No quita que podáis hacer búsqueda por vuestra cuenta🤓.

## Python y física

Respecto al primer artículo ([**átomo hidrogenoide**](https://rafajurado.com/atomo/)), recuerdo que dije que lo íbamos a mirar más de cerca usando Python. Pues bien me pusé a investigar acerca de la resolución de las ecuaciones y descubrí una cosa súper interesante: las soluciones de la ecuación de Schrödinger en coordenadas parabólicas se pueden expresar como combinación lineal de las soluciones en esféricas. Lo encontré en un libro buenísimo acerca de cuántica y átomos: `Quantum Mechanics of One- and Two-Electron Atoms. Edwin Salpeter y Hans Bethe` en la sección 6, para los curiosos.

Pues con todo ello, dije ¿qué es lo más visual que podemos representar acerca de las soluciones de la ec. de Schrödinger en esféricas? Exacto, los armónicos esféricos. Esas figuras que nos dicen donde hay probabilidad de encontrar al electrón en una determinada dirección (ojo, que no la probabilidad total). 

Y, así, me piqué este gracioso script que nos permite obtener las hermosas figuras que veréis al final del post:

```python
# Importamos todos los módulos necesarios

from numpy import sin, cos, pi, sqrt, shape, linspace, meshgrid, zeros, array
from math import factorial
import matplotlib.pyplot as plt

# Definimos funciones necesarias para nuestro cometido

def esfericas2cartesianas(r,theta,phi):

    x = r*sin(theta)*cos(phi)
    y = r*sin(theta)*sin(phi)
    z = r*cos(theta)
    
    return x, y, z

def legendre_polinomio(l,m,x):
    pmm = 1.0
    if m > 0:
        sign = 1.0 if m % 2 == 0 else -1.0
        pmm = sign*pow(factorial(2*m-1)*(1.0-x*x),((m/2)))

    if l == m:
        return pmm

    pmm1 = x*(2*m+1)*pmm
    if l == m+1:
        return pmm1

    for n in range(m+2,l+1):
        pmn = (x*(2*n-1)*pmm1-(n+m-1)*pmm)/(n-m)
        pmm = pmm1
        pmm1 = pmn

    return pmm1

# Ya tenemos todas las funciones definidas. Let's code!
    
l = int(input('Número cuántico azimutal l: '))

if l < 0:
    print('l no puede ser negativo')

m = int(input('Número cuántico magnético m: '))

if m>l or m<(-l):
    print('Número cuántico m pertenece a [-l,l]')

A = sqrt(((2*l+1)*factorial(l-abs(m)))/(4*pi*factorial(l+abs(m)))) # Constante de normalización

phi = linspace(0,2*pi,181)
theta = linspace(0,pi,91)

Phi,Theta = array(meshgrid(phi,theta))

if m>0:
        
    rho = pow(abs(sqrt(2)*A*cos(m*Phi)*legendre_polinomio(l,m,cos(Theta))),2)
        
elif m < 0:
        
    rho = pow(abs(sqrt(2)*A*sin(abs(m)*Phi)*legendre_polinomio(l,abs(m),cos(Theta))),2)
        
else:
        
    rho = pow(abs(A*legendre_polinomio(l,0,cos(Theta))),2)

x,y,z = esfericas2cartesianas(abs(rho),Theta,Phi)

# Figuras YAY!!

fig = plt.figure(f'Armónico {l},{m}')
ax = fig.add_subplot(111,projection='3d')

ax.plot_surface(x,y,z, cmap = 'Spectral')

plt.title(f'Armónico {l},{m}', fontsize = 14, fontweight = 'bold')
ax.set_xlabel('X', fontsize = 12, fontweight = 'bold')
ax.set_ylabel('Y', fontsize = 12, fontweight = 'bold')
ax.set_zlabel('Z', fontsize = 12, fontweight = 'bold')

plt.show()
```

Viene la mejor parte: ¡figuras😍😍!

{% include gallery caption="Armónicos esféricos generados con Python." %}

Y hasta aquí este pequeño comienzo con Python y ciencia, una serie de post que continuaré con cosas como los `Jupyter Notebooks` o más scripts interesantes y muchas figuras.

Para terminar os animo a que hagáis un script que calcule el número $\pi$ mediante el método de Montecarlo. El que lo consiga, me lo debe enviar a cualquiera de los enlaces de contacto a la izquierda y le mandaré de vuelta una chuleta buenísima con TODO lo necesario para manejar Python.

¡Nos vamos leyendo🤗!