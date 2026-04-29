# ERP Intelligence Bot

Automação desenvolvida em n8n para geração e distribuição de relatórios comerciais diários a partir de dados do ERP, com envio automatizado via Telegram e e-mail.


<img width="1117" height="353" alt="ChatGPT Image 28 de abr  de 2026, 16_42_31" src="https://github.com/user-attachments/assets/963f4c71-603f-4722-83d3-d8d783522994" />


## Objetivo

Transformar dados brutos do ERP em insights acionáveis, reduzindo análise manual e permitindo decisões mais rápidas e assertivas na operação do varejo.

## Impacto

- Redução de ~20 horas/mês de análise manual
- Entrega diária automatizada de indicadores comerciais
- Identificação contínua de prejuízos, margens baixas e oportunidades
- Padronização da informação para a gestão

## Funcionamento

O workflow executa diariamente, consulta endpoints da API do ERP, processa os dados e distribui relatórios estruturados.

Fluxo principal:

```text
Schedule Trigger
→ HTTP Request /resumo-completo
→ Code - Montar Mensagem
→ Telegram - Enviar Resumo
→ HTTP Request /analise-comercial
→ Code - Análise Comercial
→ Telegram - Enviar Resumo
→ HTTP Request /analise-abc
→ Code - Curva ABC
→ LLM - Resumo Executivo
→ Code - Relatório HTML
→ Gmail - Envio por e-mail
→ Telegram - Confirmação
