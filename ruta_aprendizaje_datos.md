# Ruta de Aprendizaje: De Ingeniero de Soporte a Analista de Datos Profesional

**Perfil de partida:** Ingeniero de Soporte con experiencia en hardware, software, despliegue de sistemas y automatización. Ya usas Python, Jupyter Notebook, VS Code, Excel, SQL y GitHub a nivel inicial.

**Ventaja clave que tienes y que la mayoría de estudiantes no tiene:** trabajas a diario con datos reales de auditorías de equipos, facturación de clientes, disputas con financieras y cumplimiento de hardware. **Ese es tu mejor dataset de portafolio.** A lo largo de esta ruta vas a usar tu propio contexto laboral (renta de equipos IT, Poly, Dell, Intel NUCs, auditorías, disputas de facturación) como fuente de proyectos reales — eso es lo que te va a diferenciar de alguien que solo hizo el dataset de Titanic.

---

## Cómo está organizada esta ruta

- **4 fases**, de principiante a profesional.
- **17 módulos** distribuidos en las fases según dependencias lógicas (no puedes hacer EDA sin saber Pandas, no puedes hacer dashboards ejecutivos sin saber storytelling).
- Cada módulo tiene: objetivos, conceptos clave, herramientas, ejercicios, mini proyecto, recursos y tiempo estimado.
- Al final de cada fase hay un **proyecto integrador** que junta todo lo aprendido.
- Al final de la ruta: sección completa de **documentación profesional y portafolio en GitHub**.

**Tiempo total estimado:** 8-11 meses, dedicando 8-10 horas/semana (ritmo realista compaginando con tu trabajo y la universidad). Puedes comprimirlo si dedicas más horas, o irá más lento en semanas de parciales — está pensado para que ajustes el ritmo, no el orden.

---

# FASE 1 — Fundamentos (Meses 1-2)

## Módulo 1: Fundamentos de Análisis de Datos

**Objetivos de aprendizaje**
- Entender qué hace un analista de datos día a día y en qué se diferencia de un data scientist o un BI analyst.
- Comprender el ciclo de vida de un proyecto de datos: pregunta de negocio → recolección → limpieza → análisis → comunicación → decisión.
- Aprender a traducir una pregunta de negocio ambigua en una pregunta analítica concreta.

**Conceptos clave**
- Tipos de datos: estructurados, no estructurados, semiestructurados.
- Niveles de medición: nominal, ordinal, intervalo, razón.
- KPIs y métricas de negocio.
- Diferencia entre datos, información e insight.
- Sesgos comunes en la interpretación de datos.

**Herramientas**
- Excel/Google Sheets (para pensar sin fricción técnica todavía).
- Papel y lápiz para mapas de proceso.

**Ejercicios prácticos**
1. Toma 3 preguntas vagas de "negocio" (ej. "¿por qué bajaron las ventas?") y conviértelas en preguntas analíticas específicas y medibles.
2. Clasifica 20 variables de un dataset público según su nivel de medición.

**Mini proyecto**
Documenta en un README el ciclo de vida completo de un análisis hipotético sobre **por qué ciertos clientes de tu empresa generan más disputas de facturación con las financieras** — sin tocar datos reales todavía, solo el planteamiento del problema, hipótesis y qué datos necesitarías.

**Recursos recomendados**
- Curso "Foundations of Data Science" (Coursera, Google Data Analytics Certificate — módulo 1).
- Libro: *Storytelling with Data* (Cole Nussbaumer Knaflic) — cap. 1-2, para entender el "para qué" antes del "cómo".

**Tiempo estimado:** 1 semana

---

## Módulo 2: Estadística Aplicada

**Objetivos de aprendizaje**
- Manejar estadística descriptiva e inferencial lo suficiente para interpretar datos y validar hipótesis sin caer en errores comunes.
- Entender cuándo un resultado es "significativo" y cuándo es ruido.

**Conceptos clave**
- Medidas de tendencia central y dispersión (media, mediana, moda, desviación estándar, varianza, percentiles).
- Distribuciones: normal, binomial, uniforme.
- Correlación vs. causalidad.
- Probabilidad básica.
- Pruebas de hipótesis: p-valor, intervalos de confianza, error tipo I/II.
- Tamaño de muestra y sesgo de selección.

**Herramientas**
- Excel (funciones estadísticas).
- Python con `scipy.stats` (introducción ligera, se profundiza en el módulo 5-6).

**Ejercicios prácticos**
1. Calcula media, mediana, desviación estándar y percentiles de una columna numérica (ej. `balance` o `duration` de tu dataset bancario) manualmente y con fórmulas de Excel.
2. Identifica outliers usando el método IQR (rango intercuartílico) en 3 columnas distintas.
3. Diseña una prueba de hipótesis simple: "¿el balance promedio de clientes con `housing=yes` es distinto al de `housing=no`?"

