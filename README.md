# Atividade: Normalização, escalonamento e codificação de dados categóricos

Atividade da disciplina de **Ciência de Dados** (Bacharelado em Engenharia de Software, UNIFSA).

## Sobre

Análise da base **Telco Customer Churn** (IBM), com 7.043 clientes de uma operadora de telecomunicações. O trabalho tem dois objetivos:

1. Construir um **índice de valor do cliente**, combinando tempo de relacionamento e faturamento.
2. Analisar o **cancelamento (churn)** e identificar quais características dos clientes estão associadas a ele.

## O que foi feito

- **Preparação dos dados:** conversão de `TotalCharges` para numérico e tratamento dos registros vazios (clientes com `tenure = 0`).
- **Escalonamento:** índice bruto, padronizado (z-score) e min-max, com comparação entre eles e versão final do índice sem redundância.
- **Forma da distribuição:** histogramas, assimetria e teste da transformação `log1p`.
- **Codificação de variáveis categóricas:** binárias (0 e 1), ordinal (`Contract`) e one-hot (`InternetService` e `PaymentMethod`).
- **Análise de cancelamento:** taxa por grupo, correlação com `Churn` e recomendação para a diretoria comercial.
- **Questões discursivas** sobre codificação e escalonamento.

## Principais resultados

- Contrato mensal tem 42,7% de cancelamento, contra 11,3% (um ano) e 2,8% (dois anos).
- Cheque eletrônico (45,3%) e fibra ótica (41,9%) são os grupos com maior cancelamento.
- As variáveis mais correlacionadas com `Churn` são `Contract` (-0,40), `tenure` (-0,35), `InternetService_Fiber optic` (0,31), `PaymentMethod_Electronic check` (0,30) e `InternetService_No` (-0,23).

## Como executar

1. Abra o notebook `U3_atividade_telecom.ipynb` no [Google Colab](https://colab.research.google.com/).
2. Execute as células **em ordem, do início ao fim**. A base é carregada direto de um link público, sem precisar baixar nada.

> Atenção: algumas células (conversões com `.map` e o one-hot) só funcionam na primeira execução. Para rodar de novo, reinicie a sessão e execute tudo desde o começo.

## Tecnologias

Python, Pandas, NumPy e Matplotlib.

## Autora

Pamella Roberta dos Santos Silva
