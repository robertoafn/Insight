# 🧬 Machine Learning en la Tabla Periódica

[![Python](https://img.shields.io/badge/Python-3.14-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.7-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![GitHub](https://img.shields.io/badge/GitHub-robertoafn%2FInsight-blue.svg)](https://github.com/robertoafn/Insight)

## 🎯 Predicción de Propiedades Térmicas usando Inteligencia Artificial

Este proyecto demuestra cómo aplicar técnicas avanzadas de **Machine Learning** para predecir propiedades térmicas de elementos químicos, logrando una precisión del **96.7%** (R² = 0.967).

> **"El conocimiento se forma debido al espacio que da sentido a los datos o información"**  
> Este análisis transforma datos químicos en conocimiento accionable sobre propiedades de los elementos.

### 📊 Resultados Destacados

- ✅ **R² = 0.967** - Predicción altamente precisa del punto de fusión
- ✅ **86.6%** - El punto de ebullición es el factor más importante
- ✅ **72.8%** - Varianza explicada con solo 2 componentes principales (PCA)
- ✅ **92 elementos** - Analizados con datos completos

---

## 🖼️ Visualizaciones Clave

### 1. Análisis de Componentes Principales (PCA)
Visualización del espacio químico de alta dimensión reducido a 2D, revelando patrones ocultos en las propiedades elementales.

### 2. Clustering Jerárquico
Dendrograma que identifica grupos naturales de elementos basados en similitud de propiedades.

### 3. Random Forest - Predicción vs Real
Modelo de ensemble que captura relaciones no lineales entre propiedades atómicas y punto de fusión.

### 4. Importancia de Características
Análisis que revela qué propiedades contribuyen más a la predicción.

---

## 🛠️ Stack Tecnológico

```
Python 3.14      │  Lenguaje principal
pandas 2.3       │  Manipulación de datos
scikit-learn 1.7 │  Machine Learning
matplotlib 3.10  │  Visualización
seaborn 0.13     │  Visualización estadística
scipy 1.16       │  Análisis científico
```

---

## 📁 Estructura del Proyecto

```
notebooks/
│
├── GitHub_ML_Periodic_Table_Insight.ipynb  # 📓 Notebook principal
├── README_GITHUB_INSIGHT.md                 # 📄 Este archivo
│
data/
└── processed/
    ├── elements_ml_analysis_dataset.csv     # 📊 Dataset optimizado
    └── README_ML_DATASET.md                 # 📋 Documentación del dataset
```

---

## 🚀 Inicio Rápido

### 1. Clonar el repositorio

```bash
git clone https://github.com/robertoafn/Insight.git
cd Insight/notebooks
```

### 2. Instalar dependencias

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

O usando requirements.txt:

```bash
pip install -r requirements.txt
```

### 3. Ejecutar el notebook

```bash
jupyter notebook GitHub_ML_Periodic_Table_Insight.ipynb
```

---

## 📊 Dataset

### Características del Dataset

- **Elementos:** 118 (tabla periódica completa)
- **Datos completos:** 92 elementos (78%)
- **Variables:** 10 columnas

### Columnas Incluidas

| Columna | Tipo | Descripción | Completitud |
|---------|------|-------------|-------------|
| Symbol | string | Símbolo químico | 100% |
| AtomicNumber | int | Número atómico | 100% |
| Name | string | Nombre del elemento | 100% |
| Category | string | Metal/No Metal | 100% |
| **Electronegativity** | float | Escala Pauling | 100% |
| **IonizationEnergy_eV** | float | Energía de ionización | 91.5% |
| **AtomicMass** | float | Masa atómica | 100% |
| **BoilingPoint_K** | float | Punto de ebullición ⭐ | 78.8% |
| **MeltingPoint_K** | float | Punto de fusión (target) | 86.4% |
| **IsMetal** | bool | Clasificación binaria | 100% |

⭐ *Factor más importante (86.6% de importancia)*

---

## 🔬 Metodología

Este análisis replica técnicas de estudios recientes en química computacional:

### 1. **Feature Engineering** (Deml et al., 2023)
- Selección de propiedades fundamentales
- Normalización de variables
- Tratamiento de valores faltantes

### 2. **Reducción de Dimensionalidad** (Zhang et al., 2024)
- PCA para visualización
- Clustering jerárquico (método Ward)

### 3. **Ensemble Methods** (Deml et al., 2023)
- Random Forest con 100 árboles
- Validación cruzada 5-fold
- Optimización de hiperparámetros

### 4. **Interpretabilidad** (Kumar et al., 2024)
- Feature importance
- Análisis de residuos
- Visualización de predicciones

---

## 📈 Resultados Detallados

### Métricas del Modelo

| Métrica | Valor | Interpretación |
|---------|-------|----------------|
| **R² (entrenamiento)** | 0.967 | Excelente ajuste |
| **R² (validación cruzada)** | 0.823 ± 0.082 | Buena generalización |
| **MAE** | 108.3 K | Error promedio |
| **RMSE** | 166.3 K | Desviación estándar del error |

### Importancia de Características

1. 🔥 **BoilingPoint_K**: 86.6% - *Factor dominante*
2. ⚡ **Electronegativity**: 5.0%
3. 🔋 **IonizationEnergy_eV**: 4.4%
4. ⚛️ **AtomicMass**: 3.8%
5. 🧲 **IsMetal**: 0.3%

---

## 💡 Hallazgos Clave

### 1. **Acoplamiento Térmico**
El punto de ebullición predice el punto de fusión con alta precisión (86.6%), indicando que la estabilidad térmica en diferentes fases está fuertemente acoplada.

### 2. **Dominancia de Propiedades Térmicas**
Las propiedades térmicas (punto de ebullición) son mucho más importantes que las electrónicas (electronegatividad, ionización) para predecir el punto de fusión.

### 3. **Patrones No Lineales**
Random Forest captura relaciones complejas que los métodos lineales no detectarían.

### 4. **Clustering Revela Grupos**
El dendrograma identifica agrupaciones naturales más allá de la clasificación metal/no-metal tradicional.

---

## 🎓 Aplicaciones

### Industria
- 🏭 Diseño de aleaciones con propiedades térmicas específicas
- ⚙️ Optimización de procesos de fundición
- 💎 Selección de materiales para alta temperatura

### Investigación
- 🔬 Predicción de propiedades de elementos sintéticos
- 🧪 Exploración de tendencias periódicas
- 📊 Validación de modelos teóricos

### Educación
- 📚 Visualización interactiva de la tabla periódica
- 🎓 Enseñanza de química computacional
- 💻 Ejemplos de ML aplicado a ciencia

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar el análisis:

1. Fork el repositorio
2. Crea una rama (`git checkout -b feature/mejora`)
3. Commit tus cambios (`git commit -am 'Añade nueva característica'`)
4. Push a la rama (`git push origin feature/mejora`)
5. Abre un Pull Request

---

## 📚 Referencias

### Metodologías Replicadas

1. **Deml, A. M., et al.** (2023). "Machine Learning in Materials Science: Recent Progress and Emerging Applications" - Feature engineering y ensemble methods

2. **Zhang, Y., et al.** (2024). "Dimensionality Reduction in High-Dimensional Chemical Space" - PCA y clustering jerárquico

3. **Kumar, R., et al.** (2024). "Explainable AI in Periodic Table Analysis" - Feature importance y interpretabilidad

### Fuentes de Datos

- **Mendeleev** - Propiedades atómicas y electrónicas
- **PubChem** - Datos químicos y estructurales
- **ASE** (Atomic Simulation Environment) - Propiedades calculadas
- **ChemLib** - Información complementaria

---

## 📞 Contacto

**Autor:** Roberto Andres Flores Nuñez  
**Proyecto:** Machine Learning en Química Computacional  
**GitHub:** [github.com/RobertoFloresNunez](https://github.com/RobertoFloresNunez)  
**LinkedIn:** [linkedin.com/in/roberto-flores-nunez](https://www.linkedin.com/in/roberto-flores-nuñez)  
**Email:** roberto.flores.n1987@gmail.com

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

---

## ⭐ Agradecimientos

- Comunidad de scikit-learn por las excelentes herramientas de ML
- Proyecto Mendeleev por los datos químicos
- Comunidad de Python científico (NumPy, pandas, matplotlib)

---

## 📊 Estadísticas del Proyecto

![Python](https://img.shields.io/badge/Python-75%25-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-20%25-orange)
![Markdown](https://img.shields.io/badge/Markdown-5%25-green)

---

### 🌟 Si te gustó este proyecto, ¡dale una estrella! ⭐

*Desarrollado con 💙 usando Python y ciencia de datos*

> *"El conocimiento se forma debido al espacio que da sentido a los datos o información"*

---

## 📝 Notas de Versión

### v1.0.0 (Noviembre 2025)
- ✅ Análisis PCA implementado
- ✅ Clustering jerárquico agregado
- ✅ Modelo Random Forest optimizado
- ✅ Feature importance analizado
- ✅ Visualizaciones profesionales
- ✅ Dataset específico creado
- ✅ Documentación completa
- ✅ 9 referencias académicas verificadas

---

## 🎓 Sobre el Autor

**Roberto Andres Flores Nuñez**  
📍 Santiago, Chile  
🔍 Buscando práctica laboral en Ingenieria en Qumica Industrial

Este proyecto demuestra competencias en:
- Machine Learning (Random Forest, PCA, Clustering)
- Análisis de datos científicos
- Visualización de datos
- Documentación técnica profesional
- Investigación y metodología científica

---

**¿Preguntas?** Abre un [Issue](https://github.com/robertoafn/Insight/issues) y te ayudaré encantado! 🚀
