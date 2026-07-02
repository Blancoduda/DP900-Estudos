# 📚 09 - Revisão Geral da DP-900

## 🎯 Objetivo

Revisar os principais conceitos cobrados na certificação **Microsoft DP-900: Azure Data Fundamentals**, consolidando os conteúdos estudados nos módulos anteriores.

---

# Mapa Mental da DP-900

```
DP-900
│
├── Conceitos de Dados
├── Bancos Relacionais
├── Bancos Não Relacionais
├── Processamento Transacional
├── Processamento Analítico
├── Azure SQL
├── Azure Storage
├── Azure Cosmos DB
├── Azure Synapse
├── Azure Databricks
├── Microsoft Fabric
├── Power BI
└── Governança
```

---

# Conceitos Fundamentais

✅ Dados Estruturados

- Tabelas
- Colunas
- Linhas
- SQL

---

✅ Dados Semiestruturados

- JSON
- XML

---

✅ Dados Não Estruturados

- Imagens
- Vídeos
- PDFs
- Áudios

---

# Bancos Relacionais

Características:

- SQL
- Tabelas
- Chave Primária
- Chave Estrangeira
- ACID

Exemplos:

- Azure SQL Database
- PostgreSQL
- MySQL

---

# Bancos Não Relacionais

Características:

- Flexibilidade
- Escalabilidade
- NoSQL

Modelos:

- Documento
- Chave-Valor
- Família de Colunas
- Grafo

Exemplo:

- Azure Cosmos DB

---

# OLTP

Objetivo:

Registrar transações.

Exemplos:

- Compras
- Pagamentos
- Transferências

Características:

- CRUD
- ACID
- Muitas escritas

---

# OLAP

Objetivo:

Analisar dados.

Características:

- Grandes volumes
- Dados históricos
- Dashboards
- KPIs

---

# ETL x ELT

| ETL | ELT |
|------|------|
| Transforma antes | Transforma depois |
| Data Warehouse | Lakehouse |
| Processo tradicional | Processo moderno |

---

# Data Warehouse

- Dados estruturados
- Consultas SQL
- Histórico
- Business Intelligence

---

# Data Lake

- Dados brutos
- Diversos formatos
- Alta escalabilidade

---

# Lakehouse

Combina:

- Data Lake
- Data Warehouse

---

# Azure SQL

Modelo relacional.

Tipos:

- Azure SQL Database
- Managed Instance
- SQL Server em VM

---

# Azure Storage

Serviços:

- Blob
- Files
- Queue
- Table

---

# Azure Cosmos DB

Banco NoSQL.

Características:

- Distribuição global
- Alta disponibilidade
- Baixa latência

---

# Azure Synapse Analytics

Utilizado para:

- Data Warehouse
- Engenharia de Dados
- Analytics

---

# Azure Databricks

Baseado em:

- Apache Spark

Utiliza:

- Delta Lake

---

# Microsoft Fabric

Plataforma unificada de Analytics.

Inclui:

- Data Factory
- Data Engineering
- Data Warehouse
- Data Science
- Power BI
- OneLake

---

# Microsoft Purview

Responsável por:

- Governança
- Catálogo
- Classificação
- Segurança

---

# Arquitetura Medalhão

🥉 Bronze

Dados brutos.

---

🥈 Silver

Dados tratados.

---

🥇 Gold

Dados preparados para o negócio.

---

# Power BI

Componentes:

- Desktop
- Service
- Mobile

Conceitos:

- Power Query
- DAX
- Modelo Semântico
- Relatórios
- Dashboards

---

# Comparação Geral

| Conceito | Palavra-chave |
|----------|---------------|
| OLTP | Transações |
| OLAP | Analytics |
| SQL | Relacional |
| NoSQL | Flexibilidade |
| Cosmos DB | Documento |
| Blob Storage | Arquivos |
| Fabric | Plataforma Unificada |
| Databricks | Engenharia de Dados |
| Synapse | Analytics |
| Power BI | Visualização |

---

# Checklist Final

## Conceitos

- [ ] Dados Estruturados
- [ ] Dados Semiestruturados
- [ ] Dados Não Estruturados

## Bancos

- [ ] Relacionais
- [ ] Não Relacionais

## Processamento

- [ ] OLTP
- [ ] OLAP
- [ ] ACID
- [ ] CRUD
- [ ] ETL
- [ ] ELT

## Azure

- [ ] Azure SQL
- [ ] Cosmos DB
- [ ] Azure Storage
- [ ] Synapse
- [ ] Databricks
- [ ] Fabric
- [ ] Purview

## Power BI

- [ ] Power Query
- [ ] Modelo Semântico
- [ ] DAX
- [ ] Dashboards

---

# 🎯 Dicas para a prova

- Leia atentamente os cenários apresentados.
- Identifique primeiro se a questão trata de SQL, NoSQL, Analytics ou BI.
- Associe cada serviço do Azure ao problema descrito.
- Elimine alternativas incompatíveis com o cenário.
- Memorize as diferenças entre serviços semelhantes, como Azure SQL Database, Managed Instance e SQL Server em VM.

---

# 📚 Saiba mais

- https://learn.microsoft.com/credentials/certifications/azure-data-fundamentals/
- https://learn.microsoft.com/training/paths/azure-data-fundamentals-explore-core-data-concepts/
- https://learn.microsoft.com/azure/

---

## 📌 Próximo módulo

➡️ **10 - Simulados e Questões Comentadas**