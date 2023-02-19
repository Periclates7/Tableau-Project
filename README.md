![Cabecera](https://github.com/Periclates7/Tableau-Project/blob/main/img/cabecera.jpg)
# 📉 TABLEAU PROJECT -> League of Legends World Championship 2022 Stats 🏆🎮
  
El objeto del presente proyecto es la realización de un análisis a través de un *dashboard* acerca de los datos estadísticos extraídos en el campeonato mundial del videojuego League of Legends. Para ello se ha contado con el siguiente *dataset*, [WORLDS-2022-Champs-Teams-EDA](https://www.kaggle.com/code/erenakbulut/worlds-2022-champs-teams-eda/data), contando solo con aquellos conjuntos de datos que se refieren al *main event*, es decir, la fase final del campeonato. Para hacer el análisis se ha contado con la herramienta de visualización Tableau.
  
## 🎯 OBJETIVOS DEL PROYECTO 
  
1. Crear un repositorio en GitHub con una buena organización de los recursos.
2. Extraer los datos de manera óptima.
3. Aplicar herramientas, técnicas y metodologías para la limpieza de datos acordes a nuestras necesidades:
    - Filtrado de los datos extraidos
    - Exploración del conjunto de los datos
    - Limpieza de valores nulos
    - Transformación de diferentes conjuntos de datos
    - Librerías utilizadas: Pandas, Numpy, regex, Pylab, Seaborn.
3. Exportar los datos limpios.
4. Cargar los datos en Tableau.
5. Realizar gráficos coherentes para nuestro análisis.
6. Creación de un dashboard.
  
## ⛏ EXTRACCIÓN Y LIMPIEZA DE LOS DATOS  
  
Como se mencionaba en lineas anteriores, la base del proyecto es un *dataset* extraído de Kaggle en formato .csv, del cual solo tendremos en cuenta la fase final de la competición. Estas tres tablas resultantes, están en un buen formato para cumplir nuestro objetivo de cargar los datos en Tableau y que puedan ser manejabes desde esta herramienta. La única modificación que se realiza al respecto es la transformación de ciertas columnas de valores de *str* a tipo *float* así como la eliminación de ciertos valores nulos que se generan al no cumplirse las estadísticas mínimas en partida.
  
El código empleado para este proceso se encuentra en la siguiente ruta del presente repositorio: 'src/limpieza_lolwords_stats.ipynb'
  
## 📈 REALIZACIÓN DEL DASHBOARD
  
El fin último de esta fase es la determinación de la relación existente entre la actuación en partida de los diferentes equipos y la consecución de la victoria en partida. Para ello se empieza tomando la primera de nuestras tablas, la referente a las estadísticas de cada campeón. 
  
Empleamos gráficos de barras para mostrar los campeones más escogidos y los campeones que han obtenido más victorias. De esta manera podemos comprobar que hay una clara tendencia a escoger ciertos campeones ya que en principio encajan mejor en el *meta* (estado actual del juego). Mediante el siguiente gráfico nos damos cuenta de que no necesariamente los campeones más escogidos tienen una relación con el número de victorias que proporcionan al equipo, ya que los componentes que determinan la victoria son mucho más amplios y los iremos descubriendo a lo largo de nuestro dashboard.
  
![1-Gráfico correlación pick rate vs vic](https://github.com/Periclates7/Tableau-Project/blob/main/img/1.%20pick%20rate%20vs%20win%20rate2.png)
  
Si que se puede comprobar una clara correlación entre el lado del mapa que le toca a cada equipo con su porcentaje de *win rate*. En este caso los campeones que juegan en el lado azul del mapa, tienen más probabilidades de ganar la partida.
  
![2-Correlación lados del mapa](https://github.com/Periclates7/Tableau-Project/blob/main/img/2.%20blue:red%20size2.png)  
  
Por otro lado, mediante gráficos de barras visualizamos la cantidad de asesinatos, muertes y asistencias por rol. Es interesante indagar en este asunto ya que una buena distribución de estos datos según el rol, asegura un buen rendimiento del equipo en partida.
  
![3-Gráfico kills, muertes y assists](https://github.com/Periclates7/Tableau-Project/blob/main/img/3.%20kda%20por%20rol2.png)
    
Es el momento de adentrarse en las estadísticas de los equipos. En primer lugar intento determinar la relación entre el número de muertes y número de victorias. Claramente existe una alta correlación. 
  
![4-kills vs winrate](https://github.com/Periclates7/Tableau-Project/blob/main/img/4.%20kills%20vs%20wins2.png)
  
A continuación, hago el mismo estudio tomando como variable la captura de los objetivos neutrales que aparecen en partida (Dragón, Baron y Heraldo). Llego a la conclusión de que el monstruo neutral más importante en partida es el Baron.
  
![5-Control Baron](https://github.com/Periclates7/Tableau-Project/blob/main/img/5.%20baron%2C%20drag%2C%20herald2.png)
  
El control de determinadas zonas del mapa a través de la visión que aportan nuestros guardianes, es determinante a la hora de ganar una partida. Así nos lo muestra el siguiente gráfico:
  
![6-Gráfico control vision](https://github.com/Periclates7/Tableau-Project/blob/main/img/6.%20Vision%20y%20jungla2.png)  

Por último me propuse estudiar el impacto que tienen las diferentes fases del juego en el porcentaje de winrate. Mediante el siguiente gráfico se puede observar que los equipos que dominan en fases tardías de la partida tienen más posibilidades de alcanzar la victoria.
  
![7-Gráfico control early, mid late game](https://github.com/Periclates7/Tableau-Project/blob/main/img/7.%20early:late%20game2.png)
  
## 📝 CONCLUSIONES Y EVOLUCIÓN DEL PROYECTO
  
La fase de visualización de datos en cualquier proyecto relacionado con el análisis de conjuntos de datos es imprescindible para la correcta comprensión de los mismos. Es una forma rápida y eficiente de poder llegar a conclusiones y posibilita la toma de decisiones informadas. En próximas fases de desarrollo, se pretende mediante las metodologías empleadas en el presente proyecto, poder realizar un estudio de las temporadas regulares de cada equipo y mediante Machine Learning hacer un modelo predictivo aplicado al siguiente campeonato mundial del videojuego League of Legends.
  
Para la consulta del dashboard completo, podrán hacerlo a través del enlace contenido en el siguiente archivo: 'src/main.txt'
