 # Segmentación de Clientes mediante Análisis RFM

## 📌 Descripción del Proyecto
Este proyecto implementa una segmentación estratégica de clientes basada en la metodología **RFM (Recency, Frequency, Monetary)**. A partir de datos transaccionales históricos, se evalúa el comportamiento individual de compra para clasificar a los clientes en segmentos de negocio clave (Campeones, Leales, Prometedores, En Riesgo y Dormidos).

El objetivo principal es transformar datos masivos en grupos accionables para la toma de decisiones comerciales y campañas de retención personalizadas.

---

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3 (Pandas, NumPy)
* **Entorno de Desarrollo:** Google Colab
* **Business Intelligence:** Power BI (Modelado de datos y Dashboard interactivo)
* **Formatos:** Archivos `.csv` transaccionales

---

## 💡 Metodología & Proceso de Analítica

1. **Limpieza y Preparación de Datos:**
   * Tratamiento de valores nulos y duplicados.
   * Filtrado de devoluciones y transacciones atípicas.
2. **Cálculo de Métricas RFM:**
   * **Recencia (R):** Días transcurridos desde la última compra.
   * **Frecuencia (F):** Cantidad total de transacciones únicas.
   * **Monto (M):** Suma total invertida por el cliente.
3. **Puntuación por Cuantiles (`pd.qcut`):**
   * Asignación de puntajes del 1 al 5 para cada dimensión, dividiendo la población en quintiles proporcionales (20% por categoría).
4. **Mapeo de Segmentos de Negocio:**
   * Aplicación de lógica condicional para categorizar a los clientes según sus combinación de puntuaciones:
     * 🏆 **Campeones:** Compran seguido, recientemente y con alto valor.
     * 💙 **Clientes Leales:** Compradores frecuentes y consistentes.
     * 🚀 **Prometedores / Recientes:** Clientes nuevos con potencial de desarrollo.
     * ⚠️ **En Riesgo / Atención Urgente:** Clientes de gran valor histórico que no han comprado recientemente.
     * 💤 **Dormidos / Reactivación:** Clientes con bajo compromiso reciente.

---

## 📈 Dashboard & Resultados de Negocio
* **Segmentación Clarificada:** Identificación precisa del volumen y margen aportado por cada segmento.
* **Estrategias Diferenciadas:** Definición de tácticas específicas (programas de fidelización para *Leales*, campañas de reactivación urgentes para clientes *En Riesgo*).
* **Integración BI:** Generación de archivos estructurados (`rfm_segmentado_final.csv`) consumidos por Power BI para análisis dinámico.

---
*Desarrollado por [Susana Uztáriz](https://github.com/SusanaDataLab)*
