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
