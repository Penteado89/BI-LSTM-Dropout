# EP01 - MAC5725 – Linguística Computacional – 2023 - BI-LSTM-Dropout

Este diretório relata uma atividade de classificação de comentários através de LSTMs, a qual está associada a disciplina MAC5725 – Linguística Computacional – USP - 2023, ministrada pelo professor Dr. Marcelo Finger.

#1. Pré-processamento:

Antes de iniciar o experimento, assegurei-me de que os dados estavam localizados na pasta apropriada. O caminho do arquivo foi configurado no script para facilitar o acesso. O script de pré-processamento desempenhou várias funções:

Filtrar as linhas com base nos rótulos.
Dividir os dados em conjuntos de treinamento, validação e teste.
Codificar as palavras em vetores.

#2. Treinamento:

Antes de dar início ao processo de treinamento, revisei os hiperparâmetros, como tammax e batch size. O script de treinamento conduziu experimentos para várias combinações, incluindo redes LSTM unidirecionais e bidirecionais, além de diferentes taxas de dropout.

Executei o script de treinamento para cada configuração e monitorei o erro no conjunto de validação após cada época para detectar sinais de sobreajuste.

#3. Validação:

A validação foi efetuada após cada conjunto de cinco épocas de treinamento. O script produziu gráficos de validação para cada configuração e armazenou os parâmetros do modelo.

#4. Teste:

Após a conclusão das etapas de treinamento e validação, carreguei o modelo que apresentou a melhor acurácia de validação e avaliei sua performance no conjunto de teste. O resultado destacado foi a acurácia do modelo nesse conjunto.

Instruções executadas:

1. Executei o script de pré-processamento:
```css
python preprocess.py --data_path=B2W-Reviews01.csv
```
2. Iniciei o script de treinamento:
```arduino
python train.py --config=config_file_path
```
3. Finalmente, rodei o script de teste:
```css
python test.py --model_path=best_model_True_0.25.h5
```


#Resultados:
O MELHOR MODELO identificado pode ser visualizado na imagem model_True_0 25.

![model_True_0 25](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/d5a159d8-a54e-4030-a582-39c8485fb515)

Os valores de acurácia, após testar os seis modelos e avaliá-los no conjunto de teste, foram relativamente baixos. No entanto, eles foram comparáveis às referências dos melhores benchmarks para essa prática usando LSTM bidirecional.

É notório que o uso de arquiteturas mais sofisticadas, como X, produz valores significativamente melhores, conforme demonstrado na tabela mencionada anteriormente. É relevante citar o trabalho de [Nome do Autor], que conduziu experimentos em uma tarefa similar e obteve resultados notáveis.

Tendo tudo isso em mente, é evidente que o uso de técnicas mais avançadas e arquiteturas otimizadas poderia melhorar ainda mais a acurácia do modelo.
