# Case 2: Análise de Vendas (Power BI)

# Introdução

Este projeto tem como objetivo desenvolver uma solução completa de **Business Intelligence (BI)** para avaliar o **desempenho comercial**, a **eficiência de faturamento** e o **comportamento de compra** de uma carteira de clientes ativos. A análise e a estruturação dos dados foram conduzidas integralmente no **Power BI**, cobrindo todas as etapas fundamentais de um pipeline de dados: extração, tratamento e limpeza (ETL), modelagem dimensional e design de dashboards.

O foco do projeto foi aplicar **lógica analítica**, **modelagem de dados** e engenharia de fórmulas **DAX** para transformar tabelas transacionais brutas e descentralizadas em um **painel altamente interativo**. A solução desenvolvida visa eliminar pontos cegos operacionais e fornecer diagnósticos rápidos e precisos para dar suporte estratégico à tomada de decisão.

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

# Insights e Principais achados

Após a estruturação do pipeline de dados e a construção do dashboard comercial, foi possível extrair diagnósticos valiosos sobre a saúde financeira e o comportamento da carteira de clientes:

## 1. Métricas Gerais

A página inicial do dashboard apresenta o Painel Técnico, uma visão macro projetada para fornecer à liderança diagnósticos rápidos sobre a saúde comercial do negócio. Nele, destacam-se quatro KPI's fundamentais calculados via DAX:

- **Faturamento Total:** Atingiu a marca de *5,06 Mi*. Este valor representa o desempenho financeiro bruto e indica uma operação com **escala considerável** e um fluxo de receita robusto para o período.
- **Clientes:** O painel registra *50 clientes ativos*. Este número revela uma carteira de clientes **enxuta** e **estratégica**; dada a magnitude do faturamento, cada cliente possui um alto valor para o negócio, indicando um modelo focado em grandes contas (High TKM).
- **Ticket Médio:** Consolidado em *5,06 Mil*. Este KPI sinaliza que a empresa comercializa produtos de **alto valor agregado** ou realiza **vendas em grandes lotes**, exigindo uma abordagem comercial qualificada.
- **Volume de Vendas:** Registrou o total de *1 Mil* transações. Ao cruzar este dado com a base de 50 clientes ativos, percebe-se uma alta taxa de recorrência (média de 20 pedidos por cliente), o que demonstra **fidelidade à marca** e **eficiência na retenção da carteira**.

Esses indicadores foram posicionados seguindo o padrão de **leitura em Z**, garantindo que as métricas mais críticas de desempenho e volumetria sejam as primeiras informações absorvidas pelo usuário.

## Faturamento Mensal

Logo abaixo do painel de indicadores, o gráfico de Faturamento por Mês detalha a evolução temporal das vendas ao longo de 2024, permitindo identificar padrões de sazonalidade e o ritmo de crescimento do negócio:

- **Tendência de Crescimento:** Observa-se uma clara trajetória de **ascensão** no faturamento ao longo do ano. O negócio inicia em Janeiro com 186,06 Mil e, apesar de uma leve queda em Fevereiro, demonstra uma recuperação consistente, mudando de patamar a partir do segundo semestre.
- **Pico de Performance:** O mês de outubro registra o ápice de faturamento, com 810,72 Mil, seguido de perto por novembro com 761,88 Mil. Esse comportamento sugere uma **forte sazonalidade positiva no último trimestre**, indicando que o período é crítico para o atingimento das metas anuais.
- **Volatilidade e Recuperação:** O gráfico revela pontos de oscilação, como a queda em agosto após um excelente mês de Julho. No entanto, a capacidade de recuperação imediata nos meses seguintes aponta para uma **operação comercial resiliente** e com **alto poder de reação**.
- **Maturação da Operação:** A comparação entre o primeiro e o último trimestre mostra que a empresa encerra o ciclo anual em um nível de receita muito superior ao inicial. Enquanto a média dos primeiros meses se manteve baixa, o encerramento do ano consolida valores consistentemente altos.

Num geral, a análise temporal do faturamento valida a **escalabilidade** do negócio ao longo de 2024, demonstrando que a operação não apenas cresceu em volume, mas também amadureceu em termos de previsibilidade. A identificação clara do pico de vendas nos últimos meses fornece um insumo estratégico fundamental para o planejamento preditivo . Com base nesses dados, a gestão pode realizar um provisionamento de estoque e alocação de recursos mais assertivos para os períodos de alta demanda, garantindo que o crescimento observado seja sustentado com eficiência operacional nos ciclos seguintes.

## Faturamento por Cliente

O ranking de Faturamento por Cliente destaca os principais parceiros comerciais da operação, evidenciando as contas que mais contribuíram para o resultado global. No topo da lista, destacam-se Nicole (173,81mil) e Melanie (162,78 mil), seguidas por outros clientes que mantêm uma média de faturamento acima de R$ 120 mil
.
Essa distribuição confirma a eficácia da estratégia de foco em High TKM (Ticket Médio Alto), onde o sucesso financeiro é impulsionado por um grupo seleto de clientes de alto valor agregado
. O fato de os principais clientes apresentarem valores próximos sugere uma carteira saudável e bem distribuída entre as contas estratégicas, o que reduz o risco de dependência excessiva de um único comprador
.

[Acesse o Dashboard Completo interativo aqui](https://app.powerbi.com/view?r=eyJrIjoiMmVkNjExOTItYzBmYi00ZTVkLWEzNTktZjFmZjliNzY1YjZiIiwidCI6ImIzNGMxZDU1LWE0M2UtNGEyMC05MjE4LWExYTQyZWFiMTQ5YSJ9)
