# Optimización de procesos con Python para ingenieros

Cuaderno del curso **Optimización de procesos con Python para ingenieros** de **DanLara Learning**.

Cada celda del cuaderno lleva el mismo número que en el video. Por ejemplo, la **Celda 2.4** es la que se ve en la Sección 2.

## Contenido

```
notebooks/
  curso_optimizacion.ipynb · el cuaderno del curso, de la Sección 0 a la 10 (121 celdas de código)
```

El cuaderno no necesita archivos de datos: cada celda define los suyos o los calcula.

## Cómo abrir el cuaderno

Ábrelo en Google Colab, sin instalar nada:

https://colab.research.google.com/github/lara-montano/optimizacion-procesos-python/blob/main/notebooks/curso_optimizacion.ipynb

Para ejecutar una celda, haz clic en ella y pulsa Mayúsculas + Enter. Las celdas se corren en orden, porque algunas usan lo que definió una celda anterior. Si Colab avisa que el cuaderno no lo creó Google, elige ejecutarlo de todos modos: viene de este repositorio.

## La versión de SciPy

La celda 0.1 imprime las versiones de NumPy y SciPy. Las Secciones 6, 8 y 10 leen los multiplicadores de `minimize` con `res.multipliers`, que existe desde **SciPy 1.16**. Si la celda 0.1 muestra una versión anterior, corre esto en una celda nueva y después reinicia la sesión (menú Entorno de ejecución):

```
!pip install -q "scipy>=1.16"
```

## Sobre los datos y los coeficientes

- **Coeficientes de costo:** son ilustrativos, elegidos para que el orden de magnitud sea realista. No describen ninguna planta en particular.
- **Presión de vapor del metanol (Sección 7):** los doce puntos son **sintéticos**. La celda 7.1 los calcula con las constantes de Antoine de NIST, ajustadas por NIST a los datos de D. Ambrose y C. H. S. Sprake, *J. Chem. Thermodynamics* 2 (1970) 631–645. Les agrega 0.5 % de ruido normal con la semilla 7.
- **Equilibrio acetona–cloroformo (Sección 7):** los nueve puntos a 101.3 kPa son de Q. Gao, Z. Zhao, P. Jia y X. Zhang, *Applied Sciences* 8 (2018) 1519, tabla A1, doi:10.3390/app8091519. Es un artículo de acceso abierto.
  - Constantes de Antoine: la acetona, de NIST (Ambrose, Sprake y Townsend, 1974); el cloroformo, de Felder y Rousseau, tabla B.4.
  - Parámetros de van Laar de referencia: Perry, 8.ª edición, tabla 13-2.
- **Proyecto final (Sección 10):** los coeficientes, la cota de conversión y los números de la semana son del curso. Son ilustrativos, y la cota de 0.52 es una elección dentro de las franjas que describen las patentes US 4,746,759 y US 7,132,577.

## Versiones con las que se comprobó el cuaderno

Python 3.13 con NumPy 2.3.5, SciPy 1.16.3 y Matplotlib 3.10.6.
