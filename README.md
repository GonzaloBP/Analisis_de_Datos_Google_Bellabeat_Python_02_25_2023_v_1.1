## Análisis de Caso de Estudio: Bellabeat (Proyecto Final del Certificado de Google)

Este repositorio contiene el análisis de caso de estudio para Bellabeat, el proyecto final del Certificado Profesional de Análisis de Datos de Google. El objetivo es analizar datos de uso de smartwatches de la competencia (Fitbit) para identificar tendencias y patrones que puedan guiar la estrategia de marketing de Bellabeat.
El análisis sigue el ciclo de vida completo de un proyecto de datos: Preguntar, Preparar, Procesar, Analizar, Compartir y Actuar.

link a la notebook(kaggle): https://www.kaggle.com/code/gonzalobp/an-lisis-de-datos-caso-bellabeat-python-2023

### Tarea Empresarial (Fase de Pregunta)

El objetivo principal es analizar los datos de uso de dispositivos inteligentes para descubrir tendencias y patrones clave. A partir de estos hallazgos, se deben generar recomendaciones de alto nivel que informen y guíen la futura campaña de marketing de Bellabeat, ayudando a la empresa a crecer y a mejorar sus productos.

### Fuente de Datos (Fase de Preparación)

Dataset: FitBit Fitness Tracker Data (disponible en Kaggle).
Contexto: Los datos fueron generados por 30 usuarios de Fitbit que consintieron en enviar sus datos personales de seguimiento de actividad, frecuencia cardíaca y sueño.
Autores: Furberg, R., Brinton, J., Keating, M., & Ortiz, A. (2016).
Herramientas: Se utilizó Python con las librerías Pandas, Matplotlib y Seaborn para todo el proceso, garantizando un análisis reproducible y transparente.
Limitaciones Identificadas
Un paso crucial del análisis fue la evaluación de la calidad de los datos. Se identificaron las siguientes limitaciones:
Muestra Pequeña: El dataset solo contiene datos de 30 participantes, lo que limita la generalización de los hallazgos a una población más amplia.
Antigüedad de los Datos: Los datos fueron recolectados en 2016, por lo que las tendencias de comportamiento podrían haber cambiado.
Falta de Datos Demográficos: No se incluye información sobre el sexo, la edad o el nivel de condición física de los participantes, lo cual es crítico dado que el público objetivo de Bellabeat son las mujeres.

### Proceso y Limpieza de Datos (Fase de Procesamiento)
   
Para asegurar la integridad del análisis, se llevaron a cabo los siguientes pasos de limpieza y transformación:
Carga de Datos: Se cargaron los archivos CSV dailyActivity_merged.csv, weightLogInfo_merged.csv y sleepDay_merged.csv en dataframes de Pandas.

Exploración Inicial: Se evaluó la estructura de los datos, los tipos de cada columna y la presencia de valores nulos o duplicados.
Limpieza de Datos:
Se convirtieron las columnas de fecha de tipo object a datetime para permitir análisis temporales.
Se eliminaron registros duplicados.
Se identificaron y eliminaron 78 registros irrelevantes correspondientes a días donde los usuarios no registraron pasos (TotalSteps = 0), ya que probablemente indicaban que el dispositivo no fue utilizado.
Ingeniería de Características (Feature Engineering): Se creó una nueva columna dayOfWeek para facilitar el análisis de patrones semanales.

### Análisis y Hallazgos Clave (Fase de Análisis)

El análisis se centró en encontrar relaciones entre las diferentes métricas de actividad y el gasto calórico, así como en identificar patrones de uso a lo largo de la semana.

Hallazgo 1: La Actividad Intensa es el Principal Impulsor del Gasto Calórico
El análisis de correlación de Pearson reveló una correlación positiva y moderada (r = 0.61) entre los minutos de actividad muy intensa (VeryActiveMinutes) y las calorías quemadas. Las demás formas de actividad (moderada y ligera) mostraron una correlación mucho más débil.
Insight: Los usuarios que dedican tiempo a actividades de alta intensidad son los que ven un mayor impacto en su gasto calórico.

Hallazgo 2: Los Fines de Semana son los Días de Mayor Actividad
Al analizar el gasto calórico promedio por día de la semana, se observó un ligero pero consistente aumento durante los sábados y domingos.
Insight: Los usuarios tienden a ser más activos o a realizar actividades que queman más calorías durante el fin de semana.

Hallazgo 3: La Mayor Parte del Tiempo de Actividad es de Baja Intensidad
Incluso entre los usuarios más activos, la mayor parte de los minutos registrados corresponden a actividad ligera (aprox. 70-80% del tiempo), seguida de la actividad sedentaria. Esto sugiere que las actividades cotidianas (caminar, tareas domésticas) componen la base de la actividad diaria.

Insight: Aunque la actividad intensa es la más efectiva para quemar calorías, la actividad ligera es la más frecuente.

### Recomendaciones Estratégicas (Fase de Compartir y Actuar)
Basado en los hallazgos, se proponen las siguientes recomendaciones para la campaña de marketing de Bellabeat:

-Promocionar los Beneficios de la Actividad Intensa: La campaña de marketing debería destacar cómo los productos de Bellabeat (Leaf, Time) ayudan a los usuarios a monitorear y optimizar sus entrenamientos de alta intensidad, que son los que generan un mayor gasto calórico.

-Lanzar Campañas y Retos de Fin de Semana: Bellabeat podría crear contenido, notificaciones y retos especiales en su app para los fines de semana (ej. "Reto de Pasos del Sábado", "Domingo Activo"), capitalizando la tendencia natural de los usuarios a ser más activos en esos días.

-Combatir el Sedentarismo con Notificaciones Inteligentes: Dado que el tiempo sedentario es una constante, Bellabeat puede publicitar sus funciones de recordatorio para moverse.La campaña podría enfocarse en cómo sus dispositivos ayudan a las usuarias a integrar pequeños momentos de actividad a lo largo del día.

-Crear Contenido sobre Rutinas Efectivas: Bellabeat puede ofrecer en su app y redes sociales contenido sobre rutinas cortas y de alta intensidad (HIIT), mostrando cómo maximizar la quema de calorías en poco tiempo, lo cual se alinea con el hallazgo de que la actividad intensa es la más correlacionada con este objetivo.

**Stack Tecnológico**
Lenguaje: Python
Librerías: Pandas, NumPy, Matplotlib, Seaborn
Entorno: Jupyter Notebook / Kaggle Notebooks
