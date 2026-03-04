# 🤖 Projeto TelecomX 2: Previsão de Evasão de Clientes com Machine Learning
**Analista Responsável:** Tânia Mara F. de Andrade  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/taniamara13) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/taniamara13)

---

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-blue?style=for-the-badge&logo=python&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)

## 📌 1. Visão Geral e Objetivo

Este projeto é a continuação do **Desafio Parte 2 do Programa ONE (Oracle Next Education)**.

Com os padrões de evasão identificados na Fase 1, a **Telecom X** avança para a etapa de inteligência preditiva. O objetivo é desenvolver um pipeline de Machine Learning capaz de classificar clientes em risco de cancelamento, permitindo ações proativas de retenção antes que a evasão aconteça.

## 🛠️ 2. Pipeline de Machine Learning

O projeto seguiu as etapas clássicas de um pipeline de ML:

1. **Preparação dos Dados:** Remoção de identificadores, análise de variância zero, multicolinearidade (VIF), relevância de variáveis categóricas (Qui-quadrado) e remoção de colunas redundantes.
2. **Pré-processamento:** Encoding com OneHotEncoder, verificação de desbalanceamento de classes e normalização com StandardScaler.
3. **Seleção de Variáveis:** Análise de correlação com o target e análises direcionadas por tipo de variável (contínuas, categóricas e binárias).
4. **Modelagem:** Treinamento e comparação de três algoritmos — Regressão Logística, Árvore de Decisão e Random Forest.
5. **Avaliação:** Métricas de Acurácia, Precisão, Recall e F1-Score com matrizes de confusão e análise de overfitting.
6. **Refinamento:** Poda da Árvore de Decisão para correção de overfitting, com reavaliação comparativa dos 4 modelos.
7. **Interpretação:** Análise de importância das variáveis por modelo e conclusão estratégica.

## 🏆 3. Modelo Selecionado e Resultados

A **Regressão Logística** foi selecionada como modelo final por apresentar o melhor desempenho para o problema:

- ✅ **Melhor Recall** — detecta a maior proporção de clientes que realmente cancelam
- ✅ **Melhor F1-Score** — melhor equilíbrio entre Precisão e Recall
- ✅ **Sem overfitting** — diferença mínima entre treino e teste

| Métrica | Resultado |
|---|---|
| Recall (cancela) | 0.79 |
| F1-Score (cancela) | 0.62 |
| Diferença treino/teste | < 1% |

## 🔍 4. Principais Fatores de Evasão

Com base nos coeficientes da Regressão Logística:

**Aumentam o risco de cancelamento:**
- 📡 **Fibra Óptica** — maior propensão à insatisfação com custo-benefício
- 📋 **Contrato Mensal** — flexibilidade facilita o cancelamento
- 💸 **Cobrança Total elevada** — clientes reavaliando o serviço com frequência

**Reduzem o risco de cancelamento:**
- 📅 **Tempo de Contrato (Meses)** — clientes antigos são significativamente mais leais
- 📝 **Contrato de 2 Anos** — vínculo longo reduz fortemente a evasão
- 🛡️ **Suporte Técnico e Segurança Online** — serviços que geram valor percebido e fidelização

## 💡 5. Estratégias de Retenção Recomendadas

- **Migração para contratos longos:** Oferecer descontos e benefícios para clientes que saírem do plano mensal.
- **Investigação da Fibra Óptica:** Pesquisa de satisfação direcionada para identificar problemas de qualidade ou precificação.
- **Ampliar Suporte Técnico e Segurança Online:** Incluí-los em pacotes base aumenta retenção, especialmente nos primeiros meses.
- **Programa de fidelidade para clientes novos:** Os primeiros 12 meses são a janela crítica de risco.
- **Scoring mensal de risco:** Aplicar o modelo mensalmente para priorizar ações proativas da equipe de retenção.

## 🚀 6. Como Executar
```bash
https://github.com/taniamara13/Telecom-X-2---Predi-o-de-Churn.git
```

1. Abra o notebook `Telecom_X_2_Tania.ipynb` no Google Colab ou Jupyter
2. Execute as células em ordem — os dados são carregados automaticamente via GitHub
3. Nenhuma instalação adicional é necessária além das bibliotecas padrão do Colab

## 📦 7. Bibliotecas Utilizadas

| Biblioteca | Uso |
|---|---|
| `pandas` | Manipulação e análise de dados |
| `numpy` | Operações numéricas |
| `matplotlib` / `seaborn` | Visualizações |
| `scikit-learn` | Pré-processamento, modelagem e avaliação |
| `statsmodels` | Cálculo de VIF para multicolinearidade |