**Mini proyecto**
Análisis estadístico descriptivo completo de tu `dataset_banco_limpio.csv`: medidas de tendencia central, dispersión, distribución de variables clave, y una prueba de hipótesis documentada con conclusión escrita en lenguaje de negocio (no solo el número del p-valor).

**Recursos recomendados**
- Curso: "Statistics with Python" (Coursera, Universidad de Michigan).
- Libro: *Naked Statistics* (Charles Wheelan) — muy accesible, sin jerga innecesaria.
- Khan Academy — Estadística y Probabilidad (para repasar lo básico si hace falta).

**Tiempo estimado:** 2-3 semanas

---

## Módulo 3: Excel Avanzado para Análisis

**Objetivos de aprendizaje**
- Usar Excel como herramienta profesional de análisis, no solo de captura de datos.
- Construir modelos y reportes dinámicos sin depender de fórmulas frágiles.

**Conceptos clave**
- Tablas dinámicas y gráficos dinámicos.
- Funciones avanzadas: `BUSCARX`/`XLOOKUP`, `INDICE+COINCIDIR`, `SUMAR.SI.CONJUNTO`, `CONTAR.SI.CONJUNTO`, funciones de fecha.
- Power Query (ETL dentro de Excel).
- Validación de datos y formato condicional para control de calidad.
- Tablas estructuradas (Excel Tables) vs. rangos sueltos.

**Herramientas**
- Excel (idealmente Microsoft 365 para Power Query moderno).

**Ejercicios prácticos**
1. Construye una tabla dinámica que resuma tu dataset bancario por `job` y `education`, mostrando tasa de conversión (`y=yes`).
2. Usa Power Query para importar y limpiar un CSV desordenado (fechas en texto, espacios extra) sin tocar el archivo original.
3. Reemplaza 5 fórmulas `BUSCARV` clásicas de un archivo de ejemplo por `XLOOKUP`, explicando por qué es más robusto.

**Mini proyecto**
Dashboard en Excel (con tablas dinámicas + segmentadores) sobre tu dataset bancario limpio: tasa de conversión por segmento demográfico, mes de campaña, y tipo de contacto.

**Recursos recomendados**
- Curso: "Excel Skills for Business" (Coursera, Macquarie University).
- ExcelJet.net como referencia rápida de fórmulas.
- Canal de YouTube: Leila Gharani (Power Query y Excel avanzado).

**Tiempo estimado:** 2 semanas

---

## Proyecto integrador Fase 1

**"Diagnóstico inicial de campaña bancaria"** — Usando tu `dataset_banco_limpio.csv`:
1. Documenta la pregunta de negocio (Módulo 1).
2. Análisis estadístico descriptivo completo (Módulo 2).
3. Dashboard en Excel con hallazgos clave (Módulo 3).
4. Un documento de una página con 3 hallazgos y 1 recomendación de negocio, escrito para un gerente no técnico.

---

# FASE 2 — Herramientas técnicas (Meses 3-5)

## Módulo 4: SQL desde Básico hasta Avanzado

**Objetivos de aprendizaje**
- Consultar, filtrar, agregar y combinar datos de múltiples tablas con confianza.
- Escribir SQL que un equipo de datos real consideraría limpio y eficiente.

**Conceptos clave**
- Básico: `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`, `HAVING`, alias.
- Intermedio: `JOIN` (INNER, LEFT, RIGHT, FULL), subconsultas, `UNION`.
- Avanzado: CTEs (`WITH`), funciones de ventana (`ROW_NUMBER`, `RANK`, `LAG`/`LEAD`), funciones de fecha, optimización básica de consultas, vistas.
- Modelado relacional básico: llaves primarias/foráneas, normalización (idea general, no a fondo).

**Herramientas**
- PostgreSQL o MySQL (gratis, ampliamente usados en la industria).
- DBeaver o pgAdmin como cliente.
- SQLite para practicar sin instalar servidor.

**Ejercicios prácticos**
1. 20 ejercicios progresivos en SQLBolt o Mode Analytics SQL Tutorial (básico → JOIN → subconsultas).
2. Recrea en SQL 5 de los análisis que ya hiciste en Excel con tu dataset bancario (cárgalo a una tabla PostgreSQL primero).
3. Escribe una consulta con función de ventana que calcule el ranking de clientes por `balance` dentro de cada `job`.

**Mini proyecto**
Modela una base de datos simplificada de **auditoría de equipos** (inspirada en tu trabajo): tablas de `equipos`, `clientes`, `auditorías`, `disputas`. Escribe consultas que respondan preguntas reales de tu contexto: "¿qué clientes tienen más disputas de hardware en los últimos 6 meses?", "¿qué modelos de equipo tienen mayor tasa de incumplimiento en auditoría?".

