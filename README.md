# Classificação de Dígitos Manuscritos com CNN e Avaliação de Desempenho

Este repositório contém um script Python que treina uma Rede Neural Convolucional (CNN) para classificar dígitos manuscritos usando o conjunto de dados MNIST e avalia o desempenho do modelo usando várias métricas.

## Descrição

O script `metrics_calculation.py` realiza as seguintes tarefas:

1.  **Carrega o Conjunto de Dados MNIST:** Carrega o conjunto de dados MNIST, que consiste em imagens de dígitos manuscritos (0 a 9).
2.  **Pré-processa os Dados:** Redimensiona e normaliza as imagens para o formato esperado pela CNN.
3.  **Constrói o Modelo CNN:** Cria um modelo CNN sequencial com camadas convolucionais, pooling e densas.
4.  **Treina o Modelo:** Treina o modelo usando o conjunto de dados de treinamento e valida o desempenho com o conjunto de dados de teste.
5.  **Avalia o Modelo:** Calcula e exibe várias métricas de avaliação, incluindo matriz de confusão, sensibilidade, especificidade, acurácia, precisão e F1-score, tanto para cada classe quanto em versões macro e micro.

## Pré-requisitos

* Python 3.x
* TensorFlow (2.x)
* Keras
* NumPy
* Matplotlib
* Pandas

## Você pode instalar as dependências usando o pip:

```bash
pip install tensorflow numpy matplotlib seaborn pandas
Estrutura do Projeto
seu_repositorio/
├── mnist_cnn_evaluation.py
└── log/ (diretório para logs do TensorBoard)
```
## Como Executar
Clone o repositório:

Bash

git clone [https://github.com/Zh0ny/desafio_de_projeto_calculo_de_metricas_de_avaliacao_de_aprendizado.git](https://github.com/Zh0ny/desafio_de_projeto_calculo_de_metricas_de_avaliacao_de_aprendizado.git)
cd desafio_de_projeto_calculo_de_metricas_de_avaliacao_de_aprendizado
Execute o script Python:

```Bash
python metrics_calculation.py
```
O script irá treinar o modelo e exibir as métricas de avaliação no console, além de gerar um heatmap da matriz de confusão.

##Resultados
O script exibirá as seguintes métricas de avaliação:

  -Matriz de Confusão: Visualização do desempenho do modelo para cada classe.
  -Sensibilidade (Recall): Taxa de verdadeiros positivos para cada classe.
  -Especificidade: Taxa de verdadeiros negativos para cada classe.
  -Acurácia: Proporção total de previsões corretas.
  -Precisão: Taxa de previsões positivas corretas para cada classe.
  -F1-Score: Média harmônica de precisão e sensibilidade para cada classe.
  -Métricas Macro: Médias das métricas para todas as classes.
  -Métricas Micro: Métricas calculadas globalmente, considerando todas as classes.
  
##Observações
  -O diretório log/ é usado para os logs do TensorBoard. Você pode visualizar os logs executando tensorboard --logdir log no terminal.
  -O modelo é treinado por 5 épocas. Você pode ajustar esse valor no script.
  -O script calcula as métricas de avaliação usando a matriz de confusão normalizada. Se você precisar das contagens absolutas, precisará ajustar o código.
