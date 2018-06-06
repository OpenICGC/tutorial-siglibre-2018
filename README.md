# Pirámides y estilos en vector tiles en formato abierto del ICGC

En este tutorial aprenderemos:

1. Como crear un estilo propio basandose en el estilo creado por el ICGC
2. Crear un visor de mapas con la base background VT ICGC y el estilo propio creado
3. Cargar otra fuente de datos a nuestro mapa y agregar la capa de Terreno

## Crear el estilo

### Estilo simple

Para crear un estilo simple utilizaremos la herramienta Pintamaps creada por el ICGC https://github.com/gencat/ICGC-pintamaps-omt

* Ir al editor de estilos http://betaserver.icgc.cat/ICGC-pintamaps-omt/

* Modificar el estilo para crear un estilo propio

* Guardar el estilo

* Renombrar el archivo descargado (el nuevo nombre del archivo puede ser tu_nombre_simple.json)

* Hacer un fork de repositorio del tutorial https://github.com/OpenICGC/tutorial-siglibre-2018

* Subir el estilo creado a vuestro fork

* (Opcional) Hacer un pull request al repositorio del tutorial

### Estilo complejo

Para crear un estilo complejo utilizaremos la herramienta Maputnik

#### Obtener el estilo oficial

* Ir al repositorio oficial del ICGC https://openicgc.github.io/ y copiar el enlace del estilo mundial ICGC (oficial)

``` bash
https://geoserveis.icgc.cat/stylesvector/icgc.json
```

#### Editar el estilo

* Ir al editor de estilo https://maputnik.github.io/editor/#0/0/0

* Cargar el estilo oficial ICGC

  * Seleccionar la opción **Open** del menú principal
  * Pegar la url del estilo oficial en la opción **Load from URL**
  * Hacer click en el botón **Open URL**

* Modificar el estilo para crear un estilo propio

* Guardar el estilo 

  * Seleccionar la opción **Export** del menú principal
  * Presionar el botón de **Download** para descargar el estilo
  * Renombrar el archivo descargado (el nuevo nombre del archivo puede ser tu_nombre_complejo.json)

* Subir el estilo creado a vuestro fork

* (Opcional) Hacer un pull request al repositorio del tutorial

## Crear visor de mapas

Para crear el visor de mapa adaptaremos el visor de ejemplo creado por el ICGC para visualizar diferentes estilos sobre la base background VT ICGC.

* Ir al el visor base https://openicgc.github.io/icgc-basemap.html

* Crear un nuevo archivo llamado visor.html y copiar el código del visor

* Eliminar el menú de selección de estilos (borrar líneas 112 al 126)

* Modificar la url del estilo y pegar la url de vuestro estilo simple (línea 123)

* Abrir el archivo visor.html con el navegador (Chrome) y comprobar que se ve el mapa con vuestro estilo

* Modificar la url del estilo y pegar la url de vuestro estilo complejo (línea 123)

* Recargar la página y comprobar que ahora el mapa tiene el estilo complejo

## Cargar la capa de Terreno

En nuestor estilo complejo añadiremos la capa de terreno (sólo está disponible en Catalunya)

* Ir al repo de OpenICGC https://openicgc.github.io/ y copiar la URL del estilo **Terreny** de ámbito Catalunya

* Abrir la URL del estilo **Terreny** en una nueva pestaña del navegador

* Copiar el source con id **terrain**

* Agregar el source en vuestro estilo complejo

* Copiar la capa con id **terrain**

* Agregar la capa en vuestro estilo justo despues de la capa con id **background**

* Guardar y subir el estilo modificado a vuestro fork

* Recargar la página del mapa y comprobar que aparece el terreno
