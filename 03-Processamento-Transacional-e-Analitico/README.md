# ⚙️ 03 - Processamento Transacional e Analítico

## 🎯 Objetivo

Compreender as diferenças entre processamento transacional (OLTP) e processamento analítico (OLAP), conhecer as propriedades ACID, os processos ETL e ELT, além das principais plataformas modernas de análise utilizadas no Microsoft Azure.

---

# Processamento de Dados Transacionais (OLTP)

O **OLTP (Online Transaction Processing)** representa o processamento de dados utilizado pelas aplicações do dia a dia das empresas.

Esses sistemas registram transações que representam eventos específicos do negócio.

Exemplos:

- Transferência bancária
- Compra em um e-commerce
- Cadastro de um cliente
- Emissão de uma nota fiscal

Uma transação deve ser tratada como uma unidade única de trabalho.

---

# CRUD

Os sistemas OLTP executam constantemente operações conhecidas como **CRUD**.

| Operação | Descrição |
|----------|-----------|
| Create | Criar um registro |
| Read | Consultar um registro |
| Update | Atualizar um registro |
| Delete | Excluir um registro |

Essas operações precisam manter a integridade dos dados armazenados.

---

# Propriedades ACID

Os bancos de dados transacionais seguem quatro propriedades fundamentais conhecidas como **ACID**.

---

## 🅰️ Atomicidade (Atomicity)

Cada transação é tratada como uma única unidade.

Ela será:

- totalmente concluída;
- ou totalmente cancelada.

### Exemplo

Uma transferência bancária envolve:

- Debitar dinheiro da conta A;
- Creditar dinheiro na conta B.

Se uma dessas operações falhar, toda a transação será cancelada.

---

## 🅲 Consistência (Consistency)

Uma transação sempre leva o banco de dados de um estado válido para outro estado válido.

Após uma transferência bancária, os saldos precisam refletir corretamente a movimentação realizada.

---

## 🅸 Isolamento (Isolation)

Transações executadas ao mesmo tempo não podem interferir umas nas outras.

Enquanto uma transferência está sendo realizada, outra consulta ao saldo não pode visualizar informações inconsistentes.

---

## 🅳 Durabilidade (Durability)

Depois que uma transação é confirmada, ela permanece armazenada permanentemente.

Mesmo que ocorra uma falha no servidor, os dados continuarão gravados.

---

# Processamento Analítico (OLAP)

O **OLAP (Online Analytical Processing)** é utilizado para análise de grandes volumes de dados históricos.

Esses sistemas são predominantemente de leitura.

Seu objetivo é responder perguntas do negócio através de consultas analíticas.

Exemplos:

- Qual foi o faturamento do último trimestre?
- Qual produto vendeu mais?
- Qual região apresentou maior crescimento?

---

# OLTP x OLAP

| OLTP | OLAP |
|------|------|
| Processamento transacional | Processamento analítico |
| Muitas escritas | Muitas leituras |
| Dados atuais | Dados históricos |
| CRUD | Agregações |
| Operações rápidas | Consultas complexas |
| Sistemas operacionais | Dashboards e BI |

---

# ETL e ELT

Antes que os dados possam ser analisados, eles normalmente passam por processos de integração.

Existem dois padrões principais.

---

## ETL (Extract, Transform, Load)

Os dados são:

1. Extraídos
2. Transformados
3. Carregados

Fluxo:

```text
Origem
   ↓
Extração
   ↓
Transformação
   ↓
Data Warehouse
```

Muito utilizado em arquiteturas tradicionais de Data Warehouse.

---

## ELT (Extract, Load, Transform)

Os dados são:

1. Extraídos
2. Carregados
3. Transformados

Fluxo:

```text
Origem
   ↓
Data Lake
   ↓
Transformação
   ↓
Lakehouse
```

É o padrão mais utilizado em arquiteturas modernas de Lakehouse.

---

# Data Warehouse

O **Data Warehouse** é um repositório centralizado para armazenamento de dados históricos.

Características:

- Dados estruturados
- Modelo relacional
- Consultas analíticas
- Business Intelligence

---

# Data Lake

O **Data Lake** armazena grandes volumes de dados em diversos formatos.

Pode armazenar:

- CSV
- JSON
- Parquet
- Imagens
- Vídeos
- Áudios
- Logs

Os dados normalmente permanecem em seu formato original.

---

# Lakehouse

O **Lakehouse** combina características do Data Lake e do Data Warehouse.

Ele permite:

- Armazenar dados brutos;
- Trabalhar com dados estruturados;
- Executar consultas SQL;
- Utilizar recursos analíticos modernos.

É uma das arquiteturas mais utilizadas atualmente.

