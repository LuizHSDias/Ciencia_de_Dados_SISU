# 🎓 Predição da Efetivação de Matrícula de Candidatos Convocados no SISU 2023/2 (Em Desenvolvimento)

## 📖 Sobre o Projeto

Este projeto foi desenvolvido como Trabalho Prático da disciplina de **Ciência de Dados**, tendo como objetivo resolver o **Problema B** proposto no enunciado.

O objetivo consiste em construir modelos de Machine Learning capazes de prever se um candidato **convocado na Lista de Espera do SISU 2023/2 efetivará ou não sua matrícula**, utilizando informações socioeconômicas, acadêmicas e geográficas disponíveis na base de dados.

O projeto contempla todas as etapas do processo de Ciência de Dados, desde a análise exploratória até o treinamento, ajuste e avaliação dos modelos preditivos.

---

# 🎯 Objetivo

Desenvolver e comparar modelos de classificação para responder à seguinte pergunta:

> **Dado que um candidato foi convocado, ele efetivará a matrícula?**

---

# 📂 Estrutura do Projeto

```
📦 Projeto
│
├── 01_EDA_Preprocessamento.ipynb
│
├── 02_DecisionTree.ipynb
│
├── 03_RandomForest.ipynb
│
├── 04_GradientBoosting.ipynb
│
├── 05_Comparacao_Modelos.ipynb
│
├── problema_b_treino.pkl
├── problema_b_teste.pkl
│
└── README.md
```

---

# 🗂 Base de Dados

Os dados utilizados correspondem à **Lista de Espera do SISU 2023/2**, disponibilizada para fins acadêmicos na disciplina.

A base contém informações como:

- Curso
- Instituição de Ensino Superior
- Campus
- Estado
- Município
- Modalidade de concorrência
- Cotas
- Notas do ENEM
- Nota de corte
- Situação da matrícula
- Demais informações acadêmicas

---

# 🔎 Etapas Desenvolvidas

## 1. Análise Exploratória dos Dados (EDA)

Foram realizadas as seguintes análises:

- Inspeção da base de dados
- Tipos de dados
- Valores ausentes
- Registros duplicados
- Distribuição da variável-alvo
- Estatísticas descritivas
- Identificação de outliers
- Análise gráfica dos dados

### Visualizações

- Distribuição da variável MATRÍCULA
- Distribuição geográfica dos candidatos
- Distribuição por sexo
- Histograma das notas dos candidatos
- Heatmap de correlação das notas do ENEM
- Distribuição dos cursos com maior número de candidatos

---

## 2. Pré-processamento

Foram realizadas as seguintes etapas:

- Remoção de atributos de identificação
- Remoção de variáveis com vazamento de informação (Data Leakage)
- Tratamento dos valores ausentes
- Conversão dos tipos de dados
- Engenharia de atributos
- Criação das variáveis:

  - MESMA_UF
  - MESMO_MUNICIPIO
  - IDADE

- Codificação das variáveis categóricas utilizando **Ordinal Encoding**
- Separação entre treino e teste (Holdout)
- Padronização das variáveis numéricas (StandardScaler)
- Balanceamento das classes utilizando **SMOTE**

---

# 🤖 Modelos Avaliados

Os modelos implementados encontram-se em notebooks separados.

- Decision Tree
- Random Forest
- Gradient Boosting

Cada notebook contempla:

- Treinamento
- Ajuste de hiperparâmetros
- Avaliação
- Tempo de treinamento
- Métricas de desempenho

---

# 📊 Métricas de Avaliação

Os modelos são avaliados utilizando:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Matriz de Confusão
- Tempo de treinamento

---

# 🛠 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn (SMOTE)
- Joblib

---

# 📌 Pipeline do Projeto

```
Base de Dados

↓

EDA

↓

Pré-processamento

↓

Feature Engineering

↓

Codificação

↓

Separação Treino/Teste

↓

Padronização

↓

Balanceamento (SMOTE)

↓

Treinamento

↓

Busca de Hiperparâmetros

↓

Avaliação

↓

Comparação dos Modelos
```

---

# 📈 Resultados

Os resultados obtidos para cada algoritmo encontram-se nos respectivos notebooks.

Ao final do projeto é realizada uma comparação entre os modelos, considerando desempenho preditivo, tempo de treinamento e capacidade de generalização.

---

# 👨‍💻 Autor

**Luiz Henrique Santos Dias**

Graduando em Engenharia de Computação — CEFET-MG

---

# 📄 Licença

Este projeto foi desenvolvido exclusivamente para fins acadêmicos e de portfólio.