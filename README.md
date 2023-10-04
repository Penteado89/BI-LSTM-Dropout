# EP01 - MAC5725 – Linguística Computacional – 2023 - BI-LSTM-Dropout

#1. Pré-processamento:

Antes de iniciar, verifique se os dados estão na pasta correta. Você pode configurar o caminho do arquivo no script ou passá-lo como um argumento na linha de comando.

O script de pré-processamento realizará as seguintes etapas:

Filtragem das linhas com base nos rótulos.
Particionamento dos dados em conjuntos de treinamento, validação e teste.
Codificação de palavras em vetores.

#2. Treinamento:

Antes de executar o script de treinamento, verifique os hiperparâmetros, como tammax e batch size. O script de treinamento conduzirá os experimentos para as combinações de redes unidirecionais e bidirecionais, bem como para diferentes taxas de dropout.

Execute o script de treinamento para cada configuração e monitore o erro no conjunto de validação após cada época para detectar sobreajuste.

#3. Validação:

A validação será realizada após cada cinco épocas de treinamento. O script irá gerar gráficos de validação para cada configuração e salvar os parâmetros do modelo.

#4. Teste:

Uma vez concluído o treinamento e validação, o script de teste carregará o modelo treinado com a melhor acurácia de validação e avaliará sua performance no conjunto de teste. O resultado final será a acurácia do modelo no conjunto de teste.

Instruções para execução:

Execute o script de pré-processamento:
css
Copy code
python preprocess.py --data_path=/path/to/data.csv
Execute o script de treinamento:
arduino
Copy code
python train.py --config=config_file_path
Execute o script de teste:
css
Copy code
python test.py --model_path=/path/to/best_model


#Resultados:
BEST MODEL
![model_True_0 25](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/d5a159d8-a54e-4030-a582-39c8485fb515)


os valores de acurária apresentados depois dos seis modelos testados, e finalmente testados no conjunto de teste, s=resultados valores baixos, porém se assemelham as referencias nos melhores benchmarks para essa pratica utilizando lstm biredicioal.
sabe-se que o uso de arquituras mais complexas como x apresentam valores bem significativos com o uso de , como se pode ver nessa tabela,
vale a pena citar o trablho de que testou numa tarreca parecida. etc 
