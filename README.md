L'objectif de ce notebook est de presenter une methode qui permet d'estimer le changement de la surface en eau d'un lac en comparant les images satellitaires observées à 2 dates differentes. Pour estimer ce changement nous allons utiliser deux images du satellite Sentinel-2 de l'ESA (European Space Agency). Nous allons calculer le Normalize Difference Water Index (NDWI) ou indice d’eau par différence normalisée pour chacune de ces images et comparer les resultats obtenus.

Le NDWI (McFeeters en 1996) est utilisé principalement pour détecter et surveiller de faibles changements de la teneur en eau aux bassins d’eau. En exploitant les longueurs d'ondes proche infrarouge (Near Infrared) et le vert visible (Green), le NDWI permet d’améliorer la détection des bassins d’eau sur les images satellitaires.

L'equation pour le calcul de NDWI à partir des images satellitaires sentinel-2 est : NDWI = (Band 3 - Band 8) / (Band 3 + Band 8)

Le vert visible maximise la capacité de réflexion de la surface de l’eau. Le proche infrarouge minimise la capacité de réflexion de la surface de l'eau. Ce contraste est mis à profit pour calculer le NDWI.

La valeur de l'indice NDWI varie entre -1 et 1. L'interprétation des valeurs NDWI peut varier selon l'application et le type d'environnement étudié. Pour la détection des plans d'eau, l'une des principales applications de l'indice NDWI, les valeurs de l'indice NDWI correspondent approximativement aux plages suivantes : Les valeurs de l'indice NDWI correspondent approximativement aux plages suivantes :

0.2 - 1 : Indiquent généralement des plans d'eau clairs et ouverts.
0.0 - 0.2 : Peuvent représenter des eaux peu profondes, des zones humides ou des zones à forte humidité du sol.
-0.3 - 0.0 : Indiquent généralement une sécheresse modérée, surfaces non aqueuses
-1 - -0.3 : Indiquent généralement une sécheresse, surfaces non aqueuses
McFEETERS, S. K. (1996). The use of the Normalized Difference Water Index (NDWI) in the delineation of open water features. International Journal of Remote Sensing, 17(7), 1425–1432. https://doi.org/10.1080/01431169608948714
