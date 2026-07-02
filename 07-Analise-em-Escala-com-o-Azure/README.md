# 📈 07 - Análise em Escala com o Azure

## 🎯 Objetivo

Conhecer os principais serviços do Microsoft Azure utilizados para análise de grandes volumes de dados, compreender suas funções dentro de arquiteturas analíticas modernas e identificar quando utilizar cada solução.

---

# O que é Análise em Escala?

À medida que as organizações produzem grandes volumes de dados, torna-se necessário utilizar plataformas capazes de processar, armazenar e analisar essas informações de forma eficiente.

Essas plataformas permitem:

- Processar grandes volumes de dados;
- Executar análises complexas;
- Criar Data Warehouses e Lakehouses;
- Desenvolver pipelines de dados;
- Construir dashboards e relatórios.

No Azure, destacam-se:

- Azure Synapse Analytics
- Azure Databricks
- Microsoft Fabric

---

# Azure Synapse Analytics

O **Azure Synapse Analytics** é uma plataforma analítica integrada que reúne recursos para ingestão, armazenamento, processamento e análise de dados.

Ela combina diferentes serviços em um único ambiente.

## Principais recursos

- SQL Analytics
- Apache Spark
- Pipelines de Dados
- Data Warehouse
- Integração com Power BI

---

## Quando utilizar?

Ideal para:

- Grandes volumes de dados
- Business Intelligence
- Data Warehouse
- Engenharia de Dados
- Análises corporativas

---

# Azure Databricks

O **Azure Databricks** é uma plataforma baseada no Apache Spark voltada para processamento distribuído.

É utilizada para:

- Engenharia de Dados
- Ciência de Dados
- Machine Learning
- Big Data

---

## Apache Spark

O Apache Spark é um mecanismo de processamento distribuído utilizado para trabalhar com grandes volumes de dados.

Entre suas principais vantagens:

- Processamento paralelo
- Alta velocidade
- Escalabilidade
- Suporte a diversas linguagens

---

# Delta Lake

O Delta Lake é o formato de armazenamento padrão do Azure Databricks.

Baseado em arquivos Parquet, adiciona:

- Transações ACID
- Controle de versão
- Atualizações confiáveis

---

# Microsoft Fabric

O **Microsoft Fabric** é uma plataforma SaaS unificada para análise de dados.

Ela reúne diferentes workloads em um único ambiente.

Entre eles:

- Data Factory
- Data Engineering
- Data Warehouse
- Data Science
- Real-Time Intelligence
- Power BI

---

# OneLake

O **OneLake** é o armazenamento unificado do Microsoft Fabric.

Seu objetivo é centralizar os dados utilizados pelos diferentes workloads.

Benefícios:

- Fonte única de dados
- Compartilhamento entre workloads
- Integração nativa com Fabric

---

# Data Warehouse

Um Data Warehouse é um repositório centralizado utilizado para armazenar dados históricos estruturados.

Características:

- Dados organizados
- Consultas analíticas
- Histórico
- Business Intelligence

---

# Data Lakehouse

O Lakehouse combina as vantagens do Data Lake e do Data Warehouse.

Permite:

- Armazenar dados brutos;
- Executar consultas SQL;
- Utilizar formatos modernos como Delta Lake;
- Trabalhar com Engenharia de Dados e Analytics no mesmo ambiente.

---

# Comparação

| Serviço | Principal utilização |
|----------|----------------------|
| Azure Synapse Analytics | Plataforma analítica integrada |
| Azure Databricks | Engenharia de Dados |
| Microsoft Fabric | Plataforma unificada |
| OneLake | Armazenamento unificado |
| Apache Spark | Processamento distribuído |
| Delta Lake | Armazenamento transacional |

---

# Resumo

- Azure Synapse Analytics integra diversos serviços analíticos.
- Azure Databricks utiliza Apache Spark para processamento distribuído.
- Delta Lake adiciona transações ACID ao Parquet.
- Microsoft Fabric reúne diferentes workloads analíticos.
- OneLake centraliza o armazenamento do Fabric.
- Lakehouse combina Data Lake e Data Warehouse.

---

# 🎯 O que costuma cair na DP-900

✅ Azure Synapse Analytics.

✅ Azure Databricks.

✅ Apache Spark.

✅ Delta Lake.

✅ Microsoft Fabric.

✅ OneLake.

✅ Data Warehouse.

✅ Lakehouse.

---

# 📚 Saiba mais

- https://learn.microsoft.com/azure/synapse-analytics/
- https://learn.microsoft.com/azure/databricks/
- https://learn.microsoft.com/fabric/
- https://learn.microsoft.com/fabric/onelake/
- https://learn.microsoft.com/azure/architecture/data-guide/

---

## 📌 Próximo módulo

➡️ **08 - Visualização e Análise com Power BI**