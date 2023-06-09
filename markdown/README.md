﻿---
Section: Documentación
---

# Documentación



## Generador de aplicaciones

Hay otras aplicaciones y generadores web que utilizan Markdown para convertir código Markdown en una página web. Algunas de las más populares son **Jekyll**, **Vuepress**, **Hugo**, **Gatsby** o **MkDocs**, cada uno con sus propias características y funcionalidades. Son aplicaciones muy útiles que se utilizan típicamente para escribir *blogs*, documentación técnica, o en general contenido fundamentalmente textual.

La diferencia de **Crono Pad** frente a esos otros productos es su especialización en aplicaciones de datos. **Crono Pad** permite incluir gráficos complejos y tablas con funcionalidades avanzadas dentro del mismo documento Markdown. 

El objetivo es facilitar la construcción de este tipo de aplicaciones rápidamente y poder llevar la información desde la base de datos hasta la web con facilidad, incluyendo tablas y gráficos complejos, y sin necesidad de programación.

## Servidor Crono Pad

Las aplicaciones de **Crono Pad** no son necesariamente aplicaciones estáticas con código HTML pre-generado. Existe un servidor de **Crono Pad** que atiende las peticiones y genera HTML al momento, consultando la base de datos cuando sea necesario.

**Crono Pad** ofrece un front-end predeterminado que evita la necesidad de construir uno propio con *JavaScript/Typescript* ni usar ningún framework como *Vue*, *Angular* o *React*. Tampoco es necesario construir un *Backend* con *.Net*, *Java*, o *NodeJs*... **Crono Pad** elimina la necesidad de todas estas capas, agilizando el desarrollo, reduciendo los tiempos de puesta en producción, facilitando el mantenimiento y, en definitiva, eliminando la complejidad asociada a cualquier desarrollo web.

Sin embargo, **Crono Pad** es también un *API servidor de informes*, por lo que es posible llamar a *Crono Pad* y mostrar los gráficos y tablas dentro de cualquier desarrollo a medida con *Vue*, *Angular*, *React* o cualquier otro framework...




**Markdown** es un lenguaje que se utiliza para formatear texto de forma sencilla y fácil de leer. Fue creado por John Gruber en 2004 con el objetivo de proporcionar una forma de escribir documentos que sean fáciles de leer y de escribir, y que puedan convertirse fácilmente en HTML.

En Markdown el texto se escribe utilizando una serie de símbolos que indican cómo se debe formatear el texto. Por ejemplo, un asterisco (*) alrededor de una palabra o frase indica que debe ser enfatizada (ya sea en **negrita** o en *cursiva*).

Markdown también permite crear títulos, listas con viñetas, enlaces, imágenes, bloques de código y mucho más, todo con una sintaxis simple y fácil de recordar.

Esta misma página esta escrita en Markdown. Todo el código está disponible en un [repositorio en Github](https://github.com/bifacil/pad.crono.net).

::: recuerda
El código <strong>Crono Markdown</strong> utilizado para generar esta página está disponible en
el [repositorio Github del proyecto](https://github.com/bifacil/pad.crono.net/blob/master/markdown/README.md)
:::

## Sintaxis básica

Los párrafos se escriben separados por una línea en blanco.

Se pueden destacar textos con *letra cursiva*, **letra negrita** o `letra monoespaciada`. 

Se pueden crear listas:

  * El texto se marca en *cursiva* poniéndolo entre un `*` 
  * El texto se marca en **cursiva** poniéndolo entre dos `**`
  * Usando la comilla torcida se puede escribir en `letra monoespaciada`

También se pueden crear listas numeradas:

  1. Este es el primer elemento
  2. Este es el segundo elemento
  3. Y este el tercero.

Se incluir citas precediendo el texto del carácter `>`

> Así es como se muestra un bloque de cita. 
>
> Se pueden poner varios párrafos separándolos por una línea en blanco,
> si lo desea.

También se pueden incluir carácteres UNICODE como los emojis. 😍

## Imágenes y enlaces

Es posible incluir enlaces e imágenes en un texto Markdown. Por ejemplo, esta es la página web de [Crono](https://businessintelligence.es) y este es el [manual de Crono](https://crono.org).

Así se incluyen imágenes:

![Imagen](/resources/images/image.jpg)

## Títulos, código y listas anidadas

Se pueden crear títulos H!, H2, H3, H4... precediendo el texto de los carácteres `#`, `##`

También se pueden poner literales de código. Se muestran de este modo:

``
SELECT Año,Unidades,Importe,Objetivo
FROM DATABASE [Demo Crono Pad] 
where año>=2010 and País='España'
order by Año
``

Se pueden crear listas anidadas:


 1. First, get these ingredients:

      * carrots
      * celery
      * lentils

 2. Boil some water.

 3. Dump everything in the pot and follow
    this algorithm:

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.


La sintaxis descrita hasta el momento es la más básica y la que interpretan todos los *sabores* de Markdown. Luego, cada fabricante añade características propias que facilitan la escritura de textos especializados (textos matemáticos, pies de página, etc.).




## Crono Markdown


Crono Pad usa una implementación de Markdown propia que se diferencia de todas las demás por la posibilidad de incluir gráficos y tablas con funcionalidades avanzadas. También permite construir un *layout* para organizar los diferentes elementos en la página.

En los siguientes apartados se describen los gáficos y tablas soportados en este momento.



``` data
CHARTT (ChartType='Bar')
HEADER (Title='Ventas España', Subtitle='Gráfico de barras')
LEGEND (Visible=YES)
[DATA COLUMN] (Name='Tienda', [Value]=EXPRESSION ([Tienda|yhxAmCEr]))
[DATA COLUMN] (Name='Importe 2011', [Value]=EXPRESSION ([Importe|vxbOrRSR] WHERE ([Año|DoPLIxSw]=2011)))
[DATA COLUMN] (Name='Importe 2012', [Value]=EXPRESSION ([Importe|vxbOrRSR] WHERE ([Año|DoPLIxSw]=2012)))
[DATA FILTER] ([Value]=EXPRESSION ([País|tlkjfKSm]='ESPAÑA'))
```
