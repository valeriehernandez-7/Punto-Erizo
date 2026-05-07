# 📍 Punto Erizo: Nuestra historia, nuestro mapa, nuestra Alajuela

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

* **`/geojson`**: Archivos GeoJSON resultantes de las consultas en OverPass Turbo. Contienen los datos extraídos del área de estudio para su análisis y visualización en sistemas SIG.
    * `parks.geojson`: Elementos mapeados por los integrantes del grupo (`quintsx`, `Ari Jiménez`) dentro de los polígonos del Parque Juan Santamaría y el Parque Calián Vargas.
    * `alajuela.geojson`: Todos los puntos de interés relevantes para el proyecto, extraídos para toda la ciudad de Alajuela.
* **`/layouts`**: Contiene la interfaz de botones bilingüe (`en.xml`, `es.xml`) para **OSMTracker**. Incluye iconos personalizados diseñados para una captura eficiente y sistemática en dispositivos móviles.
* **`/fieldpapers`**: Mapas analógicos utilizados para la validación espacial y anotaciones manuscritas, fundamentales para el registro de geometrías complejas.
* **`/tracks`**: Registros crudos en formato **GPX**, multimedia y notas de campo que respaldan la veracidad de los datos recolectados.

## 📝 Edición del Mapa en OpenStreetMap

Como parte del trabajo de campo, se procedió a la edición y agregado de los 10 elementos mapeados en los parques correspondientes. Las ediciones fueron realizadas utilizando el editor iD de OpenStreetMap, aplicando correctamente las etiquetas (tags) documentadas en la wiki de OSM.

### ✍ Changesets

#### 📍 Parque Calián Vargas [Ari Jiménez](https://www.openstreetmap.org/user/Ari%20Jim%C3%A9nez)

| Changeset | Enlace de descarga |
| :--- | :--- |
| `182042317` | [🔗 Descargar XML](https://www.openstreetmap.org/api/0.6/changeset/182042317/download) |
| `182169400` | [🔗 Descargar XML](https://www.openstreetmap.org/api/0.6/changeset/182169400/download) |

#### 📍 Parque Juan Santamaría [quintsx](https://www.openstreetmap.org/user/quintsx)

| Changeset | Enlace de descarga |
| :--- | :--- |
| `182043565` | [🔗 Descargar XML](https://www.openstreetmap.org/api/0.6/changeset/182043565/download) |
| `182043870` | [🔗 Descargar XML](https://www.openstreetmap.org/api/0.6/changeset/182043870/download) |
| `182044362` | [🔗 Descargar XML](https://www.openstreetmap.org/api/0.6/changeset/182044362/download) |

> 💡 Los archivos descargados contienen el registro completo de las operaciones de edición realizadas sobre OSM, incluyendo nodos, vías, relaciones y las etiquetas asignadas a cada elemento.

## 🛰️ [Consultas OverPass Turbo](https://overpass-turbo.eu/)
Utilizamos OverPass Turbo para validar y extraer los datos geoespaciales. A continuación se presentan las consultas QL utilizadas:

### 1. Extracción de elementos por usuario en los Parques : [parks.geojson](https://github.com/valeriehernandez-7/Punto-Erizo/blob/master/geojson/parks.geojson)
Esta consulta extrae todos los elementos (nodos, vías y relaciones) creados o modificados por los miembros del grupo dentro de las áreas de los dos parques de interés.

```overpass-ql
[out:json][timeout:25];
// Define the search area as Parque Juan Santamaría using geocoding
{{geocodeArea:Parque Juan Santamaría}}->.searchAreaJuanSantamaria;

// Define the search area as Parque Calián Vargas using geocoding
{{geocodeArea:Parque Calián Vargas}}->.searchAreaCalianVargas;

// Find all elements (nodes, ways, relations) created or edited by the specified users within the search area
(
  node(user:"quintsx", "Ari Jiménez")(area.searchAreaJuanSantamaria);
  way(user:"quintsx", "Ari Jiménez")(area.searchAreaJuanSantamaria);
  relation(user:"quintsx", "Ari Jiménez")(area.searchAreaJuanSantamaria);

  node(user:"quintsx", "Ari Jiménez")(area.searchAreaCalianVargas);
  way(user:"quintsx", "Ari Jiménez")(area.searchAreaCalianVargas);
  relation(user:"quintsx", "Ari Jiménez")(area.searchAreaCalianVargas);
);

// Output the results with full geometry and tags
out body;
// Output child elements (nodes of ways) for complete geometry
>;
// Output skeleton (IDs and metadata) for relations
out skel qt;
```

### 2. Extracción de POIs en toda la ciudad de Alajuela : [alajuela.geojson](https://github.com/valeriehernandez-7/Punto-Erizo/blob/master/geojson/alajuela.geojson)
Esta consulta extrae todos los elementos de interés (árboles, bancas, basureros, arte, parques infantiles, etc.) presentes en la zona urbana de Alajuela, Costa Rica.

```overpass-ql
[out:json][timeout:25];
// Define the search area as Alajuela, Costa Rica using geocoding
{{geocodeArea:Alajuela, Costa Rica}}->.searchArea;

// Find all elements (nodes, ways, relations) created or edited by the specified users within Alajuela
(
  node["natural"="tree"](area.searchArea);
  way["natural"="tree"](area.searchArea);
  relation["natural"="tree"](area.searchArea);

  node["amenity"="bench"](area.searchArea);
  way["amenity"="bench"](area.searchArea);
  relation["amenity"="bench"](area.searchArea);

  node["amenity"="waste_basket"](area.searchArea);
  way["amenity"="waste_basket"](area.searchArea);
  relation["amenity"="waste_basket"](area.searchArea);

  node["highway"="footway"](area.searchArea);
  way["highway"="footway"](area.searchArea);
  relation["highway"="footway"](area.searchArea);

  node["tourism"="artwork"](area.searchArea);
  way["tourism"="artwork"](area.searchArea);
  relation["tourism"="artwork"](area.searchArea);

  node["leisure"="playground"](area.searchArea);
  way["leisure"="playground"](area.searchArea);
  relation["leisure"="playground"](area.searchArea);  

  node["leisure"="fitness_station"](area.searchArea);
  way["leisure"="fitness_station"](area.searchArea);
  relation["leisure"="fitness_station"](area.searchArea);

  node["artwork_type"="mural"](area.searchArea);
  way["artwork_type"="mural"](area.searchArea);
  relation["artwork_type"="mural"](area.searchArea); 

  node["traffic_sign"="stop"](area.searchArea);
  way["traffic_sign"="stop"](area.searchArea);
  relation["traffic_sign"="stop"](area.searchArea);

  node["highway"="street_lamp"](area.searchArea);
  way["highway"="street_lamp"](area.searchArea);
  relation["highway"="street_lamp"](area.searchArea);  
);

// Output the results with full geometry and tags
out body;
// Output child elements (nodes of ways) for complete geometry
>;
// Output skeleton (IDs and metadata) for relations
out skel qt;
 
```