---

# Modelo Semântico (OLAP)

Após o processamento dos dados, eles podem ser organizados em um **Modelo Semântico**.

Antigamente era conhecido como **Cubo OLAP**.

Nesse modelo são criadas:

- Medidas
- Dimensões
- Hierarquias

Exemplo:

A receita pode ser analisada por:

- Produto
- Cliente
- Data
- Região

No Microsoft Azure, o exemplo mais comum é o **Modelo Semântico do Power BI**.

---

# Relatórios e Dashboards

Os dados armazenados em:

- Data Lake
- Data Warehouse
- Modelo Semântico

podem ser utilizados para gerar:

- Dashboards
- Relatórios
- KPIs
- Indicadores
- Visualizações

---

# Plataformas Modernas de Análise

O Microsoft Azure disponibiliza plataformas que cobrem praticamente todo o pipeline analítico.

As principais são:

- Microsoft Fabric
- Azure Databricks
- Microsoft Purview

---

# Microsoft Fabric

O **Microsoft Fabric** é uma plataforma SaaS (Software as a Service).

Ela reúne em um único ambiente:

- Engenharia de Dados
- Data Warehouse
- Ciência de Dados
- Business Intelligence
- Relatórios
- Armazenamento

Seu objetivo é unificar toda a plataforma analítica.

---

# Azure Databricks

O **Azure Databricks** é uma plataforma voltada para:

- Engenharia de Dados
- Ciência de Dados
- Machine Learning
- Big Data

Seu formato padrão de armazenamento é o **Delta Lake**.

O Delta Lake adiciona ao Parquet:

- Controle de versão
- Transações ACID
- Atualizações confiáveis

---

# Microsoft Purview

O **Microsoft Purview** é o serviço de governança de dados da Microsoft.

Ele permite:

- Descobrir dados
- Classificar informações
- Proteger dados
- Gerenciar conformidade
- Aplicar políticas de segurança

---

# Arquitetura Medalhão

Uma arquitetura bastante utilizada em Lakehouses é a **Arquitetura Medalhão**.

Ela organiza os dados em três camadas.

## 🥉 Bronze

Contém os dados brutos exatamente como foram recebidos.

Não são realizadas transformações.

Objetivo:

- Preservar os dados originais
- Permitir reprocessamentos

---

## 🥈 Silver

Contém dados tratados.

Nesta etapa são realizadas:

- Limpeza
- Padronização
- Remoção de duplicidades
- Correção de inconsistências

---

## 🥇 Gold

Contém dados preparados para o negócio.

São utilizados em:

- Dashboards
- Relatórios
- Indicadores
- Modelos Analíticos

---

# Comparação

| Conceito | Objetivo |
|----------|----------|
| OLTP | Registrar transações |
| CRUD | Operações básicas do banco |
| ACID | Garantir integridade das transações |
| OLAP | Análise de dados |
| ETL | Transformar antes de carregar |
| ELT | Transformar depois de carregar |
| Data Warehouse | Armazenamento analítico |
| Data Lake | Armazenamento de dados brutos |
| Lakehouse | Combinação de Data Lake e Data Warehouse |

---

# Resumo

- OLTP processa transações do dia a dia.
- CRUD representa as operações básicas dos bancos de dados.
- ACID garante integridade das transações.
- OLAP é utilizado para análise de dados.
- ETL transforma antes de carregar.
- ELT transforma após carregar.
- Data Warehouse armazena dados estruturados.
- Data Lake armazena dados em diversos formatos.
- Lakehouse une Data Lake e Data Warehouse.
- Microsoft Fabric é uma plataforma unificada de análise.
- Azure Databricks utiliza Delta Lake.
- Microsoft Purview é responsável pela governança de dados.
- A Arquitetura Medalhão organiza os dados nas camadas Bronze, Silver e Gold.

---

# 🎯 O que costuma cair na DP-900

✅ Diferença entre OLTP e OLAP.

✅ CRUD.

✅ Propriedades ACID.

✅ ETL x ELT.

✅ Data Warehouse x Data Lake x Lakehouse.

✅ Microsoft Fabric.

✅ Azure Databricks.

✅ Microsoft Purview.

✅ Arquitetura Medalhão.

---

# 📚 Saiba mais

- https://learn.microsoft.com/training/paths/azure-data-fundamentals-explore-core-data-concepts/
- https://learn.microsoft.com/fabric/
- https://learn.microsoft.com/azure/databricks/
- https://learn.microsoft.com/purview/
- https://learn.microsoft.com/azure/architecture/data-guide/

---

## 📌 Próximo módulo

➡️ **04 - Serviços de Dados Relacionais no Azure**