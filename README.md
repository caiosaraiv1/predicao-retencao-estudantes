# Predição de Retenção de Estudantes no Ensino Superior 🎓

## 📌 Descrição

Este projeto tem como objetivo analisar e prever a retenção de estudantes no ensino superior, identificando fatores que podem levar ao **abandono** (Dropout), **matrícula contínua** (Enrolled) ou **conclusão do curso** (Graduate).

Através de técnicas de **Análise Exploratória de Dados (EDA)** e **Machine Learning**, foi possível construir modelos preditivos capazes de estimar a trajetória acadêmica de um aluno com base em características **socioeconômicas**, **acadêmicas** e **institucionais**.

---

## 🎯 Objetivos

* Realizar a **análise exploratória de dados** para entender os principais fatores associados à retenção.
* Implementar **modelos de classificação** para prever a situação acadêmica do estudante.
* Comparar o desempenho dos modelos por meio de métricas adequadas.
* Exportar os melhores modelos e transformadores para **uso prático e reprodutível**.

---

## 🗂️ Estrutura do Projeto

```plaintext
predicao-retencao-estudantes/
├── data/
│   └── dataset.csv
├── modelos/
│   ├── modelo_onehotenc.pkl
│   └── modelo_random_forest.pkl
├── notebook/
│   └── Predição de Retenção de Estudantes.ipynb
├── README.md
└── requirements.txt

```

---

## 📊 Fonte dos Dados

Os dados utilizados neste projeto foram obtidos do Kaggle:
🔗 [Higher Education - Predictors of Student Retention](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention/data)

---

## ⚙️ Tecnologias e Bibliotecas

* **Linguagem:** Python 3
* **Manipulação de Dados:** pandas, numpy
* **Visualização:** plotly
* **Machine Learning:** scikit-learn
* **Serialização:** pickle

---

## 📝 Metodologia

### 1. Carregamento e Análise dos Dados

* Utilização do `pandas` para carregamento.
* Visualização exploratória com `plotly` para identificar padrões relevantes.

### 2. Pré-processamento

* Codificação de variáveis categóricas com `OneHotEncoder`.
* Normalização de variáveis numéricas com `MinMaxScaler`.
* Separação entre variáveis independentes (features) e dependente (Target).

### 3. Modelagem

* Treinamento e avaliação de diferentes algoritmos:

  * DummyClassifier (baseline)
  * DecisionTreeClassifier
  * RandomForestClassifier
  * KNeighborsClassifier

### 4. Avaliação

* Comparação de modelos utilizando **acurácia**.
* Análise de overfitting com scores de treino e teste.

### 5. Exportação

* Serialização do melhor modelo (`RandomForestClassifier`) e do transformador (`OneHotEncoder`) com `pickle`.

### 6. Predição com Novo Dado

* Simulação de predição utilizando um perfil hipotético de estudante.
* Conversão do resultado numérico para rótulo interpretável:

  * `0` → Dropout
  * `1` → Enrolled
  * `2` → Graduate

---

## 🚀 Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/caiosaraiv1/predicao-retencao-estudantes
cd predicao-retencao-estudantes
```

### 2. Crie um ambiente virtual (opcional, mas recomendado)

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Execute o notebook

Abra o arquivo `preditor_estudantes.ipynb` no Jupyter Notebook ou Google Colab e execute as células.

---
## ✅ Resultados Obtidos

| Modelo                 | Acurácia |
| ---------------------- | -------- |
| DummyClassifier        | \~0.49   |
| DecisionTreeClassifier | \~0.72   |
| RandomForestClassifier | \~0.75   |
| KNeighborsClassifier   | \~0.59   |

O **RandomForestClassifier** obteve o melhor desempenho, equilibrando **precisão** e **capacidade de generalização**.

---

## 🛠️ Funcionalidades Implementadas

* ✅ Análise Exploratória de Dados
* ✅ Pré-processamento automatizado
* ✅ Treinamento e avaliação de modelos
* ✅ Exportação de modelo e transformador
* ✅ Predição em dados novos
