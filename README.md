# BOT - Análise Geral da Loja - Telegram

Automação desenvolvida em n8n para gerar e enviar relatórios comerciais diários do Mercado Taismani via Telegram e e-mail.

## Objetivo

Centralizar indicadores operacionais e comerciais do ERP em relatórios automáticos, reduzindo análise manual e acelerando a tomada de decisão da gestão.

## Funcionamento

O workflow executa diariamente, consulta endpoints internos da API do ERP e envia resumos para o Telegram, além de gerar relatório HTML por e-mail.

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
