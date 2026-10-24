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

🔄 Fluxo de Trabalho e Pipeline de Dados (ETL)
Ingestão e Tratamento (Python):

Padronização de strings (strip(), remoção de caracteres especiais e caixa alta).

Conversão e validação de tipos de dados (datas e identificadores).

Tratamento de valores ausentes e remoção de registros duplicados.

Persistência (SQLite):

Criação da tabela Solicitacao_Farmacia_Clean no banco de dados banco.db.

Exportação do dataset limpo final para consumo direto pelo Power BI (farmacia_hospitalar_powerbi.csv).

Modelagem DAX & Visualização (Power BI):

Criação de medidas essenciais em DAX:

[Total Solicitacoes]

[Total Rupturas]

[Taxa de Atendimento %]

Desenvolvimento do painel de monitoramento focado em KPIs de nível de serviço.

💡 Principais Insights de Negócio
Concentração Crítica: Mais de 60% das rupturas registradas concentram-se em setores de alta prioridade (UTI e Pronto Socorro), com destaque para as categorias de Antibióticos e Analgésicos.

Sazonalidade e Picos: Identificou-se um aumento expressivo nas solicitações não atendidas no meio do trimestre, apontando para a necessidade de reajuste nas rotas de distribuição interna e renegociação de lead times com fornecedores chave.

Ação Recomendada: Implementação de alertas de estoque crítico no Power BI e revisão do cálculo de estoque de segurança por categoria.

🚀 Como Executar o Projeto
Clonar o Repositório:

Bash
git clone [https://github.com/jeandrade75/hospital-pharmacy-analytics.git](https://github.com/jeandrade75/hospital-pharmacy-analytics.git)
Executar o Pipeline de Tratamento:

Abra o notebook notebooks/ETL_Limpeza_Farmacia.ipynb no Google Colab ou Jupyter Notebook e execute as células sequencialmente.

Visualizar o Dashboard:

Certifique-se de ter o Power BI Desktop instalado.

Abra o arquivo dashboard/Dashboard_Farmacia_Hospitalar.pbix.

<img width="839" height="469" alt="image" src="https://github.com/user-attachments/assets/2e62aa7f-5306-4a64-8117-efcfa633a50e" />


✍️ Autor
Jean Andrade — LinkedIn | GitHub
