# Projeto de Análise de Documentos Anti-fraude com AzureAI

Este projeto consiste em um programa que analisa cartões de crédito usando AzureAI.

## Etapas De Execução:

1. Recebe arquivos de imagem (png, jpg, jpeg)
2. Os arquivos são enviados para um armazenamento blob da Microsoft Azure onde serão acessados de forma anonima.
3. O serviço da Azure de analise de documentos vai ser chamado para processar a imagem enviada.
4. Caso a imagem contenha os dados: Nome do Titular, Numero do cartão, Data e Banco emissor, o cartão é considerado válido e retornando as informações do mesmo.

## Como Executar o Projeto
1. Navegue até o diretório do projeto:
   ```bash
   cd src
   ```
2. Instale as dependecias do projeto:
   ```bash
   pip install -r requirements.txt
   ```

4. Para executar o programa no windows, abra o terminal e execute o script:
   ```bash
   streamlit run .\app.py
   ```

5. A interface web será aberta no navegador onde você poderá enviar o arquivo de imagem do cartão e receber um retorno das informações do cartão.


### OBS: 
- É necessário instalar as dependecias para execução correta código.
- Precisa ter as chaves de acesso da Azure corretamente configuradas em um arquivo```.env``` na raiz ```SRC``` para execução do código.
  ```
   ENDPOINT = "https://XXXX.cognitiveservices.azure.com/"
   SUBSCRIPTION_KEY = "KEY"
   AZURE_STORAGE_CONNECTION_STRING = "blob conection"
   CONTAINER_NAME = "cartoes"
  ```
