# ☁️ 04 - Plataformas Modernas de Análise

## 🎯 Objetivo

Conhecer as principais plataformas modernas de análise de dados do Microsoft Azure, compreender suas funções dentro do pipeline analítico e entender como elas trabalham em conjunto para engenharia de dados, análise, governança e Business Intelligence.

---

# O que são Plataformas Modernas de Análise?

As organizações modernas processam grandes volumes de dados provenientes de diversas fontes.

Para isso, utilizam plataformas capazes de realizar todo o ciclo analítico, desde a ingestão dos dados até a geração de dashboards e relatórios.

No ecossistema Microsoft, destacam-se:

- Microsoft Fabric
- Azure Databricks
- Microsoft Purview

---

# Microsoft Fabric

O **Microsoft Fabric** é uma plataforma **SaaS (Software as a Service)** que reúne diversos serviços analíticos em um único ambiente.

Seu objetivo é centralizar todas as etapas da análise de dados em um único workspace.

Entre os principais recursos estão:

- Engenharia de Dados
- Data Factory
- Data Warehouse
- Data Science
- Real-Time Intelligence
- Power BI
- OneLake

---

## Principais Benefícios

- Plataforma unificada
- Interface integrada
- Compartilhamento simplificado
- Menor necessidade de gerenciamento de infraestrutura
- Integração nativa com Power BI

---

# Azure Databricks

O **Azure Databricks** é uma plataforma de engenharia de dados e ciência de dados construída sobre o Apache Spark.

É amplamente utilizada para:

- Engenharia de Dados
- Ciência de Dados
- Machine Learning
- Big Data

---

## Delta Lake

O Azure Databricks utiliza como formato padrão o **Delta Lake**.

O Delta Lake é baseado no formato **Parquet**, adicionando recursos importantes como:

- Transações ACID
- Controle de versão
- Atualizações confiáveis
- Melhor desempenho para consultas

---

## Principais Benefícios

- Processamento distribuído
- Alta escalabilidade
- Integração com Apache Spark
- Engenharia de Dados em larga escala
- Ciência de Dados

---

# Microsoft Purview

O **Microsoft Purview** é a plataforma de governança de dados da Microsoft.

Seu objetivo é ajudar organizações a localizar, proteger e gerenciar seus ativos de dados.

---

## Funcionalidades

- Descoberta de dados
- Classificação automática
- Catálogo de dados
- Linhagem dos dados
- Políticas de segurança
- Governança
- Conformidade

---

## Benefícios

- Melhor controle dos dados corporativos
- Maior segurança
- Atendimento a requisitos regulatórios
- Visibilidade sobre todo o patrimônio de dados

---

# Arquitetura Medalhão

Um padrão bastante utilizado em ambientes Lakehouse é a **Arquitetura Medalhão**.

Ela organiza os dados em três camadas.

---

## 🥉 Bronze

Contém os dados exatamente como chegaram dos sistemas de origem.

Características:

- Dados brutos
- Sem transformações
- Mantém histórico completo
- Permite reprocessamento

---

## 🥈 Silver

Nesta camada os dados passam por tratamento.

São realizadas atividades como:

- Remoção de duplicidades
- Padronização
- Tratamento de inconsistências
- Validação

Os dados tornam-se confiáveis para análises futuras.

---

## 🥇 Gold

Camada destinada ao consumo pelo negócio.

Os dados já estão:

- Agregados
- Organizados
- Modelados

São utilizados para:

- Dashboards
- KPIs
- Relatórios
- Modelos Analíticos
- Power BI

---

# Fluxo da Arquitetura Medalhão

```text
Sistema Origem
        │
        ▼
🥉 Bronze
(Dados Brutos)
        │
        ▼
🥈 Silver
(Dados Tratados)
        │
        ▼
🥇 Gold
(Dados para Negócio)
```

---

# Comparação das Plataformas

| Plataforma | Principal objetivo |
|------------|--------------------|
| Microsoft Fabric | Plataforma analítica completa |
| Azure Databricks | Engenharia de Dados e Ciência de Dados |
| Microsoft Purview | Governança de Dados |

---

# Quando utilizar cada uma?

| Cenário | Plataforma |
|---------|------------|
| Construção de dashboards | Microsoft Fabric |
| Processamento em larga escala | Azure Databricks |
| Governança e catálogo de dados | Microsoft Purview |

---

# Resumo

- Microsoft Fabric reúne diversos serviços analíticos em um único ambiente.
- Azure Databricks é voltado para Engenharia de Dados e Ciência de Dados.
- Microsoft Purview é responsável pela governança dos dados.
- A Arquitetura Medalhão organiza os dados em Bronze, Silver e Gold.
- Delta Lake adiciona transações ACID e versionamento ao Parquet.

---

# 🎯 O que costuma cair na DP-900

✅ Microsoft Fabric

✅ Azure Databricks

✅ Microsoft Purview

✅ Delta Lake

✅ Arquitetura Medalhão

✅ Camadas Bronze, Silver e Gold

---

# 📚 Saiba mais

- https://learn.microsoft.com/fabric/
- https://learn.microsoft.com/azure/databricks/
- https://learn.microsoft.com/purview/
- https://learn.microsoft.com/azure/architecture/data-guide/

---

## 📌 Próximo módulo

➡️ **05 - Serviços de Dados do Azure**