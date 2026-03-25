# 📍 Punto Erizo: Cartografía Urbana y Datos Abiertos en Alajuela

**Punto Erizo** es una iniciativa de mapeo colaborativo nacida en el curso de **Sistemas de Información Geográfica (SIG)** del Instituto Tecnológico de Costa Rica. Más allá de un ejercicio académico, este proyecto representa un acto de **ciudadanía digital**: buscamos "iluminar" la infraestructura pública de Alajuela en el mapa global de **OpenStreetMap (OSM)**, transformando la observación de campo en datos abiertos y reutilizables para la planificación urbana, la accesibilidad y el sentido de pertenencia de la comunidad. El nombre rinde homenaje a la figura histórica de Juan Santamaría ("El Erizo"), simbolizando un mapa vivo que, al igual que nuestra identidad provincial, se construye con determinación y puntos de contacto precisos.

## 🏛️ Visión
El proyecto responde a la necesidad de contar con cartografía detallada y actualizada de los espacios de convivencia social. Académicamente, integra metodologías de **Sistemas de Información Geográfica (SIG)** con trabajo de campo riguroso:
* **Transparencia:** Democratización del acceso a la información sobre bienes públicos.
* **Metodología:** Aplicación de estándares internacionales de etiquetado y validación geoespacial.
* **Impacto:** Mejora de la navegación y visibilidad de zonas verdes y monumentos históricos en plataformas de código abierto.

## 🌳 Ámbito de Intervención
El levantamiento se concentró en dos pulmones sociales del casco central de Alajuela:
* [*Parque Calián Vargas*](https://www.openstreetmap.org/way/264040046).
* [*Parque Juan Santamaría*](https://www.openstreetmap.org/way/931893398).

## 📋 Guía de Mapeo
Hemos estandarizado la captura de 10 elementos clave, asegurando la representación de las tres geometrías fundamentales: puntos, líneas y polígonos.

| Elemento | Geometría | Etiqueta principal | Etiquetas adicionales | OSM Wiki |
| :--- | :--- | :--- | :--- | :--- |
| **Árbol** | Punto | `natural=tree` | `species=*` · `circumference=*` · `height=*` · `name=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:natural%3Dtree) |
| **Banca** | Punto<br>Línea | `amenity=bench` | `backrest=yes/no` · `direction=*` · `seats=*` · `colour=*` · `material=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:amenity%3Dbench) |
| **Basurero** | Punto | `amenity=waste_basket` | `waste=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:amenity%3Dwaste_basket) |
| **Camino** | Línea<br>Área | `highway=footway` | `bicycle=yes/no` · `surface=*` · `name=*` · `wheelchair=yes/no` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:highway%3Dfootway) |
| **Arte** | Punto<br>Línea<br>Área | `tourism=artwork` | `artwork_type=*` · `artist_name=*` · `operator=*` · `historic=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Key:artwork_type) |
| **Parque Infantil** | Punto<br>Área | `leisure=playground` | `min_age=*` · `max_age=*` · `operator=*` · `name=*` · `playground=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:leisure%3Dplayground) |
| **Parque Biosaludable** | Punto<br>Área | `leisure=fitness_station` | `sport=fitness` · `fitness_station=*` · `name=*` · `description=*` · `opening_hours=*` | [🔗](https://wiki.openstreetmap.org/wiki/ES:Tag:leisure%3Dfitness_station) |
| **Mural** | Línea<br>Área | `artwork_type=mural` | `tourism=artwork` · `artist_name=*` · `start_date=*` · `historic=*` · `artwork_subject=*` | [🔗](https://wiki.openstreetmap.org/wiki/Tag:artwork_type%3Dmural) |
| **Señal** | Punto<br>Línea | `traffic_sign=*` | `direction=*` | [🔗](https://wiki.openstreetmap.org/wiki/Key:traffic_sign) |
| **Iluminación** | Punto | `highway=street_lamp` | `ref=*` · `lamp_type=*` · `lamp_mount=*` · `lamp_model=*` · `light:colour=*` · `light:shape=*` | [🔗](https://wiki.openstreetmap.org/wiki/Tag:highway%3Dstreet_lamp) |

## 🗂️ Estructura del Repositorio
Este repositorio organiza los productos técnicos generados durante las tres semanas de ejecución:

* **`/layouts`**: Contiene la interfaz de botones bilingüe (`en.xml`, `es.xml`) para **OSMTracker**. Incluye iconos personalizados diseñados para una captura eficiente y sistemática en dispositivos móviles.
* **`/fieldpapers`**: Mapas analógicos utilizados para la validación espacial y anotaciones manuscritas, fundamentales para el registro de geometrías complejas.
* **`/tracks`**: Registros crudos en formato **GPX**, multimedia y notas de campo que respaldan la veracidad de los datos recolectados.