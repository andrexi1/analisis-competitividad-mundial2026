# Análisis del Dashboard - Copa Mundial de la FIFA 2026

Este proyecto consiste en un modelo de datos y un tablero de control desarrollado en Power BI para evaluar el panorama competitivo de las 48 selecciones clasificadas al Mundial 2026. A partir de los datos extraídos del informe oficial, el objetivo principal fue analizar cómo impacta la estructura del ranking y el historial de los equipos en la dificultad y el equilibrio de cada grupo.

## 1. Estructura y Limpieza de los Datos

El conjunto de datos procesado abarca un universo de 48 registros correspondientes a las selecciones nacionales clasificadas. Cada una cuenta con variables clave que combinan métricas cualitativas y cuantitativas:
* **Variables de Identificación:** Nombre de la selección, director técnico a cargo y grupo asignado (de la A a la L).
* **Métricas de Rendimiento Actual:** Puntaje y posición en el Ranking FIFA (`fifa_rank`).
* **Variables Históricas y Geográficas:** Confederación de origen y el mejor resultado obtenido históricamente en copas del mundo (`best_wc_result`).

El modelo se diseñó bajo un enfoque relacional plano que permite cruzar el historial deportivo con las posiciones actuales del ranking para filtrar los datos dinámicamente por confederaciones o niveles de fase alcanzados.

---

## 2. Análisis Estadístico de Competitividad por Grupos

Para determinar qué tan complejo es cada grupo, se calculó la media aritmética del Ranking FIFA de sus integrantes. Al ser el ranking una escala inversa (donde un número menor indica una mejor posición global), los promedios más bajos revelan las agrupaciones con mayor nivel técnico.

* **El Grupo F como Eje Crítico:** Registra el promedio de ranking más bajo del torneo con un **26.00**, consolidándose firmemente como el grupo estadísticamente más difícil. Sus integrantes se ubican, en promedio, tres puestos por encima del siguiente grupo más complejo.
* **Clúster de Alta Exigencia:** Detrás del Grupo F, se posicionan el **Grupo I (30.00)** y el **Grupo J (32.50)** como zonas de alto riesgo competitivo.
* **Bloque de Menor Presión:** El **Grupo C** presenta el promedio más alto con **36.00**, seguido de cerca por el **Grupo A (35.25)**, lo que los señala como los escenarios teóricamente más accesibles para avanzar a la fase de eliminación directa.

---

## 3. Análisis de Dispersión: Predictibilidad vs. Incertidumbre

Para entender la paridad real dentro de cada grupo, el análisis de los promedios se complementó con el cálculo de la Desviación Estándar ($\sigma$) del ranking. Esto permite identificar qué tan grande es la brecha de nivel entre los rivales de un mismo grupo:

* **Paridad Absoluta (Grupo B):** Registra la desviación estándar más baja de todo el torneo con un **11.90**. Esto significa que los cuatro equipos tienen un nivel sumamente equilibrado en el ranking actual. Al no existir un claro dominador en los papeles, este grupo se vuelve el más impredecible y cerrado de la primera fase.
* **Polarización Competitiva (Grupo G):** En el extremo opuesto, el Grupo G presenta la dispersión más alta llegando a **31.68**. Esta cifra describe una marcada brecha entre cabezas de serie del top mundial y selecciones con un ranking mucho menor. Estadísticamente, es un grupo con jerarquías verticales bien definidas y resultados más predecibles.

---

## 4. Contexto Histórico y Efecto de la Expansión

La distribución basada en el mejor resultado histórico de los equipos deja en evidencia la coexistencia de la tradición futbolística con la apertura del nuevo formato de 48 selecciones:

* **La Exclusividad de la Élite:** Solo un **14.58% (7 selecciones)** del total de participantes sabe lo que es levantar la copa del mundo. Este grupo minoritario concentra la mayor parte de la experiencia y el peso histórico del torneo.
* **Lealtad a la Fase Inicial:** El bloque más grande está compuesto por **13 selecciones (27.08%)** cuyo límite histórico ha sido quedarse en la Fase de Grupos.
* **El Impacto del Nuevo Formato:** Se registra la inclusión de **4 selecciones Debutantes** absolutas. El ingreso de estos equipos emergentes influye de forma directa en el aumento de la dispersión general del torneo, modificando el balance y generando los grupos polarizados detectados en el análisis estadístico.

---

## 5. Conclusiones Generales del Modelo

El tablero desarrollado permite ver que el Mundial 2026 presentará dos realidades muy claras en su fase inicial. Por un lado, zonas de alta volatilidad donde el equilibrio de nivel (baja desviación estándar) hará que la clasificación se defina por detalles mínimos, como ocurre en el Grupo B. Por el otro, grupos con una marcada brecha de rendimiento (alta desviación estándar) donde la lógica del ranking actual apunta a un desarrollo mucho más predecible. 

La integración de variables de rendimiento presente e historial pasado en este dashboard facilita una lectura rápida, visual y con sustento matemático del mapa competitivo del torneo antes de que ruede el balón.
