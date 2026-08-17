# tell-me-why-estudos

Repositório de estudos do curso **[Téo Me Why](https://cursos.teomewhy.org/material_2025)**, reunindo anotações, exercícios e projetos ao longo da trilha de dados: Bash/Git, Python, Estatística e Machine Learning.

## 📚 Módulos

### 01 — Bash, Git e GitHub
Fundamentos de linha de comando e versionamento: comandos básicos do Bash (`RESUMO_BASH_GIT_GITHUB.md`), fluxo de trabalho com branches (`GIT_FLOW.md`), além de exercícios práticos com arquivos, código e comandos de terminal.

### 02 — Python
Do básico ao uso de bibliotecas de dados:
- **Python básico** — variáveis, laços, listas, dicionários, tuplas, funções, módulos e ambientes virtuais.
- **Arquivos e APIs** — leitura/escrita de arquivos, consumo de API (busca de CEPs).
- **Pandas** — um percurso extenso, cobrindo Series/DataFrame, leitura de CSV/HTML/clipboard, filtros, ordenação, tratamento de dados (nulos, duplicatas, conversão de tipos), `apply`, `groupby`, `merge`, `concat`, integração com banco de dados (incluindo um mini-ETL) e casos específicos como `stack`/`unstack`, tabelas dinâmicas (pivot) e `explode`.

### 03 — Estatística Básica
Estatística descritiva e inferencial aplicada a dados, incluindo comparações em SQL e Python:
- Variáveis qualitativas e tabelas de frequência (Python e SQL).
- Medidas de tendência central (média, mediana, moda) e de resumo.
- Medidas de dispersão (variância, amplitude).
- Visualizações: histograma, boxplot e gráfico de dispersão, com discussão de quando usar cada um.
- Distribuições de probabilidade: Bernoulli e Normal.
- Intervalo de confiança (teoria e implementação em Python).
- Teste de hipótese.

### 04 — Machine Learning
Da introdução conceitual até um projeto completo de ponta a ponta:
- **Início** — motivação, ciclo analítico e primeiros exemplos práticos.
- **Modelos de regressão** — regressão linear (dedução matemática incluída) e árvore de decisão.
- **Classificação** — regressão logística, árvore de decisão, Naive Bayes e métricas de avaliação (matriz de confusão, acurácia, precisão, recall, especificidade, curva ROC).
- **Projeto Churn** — projeto aplicado de previsão de cancelamento de clientes, com relatório próprio (veja abaixo) e rastreamento de experimentos via **[MLflow](https://mlflow.org/)** (`train.py`, `train_mlflow.py`, histórico de execuções em `mlruns/`).

## 🎯 Projeto em destaque: Previsão de Churn

Documentado em [`04_Machine_Learning/05_Projeto_Churn/README.md`](04_Machine_Learning/05_Projeto_Churn/README.md), aplica a metodologia **SEMMA** (Sample, Explore, Modify, Model, Assess) da SAS ao problema de churn, cobrindo:
- Amostragem, incluindo separação *Out of Time* e balanceamento de classes (*under/over sampling*).
- Tratamento de dados: padronização, imputação de valores faltantes (com diferentes estratégias conforme o tipo de variável) e *binning*.
- Codificação de variáveis categóricas: One-Hot Encoding e Mean Encoder.
- Treinamento e rastreamento de experimentos com MLflow.

## 🛠️ Tecnologias utilizadas

- **Python 3**
- [Pandas](https://pandas.pydata.org/) — manipulação e tratamento de dados
- [Scikit-learn](https://scikit-learn.org/) — modelos de Machine Learning
- [SQLAlchemy](https://www.sqlalchemy.org/) — integração com banco de dados
- [MLflow](https://mlflow.org/) — rastreamento de experimentos de ML
- [Requests](https://requests.readthedocs.io/) — consumo de APIs
- SQL — comparações e exercícios em paralelo ao Pandas

## ⚙️ Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/Fefeeu/tell-me-why-estudos.git
   cd tell-me-why-estudos
   ```

2. Crie um ambiente virtual e instale as dependências (declaradas em `02_Python/01_python_basico/ambiente_virtual/requirements.txt`):
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r 02_Python/01_python_basico/ambiente_virtual/requirements.txt
   ```

3. Os exercícios estão organizados por módulo e numerados na ordem em que foram estudados — basta navegar até a pasta desejada e rodar o script:
   ```bash
   python 02_Python/01_python_basico/01_ola_mundo.py
   ```

4. Para o projeto de Churn com rastreamento via MLflow:
   ```bash
   cd 04_Machine_Learning/05_Projeto_Churn/01_code
   python train_mlflow.py
   mlflow ui   # abre a interface web para visualizar os experimentos
   ```

## 📎 Sobre o curso

Este repositório acompanha o curso **Téo Me Why**, com material disponível em [cursos.teomewhy.org/material_2025](https://cursos.teomewhy.org/material_2025) — recomendado especialmente para quem está começando na área de dados.
