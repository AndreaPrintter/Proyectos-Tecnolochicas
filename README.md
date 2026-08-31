# SISTEMA_MONITOREO_FISIOLOGICO_APP

🫀 **Cardiopulmonary Physiological Monitoring System**

Aplicación móvil para telemetría y análisis de rendimiento cardiovascular

[Descripción](#descripción) • [Características](#características) • [Instalación](#instalación) • [Uso](#uso) • [Modelos](#modelos-estadísticos-implementados) • [Tecnologías](#tecnologías)

---

## 📝 Descripción
**Cardiopulmonary Physiological Monitoring System** es una aplicación móvil especializada en el análisis de la respuesta cardiovascular y respiratoria durante el ejercicio, desarrollada en MIT App Inventor. La aplicación procesa datos fisiológicos (Frecuencia Cardíaca y Saturación de Oxígeno) obtenidos a lo largo de una sesión de 60 minutos en cinta ergométrica. 

Conectada directamente a una base de datos en Google Sheets, permite la visualización dinámica de los signos vitales, el modelado estadístico de tendencias mediante regresión lineal, y la emisión de diagnósticos asistidos por Inteligencia Artificial (mediante modelos locales con Ollama) para evaluar las fases fisiológicas del entrenamiento.

> **Aviso de Datos:** Los datos presentados en esta base de datos corresponden a resultados experimentales reales y verídicos. Todos los derechos sobre la información pertenecen exclusivamente al Autor. El acceso a estos datos no implica la cesión de ningún derecho de propiedad intelectual sobre los mismos. Su uso no autorizado está prohibido.

## ✨ Características
☑️ **Extracción de Datos:** Conexión y lectura de registros en tiempo real desde Google Sheets.

**Gráficos interactivos bidimensionales:**
* Tiempo vs Frecuencia Cardíaca (Evolución de BPM)
* Tiempo vs Saturación de Oxígeno (Dinámica de SpO2%)

**Diagnóstico Asistido por IA (Ollama):**
* Identificación automática de las fases del ejercicio (calentamiento, trabajo continuo y enfriamiento).
* Análisis de la normalidad de la respuesta cardiovascular procesado de forma local para garantizar la privacidad de los datos médicos.

## 🔬 Modelos Estadísticos Implementados

**1. Regresión Lineal (Línea de Mejor Ajuste)**

Para evaluar la tendencia del esfuerzo físico y la oxigenación a lo largo de la rutina, la aplicación calcula e implementa de forma automática la línea de mejor ajuste basada en la ecuación de la recta:

$$y = mx + b$$

**Parámetros calculados en tiempo real:**
* **$m$ (Pendiente / Slope):** Indica la tasa de cambio (aumento o disminución) del signo vital a lo largo del tiempo de ejercicio.
* **$b$ (Intersección en Y / Y-Intercept):** Valor inicial proyectado del signo vital al comenzar la prueba.
* **$R$ (Coeficiente de Correlación):** Evalúa la fuerza y dirección de la relación estadística entre el tiempo transcurrido y la respuesta fisiológica del usuario.

## 🚀 Instalación

**Requisitos Previos:**
* Cuenta de Google con acceso a Google Sheets (para alojar la base de datos `datos_caminadora_hr_spo2`).
* MIT App Inventor 2.0+ (para importar el proyecto `.aia`).
* Entorno local configurado con Ollama (para la ejecución del análisis de IA sin dependencia de la nube).
* 
