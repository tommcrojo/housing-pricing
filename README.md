# Análisis Multivariable en la Valoración de Viviendas en Mercados Dinámicos

## 📋 Problema que resuelve

Este proyecto aborda la predicción de precios inmobiliarios en California, un desafío crítico para compradores, vendedores e inversores en mercados altamente dinámicos. La precisión en la estimación de valores permite:

- **Para compradores**: Identificar propiedades infravaloradas
- **Para vendedores**: Establecer precios competitivos y realistas
- **Para inversores**: Evaluar retornos potenciales y tendencias de mercado

El modelo transforma variables geoespaciales y socioeconómicas en predicciones precisas, superando las limitaciones de métodos tradicionales que no capturan adecuadamente las complejas relaciones entre ubicación, características de la propiedad y precio.

## 🔧 Tecnologías utilizadas

- **Lenguajes**: Python 3.8+
- **Análisis de datos**: Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (Random Forest, Linear Regression)
- **Modelado**: Cross-validation, Grid Search, métricas de regresión
- **Entorno**: Jupyter Notebooks

## 🏗️ Arquitectura y metodología

El proyecto sigue un pipeline estructurado de ML:

1. **Exploración de datos**:
   - Análisis de distribuciones y outliers
   - Matriz de correlación de variables
   - Visualización geoespacial de precios

2. **Preprocesamiento**:
   - Transformación logarítmica de distribuciones sesgadas
   - One-hot encoding de variables categóricas
   - Escalado de variables numéricas

3. **Feature Engineering**:
   - Creación de ratios personalizados (dormitorios/habitación, habitaciones/hogar)
   - Integración de variables geoespaciales
   - Análisis de proximidad al océano

4. **Modelado**:
   - Entrenamiento de regresión lineal (baseline)
   - Implementación de Random Forest Regressor
   - Optimización de hiperparámetros mediante Grid Search con validación cruzada

5. **Evaluación**:
   - Comparativa de modelos
   - Análisis de métricas (MSE, RMSE, R²)
   - Interpretación de importancia de variables

## 📊 Resultados y métricas

- **Precisión del modelo**: R² = 0.81 en datos de test
- **Mejora sobre baseline**: +14% vs. regresión lineal (R² = 0.67)
- **Feature engineering**: Incremento del 15% en capacidad predictiva mediante variables derivadas
- **Variables más relevantes**: Proximidad al océano (+0.62), ingresos medianos (+0.47), latitud (-0.36)
- **Error medio**: 8% sobre el valor real de las propiedades

## 🚀 Próximos pasos

- Integrar datos temporales para capturar tendencias de mercado
- Implementar modelos de ensemble más complejos (XGBoost, LightGBM)
- Desarrollar API para consultas en tiempo real
- Añadir visualizaciones interactivas mediante Plotly
- Experimentar con técnicas avanzadas de feature selection

## 📝 Licencia

MIT

---

*Este proyecto forma parte de mi portfolio de Data Science y está abierto a contribuciones y sugerencias.*
