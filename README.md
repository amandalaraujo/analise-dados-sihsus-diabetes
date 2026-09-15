# Predição de Risco de Óbito em Internações por Diabetes (SIHSUS)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

---

## Visão Geral do Projeto

Este repositório contém um projeto prático de **Análise de Dados e Aprendizado de Máquina (Machine Learning)** aplicado à saúde pública. O objetivo principal é identificar padrões clínicos e sociodemográficos associados ao desfecho grave (óbito) em internações motivadas por **Diabetes Mellitus (CID-10: E10 a E14)** no ecossistema do **SIHSUS** (Sistema de Informações Hospitalares do SUS).

A partir dessas análises, foi treinado um modelo preditivo de **Regressão Logística** capaz de estimar a probabilidade de óbito ou complicações graves para cada paciente internado.

---

## Definição do Problema

* **Problema:** Prever o risco de desfecho grave (óbito) durante a internação hospitalar de pacientes diabéticos.
* **Pergunta de Negócio/Pesquisa:** Dado o perfil do paciente (idade, sexo, raça/cor, tempo de permanência, uso de UTI, região), qual a probabilidade de evolução para óbito durante a internação?
* **Variável Alvo:** `MORTE` (0 = Sobreviveu, 1 = Óbito).
* **Impacto Prático:** A identificação precoce do perfil de maior risco permite auxiliar no direcionamento e priorização de recursos hospitalares (como leitos de UTI e monitoramento intensivo) e embasamento de decisões em saúde pública.

---

## Tecnologias e Ferramentas Utilizadas

* **Linguagem:** Python
* **Manipulação e Análise de Dados:** Pandas, NumPy
* **Visualização de Dados:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Regressão Logística, métricas de avaliação)
* **Ambiente de Desenvolvimento:** Google Colab

---

## Fluxo de Desenvolvimento

1. **Definição do Problema e Contextualização:** Alinhamento dos objetivos clínicos e epidemiológicos.
2. **Configuração do Ambiente e Ingestão de Dados:** Carga dos microdados brutos extraídos do SIHSUS.
3. **Análise Exploratória de Dados (EDA):** Identificação de distribuições, correlações e fatores mais relevantes nas internações.
4. **Modelagem Preditiva:** Treinamento do modelo de **Regressão Logística** e divisão entre conjuntos de treino e teste.
5. **Avaliação do Modelo:** Análise de métricas (Acurácia, Precisão, Recall, F1-Score, Curva ROC/AUC).

---

## Principais Resultados e Aprendizados

- AUC-ROC de 0,78 indicando boa capacidade de discriminação entre pacientes de alto e baixo risco de óbito.
- Sensibilidade de ~71% e Especificidade de ~70%, um equilíbrio adequado para um problema de saúde fortemente desbalanceado (apenas 3,7% de óbitos na base).
- A análise de limiares de decisão confirmou que o ponto de corte padrão (0,5) já representa um bom equilíbrio entre "captar óbitos" e "evitar falsos alarmes" para este modelo.
- Principais achados clínicos da EDA:
1. Internações mais longas estão associadas a maior risco de óbito.
2. Coma diabético é a complicação com maior letalidade (~8%), seguida de cetoacidose (~4,5%), ambas acima da média geral de óbitos (3,7%).

---

## Como Executar o Projeto

1. Você pode abrir o notebook diretamente no **Google Colab** clicando no botão disponível no topo do repositório ou no arquivo `.ipynb`.
2. Assegure-se de carregar a base de dados (ou utilizar a amostra fornecida no repositório) para execução completa do pipeline de código.

---

## Origem do Projeto

Este projeto foi desenvolvido como estudo acadêmico aplicado durante a graduação, com o objetivo de consolidar práticas de pré-processamento de dados, análise descritiva e algoritmos supervisionados em problemas reais.
