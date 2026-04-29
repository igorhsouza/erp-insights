# ERP Intelligence Bot

Automação desenvolvida em n8n para geração e distribuição de relatórios comerciais diários a partir de dados do ERP, com envio automatizado via Telegram e e-mail.

## Arquitetura do Workflow

<img width="1117" height="353" alt="workflow" src="https://github.com/user-attachments/assets/4e3d8c3c-7d14-4ed2-bed7-3256f9519b1a" />

## Resultados Diários
<img width="290" height="407" alt="exm 1" src="https://github.com/user-attachments/assets/4777b432-0f99-439e-83cd-7a8389e32ade" />   

## Resultados Diários
<img width="252" height="343" alt="exm 2" src="https://github.com/user-attachments/assets/c004011e-96af-4ca2-b796-df9bcc10abe3" />  

## Resultados Diários
<img width="220" height="209" alt="exm 3" src="https://github.com/user-attachments/assets/44b3a346-9bf8-45a6-b3a1-06888fc484ba" />

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