**Recursos recomendados**
- SQLBolt (interactivo, gratis).
- Mode Analytics SQL Tutorial.
- Curso: "SQL for Data Science" (Coursera, UC Davis).
- Libro de referencia: *SQL Practice Problems* (Sylvia Moestl Vasilik).

**Tiempo estimado:** 4 semanas

---

## Módulo 5: Python para Análisis de Datos

**Objetivos de aprendizaje**
- Dominar Python como lenguaje de propósito general aplicado a análisis: sintaxis, estructuras de control, funciones, manejo de errores.
- Escribir código legible y reutilizable, no solo scripts de una sola vez.

**Conceptos clave**
- Tipos de datos, estructuras (listas, tuplas, diccionarios, sets).
- Control de flujo, funciones, comprensión de listas.
- Manejo de excepciones (`try/except`).
- Módulos y entornos virtuales (`venv`).
- Buenas prácticas: PEP8, nombres descriptivos, funciones pequeñas.

**Herramientas**
- VS Code (ya lo usas) + extensión de Python + linter (`pylint` o `ruff`).
- Jupyter Notebook (para exploración) y scripts `.py` (para código reutilizable).

**Ejercicios prácticos**
1. 15 ejercicios de lógica en Python puro (sin librerías) usando estructuras de datos.
2. Escribe una función que valide y limpie una lista de strings con formatos inconsistentes (mayúsculas, espacios) — igual al problema que resolviste manualmente en tu notebook de limpieza.
3. Convierte 3 celdas sueltas de tu notebook actual en funciones reutilizables con docstrings.

**Mini proyecto**
Script en Python (`.py`, no notebook) que automatice un chequeo de calidad de datos: recibe un CSV, reporta nulos, duplicados y tipos de dato inconsistentes, y genera un log de texto con el resultado. (Esto conecta directo con tu experiencia en automatización de sistemas.)

**Recursos recomendados**
- Curso: "Python for Everybody" (Coursera, Dr. Chuck).
- Libro: *Automate the Boring Stuff with Python* (Al Sweigart) — gratis online, muy alineado a tu perfil de soporte/automatización.
- Real Python (artículos de referencia).

**Tiempo estimado:** 3 semanas

---

## Módulo 6: Manipulación de Datos con Pandas y NumPy

**Objetivos de aprendizaje**
- Limpiar, transformar y combinar datasets de forma eficiente y vectorizada (sin loops innecesarios).
- Ya tienes una base práctica de esto por tu notebook de limpieza — este módulo la formaliza y la lleva a nivel profesional.

**Conceptos clave**
- Series y DataFrames, indexación (`.loc`, `.iloc`).
- Filtrado, agrupación (`groupby`), pivoteo (`pivot_table`), fusión (`merge`, `concat`, `join`).
- Manejo de valores nulos y duplicados a fondo (ya lo practicaste; aquí se profundiza con estrategias de imputación).
- NumPy: arrays, operaciones vectorizadas, broadcasting.
- Funciones `apply`, `map`, `applymap` y cuándo evitarlas por rendimiento.

**Herramientas**
- Pandas, NumPy en Jupyter Notebook / VS Code.

**Ejercicios prácticos**
1. Retoma tu notebook `analisis_py.ipynb` y refactoriza el pipeline de limpieza en funciones reutilizables (ej. `unificar_categorias(df, mapeo)`).
2. Combina tu dataset bancario con una tabla auxiliar simulada (ej. tasas de interés por mes) usando `merge`.
3. Construye 3 `pivot_table` distintas para responder preguntas de negocio del dataset bancario.

**Mini proyecto**
Reescribe completamente tu proceso de limpieza de datos como un **pipeline documentado y parametrizable** (funciones + un notebook que solo las orquesta), aplicable no solo a tu dataset actual sino a cualquier CSV con estructura similar.

**Recursos recomendados**
- Curso: "Data Analysis with Python" (freeCodeCamp) o "Pandas" de Kevin Markham (YouTube, "Data School").
- Documentación oficial de Pandas (10 Minutes to Pandas + User Guide).
- Libro: *Python for Data Analysis* (Wes McKinney, creador de Pandas).

**Tiempo estimado:** 4 semanas

---

## Proyecto integrador Fase 2

**"Sistema de auditoría de equipos IT simulado"** — Diseña una base de datos SQL con datos simulados (o anonimizados) inspirados en tu trabajo real de auditorías y disputas de hardware. Extrae los datos a Python con Pandas, limpia y transforma, y responde con SQL + Pandas 5 preguntas de negocio reales de tu día a día laboral.

---

# FASE 3 — Análisis, visualización y comunicación (Meses 6-8)

## Módulo 7: Visualización de Datos (Matplotlib, Seaborn, Power BI)

**Objetivos de aprendizaje**
- Elegir el tipo de gráfico correcto según la pregunta y la audiencia.
- Pasar de gráficos exploratorios (Python) a dashboards interactivos de negocio (Power BI).

