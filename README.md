# Dashboard executivo de performance comercial no Power BI

Este projeto é um dashboard executivo criado no Power BI para acompanhar indicadores de clientes, consumo e segmentos de gasto.

A ideia foi transformar uma análise exploratória feita em Python em uma visão mais visual e direta para acompanhamento de negócio.

## Preview

![Preview do dashboard](images/dashboard_preview.png)

## Objetivo

Criar um painel simples para responder perguntas como:

- Quantos clientes existem na base?
- Qual é a renda média dos clientes?
- Qual é o gasto total e o gasto médio por cliente?
- Quais segmentos concentram maior gasto?
- Como os clientes se distribuem por escolaridade e estado civil?
- Quais categorias de produto concentram mais consumo?

## Principais indicadores

- Total de clientes
- Renda média
- Gasto total
- Gasto médio por cliente
- Total de compras
- Compras médias por cliente

## Visuais criados

- Gasto por segmento
- Gasto médio por segmento
- Gasto por escolaridade
- Clientes por estado civil
- Filtros por escolaridade, estado civil e segmento de gasto

## Ferramentas usadas

- Power BI
- Power Query
- DAX
- CSV
- GitHub

## Medidas DAX

DAX
Total Clientes = DISTINCTCOUNT(customers_clean[ID])

Renda Média = AVERAGE(customers_clean[Income])

Gasto Total = SUM(customers_clean[Total_Spent])

Gasto Médio por Cliente = DIVIDE([Gasto Total], [Total Clientes])

Total Compras = SUM(customers_clean[Total_Purchases])

Compras Médias por Cliente = DIVIDE([Total Compras], [Total Clientes])

Idade Média = AVERAGE(customers_clean[Age])

Clientes com Reclamação = SUM(customers_clean[Complain])