# 🎲 Yahtzee — Simulación de Montecarlo en Python

Este repositorio contiene una implementación completa y paso a paso en Python para simular partidas de **Yahtzee (Generala)** y analizar su comportamiento estadístico mediante experimentos de **Montecarlo** (1.000 y 10.000 partidas).

El proyecto modela la lógica del juego, las heurísticas de decisión para conservar dados y las reglas oficiales de puntuación (incluyendo la bonificación de la sección superior y las reglas especiales del **Joker** para Yahtzees adicionales).

---

## 📋 Contenido del Proyecto

El desarrollo del algoritmo y la simulación se divide en las siguientes etapas clave:

1. **Generación de Dados:** Simulación de lanzamientos de dados mediante distribuciones uniformes.
2. **Estrategia de Conservación:** Heurística paso a paso para decidir qué dados conservar y cuáles relanzar en cada uno de los 3 tiros permitidos por turno.
3. **Motor de Puntuación:** Implementación matemática de las 13 categorías puntuables.
4. **Regla de Joker:** Lógica para asignar Yahtzees adicionales cuando la categoría principal ya ha sido utilizada.
5. **Simulación y Validación de Partidas:** Sistema automatizado de pruebas y aserciones para garantizar que no haya inconsistencias en el flujo de juego.
6. **Simulación de Montecarlo:** Ejecución masiva de experimentos con control de semilla aleatoria (`SEED`) para garantizar la reproducibilidad de los resultados.
7. **Análisis Gráfico y Estadístico:** Comparación de métricas de desempeño entre dos jugadores utilizando librerías como `pandas`, `numpy` y `matplotlib`.

---

## ⚙️ Decisiones Técnicas y de Diseño

* **Semilla Determinista:** Se utiliza la semilla estática `SEED = 20261017` en el generador pseudoaleatorio de Python para asegurar la reproducibilidad exacta de los lanzamientos y las partidas.
* **Arquitectura Orientada a Objetos:** La clase `Jugador` encapsula de forma independiente la tarjeta de puntuación, el historial de turnos y las lógicas de cálculo de bonificaciones.
* **Frecuencias Diferenciadas:** El sistema registra de manera independiente las combinaciones **observadas** durante los lanzamientos intermedios frente a las categorías **utilizadas** finalmente para puntuar en la tarjeta.

---

## 🛠️ Requisitos e Instalación

Para ejecutar este notebook de forma local o en entornos interactivos, necesitas contar con Python 3 y las siguientes librerías científicas instaladas:

```bash
pip install numpy pandas matplotlib
