# ponderada-transformers
Repositório para a ponderada sobre transformers

O arquivo Hiperparametros_modificados_de_Ponderada_Transformers.ipynb possui os seguintes hiperparâmetros modificados em relação ao tutorial do Tensorflow:

- **num_layers = 4**  
  *Aumento no número de camadas para capturar representações mais complexas na codificação e decodificação.*

- **d_model = 256**  
  *Aumento na dimensionalidade dos embeddings e das saídas das camadas para fornecer uma representação mais rica dos dados.*

- **dff = 1024**  
  *Aumento da dimensionalidade da camada de feed-forward, melhorando a capacidade do modelo de aprender relações não-lineares.*

- **num_heads = 8**  
  *Mantém-se o número de cabeças de atenção, garantindo que `d_model` seja divisível por `num_heads`.*

- **dropout_rate = 0.2**  
  *Aumento da taxa de dropout para reduzir o overfitting e melhorar a generalização do modelo.*

- **warmup_steps = 5000**  
  *Aumento dos passos de warmup na estratégia de ajuste da taxa de aprendizagem para uma transição mais suave no início do treinamento.*

# Pontos Positivos
Representação Mais Rica:
Aumentar a dimensionalidade dos embeddings (d_model) e das camadas feed-forward (dff) permitiu que o modelo capturasse relações mais complexas e nuances semânticas nos dados, levando a uma melhor qualidade das traduções ou previsões.

Profundidade Adicional:
Um maior número de camadas (num_layers) ajudou o modelo a aprender representações hierárquicas, melhorando a capacidade de entender contextos mais longos e variados.

Regularização com Dropout:
Aumentar a taxa de dropout reduziu o risco de overfitting e ajudou na generalização do modelo.

Estratégia de Warmup Refinada:
Ajustar os passos de warmup no scheduler de taxa de aprendizagem estabilizou o início do treinamento, permitindo uma convergência mais suave e eficaz.

# Pontos Negativos
Custo Computacional e de Memória:
Aumentar d_model, dff e o número de camadas também aumentou significativamente o custo computacional e o uso de memória. Isso levou a tempos de treinamento mais longos e exigiu mais da GPU.

Risco de Overfitting:
Modelos muito complexos podem aprender ruídos específicos do conjunto de treinamento. Mesmo com dropout, é necessário um cuidado extra, principalmente se o dataset não for muito grande.

Dificuldade na Otimização:
Hiperparâmetros mais altos podem tornar a convergência do modelo mais difícil, exigindo ajustes finos na taxa de aprendizagem e outras configurações de otimização.

Complexidade na Experimentação:
Alterações nesses hiperparâmetros exigiu experimentação cuidadosa, pois pequenas mudanças tiveram impactos significativos e encontrar o equilíbrio ideal demanda bastante tempo e recursos.
