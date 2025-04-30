# Análise de Dados de Filmes - The Movies Dataset

Este projeto tem como objetivo explorar e transformar os dados do [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset), disponível no Kaggle, com foco na preparação e limpeza dos dados para futuras análises e visualizações.

## Objetivo

O principal objetivo inicial deste projeto é realizar a **limpeza e transformação** de colunas que estão no formato JSON (armazenadas como string) para estruturas mais apropriadas, como tabelas normalizadas. Com isso, é possível facilitar análises posteriores, como:

- Gêneros mais comuns em filmes;
- Relação entre nota média e orçamento;
- Evolução da produção cinematográfica ao longo dos anos;
- Possíveis sistemas de recomendação no futuro.

## Fonte dos Dados

- **Dataset:** [The Movies Dataset - Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)
- Arquivos utilizados:
  - `movies_metadata.csv`

## Principais Etapas Realizadas

1. **Carregamento dos dados com Pandas**
   - Tratamento de avisos de tipo (`DtypeWarning`)
   - Conversão de colunas problemáticas para string ou uso de `low_memory=False`

2. **Limpeza de dados**
   - Remoção de valores inválidos e nulos

3. **Transformação de colunas JSON-like**
   - Colunas como `genres`, `production_companies`, `spoken_languages`, entre outras, estavam armazenadas como listas de dicionários em formato texto
   - Utilização de `ast.literal_eval` para converter para estruturas Python reais
   - Criação de colunas intermediárias e tabelas auxiliares (por exemplo, `genres`, `movies_genres`) para normalização

4. **Preparação para análises futuras**
   - Dataset pronto para ser utilizado em dashboards, visualizações e modelos preditivos

## Ferramentas Utilizadas

- **Python**
- **Pandas**
- **Jupyter Notebook**


## Como Reproduzir

1. Clone este repositório:
   ```bash
   git clone https://github.com/ivitor0/movies-dataset.git
   cd seu-repositorio