**Conceptos clave**
- Gramática de gráficos: qué comunica cada tipo (barras, líneas, dispersión, boxplot, heatmap).
- Principios de diseño: ruido vs. señal, uso de color, evitar gráficos engañosos.
- Matplotlib como base de bajo nivel; Seaborn para estadística visual rápida.
- Power BI: modelo de datos, relaciones, DAX básico, segmentadores, publicación.

**Herramientas**
- Matplotlib, Seaborn (Python).
- Power BI Desktop (gratis).

**Ejercicios prácticos**
1. Recrea en Matplotlib/Seaborn los boxplots que ya usaste para detectar outliers en tu limpieza, pero ahora con anotaciones y formato profesional.
2. Construye 5 visualizaciones distintas del dataset bancario (barras, heatmap de correlación, distribución) explicando en un comentario qué pregunta responde cada una.
3. Importa tu `dataset_banco_limpio.csv` a Power BI y construye un modelo simple con al menos 2 medidas DAX (ej. tasa de conversión).

**Mini proyecto**
Dashboard interactivo en Power BI del dataset bancario: filtros por mes/job/education, KPIs de tasa de conversión, y al menos una visual de tendencia temporal.

**Recursos recomendados**
- Curso: "Data Visualization with Python" (Coursera, IBM).
- Curso: "Microsoft Power BI Desktop for Business Intelligence" (Udemy, Maven Analytics).
- Libro: *Storytelling with Data* (ya mencionado, capítulos 3-6 aplican directo aquí).

**Tiempo estimado:** 4 semanas

---

## Módulo 8: Documentación de Proyectos y Buenas Prácticas

**Objetivos de aprendizaje**
- Documentar como lo haría un analista senior: cualquier persona debe poder entender tu proyecto sin hablar contigo.

*(Ver la sección dedicada "Documentación Profesional" al final de este documento — ahí está el detalle completo de estructura de carpetas, README, convenciones de nombres, etc.)*

**Conceptos clave**
- Documentación como parte del entregable, no como paso final opcional.
- Diferencia entre documentar para ti mismo (reproducibilidad) y documentar para otros (comunicación).

**Herramientas**
- Markdown, README.md, Jupyter Notebook con celdas de markdown estructuradas.

**Ejercicios prácticos**
1. Toma tu notebook de limpieza actual y agrégale una celda de markdown al inicio de cada sección explicando el "por qué", no solo el "qué".
2. Escribe un README.md para tu proyecto de limpieza bancaria siguiendo la plantilla de la sección final de este documento.

**Mini proyecto**
Documenta retroactivamente el proyecto de limpieza del dataset bancario (el que ya hicimos juntos) con README completo, estructura de carpetas y notebook comentado profesionalmente.

**Recursos recomendados**
- Guía de estilo: "Google Developer Documentation Style Guide".
- Make a README (makeareadme.com).

**Tiempo estimado:** 1 semana

---

## Módulo 9: Análisis Exploratorio de Datos (EDA)

**Objetivos de aprendizaje**
- Ejecutar un EDA sistemático y repetible, no una exploración desordenada.

**Conceptos clave**
- Estructura estándar de un EDA: forma del dataset, tipos, nulos, duplicados, distribución univariada, relaciones bivariadas/multivariadas, hipótesis iniciales.
- Detección de patrones y anomalías.
- Cuándo un EDA está "completo" (criterio de cierre, no exploración infinita).

**Herramientas**
- Pandas, Seaborn, `pandas-profiling`/`ydata-profiling` como acelerador (no reemplazo del criterio propio).

**Ejercicios prácticos**
1. Ejecuta un EDA completo y estructurado sobre tu `dataset_banco_limpio.csv` siguiendo la secuencia estándar.
2. Genera un reporte automático con `ydata-profiling` y compáralo contra tu EDA manual: ¿qué encontró la herramienta que tú no viste, y viceversa?

**Mini proyecto**
Notebook de EDA completo y documentado sobre el dataset bancario, cerrando con una sección de "hallazgos e hipótesis para la fase de modelado".

**Recursos recomendados**
- Curso: "Exploratory Data Analysis" (Coursera, IBM Data Analyst Path).
- Kaggle Learn: "Data Cleaning" y "Data Visualization" (gratis, cortos).

**Tiempo estimado:** 2 semanas

---

## Módulo 10: Limpieza y Transformación de Datos (nivel avanzado)

**Objetivos de aprendizaje**
- Ya tienes la base práctica; este módulo la lleva a escenarios más complejos: texto libre, fechas irregulares, datos de múltiples fuentes.

**Conceptos clave**
- Feature engineering básico (crear variables nuevas a partir de existentes).
- Encoding de categóricas (one-hot, ordinal) como preparación para ML.
- Escalado/normalización de variables numéricas.
- Manejo de series de tiempo irregulares.

**Herramientas**
- Pandas, `scikit-learn` (`preprocessing`).

