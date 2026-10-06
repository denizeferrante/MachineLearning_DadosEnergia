# Aplicações de Machine Learning para dados de energia
Este repositório será utilizado para o desenvolvimento da atividade da matéria Soluções em Energias Renováveis, composto por quatro partes relacionadas à aplicação de técnicas de Machine Learning em dados de estabilidade de redes elétricas.

As atividades utilizarão como referência o conjunto de dados Electrical Grid Stability Simulated Data, disponibilizado pela UCI Machine Learning Repository.

Fonte dos dados: Electrical Grid Stability Simulated Data – UCI

Organização do Checkpoint
O Checkpoint será distribuído em quatro partes:

## Parte 1 – Classificação (Aula 06)
Desenvolvimento de um modelo de classificação utilizando Regressão Logística para prever a condição da rede elétrica.

variável target: stabf;
classes previstas: estável ou instável;
separação dos dados em treino e teste;
treinamento do modelo;
geração das previsões;
avaliação dos resultados por meio de métricas de classificação e matriz de confusão.
O notebook da aula anterior poderá ser utilizado como referência para o desenvolvimento desta parte.

## Parte 2 – Regressão (Aula 07)
Desenvolvimento de modelos de Regressão Linear para prever o valor numérico da variável stab.

Nesta etapa, deverão ser treinados e comparados dois modelos:

modelo utilizando as cinco variáveis com maior correlação absoluta com stab;
modelo utilizando todas as variáveis cujos nomes começam com tau ou g.
Os modelos deverão ser avaliados comparativamente por meio das métricas:

R²;
MAE;
MSE.
A análise deverá considerar os resultados dos dois modelos, identificando o efeito da seleção das variáveis sobre o desempenho das previsões.

## Parte 3 – Clustering
Aplicação de uma técnica de aprendizado não supervisionado para identificar agrupamentos entre os registros do dataset.

Nesta parte, serão realizadas a preparação das variáveis, a criação dos grupos e a análise das características observadas em cada agrupamento.

As orientações específicas e os critérios para interpretação dos clusters serão apresentados no respectivo roteiro da atividade.

## Parte 4 – Desafio final e apresentação
Desenvolvimento de um desafio final que reunirá os conhecimentos trabalhados nas etapas anteriores.

O grupo deverá analisar os resultados obtidos, justificar as decisões tomadas durante o desenvolvimento e preparar uma apresentação do trabalho.

As orientações do desafio final, os itens obrigatórios e o formato da apresentação serão divulgados na etapa correspondente.

## Integrantes

| Nome completo | RM |
|---|---|
| _preencher_ | _preencher_ |

## Estrutura do repositório

```text
MachineLearning_DadosEnergia/
├── README.md
├── dados/
│   └── Data_for_UCI_named.csv
├── parte_1_classificacao/
│   └── classificacao__estabilidade.ipynb   # Regressão Logística (target: stabf)
├── parte_2_regressao/
│   └── regressao_estabilidade.ipynb        # Regressão Linear (target: stab)
├── parte_3_clustering/
│   ├── clustering_energia.ipynb            # K-Means (Python)
│   ├── consumidores_energia_proposto.csv   # base de entrada
│   ├── README.md                           # escolha de k, perfis e ações
│   ├── imagens/                            # gráficos do Python
│   └── orange/                             # fluxo .ows, CSV com clusters e prints do Orange
└── parte_4_desafio_final/                  # a divulgar
```

## Resultados

| Parte | Modelo | Resultado principal |
|---|---|---|
| 1 – Classificação | Regressão Logística (12 features) | Acurácia 81,70% |
| 2 – Regressão | Modelo 1: 5 maiores correlações (g3, g2, tau2, g1, tau3) | R² 0,4018 · MAE 0,0233 · MSE 0,000811 |
| 2 – Regressão | Modelo 2: todas as variáveis tau e g | R² 0,6452 · MAE 0,0176 · MSE 0,000481 |
| 3 – Clustering | K-Means, k = 4 (consumo, demanda, % noturno) | Silhouette 0,667 · 4 perfis de 15 consumidores |
