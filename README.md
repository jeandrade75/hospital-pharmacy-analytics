# 🏥 Gestão e Prevenção de Rupturas na Farmácia Hospitalar

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

---

## 📌 Visão Geral do Projeto

Este projeto tem como objetivo otimizar a gestão de estoque e prevenir a **ruptura (desabastecimento)** de medicamentos e insumos na farmácia de um complexo hospitalar (**Ticket #8402**).

A solução engloba desde o pipeline de engenharia de dados (limpeza, padronização e persistência em banco relacional) até a construção de um painel analítico interativo no **Power BI** para apoio à tomada de decisão da **Diretoria de Operações**.

---

## 🎯 Desafios de Negócio (Problemática)

As rupturas em setores críticos como **UTI** e **Centro Cirúrgico** trazem riscos diretos à saúde dos pacientes e geram gargalos na rotina hospitalar.
O objetivo principal deste projeto foi responder a três perguntas estratégicas:

1. **Onde estão os gargalos?** Quais setores e categorias concentram o maior número de solicitações não atendidas?
2. **Qual é a evolução temporal?** O volume de rupturas está aumentando ou diminuindo ao longo dos meses?
3. **Quais ações tomar?** Como reestruturar o nível de estoque mínimo (*safety stock*) e alinhar os prazos com fornecedores?

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

* **Linguagem:** `Python` (Manipulação e tratamento de dados via `Pandas`)
* **Ambiente de Desenvolvimento:** `Google Colab`
* **Banco de Dados / Armazenamento:** `SQLite` (Persistência relacional)
* **Visualização de Dados / Dashboard:** `Power BI` (Modelagem em DAX e visuais interativos)
* **Controle de Versão:** `Git` e `GitHub`

---

## 📁 Estrutura do Repositório

```text
hospital-pharmacy-analytics/
 ├── 📁 data/
 │   ├── raw/                           # Bases brutas (CSV)
 │   └── processed/                     # Base tratada (farmacia_hospitalar_powerbi.csv)
 ├── 📁 database/
 │   ├── banco.db                       # Banco de dados SQLite persistido
 │   └── queries_limpeza.sql            # Scripts e queries de consulta SQL
 ├── 📁 notebooks/
 │   └── ETL_Limpeza_Farmacia.ipynb    # Notebook com pipeline completo de limpeza
 ├── 📁 dashboard/
 │   └── Dashboard_Farmacia_Hospitalar.pbix  # Arquivo do Power BI
 ├── .gitignore                         # Configuração de arquivos ignorados
 └── README.md                          # Documentação do projeto