**Ejercicios prácticos**
1. Crea 3 variables nuevas en el dataset bancario (ej. rango etario, si tuvo contacto previo exitoso).
2. Aplica one-hot encoding a las categóricas del dataset bancario y compáralo contra ordinal encoding, explicando cuándo usarías cada uno.

**Mini proyecto**
Extiende el pipeline de limpieza del dataset bancario con feature engineering, dejándolo listo para un modelo de Machine Learning (Fase 4).

**Recursos recomendados**
- Documentación de `scikit-learn` — módulo `preprocessing`.
- Kaggle Learn: "Feature Engineering".

**Tiempo estimado:** 2 semanas

---

## Módulo 11: Creación de Dashboards e Informes Ejecutivos

**Objetivos de aprendizaje**
- Pasar de "mostrar datos" a "contar una historia que lleva a una decisión".

**Conceptos clave**
- Estructura de un informe ejecutivo: contexto, hallazgo, implicación, recomendación (no solo gráficos sueltos).
- Diseño de dashboards: jerarquía visual, máximo de KPIs por vista, evitar sobrecarga.
- Diferencia entre dashboard operativo (actualización frecuente, detalle) y dashboard ejecutivo (resumen, tendencia, decisión).

**Herramientas**
- Power BI (dashboard interactivo).
- PowerPoint o Word (informe ejecutivo estático) — o notebook exportado a PDF/HTML.

**Ejercicios prácticos**
1. Rediseña el dashboard de Power BI del Módulo 7 aplicando jerarquía visual (KPIs arriba, detalle abajo, máximo 6-8 visuales).
2. Escribe un informe ejecutivo de 1 página sobre los hallazgos del dataset bancario, dirigido a alguien que nunca vería el dashboard.

**Mini proyecto**
Dashboard ejecutivo final del dataset bancario + informe de una página, ambos consistentes entre sí (mismos números, misma narrativa).

**Recursos recomendados**
- Libro: *Storytelling with Data* (capítulos finales, sobre dashboards).
- SQLBI.com (para profundizar en Power BI/DAX cuando lo necesites).

**Tiempo estimado:** 2 semanas

---

## Proyecto integrador Fase 3

**"Informe ejecutivo de campaña bancaria"** — Proyecto de punta a punta: EDA completo → limpieza avanzada con feature engineering → dashboard en Power BI → informe ejecutivo de una página. Este proyecto va directo a tu portafolio de GitHub.

---

# FASE 4 — Ciencia de Datos y profesionalización (Meses 9-11)

## Módulo 12: Introducción a Machine Learning

**Objetivos de aprendizaje**
- Entender qué es un modelo de ML, cuándo tiene sentido usarlo y cómo evaluarlo — sin pretender ser un ML engineer todavía.

**Conceptos clave**
- Aprendizaje supervisado vs. no supervisado.
- Regresión vs. clasificación.
- Train/test split, overfitting/underfitting, validación cruzada.
- Métricas de evaluación: accuracy, precision, recall, F1, RMSE (según el caso).
- Modelos base: regresión lineal/logística, árboles de decisión, random forest (a nivel de uso, no de matemática profunda).

**Herramientas**
- `scikit-learn`.

**Ejercicios prácticos**
1. Entrena un modelo de regresión logística sobre el dataset bancario para predecir `y` (si el cliente se suscribió), usando las variables ya limpiadas.
2. Evalúa el modelo con matriz de confusión, precision, recall y F1 — e interpreta qué significa cada métrica en términos de negocio (¿qué es peor: un falso positivo o un falso negativo, para una campaña bancaria?).

**Mini proyecto**
Modelo de clasificación completo (baseline + un modelo más complejo tipo random forest) sobre el dataset bancario, con comparación de métricas y una conclusión de negocio: "¿qué variables predicen mejor la conversión, y qué debería hacer el banco con eso?"

**Recursos recomendados**
- Curso: "Machine Learning" (Andrew Ng, Coursera/DeepLearning.AI) — la introducción clásica.
- Curso: "Introduction to Machine Learning" (Kaggle Learn, corto y práctico).
- Documentación de `scikit-learn`.

**Tiempo estimado:** 4 semanas

---

## Módulo 13: Fundamentos de Ciencia de Datos

**Objetivos de aprendizaje**
- Entender el rol del data scientist frente al analista/BI, y cómo se integran en un equipo de datos real.

**Conceptos clave**
- Ciclo de vida de un proyecto de ciencia de datos (CRISP-DM u OSEMN).
- Diferencia entre pregunta de analista ("¿qué pasó?") y de científico de datos ("¿qué va a pasar / qué deberíamos hacer?").
- Ética de datos: privacidad, sesgo algorítmico, uso responsable de modelos predictivos.
- Introducción a A/B testing como puente entre estadística y decisiones de producto/negocio.

