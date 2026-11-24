AI Challenge: K-Means y KNN

Este proyecto implementa un flujo completo de análisis de datos y aprendizaje automático en Python. Su objetivo principal es simular el rendimiento académico de 500 estudiantes y aplicar dos enfoques fundamentales de inteligencia artificial: el agrupamiento no supervisado (K-Means) para descubrir perfiles estudiantiles y la clasificación supervisada (KNN) para predecir si un alumno aprobará o reprobará la materia.

¿Qué hace exactamente el programa?

El código se ejecuta de manera secuencial en cinco etapas bien definidas:

Generación y Preparación de Datos Sintéticos
El sistema inventa un conjunto de datos realista para 500 estudiantes utilizando generación de números aleatorios controlada. Para cada estudiante crea tres variables: horas de estudio semanales, porcentaje de asistencia y porcentaje de tareas entregadas. A partir de estos datos, calcula una calificación final (de 0 a 100) aplicando una fórmula ponderada más una pequeña variación aleatoria para simular casos reales. Finalmente, clasifica a cada estudiante como Aprobado (1) si su nota es mayor o igual a 60, o Reprobado (0) en caso contrario, y estandariza los datos para que todas las variables tengan el mismo peso matemático.

Segmentación de Perfiles con K-Means (Aprendizaje No Supervisado)
El programa analiza los datos sin mirar las calificaciones finales para descubrir patrones ocultos. Agrupa a los estudiantes por similitud en 3 grupos diferentes y luego repite el experimento dividiéndolos en 4 grupos. Para cada escenario, imprime en consola el promedio de horas, asistencia, tareas y nota de cada grupo, y genera gráficos de dispersión visuales para observar cómo se distribuyen los perfiles (por ejemplo: estudiantes de alto rendimiento, rendimiento medio y bajo rendimiento).

Entrenamiento y Experimentación con KNN (Aprendizaje Supervisado)
El sistema divide los datos en dos partes: 75 por ciento para entrenar al modelo y 25 por ciento para ponerlo a prueba. Luego entrena múltiples clasificadores K-Nearest Neighbors (Vecinos Más Cercanos) probando distintos valores de vecinos (k = 1, 3, 5, 7, 11, 15 y 21). El propósito de este experimento es demostrar la importancia del preprocesamiento de datos: evalúa qué tan preciso es el algoritmo cuando los datos están normalizados frente a cuando se usan en su escala original sin normalizar.

Comparación Visual de Resultados
El programa construye e imprime en pantalla una tabla comparativa con los porcentajes de exactitud obtenidos en cada prueba y dibuja una gráfica de líneas. Esto permite visualizar de forma inmediata cómo afecta la normalización al rendimiento del modelo y cuál cantidad de vecinos ofrece las mejores predicciones.

Predicción de un Caso Nuevo (Desafío Final)
De forma automática, el script selecciona la configuración de vecinos (k) que obtuvo la mayor exactitud durante las pruebas. Con este modelo óptimo ya entrenado, evalúa el caso de un estudiante hipotético nuevo (4 horas de estudio, 55 por ciento de asistencia y 50 por ciento de tareas), predice si aprobará o reprobará el curso y muestra en consola el porcentaje exacto de probabilidad calculado para cada resultado.

Requisitos Previos

Para ejecutar este software se requiere tener instalado:

Python 3.8 o superior.

Bibliotecas externas: numpy, pandas, matplotlib y scikit-learn.

Instalación de Dependencias

Paso 1: Creación y activación del entorno virtual (Opcional, recomendado)

En sistemas Windows:
python -m venv .venv
..venv\Scripts\activate

En sistemas Linux o macOS:
python3 -m venv .venv
source .venv/bin/activate

Paso 2: Instalación de bibliotecas requeridas

Ejecute el siguiente mandato en su consola:
pip install numpy pandas matplotlib scikit-learn

Si utiliza el gestor de paquetes uv:
uv pip install numpy pandas matplotlib scikit-learn

Ejecución del Programa

Guarde el código en un fichero (ejemplo: ai_challenge.py) y ejecútelo desde su terminal mediante:

python ai_challenge.py

Nota operativa: Durante la ejecución se abrirán tres ventanas emergentes con gráficos estadísticos. Es necesario cerrar manualmente cada ventana gráfica para que el programa avance hacia la siguiente etapa y muestre los resultados finales en la consola.