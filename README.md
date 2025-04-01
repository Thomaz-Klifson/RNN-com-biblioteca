# Rede Neural Recorrente (RNN) para prever o preço de fechamento do Bitcoin.

Os dados utilizados são provenientes de arquivos CSV contendo séries temporais dos preços de fechamento da criptomoeda. O código segue um fluxo estruturado que envolve carregamento e processamento dos dados, definição do modelo de RNN, treinamento e avaliação.

Inicialmente, os dados são carregados utilizando a biblioteca pandas e são normalizados para melhorar a eficiência do treinamento. A normalização é realizada subtraindo a média e dividindo pelo desvio padrão dos dados de treino. Em seguida, os dados são transformados em sequências para que o modelo possa aprender padrões temporais, onde cada entrada contém um conjunto de cinco valores consecutivos usados para prever o próximo valor da sequência.

O modelo de RNN é definido utilizando o PyTorch. Ele possui uma camada recorrente seguida por uma camada linear para transformar a saída da RNN na previsão desejada. Durante o treinamento, o modelo é otimizado utilizando o algoritmo Adam e a função de erro MSELoss para minimizar a diferença entre os valores reais e preditos.

Após o treinamento, o modelo é avaliado utilizando os dados de teste. A normalização é revertida para trazer os valores previstos de volta à escala original, permitindo uma melhor interpretação dos resultados. Finalmente, os preços reais e preditos são visualizados por meio de um gráfico utilizando a biblioteca Matplotlib, facilitando a análise da performance do modelo na previsão dos preços de fechamento do Bitcoin.
