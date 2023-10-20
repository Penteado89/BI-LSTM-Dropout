# MAC5725 – Linguística Computacional – 2023 - EP 1: RNNs Bidirecionais, Overfitting, Underfitting

*Pré-requisitos*

Google Colab: A execução deste projeto requer o uso do Google Colab. Certifique-se de ter uma conta Google para acessar esta ferramenta.

Google Drive: Este projeto requer o uso do Google Drive para armazenar e acessar os dados e os embeddings necessários. Certifique-se de ter espaço suficiente disponível no seu Drive.

*Preparação dos Dados*

Upload dos Arquivos: Faça o upload dos seguintes arquivos para a pasta content/ no seu Google Drive montado no Google Colab:

B2W-Reviews01.csv

requirements.txt

preprocessing.py

*Download e Upload do Embedding:*

Faça o download do arquivo de embeddings a partir do seguinte link: glove_s300.zip
Após o download, faça o upload do arquivo glove_s300.zip para a pasta content/ no seu Google Drive montado no Google Colab.

*Pré-processamento de Dados*

Carregamento e Visualização dos Dados Brutos: Carregamento do dataset e visualização inicial para entender a estrutura e os dados contidos no dataset.

Remoção de Colunas Desnecessárias: Manter apenas as colunas 'review_text' e 'overall_rating', e remover as demais.

Tratamento de Valores Ausentes: Eliminar as linhas que possuem valores ausentes nas colunas 'review_text' ou 'overall_rating'.

Divisão do Dataset: Dividir o dataset em conjuntos de treinamento, validação e teste.


*Modelo*

Objetivo Principal:
Prever a 'overall_rating' com base no conteúdo de 'review_text'.


*Arquiteturas LSTM Implementadas:*
LSTM Unidirecional: Implementação de uma arquitetura LSTM unidirecional.
LSTM Bidirecional: Implementação de uma arquitetura LSTM bidirecional.

Para ambas as arquiteturas, foram implementadas variações com diferentes taxas de dropout (0.0, 0.25, 0.5) para prevenir o overfitting.

*Instalação das Dependências*

Abra o notebook EP01_MAC5725_–_Linguística_Computacional_–_2023.ipynb no Google Colab.
Execute a célula que contém o comando !pip install -r requirements.txt para instalar todas as dependências necessárias.


*Execução do Projeto*
Pré-processamento:

Execute a célula correspondente no notebook para realizar o pré-processamento dos dados.

Treinamento:

Execute as células correspondentes para treinar o modelo com os dados pré-processados.

Teste:

Finalmente, execute as células de teste para avaliar o desempenho do modelo.


Informações Adicionais
Os embeddings foram obtidos do NILC (Núcleo Interinstitucional de Linguística Computacional).
Os dados utilizados neste projeto são avaliações de produtos da B2W.

Autor: Ricardo Cabral Penteado
NUSP: 13813331
