# 🚀 Proyecto de Ingeniería de Datos y Detección de Fraude - Pasarela de Pagos (Izipay)

Repositorio oficial para la evaluación académica y técnica de Ciencia de Datos. El proyecto implementa una **Arquitectura Medallion (Bronze ➔ Silver ➔ Gold)** sobre un entorno de almacenamiento S3 (MinIO), procesando un universo transaccional de alta volumetría para la detección y análisis de fraude en pasarelas de pagos.

---

## 🛠️ Arquitectura y Stack Tecnológico
- **Almacenamiento Distribuido:** MinIO (Object Storage compatible con S3).
- **Procesamiento y Lenguaje:** Python / Jupyter Notebooks.
- **Librerías de Análisis y Visualización:** Pandas, NumPy, Matplotlib y Seaborn.


---

# 🚀 Mapeo del Informe Técnico vs. Notebooks

Para facilitar la revisión  se detalla dónde se implementó y ejecutó cada sección del informe técnico dentro de los notebooks y carpetas del repositorio:

Sección del Informe Técnico	Notebook / Ubicación Asociada	Descripción de la Ejecución en el Código
1. Introducción y Contexto:	Cuadernos/5.1.Carga_Exploracion_Datos.ipynb	Definición del problema, carga inicial del dataset IEEE-CIS y análisis de la tasa de fraude global (3.50%).
2. Arquitectura Medallion	Conexión a S3 / MinIO en los notebooks	Configuración del bucket S3 y estructuración de capas: Bronze (datos crudos), Silver (limpios) y Gold (analíticos).
3. Limpieza y Calidad de Datos:	Cuadernos/5.2.Limpieza_Calidad_Datos.ipynb	Tratamiento de nulos, eliminación de duplicados, manejo de valores atípicos (outliers) y estandarización de esquemas.
4. Transformación e Integración:	Cuadernos/5.3 y 5.4	Enriquecimiento de variables, conversión de moneda a Soles Peruanos (PEN) y uniones de tablas de transacciones e identidad.
5. Preprocesamiento para Modelado:	Cuadernos/5.5.Preprocesamiento_Datos.ipynb	Aplicación de codificación (One-Hot Encoding), escalado numérico y preparación de la matriz de características.
6. Resultados y KPIs (Capa Gold):	Cuadernos/6.1.Analisis_Descriptivo.ipynb	Generación de métricas de riesgo temporal, impacto económico, frecuencia de tarjetas y perfiles de dispositivos.
6.3 Hallazgos Principales:	Cuadernos/6.1.Analisis_Descriptivo.ipynb	Evidencia numérica de los picos de fraude en madrugadas de fines de semana y tickets elevados (> $200 USD).
9. Anexos (Figuras y Gráficas):	Carpeta Imágenes/	Contiene las figuras renderizadas (figura_1 a figura_4) listas para su visualización estática y validación visual.


## 📂 Estructura del Repositorio

El repositorio se encuentra organizado de la siguiente manera para facilitar la auditoría del código y los resultados:

```text
📦 Proyecto-fraude-izipay
│
├── 📂 Cuadernos/                  # Notebooks ejecutados con todo el pipeline de datos
│   ├── 5.1.Carga_Exploracion_Datos.ipynb
│   ├── 5.2.Limpieza_Calidad_Datos.ipynb
│   ├── 5.3.Manipular_Transformar_Datos.ipynb
│   ├── 5.4.Integracion_Validacion_Datos.ipynb
│   ├── 5.5.Preprocesamiento_Datos.ipynb
│   └── 6.1.Analisis_Descriptivo.ipynb
│
├── 📂 Imágenes/                   # Evidencias gráficas de la Capa Gold (utilizadas en el informe)
│   ├── figura_1_riesgo_temporal.png
│   ├── figura_2_impacto_economico.png
│   ├── figura_3_riesgo_dispositivos.png
│   └── figura_4_velocidad_transaccional.png
│
└── Léame.md                       # Documentación principal del proyecto



#🔍 Resumen de Hallazgos Clave

- Concentración Temporal

- Severidad Económica

- Vulnerabilidad por Dispositivo y Frecuencia

Link de Streamlit:

http://169.58.96.176:8501/



