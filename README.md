# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

O presente repositório faz parte do desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas". Neste Lab da DIO, tive a oportunidade de aplicar conceitos práticos de Machine Learning (ML) utilizando o SageMaker Canvas para criar previsões de estoque.

## 🎯 Objetivos Deste Desafio de Projeto (Lab)

O objetivo principal do desafio foi utilizar a ferramenta SageMaker Canvas para a criação do modelo preditivo, utilizando séries temporais para a realização do treinamento de máquina.

## 🚀 Passo a Passo

### 1. Seleção do Dataset

Escolhi como dataset o terceiro arquivo do repositório para realização do treinamento

### 2. Construção/Treinamento

Após a importação do dataset escolhido, configurei as variáveis de entrada e saída de acordo com os dados e iniciei o treinamento do modelo (via Quick build).

### 3. Análise

Após o treinamento, obtive as seguintes métricas de performance do modelo e suas respectivas implicações realcionadas aos estoques:
  
-   Avg. wQL - 0.086 (Métrica de perda ou custo ponderado da quantile =  Modelo ajustou bem os quantiles de previsão, crucial para definir bem o estoque de segurança.)
-   MAPE - 0.290 (Erro Percentual Absoluto Médio = Embora 29% pareça alto em alguns contextos, para séries temporais e previsão de demanda, onde a volatilidade é grande, este é geralmente um valor considerado aceitável.)
-   WAPE - 0.152 (Erro Absoluto Ponderado = Significa que, no geral, o erro absoluto do modelo representa apenas 15,2% do volume total previsto, indicando alta fidelidade nas previsões agregadas. É considerado um valor excelente.)
-   RMSE - 1.535 (Raiz do Erro Quadrático Médio = A função é penalizar erros grandes no estoque. Para modelos com estoque médio elevado, por exemplo, acima de 500 unidades, o erro de 1.5 unidades para mais ou para menos é considerado insignificante. Por outro lado, se o estoque médio for baixo, ainda assim é considerado um número controlável.)
-   MASE - 0.180 (Erro Absoluto Escalonado Médio = Ao comparar o erro do modelo com um baseline simples, o valor de 0.18 é excepcional, indicando que o erro é 82% menor que o modelo baseline.)

### 4. Previsão

O modelo em questão performa bem e é confiável para auxiliar na tomada de decisões de reabastecimento e gestão de buffer de segurança. O desempenho permite a transição de uma gestão de estoque reacional para uma preditiva e otimizada. Além disso, apresenta como vantagens:

-   Redução do custo total de erro: pode ser utilizado para reduzir o excesso e, ao mesmo tempo, minimizar a falta de estoque, levando a uma melhor saúde financeira da cadeia de suprimentos.
-   Confiança na margem de erro: oferece alta confiança na definição dos níveis de reabastecimento e permite que definir o estoque de segurança (buffer) de forma mais enxuta, liberando capital de giro.
-   Vantagem competitiva: O método de previsão é estatisticamente muito superior às abordagens baseadas em regras simples ou médias históricas, tornando um diferencial competitivo no planejamento e garantindo que as decisões de compra sejam baseadas em uma estimativa de demanda de alta qualidade.

Em resumo, o modelo testado é um ativo valioso que pode ser implantado para automatizar as decisões de reabastecimento e otimizar o capital alocado nos estoques.


