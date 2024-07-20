# Introducción

Los incendios forestales son fenómenos naturales presentes desde tiempos inmemoriales. Sin embargo, en las últimas décadas, su frecuencia y severidad han aumentado significativamente debido a factores como el cambio climático, la deforestación y la actividad humana. Estos incendios tienen un impacto devastador en los ecosistemas, destruyendo la flora y fauna, afectando la calidad del aire y contribuyendo al cambio climático mediante la liberación de grandes cantidades de dióxido de carbono. Además, pueden tener consecuencias graves para las comunidades humanas, incluyendo la pérdida de vidas, propiedades y medios de subsistencia.

En este contexto, se realiza un diagnóstico y un análisis predictivo de la situación actual del fenómeno El Niño en 80 municipios específicos de Colombia. Este análisis, realizado entre el 3 de noviembre de 2023 y el 10 de mayo de 2024, utiliza herramientas tecnológicas para aportar conocimiento a las principales entidades implicadas en la gestión de incendios forestales, facilitando así la capacitación, control y monitoreo.

# Objetivos del Seguimiento y Monitoreo

Para mitigar los impactos de los incendios forestales, es crucial contar con sistemas eficientes de seguimiento y monitoreo de las áreas afectadas. Estos sistemas permiten:

1. **Detectar y evaluar rápidamente los incendios**: Proveer información oportuna para la toma de decisiones inmediatas durante un incendio.
2. **Analizar el impacto post-incendio**: Evaluar las cicatrices de quema para entender la extensión y severidad del daño causado.
3. **Planificar estrategias de recuperación**: Facilitar la restauración de las áreas afectadas mediante la identificación de zonas prioritarias.
4. **Prevenir futuros incendios**: Utilizar los datos históricos para identificar patrones y áreas de riesgo, mejorando las estrategias de prevención y gestión.

# Desarrollo del Algoritmo

El algoritmo para el monitoreo de cicatrices de quema se basa en el análisis de imágenes satelitales y el uso de técnicas avanzadas de procesamiento digital de imágenes y análisis geoespacial. A continuación, se describen los principales componentes y etapas del algoritmo:

1. **Recolección de imágenes satelitales**: Utilización de fuentes como Landsat y Sentinel, que proporcionan imágenes de alta resolución y con frecuencia temporal adecuada para el monitoreo continuo. Se empleó Google Earth Engine, una plataforma gratuita que facilita la búsqueda y utilización de información satelital a diferentes escalas.
   
2. **Detección de cambios**: Aplicación de técnicas de detección de cambios para identificar áreas que han sufrido alteraciones significativas, indicando la presencia de cicatrices de quema. Se utilizó interpretación visual con falso color usando bandas 'B8A', 'B4', 'B3', verificando posibles quemas mediante un polígono y dos fechas inicial y final para detectar la severidad del incendio.
   
3. **Clasificación de la severidad de quema**: Uso del Índice Normalizado de Área Quemada (NBR) para categorizar las cicatrices de quema según su severidad. Este índice resalta áreas quemadas en grandes zonas de incendio combinando longitudes de onda de infrarrojo cercano (NIR) e infrarrojo de onda corta (SWIR).
   
4. **Validación y calibración**: Comparación de los resultados del algoritmo con datos de campo tomados de GobFire Perimeters y otras fuentes para asegurar la precisión y confiabilidad de las detecciones.

# Fuentes de Información

Para la conformación de la línea base de áreas afectadas por incendios forestales, se utilizaron diversas fuentes de información, incluyendo:

- **Datos históricos de incendios**: Proporcionados por GobFire [GobFire Perimeters](https://gwis.jrc.ec.europa.eu/apps/country.profile/downloads).
- **Imágenes satelitales**: De alta resolución y frecuencia temporal, obtenidas de la plataforma [Google Earth Engine](https://developers.google.com/earth-engine).
- **Puntos de calor**: Para entender las condiciones que favorecen la ocurrencia y propagación de incendios [Puntos de Calor IDEAM](http://puntosdecalor.ideam.gov.co/?from_date=2024-04-01&to_date=2024-05-10&extent=(13.561133682107315_-93.42773437500001_-6.969465425858813_-55.04150390625001)&region=colombia).