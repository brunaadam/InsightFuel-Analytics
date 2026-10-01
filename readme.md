# InsightFuel Analytics

Projeto desenvolvido como parte de um trabalho da **Pós-Graduação em Engenharia e Ciência de Dados**.

## Sobre o projeto

O **InsightFuel Analytics** é uma proposta de plataforma de análise territorial e estratégica voltada ao mercado de combustíveis.

O projeto utiliza dados históricos de preços de combustíveis da **ANP**, enriquecidos com informações socioeconômicas do **IBGE**, com o objetivo de organizar, integrar e analisar os dados para identificar padrões e relações entre preços de combustíveis e características dos municípios.

O período analisado compreende os anos de **2021 a 2023**.

## Bases de dados utilizadas

### ANP – Série Histórica de Preços de Combustíveis

Base principal do projeto, contendo informações sobre:

- UF;
- Município;
- Produto;
- Data/período;
- Preços de combustíveis.

### IBGE – Censo Demográfico 2022

Utilizada para enriquecimento dos dados municipais, principalmente com:

- Código IBGE;
- UF;
- Município;
- População.

### IBGE – PIB dos Municípios

Utilizada para adicionar informações econômicas aos municípios:

- Código IBGE;
- Município;
- Ano;
- PIB;
- PIB per capita.

## Tecnologias utilizadas

- **Python** – tratamento, transformação e análise dos dados;
- **Pandas** – manipulação dos dados;
- **DuckDB** – armazenamento e consultas analíticas;
- **Jupyter Notebook** – desenvolvimento e execução do pipeline;
- **Excel/CSV** – formatos das bases de dados de origem.

## Pipeline de dados

O projeto utiliza uma arquitetura baseada em camadas:

```text
Dados de origem
      │
      ▼
┌──────────────┐
│    BRONZE    │
│ Dados brutos │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│    SILVER    │
│ Limpeza e    │
│ transformação│
└──────┬───────┘
       │
       ▼
┌──────────────┐
│     GOLD     │
│ Dados        │
│ integrados e │
│ analíticos   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Visualização │
│ e análises   │
└──────────────┘