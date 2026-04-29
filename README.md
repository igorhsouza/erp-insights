<h1 align="center">⚡ ERP Intelligence Bot ⚡</h1>

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&pause=1000&color=8A2BE2&center=true&vCenter=true&width=700&lines=ERP+Data+Automation;Commercial+Intelligence+System;Daily+Business+Insights;Built+with+n8n+%2B+LLMs" />
</p>

<p align="center">
<img src="https://img.shields.io/badge/n8n-Automation-111111?style=for-the-badge"/>
<img src="https://img.shields.io/badge/ERP-Data-8A2BE2?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Telegram-Delivery-111111?style=for-the-badge"/>
<img src="https://img.shields.io/badge/AI-Insights-8A2BE2?style=for-the-badge"/>
</p>

---

## Overview

Sistema de automação para geração e distribuição de relatórios comerciais diários a partir de dados do ERP.

O foco é transformar dados brutos em informação útil para tomada de decisão.

---

## Impact

- redução de ~20h/mês de análise manual  
- entrega diária automatizada de indicadores  
- identificação contínua de prejuízos e oportunidades  
- padronização da informação para gestão  

---

## Architecture

<p align="center">
<img width="1117" height="353" src="https://github.com/user-attachments/assets/4e3d8c3c-7d14-4ed2-bed7-3256f9519b1a" />
</p>

---

## Output (Telegram)

<p align="center">
<img width="290" src="https://github.com/user-attachments/assets/4777b432-0f99-439e-83cd-7a8389e32ade" />
<img width="252" src="https://github.com/user-attachments/assets/c004011e-96af-4ca2-b796-df9bcc10abe3" />
<img width="220" src="https://github.com/user-attachments/assets/44b3a346-9bf8-45a6-b3a1-06888fc484ba" />
</p>

---

## Stack

- n8n  
- ERP API  
- Telegram  
- OpenAI  

---

## Flow

Schedule Trigger → Data Fetch → Processing → Analysis → AI Summary → Delivery


---

## Detailed Flow

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


---

## Notes

A lógica principal não depende de IA.

IA é utilizada apenas para organizar e resumir os dados,  
enquanto a análise crítica é baseada em regras de negócio.

---

## Author

Igor Henrique  
Automation • Data • Systems
