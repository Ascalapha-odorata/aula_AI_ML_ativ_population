# aula_AI_ML_ativ_population
# Laboratório de Inteligência Artificial: Machine Learning e Random Forest

Este repositório contém um Jupyter Notebook desenvolvido para a disciplina de Inteligência Artificial do curso de Ciência da Computação (PUC-SP). O objetivo principal é introduzir conceitos fundamentais de Machine Learning e aplicar na prática algoritmos baseados em árvores de decisão utilizando a biblioteca `scikit-learn`.

## 🧠 Fundamentos Teóricos Explorados

O notebook consolida a base teórica necessária para o entendimento de modelos preditivos:
* **Conceitos de IA e ML:** Diferenciação clara entre Inteligência Artificial (reprodução de padrões cognitivos humanos) e Machine Learning (sistemas que aprendem via dados sem programação explícita de regras).
* **Decision Tree vs. Random Forest:** Análise crítica detalhando os prós e contras de cada abordagem, contrastando a simplicidade e o risco de *overfitting* das Árvores de Decisão com a robustez, estabilidade e o maior custo computacional da Floresta Aleatória.

## 📊 Aplicação Prática: Dataset Population (Regressão)

A parte prática foca na previsão populacional utilizando dados demográficos históricos (`vega-datasets`). As etapas desenvolvidas no código incluem:

1. **Análise Exploratória e Limpeza (EDA):** Carregamento via `pandas`, verificação de valores nulos e extração de estatísticas descritivas básicas.
2. **Visualização de Dados:** Uso do `matplotlib` para entender a distribuição da população por sexo ao longo das décadas.
3. **Treinamento do Modelo:** Separação dos dados (80/20) e treinamento de um `RandomForestRegressor` (com `n_estimators=100`) usando as *features* `year`, `age` e `sex` para prever a variável alvo `people`.
4. **Avaliação de Métricas:** Validação do desempenho preditivo através do Erro Médio Absoluto (MAE), Raiz do Erro Quadrático Médio (RMSE) e Coeficiente de Determinação ($R^2$).
5. **Interpretação Visual e Importância das Variáveis:** 
   * Geração de um gráfico de dispersão (*Scatter Plot*) comparando os dados reais aos previstos (avaliando o alinhamento em uma diagonal crescente).
   * Extração do `feature_importances_`, revelando que as variáveis `year` (51.92%) e `age` (47.76%) dominam a decisão do modelo, enquanto a variável `sex` (0.32%) tem impacto quase nulo na predição populacional para este recorte.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Bibliotecas:** `pandas` (manipulação), `matplotlib` (gráficos), `scikit-learn` (Machine Learning e métricas), `numpy` (cálculos algébricos).

## 🚀 Como Executar

1. Clone o repositório ou faça o download do arquivo `.ipynb`.
2. Abra o arquivo no Google Colab ou em um ambiente local com Jupyter Notebook.
3. Execute as células sequencialmente. O download do dataset populacional em JSON será feito de forma automática pela URL da CDN via `pandas`.
