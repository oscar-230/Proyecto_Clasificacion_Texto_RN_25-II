# 🧠 Clasificación de Texto con Redes Neuronales  
**Análisis de Sentimientos en Tweets de Aerolíneas**

## 📚 Información del Curso
- **Asignatura:** Redes Neuronales  
- **Universidad:** Universidad del Valle  
- **Programa:** Ingeniería de Sistemas y Computación  
- **Semestre:** 2025-2  

## 👨‍🎓 Autor
- **Oscar David Cuaical Lopez**  
- **Código:** 202270657  
- **Email:** cuaical.oscar@correounivalle.edu.co  

---

## 📌 Descripción del Proyecto

Este proyecto tiene como objetivo aplicar y comparar diferentes arquitecturas de redes neuronales para resolver un problema de **clasificación de texto multiclase**.

Se analizan tres enfoques principales:

- Perceptrón Multicapa (**MLP**)  
- Red Neuronal Recurrente (**SimpleRNN**)  
- Red LSTM (**Long Short-Term Memory**)  

El desarrollo se divide en dos partes:

- **Parte 1:** Modelo basado en MLP con características TF-IDF  
- **Parte 2:** Modelos secuenciales (RNN y LSTM) para procesamiento de texto  

---

## 📊 Dataset

- **Nombre:** Twitter US Airline Sentiment Dataset  
- **Fuente:** https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment  
- **Tamaño:** 14,640 muestras  

### Descripción
Tweets en inglés sobre aerolíneas de Estados Unidos clasificados en:

- `positive`  
- `neutral`  
- `negative`  

---

## ⚙️ Tecnologías y Librerías

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- NLTK  
- Matplotlib, Seaborn  

---

## 🔹 Parte 1: MLP con TF-IDF

### 🧩 Técnicas utilizadas
- Vectorización de texto con **TF-IDF (1-2 gramas)**  
- Reducción de dimensionalidad con **SVD (300 componentes)**  
- Escalado de datos  
- Manejo de desbalance con **pesos de clase**  

### 🧠 Modelo
- Entrada: 300 características  
- Capas ocultas:
  - 32 neuronas + ReLU + regularización L2  
  - 16 neuronas + ReLU + regularización L2  
- Dropout: 50%  
- Salida: Softmax (3 clases)  

### 📈 Resultados
- **Accuracy en test:** ~0.70  

| Clase     | Precisión | Recall | F1-score |
|----------|----------|--------|----------|
| Negativo | 0.89     | 0.70   | 0.78     |
| Neutral  | 0.48     | 0.69   | 0.57     |
| Positivo | 0.56     | 0.71   | 0.63     |

---

## 🔹 Parte 2: RNN y LSTM

### 🧩 Técnicas utilizadas
- Limpieza de texto:
  - Minúsculas  
  - Eliminación de URLs y menciones  
  - Eliminación de caracteres especiales  
  - Eliminación de stopwords  
- Tokenización y padding  
- Embeddings de palabras  
- Manejo de desbalance con pesos de clase  

---

### 🧠 Modelos

#### 🔹 SimpleRNN
- Capa Embedding  
- SpatialDropout  
- Capa SimpleRNN  
- Capa densa (Softmax)  

#### 🔹 LSTM
- Capa Embedding  
- SpatialDropout  
- Capa LSTM con:
  - Dropout  
  - Recurrent dropout  
  - Regularización L2  
- Capa densa (Softmax)  

---

### 📈 Resultados

#### ✅ SimpleRNN
- **Accuracy:** ~0.68  

| Clase     | Precisión | Recall | F1-score |
|----------|----------|--------|----------|
| Negativo | 0.84     | 0.74   | 0.79     |
| Neutral  | 0.45     | 0.50   | 0.48     |
| Positivo | 0.49     | 0.65   | 0.56     |

---

#### 🚀 LSTM (Mejor modelo)
- **Accuracy:** ~0.76  

| Clase     | Precisión | Recall | F1-score |
|----------|----------|--------|----------|
| Negativo | 0.87     | 0.82   | 0.85     |
| Neutral  | 0.56     | 0.65   | 0.60     |
| Positivo | 0.66     | 0.70   | 0.68     |

---

## 📊 Conclusiones

- El dataset presenta **desbalance de clases**, lo que afecta el entrenamiento  
- El modelo MLP funciona como una buena línea base  
- Las redes recurrentes mejoran el rendimiento al capturar secuencias  
- **LSTM obtiene el mejor desempeño**, especialmente en precisión general  
- El preprocesamiento del texto es clave para buenos resultados  

---

## 🧪 Estrategias utilizadas

- Early Stopping para evitar sobreajuste  
- Dropout y regularización L2  
- Ajuste de tasa de aprendizaje  
- Uso de pesos de clase  

---

## 📉 Métricas de evaluación

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Matriz de confusión  

---

## 🚀 Trabajo futuro

- Implementar GRU o Transformers  
- Usar embeddings preentrenados (Word2Vec, GloVe)  
- Optimización de hiperparámetros  
- Aumentar datos de entrenamiento  

---

## 📁 Estructura del proyecto

├── Parte_1_MLP.ipynb

├── Parte_2_RNN_LSTM.ipynb

├── README.md


---

## 📌 Nota

Este proyecto fue desarrollado como parte del curso de **Redes Neuronales**, con el objetivo de aplicar técnicas de aprendizaje profundo a un problema real de procesamiento de lenguaje natural.

---
