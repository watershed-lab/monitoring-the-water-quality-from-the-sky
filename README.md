## DEMOSTRACIÓN DE TELEDETECCIÓN CON APRENDIZAJE NO SUPERVISADO DE VARIACIONES EN LA CALIDAD DEL AGUA

Sobre una escenas de Landsat8 correspondiente al entorno del embalse de la Cuerda del Pozo (España) con este lleno, se usan las 7 primeras bandas monoespectrales de su sensor óptico y el algoritmo k-means para obtener en primer lugar los diferentes usos del suelo. A continuación se crea una máscara, que georeferenciada se convierte en un shapefile de ESRI. Este shape se retoca manualmente con QGIS para después, sobre otras 3 escenas más, con esas mismas bandas monoespectrales, se aplica la máscara para recortar el contorno de la lámina de agua.

Con una segunda aplicación de k-means ahora sobre las imágenes recortadas, se consigue forzar al algoritmo a que detecte zonas con diferencias espectrales en la masa de agua. Se obtiene también el perímetro de estas zonas con el algoritmo de Canny.

Por último, se extraen las variaciones espectrales a lo largo de dos secciones en diferentes escenas, y la firma espectral de un punto en las cuatro escenas; y se relacionan estas con las variaciones en la calidad del agua, fundamentalmente eutrofización y turbidez.


Ejecutable en pc's domésticos. Recomendado i5 de 4 procesadores o superior y memoria RAM de 8Gb o superior.

Se incluyen las imágenes originales obtenidas de Landsat, las máscaras generadas en formato txt, geotiff y shp; el shp editado para eliminar el resto de valores y otras pequeñas láminas de agua, y las imágenes recortadas.


### Rutas para la ejecución

El archivo con el cuaderno debe ponerse en la carpeta del usuario. 
Las imágenes y el resto de archivos se deben colocar en sus correspondientes carpetas, a partir de la que contiene este cuaderno, siguiendo la misma estructura que en este GitHub.

