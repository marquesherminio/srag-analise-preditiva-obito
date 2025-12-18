# 📊 Dados do Projeto – SRAG

Devido ao grande volume dos arquivos da base SRAG, **os dados não são versionados neste repositório**.

## 📌 Fonte dos Dados
Os dados utilizados neste projeto são públicos e disponibilizados pelo Ministério da Saúde:

- OpenDataSUS – SRAG  
- https://opendatasus.saude.gov.br

## 🗂️ Arquivos Utilizados
Foram utilizados arquivos anuais no formato **Parquet**, correspondentes aos anos:

- INFLUD19.parquet  
- INFLUD20.parquet  
- INFLUD21.parquet  
- INFLUD22.parquet  
- INFLUD23.parquet  
- INFLUD24.parquet  

## 📥 Como obter os dados
Os arquivos podem ser obtidos de duas formas:

### Opção 1 — Download manual
1. Acesse o portal OpenDataSUS
2. Baixe os arquivos SRAG dos anos desejados
3. Coloque os arquivos na pasta `dados/`

### Opção 2 — Download automatizado (Recomendado)
O notebook do projeto realiza o download automático dos arquivos via Google Drive público, utilizando a biblioteca `gdown`.

Basta executar as primeiras células do notebook para obter os dados automaticamente.
