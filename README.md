# 🎓 Predição da Efetivação de Matrícula de Candidatos Convocados no SISU 2023/2

> **Status:** 🚧 Em desenvolvimento

---

# 📖 Sobre o Projeto

Este projeto foi desenvolvido como Trabalho Prático da disciplina de **Ciência de Dados**, tendo como objetivo resolver o **Problema B** proposto no enunciado.

O objetivo consiste em construir modelos de Machine Learning capazes de prever se um candidato **convocado na Lista de Espera do SISU 2023/2 efetivará ou não sua matrícula**, utilizando informações socioeconômicas, acadêmicas e geográficas disponíveis na base de dados.

O projeto contempla todas as etapas do processo de Ciência de Dados, desde a análise exploratória até o treinamento, ajuste e avaliação dos modelos preditivos.

---

# 🎯 Objetivo

Desenvolver e comparar modelos de classificação para responder à seguinte pergunta:

> **Dado que um candidato foi convocado, ele efetivará a matrícula?**

---

# 🚧 Status do Projeto

### ✅ Etapas concluídas

- Análise Exploratória dos Dados (EDA)
- Pré-processamento
- Engenharia de Atributos
- Seleção de Variáveis
- Codificação das Variáveis Categóricas
- Separação entre Treino e Teste (Holdout)
- Padronização das Variáveis
- Balanceamento das Classes (SMOTE)
- Exportação da Base Processada
- Implementação da Random Forest

### ⏳ Próximas etapas

- Implementação da Decision Tree
- Implementação do Gradient Boosting
- Ajuste de Hiperparâmetros
- Avaliação dos Modelos
- Comparação Final

---

# 📂 Estrutura do Projeto

```text
📦 CIENCIA_DE_DADOS_SISU
│
├── 01_EDA_Preprocessamento.ipynb
│
└── README.md
```

> Novos notebooks serão adicionados conforme o desenvolvimento do projeto.

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
- Sistema de cotas
- Notas do ENEM
- Nota de corte
- Situação da matrícula
- Informações acadêmicas do candidato

---

# 🔎 Etapas Desenvolvidas

## 1. Análise Exploratória dos Dados (EDA)

Foram realizadas as seguintes análises:

- Inspeção do conjunto de dados
- Tipos de dados
- Valores ausentes
- Registros duplicados
- Distribuição da variável-alvo
- Estatísticas descritivas
- Identificação de possíveis outliers
- Análise gráfica dos dados

### Visualizações

- Distribuição da variável MATRÍCULA
- Distribuição geográfica dos candidatos
- Distribuição dos candidatos por sexo
- Histograma da nota do candidato
- Heatmap de correlação das notas do ENEM
- Distribuição dos cursos com maior número de candidatos

---

## 2. Pré-processamento

As seguintes etapas foram realizadas:

- Remoção de atributos de identificação
- Remoção de variáveis com vazamento de informação (*Data Leakage*)
- Tratamento dos valores ausentes
- Conversão dos tipos de dados
- Engenharia de atributos
- Criação das variáveis:

  - **MESMA_UF**
  - **MESMO_MUNICIPIO**
  - **IDADE**

- Seleção de atributos
- Codificação das variáveis categóricas utilizando **Ordinal Encoding**
- Separação entre treino e teste utilizando Holdout Estratificado
- Padronização das variáveis numéricas utilizando **StandardScaler**
- Balanceamento das classes utilizando **SMOTE**

---

# 🧠 Principais Decisões Metodológicas

Durante o desenvolvimento do projeto foram adotadas as seguintes estratégias:

- Utilização da estratégia Holdout com divisão estratificada (80% treino e 20% teste);
- Aplicação do StandardScaler somente após a divisão treino/teste, evitando *Data Leakage*;
- Balanceamento apenas do conjunto de treinamento utilizando SMOTE;
- Remoção de atributos de identificação e variáveis com vazamento de informação;
- Criação das features derivadas **MESMA_UF**, **MESMO_MUNICIPIO** e **IDADE**;
- Utilização de Ordinal Encoding para reduzir a dimensionalidade da base de dados.

---

# 🤖 Modelos de Machine Learning

Os modelos abaixo serão implementados nas próximas etapas do projeto:

- Decision Tree
- Random Forest
- Gradient Boosting

Cada modelo possuirá um notebook específico contendo:

- Treinamento
- Ajuste de hiperparâmetros
- Avaliação
- Comparação de desempenho

---

# 📊 Métricas de Avaliação

Os modelos serão avaliados utilizando as seguintes métricas:

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
- Google Colab

---

# 📌 Pipeline do Projeto

```text
Base de Dados
        │
        ▼
Análise Exploratória (EDA)
        │
        ▼
Pré-processamento
        │
        ▼
Engenharia de Atributos
        │
        ▼
Codificação das Variáveis
        │
        ▼
Separação Treino/Teste
        │
        ▼
Padronização
        │
        ▼
Balanceamento (SMOTE)
        │
        ▼
Treinamento dos Modelos
        │
        ▼
Busca de Hiperparâmetros
        │
        ▼
Avaliação
        │
        ▼
Comparação dos Modelos
```

---

# 📈 Resultados

Os resultados serão apresentados após a implementação dos modelos de Machine Learning.

Ao final do projeto será realizada uma comparação entre os algoritmos considerando:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Tempo de treinamento

---

# ▶️ Como Executar

1. Clone este repositório.

```bash
git clone https://github.com/LuizHSDias/Ciencia_de_Dados_SISU
```

2. Instale as bibliotecas necessárias.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn joblib
```

3. Abra o notebook:

```text
01_EDA_Preprocessamento.ipynb
```

4. Execute as células na ordem apresentada.

---

# 👨‍💻 Autor

**Luiz Henrique Santos Dias**

Graduando em Engenharia de Computação — CEFET-MG

---

# 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos e de portfólio.
