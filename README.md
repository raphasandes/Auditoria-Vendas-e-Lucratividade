# 📊 Dashboard de Vendas e Auditoria de Lucratividade

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge)](https://learn.microsoft.com/en-us/dax/)
[![Data Modeling](https://img.shields.io/badge/Star_Schema-4CAF50?style=for-the-badge)](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)

## 📌 Visão Geral
Este projeto apresenta um **Dashboard de Vendas e Auditoria de Dados** focado na transformação de dados brutos em inteligência de negócio. O trabalho foi desenvolvido para diagnosticar uma crise de rentabilidade, revelando um prejuízo operacional severo causado por falhas de precificação e gestão de custos.

## 💼 Contexto e Origem dos Dados
Este projeto foi desenvolvido utilizando uma **base de dados real**, disponibilizada por uma empresa em um **processo seletivo** para o cargo de **Analista de Dados**.
* **Autorização:** A empresa autorizou a disponibilização dos dados para fins de portfólio.
* **Privacidade:** Dados sensíveis foram **anonimizados**, preservando a lógica de negócio e as métricas financeiras originais.

---

## 📸 Interface do Dashboard
<img width="584" height="333" alt="image" src="https://github.com/user-attachments/assets/13e9f798-1712-4013-85db-1907f20dabdd" />


---

## 🛠️ Processo de Desenvolvimento

### 1. ETL e Preparação (Power Query)
A base de dados, composta por tabelas de vendas, metas, produtos e clientes, passou por:
* **Padronização de Tipos:** Conversão de IDs para texto e ajuste de colunas financeiras para Número Decimal.
* **Limpeza:** Validação de integridade e análise de outliers.
* **Dimensão Tempo:** Criação de uma tabela `Dim_Tempo` via DAX com lógica de ordenação cronológica para garantir a análise temporal correta.

### 2. Modelagem de Dados (Star Schema)
Estrutura otimizada para performance e escalabilidade:
* **Tabela Fato:** `Vendas`.
* **Tabelas Dimensão:** `Produtos`, `Clientes`, `Metas` e `Dim_Tempo`.
* **Relacionamentos:** Cardinalidade 1:N com filtros unidirecionais.

### 3. Cálculos Avançados (DAX)
Desenvolvimento de medidas críticas para o diagnóstico:
* **Custo Total:** Calculado via `SUMX` e `RELATED` para capturar o custo real de cada transação.
* **Lucro Bruto:** Revelou um déficit de **R$ 190,18 Mil**.
* **Margem Bruta (%):** Identificação de uma rentabilidade negativa de **-197,24%**.
* **Qtd Itens Negativos:** Medida diagnóstica para identificar produtos operando abaixo do custo.

---

## 🔍 Diagnóstico e Insights de Negócio
* **Causa Raiz:** Identificou-se que o Valor Unitário de venda é inferior ao Custo Unitário nos itens "Notebook" e "Monitor".
* **Performance vs Meta:** Apenas **31,88%** da meta de faturamento foi atingida no período.
* **Visualização:** Uso de formatação condicional estratégica para destacar instantaneamente os pontos de prejuízo.

## 🚀 Recomendações e Providências
1.  **Bloqueio de Vendas:** Suspensão imediata dos itens com margem negativa.
2.  **Auditoria de Contratos:** Revisão de acordos com clientes deficitários.
3.  **Trava de Sistema:** Impedir vendas onde o preço seja inferior ao custo unitário.

---

## 🤖 Uso de IA
Como parte da metodologia, utilizou-se IA como suporte para:
* Validação da lógica de cálculos DAX complexos.
* Estruturação da tabela Dim_Tempo.
* Revisão técnica e qualidade do relatório final.

---
**Elaborado por:** Raphael Sandes  
**Conecte-se comigo:** [Seu LinkedIn Aqui](https://www.linkedin.com/in/SEU_PERFIL)