**Herramientas**
- No requiere herramienta nueva — es conceptual, aplicado sobre lo ya construido.

**Ejercicios prácticos**
1. Diseña (en papel/documento) un experimento A/B hipotético para probar si un nuevo guion de llamada mejora la tasa de conversión del banco.
2. Identifica posibles sesgos en el dataset bancario (¿está sub-representado algún grupo? ¿el modelo del Módulo 12 podría discriminar por edad o educación de forma injusta?).

**Mini proyecto**
Documento de "consideraciones éticas y de negocio" sobre el modelo predictivo del Módulo 12: limitaciones, riesgos de sesgo, y recomendaciones de uso responsable.

**Recursos recomendados**
- Curso: "What is Data Science?" (Coursera, IBM).
- Artículo: "The CRISP-DM Model" (referencia estándar de la industria).

**Tiempo estimado:** 1-2 semanas

---

## Módulo 14: Uso de Jupyter Notebook y Documentación Técnica

**Objetivos de aprendizaje**
- Ya usas Jupyter; este módulo lo lleva a nivel profesional: notebooks que se pueden compartir, revisar y reproducir.

**Conceptos clave**
- Estructura estándar de un notebook profesional (contexto → carga → limpieza → EDA → análisis/modelo → conclusiones).
- Markdown efectivo dentro de notebooks (títulos, explicaciones, no solo código).
- Exportar notebooks a HTML/PDF para compartir con no técnicos.
- Reproducibilidad: fijar semillas aleatorias, declarar versiones de librerías (`requirements.txt`).

**Herramientas**
- Jupyter Notebook/Lab, `nbconvert`, extensión Jupyter de VS Code.

**Ejercicios prácticos**
1. Audita tu notebook `analisis_py.ipynb` original contra la estructura estándar y reorganízalo.
2. Exporta un notebook a HTML y verifica que se vea bien sin ejecutar código (para alguien no técnico).

**Mini proyecto**
Versión final, pulida y reproducible del notebook de limpieza del dataset bancario, con `requirements.txt` generado.

**Recursos recomendados**
- Documentación oficial de Jupyter.
- Guía: "Ten Simple Rules for Reproducible Computational Research" (aplica directo a notebooks).

**Tiempo estimado:** 1 semana

---

## Módulo 15: Control de Versiones con Git y GitHub

**Objetivos de aprendizaje**
- Usar Git como lo usaría un equipo de datos real: commits significativos, ramas, historial limpio.

**Conceptos clave**
- `git init`, `add`, `commit`, `push`, `pull`, `clone`.
- Ramas (`branch`), fusión (`merge`), resolución de conflictos básicos.
- `.gitignore` (crítico para no subir datasets pesados o credenciales).
- Mensajes de commit descriptivos (convención tipo "feat:", "fix:", "docs:").
- GitHub: repositorios, Issues, README como landing page del proyecto.

**Herramientas**
- Git, GitHub, GitHub Desktop o terminal (dado tu perfil técnico, te recomiendo terminal directo).

**Ejercicios prácticos**
1. Sube el proyecto de limpieza del dataset bancario a un repositorio nuevo, con `.gitignore` correcto y al menos 5 commits con mensajes descriptivos (no "cambios varios").
2. Practica un flujo de rama: crea una rama `feature/eda`, trabaja ahí, y haz merge a `main`.

**Mini proyecto**
Repositorio completo en GitHub del proyecto de campaña bancaria (Fase 3), con historial de commits limpio y README profesional.

**Recursos recomendados**
- "Git and GitHub for Beginners" (freeCodeCamp, YouTube).
- Pro Git Book (gratis, progit.org) — capítulos 1-3 son suficientes para este nivel.

**Tiempo estimado:** 1-2 semanas

---

## Módulo 16: Creación de Portafolio Profesional en GitHub

**Objetivos de aprendizaje**
- Convertir tus proyectos dispersos en un portafolio coherente que un reclutador o cliente pueda evaluar en minutos.

**Conceptos clave**
- Qué proyectos incluir (calidad sobre cantidad: 3-5 proyectos sólidos ganan a 15 mediocres).
- README de perfil de GitHub (el que aparece en tu página de usuario).
- Consistencia visual y de nomenclatura entre repositorios.
- Cómo destacar el "storytelling" de negocio, no solo el código.

**Herramientas**
- GitHub (repos + README de perfil).
- Opcional: GitHub Pages para un portafolio web simple.

**Ejercicios prácticos**
1. Audita tus repositorios actuales contra la checklist de la sección de documentación (al final de este documento).
2. Escribe tu README de perfil de GitHub, conectando tu experiencia en soporte/hardware con tu nueva dirección en datos (esa combinación es tu diferencial).

**Mini proyecto**
Portafolio de GitHub organizado con al menos 3 proyectos de esta ruta (limpieza bancaria, sistema de auditoría IT simulado, modelo predictivo), cada uno con README completo.

