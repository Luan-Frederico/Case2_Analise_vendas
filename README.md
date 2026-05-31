# Case 2: Análise de Vendas (Power BI)

# Introdução

Este projeto tem como objetivo desenvolver uma solução completa de **Business Intelligence (BI)** para avaliar o **desempenho comercial**, a **eficiência de faturamento** e o **comportamento de compra** de uma carteira de clientes ativos. A análise e a estruturação dos dados foram conduzidas integralmente no **Power BI**, cobrindo todas as etapas fundamentais de um pipeline de dados: extração, tratamento e limpeza (ETL), modelagem dimensional e design de dashboards.

O foco do projeto foi aplicar lógica analítica, modelagem de dados e engenharia de fórmulas DAX para transformar tabelas transacionais brutas e descentralizadas em um painel altamente interativo. A solução desenvolvida visa eliminar pontos cegos operacionais e fornecer diagnósticos rápidos e precisos para dar suporte estratégico à tomada de decisão.

<p align="center">
  <img src="dashboard_vendas_pt1.png" alt="Dashboard de Inteligência Comercial - Visão Geral" style="max-width: 100%; height: auto;">
</p>

<p align="center">
  <img src="dashboard_vendas_pt3.png" alt="Dashboard de Inteligência Comercial - Análise Detalhada" style="max-width: 100%; height: auto;">
</p>

---

# Contexto e Problema de Negócio

A liderança comercial enfrentava dificuldades para obter uma leitura clara e centralizada da performance de vendas e do comportamento da carteira de clientes. As informações de faturamento e operações encontravam-se descentralizadas e em formato bruto, gerando pontos cegos estratégicos e morosidade na extração de indicadores confiáveis.

Para direcionar o crescimento do negócio, a gestão técnica de Inteligência estipulou um projeto que foi estruturado para mitigar as seguintes dores de negócio:

- **Falta de Visibilidade de KPIs Críticos:** Inexistência de um fluxo automatizado para acompanhar métricas essenciais de saúde comercial, como Faturamento Total, Ticket Médio por transação e a evolução temporal das vendas.
- **Pontos Cegos na Carteira de Clientes:** Dificuldade para mensurar a volumetria de Clientes Ativos e suas quantidades de vendas e identificar com rapidez assimetrias e dispersões no comportamento de compra da carteira.
- **Estrutura de Dados Descentralizada:** Necessidade de consolidar e auditar dados brutos provenientes de tabelas transacionais e cadastros auxiliares, exigindo um pipeline rigoroso de tratamento e modelagem para garantir a consistência das informações antes da tomada de decisão.

---

# Tecnologias e Ferramentas Utilizadas

- **Power BI:** Construção, Modelagem e Visualização de dados.
- **Power Query:** Processos de ETL (Extração, Transformação e Carregamento).
- **Modelagem de dados e Relacionamentos:** Arquitetura **Star Schema** com conexões 1:N e integridade referencial.
- **DAX (Data Analysis Expressions):** Criação de Métricas e Indicadores de negócio.

---

# Pipeline de dados e Arquitetura

## 1. Extração e Tratamento de dados (ETL)
Utilizando o **Power Query**, foi realizado o pipeline completo de limpeza e transformação da base bruta:
- Eliminação de redundâncias, tratamento de valores nulos e tipagem correta dos dados.
- Otimização da base para garantir a performance de carregamento e atualização do relatório.

## 2. Modelagem Dimensional (Star Schema)
Para garantir eficiência e escalabilidade nas consultas, os dados foram estruturados seguindo o modelo **Star Schema**:
- **Tabela Fato:** Centralização dos registros operacionais e históricos de vendas.
- **Tabela Dimensão:** Tabelas auxiliares (Clientes, Produtos, Vendedores) conectadas via relacionamentos de *1:N* (um para muitos), otimizando a performance dos filtros e do motor analítico.

## 3. Engenharia de Métricas com DAX
Desenvolvimento de uma camada robusta de medidas em **DAX** para extrair os principais indicadores de performance (KPI's) comerciais, que são:
- **Faturamento Total:** Valor arrecadado pela empresa.
- **Ticket Médio:** Valor médio gasto por cliente em transação/pedido.
- **Clientes Ativos:** Quantidade de clientes únicos que realizaram pelo menos uma compra no período.
- **Volume de Vendas:** Quantidade total de itens ou transações comerciais realizadas.

Além disso, a análise foi desdobrada para avaliar a performance do faturamento por **Cliente, Vendedor, Produto, Categoria e Subcategoria, e por Mês**. A disposição desses elementos no dashboard foi planejada utilizando gráficos adequados para cada segmento, respeitando o padrão de **Leitura em Z** e aplicando boas práticas de **Storytelling e Direcionamento Visual Claro**, garantindo que o usuário final encontre as respostas estratégicas de forma fluida e intuitiva.

---

# Estrutura do Dashboard

O relatório foi desenvolvido em **Dark Mode** (Fundo escuro moderno para melhor contraste visual e destacar KPI's), aplicando conceitos modernos de UI/UX, navegação intuitiva por **botões** e foco na **redução da fadiga visual** do usuário técnico. Ele é dividido em duas visões estratégicas:

1. **Painel Técnico (KPI's Gerais):** Visão macro voltada para a liderança, consolidando os principais indicadores de saúde comercial, faturamento e metas de forma rápida e direta.
2. **Painel Criativo (Diagnósticos Avançados):** Visão analítica profunda que utiliza visuais avançados, como **Gráficos de Dispersão** e **Árvores de Decomposição**, permitindo ao analista identificar tendências, relações, anomalias e assimetrias e mapear diagnósticos e gargalos operacionais ou de vendas.

---

# Como Visualizar o Projeto
1. Faça o download do arquivo *.pbix* presente neste repositório.
2. Abra o arquivo utilizando o **Power BI Desktop (ou na nuvem)**.
3. Explore as interações, filtros cruzados e navegações entre as páginas.

---

[Acesse o Dashboard Completo interativo aqui](https://app.powerbi.com/view?r=eyJrIjoiMmVkNjExOTItYzBmYi00ZTVkLWEzNTktZjFmZjliNzY1YjZiIiwidCI6ImIzNGMxZDU1LWE0M2UtNGEyMC05MjE4LWExYTQyZWFiMTQ5YSJ9)
