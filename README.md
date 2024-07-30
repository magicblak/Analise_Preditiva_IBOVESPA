# Analise_Preditiva_IBOVESPA
## Introdução
Este trabalho visa desenvolver um modelo preditivo para os valores de fechamento da IBOVESPA, com o objetivo de atingir uma acurácia mínima de 70%. 
Esse processo foi dividido em 4 fases, descritas a seguir:

## 1 - Análise Exploratória de Dados (EDA)
O primeiro passo nesse processo foi realizar a análise exploratória de dados (EDA), para conhecer nossa base e obter informações para a seleção e otimização do modelo.
A análise revelou que a base de dados da IBOVESPA é uma série temporal, ou seja, um conjunto de dados coletados em intervalos regulares de tempo (diariamente, nesse caso), ao longo de 10 anos. Essa característica é fundamental para a escolha de modelos preditivos adequados.
Essa análise permitiu identificar padrões sazonais, tendências de longo prazo, a autocorrelação, ou seja, a relação entre os valores da série temporal em diferentes pontos no tempo. 

## 2 - Engenharia de Atributos (Feature Engineering)
Após a análise exploratória, foi realizado um processo de engenharia de atributos, ajustando e transformando os dados para otimizar o desempenho do modelo. 
Novas variáveis, como médias móveis e características dia, mês e ano, foram criadas para capturar informações adicionais e melhorar a capacidade preditiva do modelo.
Transformações logarítmicas foram aplicadas para ajustar a distribuição dos dados e melhorar a performance dos modelos.

## 3 - Modelagem Preditiva
Com base nas características da série temporal e nas informações obtidas durante a EDA, foram selecionados três modelos preditivos comumente utilizados em séries temporais:
- **Seasonal Naive**: Modelo simples que utiliza o valor do período anterior como previsão para o período atual, considerando a sazonalidade dos dados.
- **ARIMA (Autoregressive Integrated Moving Average)**: Modelo estatístico que utiliza autocorrelações passadas e médias móveis para prever valores futuros. A ordem do modelo (p, d, q) foi determinada com base na análise de autocorrelação.
- **Redes Neurais Recorrentes (LSTM)**: Modelo de aprendizado de máquina que utiliza redes neurais para capturar padrões complexos nas séries temporais e realizar previsões.

## 5 - Comparação de Desempenho
Os três modelos preditivos - Seasonal Naive, ARIMA e LSTM - foram treinados e testados utilizando dados históricos da IBOVESPA. A performance dos modelos foi avaliada através de um conjunto abrangente de métricas, buscando o modelo com melhor desempenho e capaz de atingir a meta de 70% de acurácia. As métricas utilizadas foram:
- **Erro Absoluto Médio (MAE)**: Calcula a média do valor absoluto da diferença entre os valores reais e as previsões, fornecendo uma medida da magnitude média do erro.
- **Raiz do Erro Quadrático Médio (RMSE)**: Calcula a média dos quadrados das diferenças entre os valores reais e as previsões, penalizando erros maiores.
- **Erro Simétrico Absoluto Percentual Médio (SMAPE)**: Calcula a média do erro percentual absoluto simétrico, que considera tanto erros de subestimação quanto de superestimação, proporcionando uma medida mais equilibrada do desempenho.