**Recursos recomendados**
- Ejemplos de portafolios de analistas en GitHub (busca "data analyst portfolio github" para inspiración de estructura, no para copiar contenido).
- GitHub Docs: "About READMEs".

**Tiempo estimado:** 1-2 semanas

---

## Módulo 17: Metodologías y Flujo de Trabajo de un Proyecto Real de Datos

**Objetivos de aprendizaje**
- Entender cómo se organiza el trabajo de datos en un equipo real, más allá de tu proyecto individual.

**Conceptos clave**
- Metodologías ágiles aplicadas a datos (Scrum/Kanban ligero).
- Roles típicos en un equipo de datos (analista, ingeniero de datos, científico de datos, BI) y cómo interactúan.
- Gestión de requerimientos: cómo levantar una necesidad de un stakeholder no técnico.
- Control de calidad de datos como proceso continuo, no un paso único.

**Herramientas**
- Trello/Notion/GitHub Projects (para simular gestión de un proyecto).

**Ejercicios prácticos**
1. Simula un tablero Kanban para el proyecto final (Fase 4) con columnas Backlog/En progreso/Revisión/Hecho.
2. Escribe una "historia de usuario" desde la perspectiva de un gerente que pide el análisis de campaña bancaria.

**Mini proyecto**
Documento de "flujo de trabajo" para tu proyecto final, incluyendo cronograma, roles simulados y checkpoints de calidad.

**Recursos recomendados**
- "Agile Data Science" (concepto general, no necesitas el libro completo).
- Notion/Trello — plantillas gratuitas de gestión de proyectos de datos.

**Tiempo estimado:** 1 semana

---

## PROYECTO FINAL DE LA RUTA

**"Sistema de análisis predictivo de conversión bancaria — de punta a punta"**

Integra todo lo aprendido en un solo proyecto profesional, publicado en GitHub:

1. **Planteamiento del problema** (Módulo 1) y flujo de trabajo documentado (Módulo 17).
2. **Modelo de datos en SQL** con al menos 2 tablas relacionadas (Módulo 4).
3. **Pipeline de limpieza y transformación** en Python/Pandas, con funciones reutilizables (Módulos 5, 6, 10).
4. **EDA completo y documentado** (Módulo 9).
5. **Análisis estadístico** con al menos una prueba de hipótesis (Módulo 2).
6. **Modelo de Machine Learning** de clasificación, con evaluación e interpretación de negocio (Módulo 12).
7. **Dashboard en Power BI** + **informe ejecutivo de una página** (Módulos 7, 11).
8. **Repositorio de GitHub completo**: README, estructura de carpetas, notebooks documentados, `requirements.txt` (Módulos 14, 15, 16).
9. Reflexión ética sobre el uso del modelo (Módulo 13).

Este proyecto es el que muestras en entrevistas. Debe poder explicarse en 5 minutos a un no técnico y sostenerse en detalle técnico ante un analista senior.

---

# Documentación Profesional de Proyectos de Datos

## Estructura de carpetas recomendada

```
nombre-proyecto/
│
├── README.md                  # Landing page del proyecto
├── requirements.txt           # Librerías y versiones usadas
├── .gitignore                 # Excluir datos pesados, credenciales, __pycache__
│
├── data/
│   ├── raw/                   # Datos originales, NUNCA se modifican
│   └── processed/             # Datos limpios, resultado del pipeline
│
├── notebooks/
│   ├── 01_exploracion.ipynb
│   ├── 02_limpieza.ipynb
│   ├── 03_eda.ipynb
│   └── 04_modelo.ipynb
│
├── src/                        # Código reutilizable (funciones, no exploración)
│   ├── limpieza.py
│   └── utils.py
│
├── reports/
│   ├── figures/                # Gráficos exportados
│   └── informe_ejecutivo.pdf
│
└── dashboard/                  # Archivo .pbix o export de Power BI
```

**Regla de oro:** `data/raw/` es de solo lectura conceptual — nunca sobrescribes el archivo original, tal como ya practicaste al guardar `dataset_banco_limpio.csv` como un archivo nuevo.

## Convenciones de nombres

- Carpetas y archivos en minúsculas, con guiones bajos (`snake_case`): `dataset_banco_limpio.csv`, no `Dataset Banco Limpio.csv`.
- Notebooks numerados por orden de ejecución: `01_exploracion.ipynb`, `02_limpieza.ipynb` — así cualquiera sabe el flujo sin preguntarte.
- Nombres descriptivos, no genéricos: `limpieza_dataset_banco.py`, no `script1.py` o `final_v2_definitivo.py`.
- Commits de Git con prefijo semántico: `feat:` (nueva funcionalidad), `fix:` (corrección), `docs:` (documentación), `refactor:` (reorganización sin cambiar comportamiento). Ejemplo: `fix: unificar sinonimos en columnas categoricas`.

