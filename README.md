

# Ingeniero Topògrafo Geomático 1604

# PE-ITP
    
Daniel Alexander Peralta Landin
correo electronico: 
dperalta1@ucol.mx


# Abstract

Se pretende calcular con exactitud el calculo de vegetacion sana para poder dar una respuesta a autoridades gubernamentales, esto con la clara finalidad de gestionar proyectos que promuevan la prosperacion de la flora y de manera secundaria de la fauna.

# 1. 	Introduction 

El proyecto que se aboradara en este documento  es uno de NDVI ( Indice de vegetación diferencial normalizado o indice), para poder entender mejor de lo que estamos hablando abordaremos los principales conceptos los cuales son el mencionado anteriormente NDVI (Indice de vegetació diferencial normalizado o indice), el cual cumple con la finalidad de calcular mediante determinadas bandas satelitales la reflectancia de longitudes de onda en diferentes secciones del espectro electromagnetico, por lo cual se puede calcular las diferentes longitudes de onda.De manera similar un programa informatico, cumple con la obligacion de seguir una secuaencia de instrucciones, el cual toma la estructura de un codigo fuente que es entendible para humanos y logicamente leido por los computadores. 

# 2. 	palabras clave

rograma informatico, calculo, medio ambiente, proyecto.

![primer imagen](https://user-images.githubusercontent.com/52055695/83090884-7300f000-a05f-11ea-8a36-646422c117bf.jpg)

# 2.1. 	Manejo de datos

# 1.	Tratamiento de datos

El programa tomara los datos recaba-dos de archivos vectoriales, que el usuario ingrese en este, de esta manera las instrucciones en el código seguirán hasta que se obtenga lo buscado.

![PalabrasdelTextoAlternativo](https://github.com/agonzalez53/ILIMUNADO-VIAL/blob/master/IMAGENES/poli.jpg)

Archivo vectorial de la mancha urbana del municipio de Coquimatlán.

2.	Plataforma

Se pretende que este programa funcio-né con la plataforma Windows, anqué se espera que para poder aumentar el uso de este programa se convierta en multiplataforma.

3.	Programas

El programa que tiene una gran rele-vancia en este proyecto es el de PyQgis. Esto por  la gran cantidad de li-brerías que podrán facilitar estos proce-dimientos.

# 2.2. 	Resultados

# Tratamiento de datos

El programa tomara los datos recabados de archivos vectoriales, que el usuario ingrese en este, de esta manera las instrucciones en el código seguirán hasta que se obtenga lo buscado.

![PalabrasdelTextoAlternativo](https://github.com/agonzalez53/ILIMUNADO-VIAL/blob/master/IMAGENES/poli.jpg)

Archivo vectorial de la mancha urbana del muni-cipio de Coquimatlán.

Se pretende que este programa funcioné con la plataforma Windows, anqué se espera que para poder aumentar el uso de este programa se convierta en multiplataforma.
Programas
El programa que tiene una gran relevancia en este proyecto es el de PyQgis. Esto por  la gran cantidad de librerías que podrán facilitar estos procedimientos.

Las coordenadas que se mandan llamar por medio de un código ya establecido hacen que se relacionen con  lugares en la tierra reales. La decisión sobre el sistema de proyecciones y el sistema de coordenadas de referencia a usar depende de la zona que se desea trabajar, del análisis que se pretende hacer y  a menudo de la disponibilidad.

También como el sistema de proyecciones de coordenadas existen otra forma de representar la tierra que es muy útil y en este caso a noso-tros nos facilitó un poco más las cosas para poder llevar con mayor facilidad el proyecto para representar la forma del lugar donde será el estudio.

Pueden existir algunos problemas con este enfoque, ya que en la mayoría se consérvenla mayor parte de la forma de la tierra e ilustra la configuración espacial de los objetos del tamaño continental.

![PalabrasdelTextoAlternativo](https://github.com/agonzalez53/ILIMUNADO-VIAL/blob/master/IMAGENES/poli%20pun.jpg)

En esta muestra ya se dan a conocer los puntos la localización que son los que se buscan para tener mejor la iluminación, son los que se pre-tenden instalar para que en esta área que se llevó el proyecto en práctica  tenga una mejor ycómoda iluminación para los habitantes de esta colonia del municipio de Coquimatlán.

Para poder llegar a tener la localización de cada punto estos fueron llamados de un archivo en  con extensión  de csv. Que  se tenían   con coordenadas. 

Una vez que ya se tenían las coordenadas esto trajo consigo cada punto como se muestra en la imagen. Teniendo también con este procesa-miento se puede obtener el área total de la su-perficie a trabajar y tener en cuenta los gastos que se llegaran a utilizar en un proyecto como este si es que se llevara a la vida cotidiana.

Posteriormente ya que se ubicaron los punto  y se obtuvo el área en una base de dato se guar-daron todo los datos obtenidos, llamándole a esta base de datos postes de luz.

![PalabrasdelTextoAlternativo](https://github.com/agonzalez53/ILIMUNADO-VIAL/blob/master/IMAGENES/poste.jpg)

Finalmente todos los datos obtenidos de dicho código de dicho proyecto quedaran guardados  en esta base de datos.

# CODIGO

capa = QgsVectorLayer(data_source, layer_name, provider_name)
if not layer.isValid():
  print "Layer failed to load!"
#creamos una memoria layer
mem_layer = QgsVectorLayer("Point?crs=epsg:4326&field=id:integer""&field=area:double&index=yes",
                            "Points",
                            "memory")
                              
  
#agregamos un mapa
QgsMapLayerRegistry.instance().addMapLayer(mem_layer)
  
#Preparamos el mapa para editar
mem_layer.startEditing()
  
#agregamos puntos
points = [QgsPoint(-150,61),QgsPoint(-151,61),QgsPoint(-151,62)]
 
#calculamos el numero de puntos
n = len(points)
if n <= 0:
    print ("area =", n*5)
feature = []
 
for i in range(n):
    feat =QgsFeature()
    feature.append(feat)

  
#set attributes values 
for i in range(n):
    feature[i].setGeometry(QgsGeometry.fromPoint(points[i]))  #Set geometry
    feature[i].setAttributes([i,area[i]])
    mem_layer.addFeature(feature[i], True)
  
#paramos la edicion
mem_layer.commitChanges()
 
#hacemos zoom a la layer y la activmos
iface.zoomToActiveLayer()


# PÓSTER

![PalabrasdelTextoAlternativo](https://github.com/agonzalez53/ILIMUNADO-VIAL/blob/master/IMAGENES/POSTER.jpg)

# CONLUCIONES


# Daniel Alexandro Peralta Landin

Este proyecto me ayudo mucho en la materia de programación, esto debido a que en la necesidad de crear un programa que automatice los pasos para agilizar cualquier tratamiento de datos. 

En general el proyecto me ayudo en mejorar mis habilidades con PyQGIS, principalmente por que no había utilizado todos estos pasos en un proyecto real, pero al poco tiempo de estar trabajando en este proyecto me percate de mis debilidades y fortalezas en el área. 
