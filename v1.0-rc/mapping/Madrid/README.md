# Ejemplos
En esta carpeta se incluye un ejemplo de transformación de datos abiertos existentes en el portal de datos abiertos del Ayuntamiento de Madrid (https://datos.madrid.es) a RDF, de acuerdo con el vocabulario que se desarrolla en este repositorio. 

La carpeta contiene los siguientes ficheros:

## alumbrado-publico.csv
Este es el conjunto de datos sobre alumbrado público que está publicado en el portal de datos abiertos del Ayuntamiento de Madrid 
- https://datos.madrid.es/sites/v/index.jsp?vgnextoid=72b76cc09a800810VgnVCM1000001d4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD
- Origen de los datos: Ayuntamiento de Madrid 
- Licencia: https://datos.madrid.es/egob/catalogo/aviso-legal

## mapping.rml
Este archivo contiene los mapeos declarativos que se utilizan para la transformación de los datos del CSV a RDF, de acuerdo con el vocabulario. Se consideran los siguientes atributos en el proceso de transformación.

  - tipoLampara: Representa el modelo específico de la bombilla.
  - tipoLuminaria: Tiene tres posibilidades a representar, la primera sería tipo LED, la segunda opción sería de tipo DESCARGA (es lo mismo que las antiguas de incandescencia, halogenuros, etc) y por último el tipo LED-DESCARGA cuando se combinan ambos tipos.
  - tipoVia: Representa el tipo de vía de un lugar.
  - numeroCalle: Representa el número de la calle en la que está la unidad luminosa.
  - calle: Representa el nombre de la calle o vía.
  - codigo: Representa el código que comparten un número de unidades luminosas que están en la misma calle.
  - distrito: Representa los 21 distritos de Madrid.
  - barrio: Represente los barrios que hay en Madrid.
  - Longitude: Representa la coorddenada X.
  - Latitude: Representa la coordenada Y.

# alumbrado-publico.nt
Es el resultado obtenido (en formato N-Triples) tras realizar el procesamiento de los datos del CSV con herramientas de transformación, como RMLMapper o morph-kgc.
