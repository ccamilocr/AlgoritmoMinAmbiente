Monitoreo de cicatrices de quema a través de imágenes satelitales
Indice espectral NBR Analisis en GEE (Google Earth Engine)
NOTA: Las librerías solo la primera vez que se corre el código se instalan quitando el numeral para que funcionen los !pip install

Índice Normalizado de Área Quemada (NBR)
El índice Normalizado de Área Quemada (NBR) es un índice diseñado para resaltar áreas quemadas en grandes zonas de incendio. La fórmula es similar a NDVI, excepto que combina el uso de longitudes de onda de infrarrojo cercano (NIR) e infrarrojo de onda corta (SWIR).

𝑁𝐵𝑅=𝑁𝐼𝑅−𝑆𝑊𝐼𝑅𝑁𝐼𝑅+𝑆𝑊𝐼𝑅
 
𝑁𝐼𝑅=Infrarojo cercano𝑆𝑊𝐼𝑅=Infrarojo de onda corta}Regiones del NBR
 
Instale la API de Python de Earth Engine y geemap. El paquete geemap Python se basa en los paquetes ipyleaflet y folium e implementa varios métodos para interactuar con las capas de datos de Earth Engine, como Map.addLayer (), Map.setCenter () y Map.centerObject (). El siguiente script comprueba si el paquete geemap ha sido instalado. De lo contrario, instalará geemap, que instala automáticamente sus dependencias, incluidas earthengine-api, folium e ipyleaflet.

Nota importante: una diferencia clave entre folium e ipyleaflet es que ipyleaflet se basa en ipywidgets y permite la comunicación bidireccional entre el front-end y el backend, lo que permite el uso del mapa para capturar la entrada del usuario, mientras que el folium está destinado a mostrar solo datos estáticos ( fuente). Tenga en cuenta que Google Colab actualmente no es compatible con ipyleaflet (fuente). Por lo tanto, si está usando geemap con Google Colab, debe usar import geemap.eefolium. Si está utilizando geemap con Binder o un servidor local Jupyter, puede usar import geemap, que proporciona más funcionalidades para capturar la entrada del usuario (por ejemplo, hacer clic y mover el mouse).
