# ElCreador

Este repositorio contiene los archivos base del libro _El Creador_, de Mynona, también conocido como Salomo Friedländer. 

## Licencia


<p class="licencia"> <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Licencia de Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />Este obra está bajo una <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">licencia de Creative Commons Reconocimiento-NoComercial-CompartirIgual 4.0 Internacional</a>.</p>

## Descripción de los archivos contenidos aquí:

- Archivo base en markdown (ver historia de correcciones aquí). Incluye el prólogo escrito para el libro por Claudio Naranjo.
- CSS base para los libros de la editorial (tuneado del repo de Matt Harrison)
- Carpeta de imágenes para construir el libro (las imágenes son fotografías analógicas de Jerónimo Rüedi & Josué Eber Morales, en formato JPG)

## ¿Que falta?

la primera versión del archivo EPUB ha sido liberada, a continuación, el roadmap incluye:

- una versión ligera utilizando una hoja de estilos específica para personas con dislexia y estructurada con las recomendaciones de accesibilidad.
- una versión de audiolibro en formato document del W3 consortium (una vez consigamos entender las especificaciones del formato)

## Test

el EPUB resultante ha sido probado con éxito en Calibre, Thorium y MoonReader (android). falta probar en Ibooks (pendiente)

## Requerimientos

Pandoc, Git, Sigil (para modificar archivos y editar metadata)

## ¿Cómo?

Situarse en el directorio donde reside el proyecto (previamente, hará falta clonar el repo) y correr en la consola (linux y mac) o en Power Shell (Windows):

````
pandoc elCreador.md -t epub3 -s --epub-embed-font=fonts/AvenirLTStd-*.otf  --epub-embed-font=fonts/FluidSpiral.ttf --epub-embed-font=fonts/SabonLTStd-*.otf --epub-chapter-level=2 -o elCreador.epub
````

Donde: pandoc (invocamos el ejecutable) elCreador.md (llamamos el archivo base) -t epub3 (le decimos a qué formato queremos convertir el archivo en markdown) -s (para que cree un único archivo epub) --epub-embed-font= (para que incluya las fuentes de nuestra elección, podemos omitirlo y funcionara igual con las fuentes del sistema que ocupemos para leer el ebook), --epub-chapter-level=2 (para que pandoc busque los encabezados de segundo nivel y separe el archivos en capítulos) -o elCreador.epub (el nombre del archivo y el formato de salida).

Para comprobar si todo está bien, nada mejor que utilizar sigil y comprobar el epub. 












