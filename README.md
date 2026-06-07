# 📊 Análisis de Experimento A/B: Optimización de Conversión y Ticket Promedio

Este proyecto evalúa los resultados de un experimento A/B implementado en una plataforma digital con el objetivo de validar si un rediseño estructural de la interfaz (Versión B) supera a la versión actual de control (Versión A) tanto en el volumen de transacciones como en el valor monetario de las mismas. 

El análisis abarca pruebas de hipótesis estadísticas para variables numéricas (gasto promedio) y categóricas (tasas de conversión, fuentes de tráfico y perfiles de usuario).

---

## 🚀 Estructura del Proyecto

El flujo de trabajo se divide en las siguientes etapas metodológicas dentro del Jupyter Notebook:
1. **Paso 1:** Análisis exploratorio de datos (EDA) y limpieza de la muestra.
2. **Paso 2:** Comparación del gasto promedio entre la Página A y B (Prueba de hipótesis paramétrica/no paramétrica).
3. **Paso 3:** Comparación de la tasa de conversión entre ambas versiones de página.
4. **Paso 4:** Análisis de la relación e impacto de los canales de adquisición (Fuente de Tráfico).
5. **Paso 5:** Análisis del impacto según la antigüedad o historial del cliente (Tipo de Usuario).
6. **Paso 6:** Visualización avanzada de proporciones y distribuciones absolutas de variables categóricas.
7. **Paso 7 / 8:** Conclusiones ejecutivas y recomendaciones estratégicas de negocio (*Stakeholder Insights*).

---

## 📈 Hallazgos Clave y Resultados Estadísticos

### 1. Rendimiento de la Página (A vs B)
* **Tasa de Conversión:** La **Versión B (Página de prueba)** demostró una superioridad estadística contundente sobre la Versión A. Al aplicar una prueba de Chi-cuadrada / Z-test, el *p-value* resultó significativamente menor al nivel de significancia estandarizado ($\alpha = 0.05$), rechazando la hipótesis nula ($H_0$) y demostrando que las optimizaciones de diseño e interfaz incrementan de forma real la probabilidad de compra.
* **Gasto Promedio:** Además de convertir a un mayor volumen de usuarios, la **Versión B** incrementó significativamente el ticket promedio por cliente convertido. Las pruebas de hipótesis correspondientes y el análisis visual de intervalos de confianza confirmaron que la diferencia en el valor monetario de las compras es sólida y no es producto de fluctuaciones aleatorias.

### 2. Canales de Adquisición (Fuentes de Tráfico)
* La prueba de Chi-cuadrada de independencia confirmó la existencia de una relación estadísticamente significativa (*p-value* $< 0.05$) entre la fuente de tráfico (`traffic_source`) y el éxito de conversión. 
* A través del análisis de proporciones relativas, se identificaron canales específicos de marketing que atraen leads con una intención de compra e índice de éxito sustancialmente más elevados, lo que marca una pauta clave para la distribución de pauta publicitaria.

### 3. Perfil de Usuario (Nuevo vs Recurrente)
* Contrario a las fuentes de tráfico, la prueba de Chi-cuadrada de independencia para la variable `user_type` devolvió un *p-value* mayor a $0.05$, lo que obligó a **no rechazar la hipótesis nula ($H_0$)**. 
* Visualmente, las proporciones de conversión se mantuvieron simétricas e idénticas en ambos grupos. Esto demuestra que el rendimiento de la Versión B es robusto y homogéneo: es igual de persuasiva para un visitante primerizo como para un cliente recurrente.

---

## 💡 Recomendaciones Estratégicas de Negocio

1. **Despliegue Inmediato al 100%:** Se recomienda implementar de manera definitiva la **Versión B** en la plataforma productiva de forma global. La evidencia de datos garantiza un impacto económico positivo doble: mayor volumen neto de transacciones y un ticket de compra más elevado por cliente.
2. **Optimización del Retorno de Inversión (ROI):** El equipo de Growth Marketing debe auditar la asignación de recursos, recortando presupuesto de los canales de adquisición de bajo rendimiento estadístico y concentrando la inversión en escalar el tráfico de las fuentes identificadas como de alta conversión.
3. **Estandarización del Embudo:** Dado que la conversión es independiente de la antigüedad del cliente, no es necesario segmentar o invertir recursos técnicos en flujos hiper-personalizados separados para usuarios nuevos y recurrentes; la landing page actual responde con excelencia de manera generalizada.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3.9+**
* **Pandas & NumPy:** Manipulación de datos y construcción de tablas de contingencia.
* **SciPy (stats):** Aplicación de pruebas de Chi-cuadrada de independencia (`chi2_contingency`) y pruebas de hipótesis para comparación de medias.
* **Matplotlib & Seaborn:** Creación de gráficos de barras apiladas, histogramas, diagramas de caja y visualización de volumen absoluto y proporcional.

---