## Cómo crear un README efectivo

Estructura mínima que debe tener todo README de proyecto:

```markdown
# Nombre del Proyecto

## Descripción
1-2 párrafos: qué problema resuelve, por qué importa.

## Pregunta de negocio
La pregunta específica que el análisis responde.

## Datos
Fuente, tamaño, período que cubren, diccionario de variables si es necesario.

## Metodología
Pasos generales: limpieza → EDA → análisis/modelo. No el detalle técnico completo, eso vive en los notebooks.

## Hallazgos clave
3-5 bullets con los insights más importantes, en lenguaje de negocio.

## Cómo reproducir este proyecto
Instrucciones paso a paso: instalar requirements, orden de notebooks a ejecutar.

## Estructura del repositorio
Árbol de carpetas breve.

## Herramientas utilizadas
Python, Pandas, SQL, Power BI, etc.

## Autor
Tu nombre y forma de contacto/LinkedIn.
```

## Cómo documentar notebooks

- **Celda de markdown al inicio**: contexto del notebook (qué hace, qué recibe, qué produce).
- **Una celda de markdown antes de cada sección de código**, explicando el "por qué" de esa transformación — no solo repetir en palabras lo que el código ya dice.
- **Comentarios en código solo donde la lógica no es obvia** (evita comentar `# sumar 1 a x` sobre `x += 1`).
- **Celda final de conclusiones**: qué se encontró, qué queda pendiente, próximos pasos.
- Antes de subir a GitHub: **"Restart & Run All"** para verificar que el notebook corre de principio a fin sin errores ni celdas fuera de orden — esto es lo primero que revisa cualquier revisor técnico.

## Cómo registrar hallazgos y conclusiones

- Sepára siempre **hallazgo** (lo que los datos muestran) de **interpretación** (lo que tú crees que significa) y de **recomendación** (qué deberían hacer con eso). Mezclar los tres sin distinguirlos es el error más común de analistas junior.
- Ejemplo de buen registro:
  > **Hallazgo:** la tasa de conversión en llamadas de mayo es 3x menor que en marzo, pese a tener 5x más volumen de contactos.
  > **Interpretación:** posible saturación de la campaña o peor segmentación de contactos en mayo.
  > **Recomendación:** revisar criterios de segmentación de mayo antes de repetir el volumen de contactos.
- Guarda estos registros en un `CHANGELOG.md` o sección de "Hallazgos" del README — no solo en tu cabeza o en un chat.

## Cómo presentar resultados a audiencias técnicas vs. no técnicas

| | Técnica (otro analista/dev) | No técnica (gerente, cliente) |
|---|---|---|
| **Formato** | Notebook completo, repo de GitHub, código visible | Informe de 1 página, dashboard, presentación |
| **Lenguaje** | Términos estadísticos/técnicos está bien | Cero jerga: "tasa de conversión" sí, "p-valor de 0.03" no |
| **Foco** | Metodología, reproducibilidad, decisiones técnicas | Hallazgo, impacto de negocio, recomendación accionable |
| **Nivel de detalle** | Todo el proceso, incluidos intentos fallidos | Solo la conclusión y 1-2 gráficos de apoyo |
| **Estructura** | README + notebooks + código | "¿Qué encontramos? → ¿Qué significa? → ¿Qué hacemos?" |

**Regla práctica:** si tu audiencia no técnica necesita más de 2 minutos para entender el punto principal de un gráfico, el gráfico está mal diseñado para esa audiencia, no falta explicación adicional.

---

## Resumen de tiempos por fase

| Fase | Módulos | Tiempo estimado |
|---|---|---|
| Fase 1 — Fundamentos | 1-3 | 5-6 semanas |
| Fase 2 — Herramientas técnicas | 4-6 | 11 semanas |
| Fase 3 — Análisis y comunicación | 7-11 | 11 semanas |
| Fase 4 — Ciencia de datos y profesionalización | 12-17 | 10-11 semanas |
| **Total** | **17 módulos** | **~8-11 meses** (8-10 h/semana) |

---

## Cómo usar esta ruta a partir de hoy

1. Ya tienes el dataset bancario limpio — úsalo como hilo conductor de casi toda la ruta (Módulos 2, 3, 6, 7, 9, 10, 11, 12) en vez de saltar entre datasets distintos. La repetición sobre el mismo dataset, viéndolo cada vez con una herramienta nueva, es lo que consolida el aprendizaje.
2. El "sistema de auditoría de equipos IT simulado" (Módulo 4 y proyecto integrador Fase 2) es tu proyecto diferenciador — nadie más en un bootcamp va a tener ese caso de uso, porque sale de tu trabajo real.
3. Cuando termines cada módulo, vuelve aquí y dime en qué vas — puedo revisarte código, notebooks, consultas SQL o el dashboard, igual que hicimos con la limpieza de datos.
