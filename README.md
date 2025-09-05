# 🎭 Showz - Marketing
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)


## 📌 Introducción  
Este proyecto se centra en el **análisis de datos de Showz**, una empresa dedicada a la venta de entradas para eventos.  
El objetivo principal es **optimizar la inversión en marketing** mediante la evaluación del comportamiento de los clientes, las compras realizadas y la rentabilidad de cada fuente de adquisición.  

---

## 🎯 Objetivos del Proyecto  
- Analizar el **comportamiento de los clientes** en el sitio web.  
- Identificar **patrones de compra** y tiempos de conversión.  
- Calcular métricas clave como:  
  - **Ingresos por cliente**.  
  - **Costo de Adquisición de Clientes (CAC)**.  
  - **Tasa de retención** por cohortes.  
- Evaluar el **punto de equilibrio** entre inversión en marketing e ingresos.  

---

## 📂 Conjunto de Datos  
El análisis utiliza tres fuentes principales (enero 2017 – diciembre 2018):  

1. **`visits_log`**: Registros del servidor sobre visitas al sitio web.  
   - `uid`: Identificador único del usuario.  
   - `device`: Dispositivo utilizado.  
   - `start_ts`: Fecha/hora de inicio de la sesión.  
   - `source_id`: Identificador de la fuente de anuncios.  

2. **`orders_log`**: Información de pedidos realizados.  
   - `uid`: Identificador único del comprador.  
   - `buy_ts`: Fecha/hora de compra.  
   - `revenue`: Ingreso generado por el pedido.  

3. **`costs`**: Estadísticas de gasto en marketing.  
   - `source_id`: Fuente de anuncios.  
   - `dt`: Fecha.  
   - `costs`: Gasto por día y fuente.  

---

## ⚙️ Preparación y Limpieza de Datos  
- Corrección de nombres de columnas.  
- Conversión de variables de fecha a formato `datetime`.  
- Verificación de **datos duplicados o ausentes** (no se encontraron).  
- Creación de columnas adicionales para análisis temporal (`visit_day`, `visit_week`, `visit_month`).  

---

## 🔎 Análisis Exploratorio  

### 👥 Uso del servicio  
- **DAU promedio**: ~908 usuarios.  
- **WAU promedio**: ~5716 usuarios.  
- **MAU promedio**: ~23,228 usuarios.  
- Duración promedio de cada sesión: **643.5 segundos (~10 min)**.  

### 🔄 Retención de usuarios  
- La **tasa de retención** cae bruscamente después del primer mes (< 8%).  
- A largo plazo, solo un **5 % de usuarios** regresa mensualmente.  

### 🛒 Comportamiento de compras  
- La mayoría de los usuarios compra el **mismo día de su primera visita**.  
- Cohortes muestran que la recurrencia de compras es baja después de los primeros meses.  

---

## 📊 Visualizaciones  
El proyecto incluye:  
- Series temporales de visitas y sesiones.  
- Histogramas de duración de sesiones y días hasta la compra.  
- **Mapas de calor de retención** y de frecuencia de compras por cohorte. 

---

## 🛠️ Tecnologías Utilizadas  
- **Python**  
- **Pandas**  
- **Matplotlib**  
- **Seaborn**  
- **Jupyter Notebook**  

---

## ✅ Conclusiones Resumidas  

🧠💡 **Hallazgos principales**  
- No todas las fuentes de adquisición son igual de rentables.  
- La **fuente 1** es la más eficiente y consistente.  
- La **retención de usuarios es baja**: el LTV cae después del primer mes, limitando el retorno global.  
- Una parte importante de usuarios activos **no está vinculada a ningún canal conocido**, lo que dificulta medir el impacto real de las campañas.  

📌 **Recomendaciones estratégicas**  
- **Invertir en la fuente 1**, la más rentable.  
- **Fuente 2**: investigar el caso de éxito de la cohorte 2017-09 y aplicar mejoras.  
- **Fuente 5**: revisar causas de la caída en ROMI en cohortes recientes.  
- **Fuentes 4, 9 y 10**: suspender temporalmente inversión (resultados regulares a malos).  
- **Fuente 3**: cesar inversión de inmediato (ROMI extremadamente bajo).  
- Implementar **estrategias de retención y fidelización** para alargar el ciclo de vida del cliente.  
- Mejorar el **seguimiento de campañas y visitas** para reducir el número de usuarios sin canal identificado.  

