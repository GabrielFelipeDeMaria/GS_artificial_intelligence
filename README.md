# GS de Inteligência Artificial

*Autores:* 
- Gabriel Felipe De Maria
- Caio Manoel Bezerra de Araujo
- Lucas Ferraz Martins

# Descrição do Problema

Com o aumento do uso de veículos elétricos, a demanda por energia em estações de carregamento está crescendo rapidamente. Gerenciar eficientemente essa demanda é essencial para evitar sobrecargas no sistema elétrico e reduzir custos operacionais. Este projeto tem como objetivo prever a demanda futura (kWh) de energia em estações de carregamento usando dados históricos e técnicas de Machine Learning.

# Metodologia

<h4> Dados Utilizados </h4>

O dataset foi obtido de um arquivo CSV fornecido, contendo informações detalhadas sobre sessões de carregamento, incluindo:

kwhTotal: Total de energia consumida (kWh) por sessão.
dollars: Custo em dólares de cada sessão.
chargeTimeHrs: Tempo total de carregamento (horas).
weekday: Dia da semana da sessão.
Outras colunas: Informações complementares, como IDs de estação e usuário.

<h4> Pré-Processamento </h4>

Criação da Variável Alvo:

Foi criada a coluna future_demand, que representa a demanda de energia da próxima sessão, utilizando o método "shift(-1)".

Tratamento de Dados:
Remoção de valores nulos gerados pelo método shift.
Seleção de colunas numéricas para uso no modelo.

<h4> Divisão dos Dados </h4>

Os dados foram divididos em:

Conjunto de Treinamento: 80% dos dados.
Conjunto de Teste: 20% dos dados.

# Modelagem

<h4> Algoritmo Utilizado </h4>

Random Forest Regressor: Um modelo de aprendizado de máquina baseado em árvores de decisão, adequado para prever valores contínuos.

<h4> Métricas de Avaliação </h4>

Foram utilizadas as seguintes métricas para avaliar o modelo:

Erro Quadrático Médio (MSE): Mede a magnitude média dos erros quadráticos.
Erro Absoluto Médio (MAE): Mede a magnitude média dos erros absolutos.

# Resultados

<h4> Desempenho do Modelo </h4>

Após o treinamento e a avaliação, os resultados foram os seguintes:

Erro Quadrático Médio (MSE): 2.8943553169313305
Erro Absoluto Médio (MAE): 1.1967834763948497

<h4> Visualização </h4>

Gráfico de comparação entre valores reais e previstos (necessário incluir ao executar o código).

# Conclusão

O sistema desenvolvido demonstrou ser capaz de prever a demanda de energia de sessões futuras com uma precisão aceitável, considerando os dados disponíveis. As principais conclusões incluem:

A coluna kwhTotal foi adequada para prever a demanda futura.
O modelo Random Forest apresentou resultados sólidos, com baixos erros.

<h4> Melhorias Futuras </h4>

Expansão de Dados: Incluir dados climáticos e padrões de tráfego.
Modelos Alternativos: Experimentar Redes Neurais (LSTM) para capturar relações temporais complexas.
Integração com Visão Computacional: Usar câmeras para monitorar ocupação de estações.

# Referências

Dataset utilizado: [Electric Vehicle Charging Dataset](https://www.kaggle.com/datasets/michaelbryantds/electric-vehicle-charging-dataset?select=station_data_dataverse.csv)
