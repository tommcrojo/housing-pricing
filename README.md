# Análisis Multivariable en la Valoración de Viviendas en Mercados Dinámicos

## 📋 Problema que resuelve

Este proyecto aborda la predicción de precios inmobiliarios en California, un desafío crítico para compradores, vendedores e inversores en mercados altamente dinámicos. La precisión en la estimación de valores permite:

- **Para compradores**: Identificar propiedades infravaloradas
- **Para vendedores**: Establecer precios competitivos y realistas
- **Para inversores**: Evaluar retornos potenciales y tendencias de mercado

El modelo transforma variables geoespaciales y socioeconómicas en predicciones precisas, superando las limitaciones de métodos tradicionales que no capturan adecuadamente las complejas relaciones entre ubicación, características de la propiedad y precio.

## 🔧 Tecnologías utilizadas

- **Lenguajes**: Python 3.x
- **Análisis de datos**: Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (Random Forest, Linear Regression)
- **Optimización**: GridSearchCV, validación cruzada (5-fold)
- **Preprocesamiento**: StandardScaler, transformaciones logarítmicas, one-hot encoding
- **Entorno**: Jupyter Notebooks

## 🏗️ Arquitectura y metodología

El proyecto sigue un pipeline estructurado de ML:

1. **Exploración de datos**:
   - Análisis de distribuciones y valores nulos
   - Matriz de correlación de variables
   - Identificación de la alta correlación entre ingresos medianos y precio (0.69)

2. **Preprocesamiento**:
   - Transformación logarítmica de variables numéricas sesgadas (total_rooms, total_bedrooms, population, households)
   - One-hot encoding de 'ocean_proximity' (5 categorías)
   - Escalado de variables mediante StandardScaler

3. **Feature Engineering**:
   - Creación de 'bedroom_ratio' (total_bedrooms/total_rooms)
   - Desarrollo de 'household_rooms' (total_rooms/households)

4. **Modelado**:
   - Implementación de regresión lineal como baseline (R² = 0.68)
   - Entrenamiento de Random Forest Regressor con y sin escalado
   - Optimización mediante GridSearchCV con 36 combinaciones de hiperparámetros

5. **Evaluación**:
   - Comparación de rendimiento entre modelos
   - Evaluación en conjunto de test (25% de los datos)

## 📊 Resultados y métricas

- **Precisión del mejor modelo**: R² = 0.83 (Random Forest con escalado)
- **Mejora sobre baseline**: +15% vs. regresión lineal (R² = 0.68)
- **GridSearchCV**: Optimización con 36 combinaciones de hiperparámetros (n_estimators, min_samples_split, max_depth)
- **Variables más relevantes**: Los ingresos medianos mostraron la mayor correlación (0.69) con el precio inmobiliario
- **Dataset**: 20,433 registros después de eliminar valores nulos (~200 filas)

## 🚀 Próximos pasos

- Implementar técnicas avanzadas de feature selection
- Explorar modelos de ensemble adicionales (XGBoost, Gradient Boosting)
- Añadir análisis de importancia de características
- Implementar visualizaciones geoespaciales para representar la distribución de precios
- Experimentar con estrategias de validación temporal para simular predicciones en el mundo real

## 📝 Licencia

MIT

---

*Este proyecto forma parte de mi portfolio de Data Science & ML y está abierto a contribuciones y sugerencias.*
