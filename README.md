<h2>Descripción del Código</h2>
<h3>1. Carga de Datos</h3>
Preparación del entorno de trabajo utilizando las siguientes librerías:<br>
Pandas, Numpy, Matplotlib, Seaborn, Plotly: Para análisis exploratorio y visualización interactiva.<br>
Sklearn y Statsmodels: Para modelado predictivo y análisis de series de tiempo.<br>
Se lee el archivo .csv que contiene los registros diarios de rendimiento de los equipos de carguío y transporte de mineral (CAEX y palas). Este archivo incluye información clave como tonelaje, ciclos del equipo, distancia recorrida y fechas.
Se verifica la estructura del dataset para asegurar la integridad de los datos.
<h3>2. Preprocesamiento</h3>
Conversión de fechas: La columna de fechas se convierte a formato datetime para facilitar el análisis temporal.<br>
Limpieza de datos: Se gestionan valores nulos o inválidos, reemplazando valores infinitos y eliminando filas con NaN en variables críticas como eficiencia_ciclo, tonelaje y distancia.<br>
Este paso asegura que los datos sean adecuados para el análisis y evita errores en el modelado.<br>
<h3>3. Exploración</h3>
Análisis estadístico descriptivo de las variables principales:<br>
Eficiencia por ciclo: Tonelaje transportado dividido por el ciclo de carguío.<br>
Análisis temporal: Visualización de las series de tiempo del ciclo total del camión y su relación con el tonelaje transportado.<br>
Gráficos exploratorios: Gráficos de dispersión y series temporales para entender las relaciones clave entre variables.<br>
<h3>4. Análisis de Rendimiento de los Equipos</h3>
Análisis de eficiencia de los equipos en series de tiempo, media móvil y tendencias:<br>
4.1 Serie de tiempo, media móvil y tendencia del ciclo del CAEX.<br>
4.2 Serie de tiempo, media móvil y tendencia del ciclo de la Pala. <br>
4.3 Relación entre tonelaje movido y ciclo del camión. <br>
4.4 Eficiencia de tonelaje por ciclo: camiones y palas. <br>
<h3>5. Ranking de Rendimiento</h3>
Cálculo del rendimiento de los equipos en operaciones: <br>
5.1 Calculo y ranking de rendimiento diario.<br>
5.1.1 Ranking de rendimiento de los equipos CAEX por puntaje total. <br>
5.2 Análisis de productividad: paladas por ciclo. <br>
5.3 Identificación de las mejores combinaciones de pala y CAEX.<br>
5.4 Ranking de rendimiento de las palas. <br>
5.5 Desempeño de los equipos de carguío y transporte. <br>
5.6 Rendimiento de los equipos CAEX a lo largo del tiempo. <br>
5.7 Rendimiento de las palas a lo largo del tiempo. <br>
5.8 Identificación de factores críticos. <br>
<h3>6. Modelado Predictivo</h3>
Aplicación de modelos para predecir el rendimiento:<br>
Modelo ARIMA: Para prever los tiempos de ciclo de los camiones en función de los datos históricos.<br>
Regresión lineal con Sklearn: Para identificar las combinaciones más eficientes de pala y CAEX.<br>
Statsmodels: Para ajuste y análisis predictivo de series temporales.<br>
<h3>7. Análisis Estadístico para Identificar Factores Criticos.</h3>
7.1 Importancia de las variables predictoras en la regresión lineal.<br>
7.2 Conclusión de factores críticos:<br>
Eficiencia de carguío: Influencia del tonelaje por ciclo.<br>
Distancia recorrida: Impacto tanto en vacío como en lleno.<br>
Número de paladas necesarias: Efecto en el tiempo total del ciclo.<br>
Ciclos del camión y la pala: Sincronización y tiempo de espera.<br>
Estas variables son determinantes para evaluar la productividad en las operaciones de transporte y carguío.<br>

<h3>8. Propuesta de Mejora Operativa</h3>
Recomendaciones basadas en el análisis:<br>
Optimización de la distancia recorrida: Reducir la distancia entre la zona de carguío y descarga.<br>
Mejora en la sincronización entre pala y camión: Reducir tiempos de espera innecesarios.<br>
Monitoreo continuo de eficiencia: Implementar modelos predictivos para anticipar caídas en la productividad.<br>
