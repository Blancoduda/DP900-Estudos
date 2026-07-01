# ⚙️ 03 - Processamento Transacional e Analítico

## 🎯 Objetivo

Compreender como os dados são processados em sistemas transacionais (OLTP) e analíticos (OLAP), conhecer as propriedades ACID, os processos ETL e ELT, além das plataformas modernas de análise disponíveis no Microsoft Azure.

---

# Processamento de Dados Transacionais (OLTP)

Um sistema de processamento de dados transacionais (**OLTP - Online Transaction Processing**) é o que a maioria das pessoas considera a principal função da computação empresarial.

Um sistema transacional registra transações que encapsulam eventos específicos que a organização deseja controlar.

Uma transação pode ser:

- Financeira, como uma transferência entre contas bancárias;
- Comercial, como o pagamento de um pedido em um e-commerce;
- Operacional, como o cadastro de um cliente.

Pense na transação como uma unidade de trabalho pequena e discreta.

---

# Operações CRUD

As soluções OLTP dependem de um banco de dados otimizado para operações de leitura e gravação.

Essas operações são conhecidas como **CRUD**:

| Operação | Descrição |
|----------|-----------|
| Create | Criar um registro |
| Read | Ler um registro |
| Update | Atualizar um registro |
| Delete | Excluir um registro |

Essas operações são executadas de maneira transacional para garantir a integridade dos dados.

---

# Propriedades ACID

Os sistemas OLTP utilizam transações compatíveis com as propriedades **ACID**.

## Atomicidade (Atomicity)

Cada transação é tratada como uma única unidade.

Ela será:

- totalmente concluída;
- ou totalmente cancelada.

**Exemplo**

Uma transferência bancária precisa:

- Debitar uma conta;
- Creditar outra conta.

Se uma das operações falhar, toda a transação será cancelada.

---

## Consistência (Consistency)

Uma transação só pode levar o banco de dados de um estado válido para outro estado válido.

Após uma transferência bancária, os saldos das contas devem refletir corretamente a movimentação realizada.

---

## Isolamento (Isolation)

Transações simultâneas não podem interferir umas nas outras.

Enquanto uma transferência está acontecendo, outra consulta ao saldo deve retornar informações consistentes.

---

## Durabilidade (Durability)

Depois que uma transação é confirmada, seus dados permanecem armazenados.

Mesmo que o banco seja desligado logo após a confirmação, as alterações continuarão gravadas.

---

# Processamento Analítico (OLAP)

O processamento analítico (**OLAP - Online Analytical Processing**) utiliza sistemas predominantemente de leitura.

Esses sistemas armazenam grandes volumes de dados históricos ou métricas de negócio.

A análise pode ser baseada:

- em um único momento;
- ou em vários períodos históricos.

---

# ETL e ELT

Os dados operacionais são preparados para análise utilizando processos de integração de dados.

## ETL

**Extract → Transform → Load**

Os dados são:

1. Extraídos;
2. Transformados;
3. Carregados.

Esse modelo é tradicionalmente utilizado em Data Warehouses.

---

## ELT

**Extract → Load → Transform**

Os dados são:

1. Extraídos;
2. Carregados;
3. Transformados posteriormente.

Esse padrão é muito comum em arquiteturas modernas de Lakehouse.

---

# Data Warehouse e Data Lakehouse

Após o processamento ETL ou ELT, os dados são carregados em um esquema de tabelas.

Isso normalmente ocorre em:

- um **Data Warehouse**, utilizando um mecanismo SQL relacional;
- um **Data Lakehouse**, utilizando abstrações tabulares sobre arquivos armazenados em um Data Lake.

---

# Modelo Semântico (OLAP)

Os dados do Data Warehouse podem ser agregados em um modelo OLAP.

Atualmente, esse modelo é mais conhecido como **Modelo Semântico** (Semantic Model).

Historicamente, era chamado de **Cubo OLAP**.

Valores numéricos (medidas) são agregados a partir das tabelas fato utilizando as dimensões.

**Exemplo**

A receita de vendas pode ser analisada por:

- Data;
- Cliente;
- Produto.

Os modelos semânticos do **Power BI** são um exemplo bastante comum dessa abordagem.

---

# Relatórios e Dashboards

Os dados armazenados no:

- Data Lake;
- Data Warehouse;
- Modelo Semântico;

podem ser utilizados para produzir:

- Relatórios;
- Dashboards;
- Visualizações;
- Indicadores.

---

# Plataformas Modernas de Análise

O Microsoft Azure oferece diversos serviços gerenciados que abrangem todo o pipeline analítico, desde a ingestão dos dados até a geração de relatórios.

As principais plataformas são:

- Microsoft Fabric
- Azure Databricks
- Microsoft Purview

---

# Microsoft Fabric

O **Microsoft Fabric** é uma plataforma SaaS (Software as a Service) unificada.

Ela reúne em um único workspace recursos de:

- Armazenamento;
- Engenharia de Dados;
- Data Warehouse;
- Ciência de Dados;
- Business Intelligence;
- Relatórios.

---

# Azure Databricks

O **Azure Databricks** é uma plataforma voltada para:

- Engenharia de Dados;
- Ciência de Dados;
- Big Data;
- Machine Learning.

Seu formato padrão de armazenamento é o **Delta Lake**, baseado em:

- Parquet;
- Log de transações.

Esse formato permite:

- Controle de versão;
- Transações ACID;
- Atualizações confiáveis.

---

# Microsoft Purview

O **Microsoft Purview** é o serviço responsável por:

- Governança de Dados;
- Segurança;
- Classificação;
- Descoberta;
- Conformidade.

Ele permite descobrir, proteger e gerenciar dados em diferentes fontes.

---

# Arquitetura Medalhão

Uma arquitetura bastante utilizada em Lakehouses é a **Arquitetura Medalhão**.

Ela organiza os dados em três camadas.

## Bronze 🥉

Dados brutos provenientes dos sistemas de origem.

Não há transformações.

O objetivo é preservar os dados originais para reprocessamentos futuros.

---

## Silver 🥈

Dados limpos.

Nesta etapa são realizadas transformações como:

- Remoção de duplicidades;
- Padronização de tipos;
- Tratamento de inconsistências.

---

## Gold 🥇

Dados agregados e preparados para consumo pelo negócio.

São utilizados em:

- Dashboards;
- Relatórios;
- Indicadores;
- Análises.

---

# Resumo

- OLTP → processamento transacional.
- CRUD → operações básicas em bancos de dados.
- ACID → propriedades que garantem integridade das transações.
- OLAP → processamento analítico.
- ETL → Extrair, Transformar e Carregar.
- ELT → Extrair, Carregar e Transformar.
- Data Warehouse → armazenamento analítico estruturado.
- Lakehouse → arquitetura moderna baseada em Data Lake.
- Modelo Semântico → camada utilizada pelo Power BI.
- Microsoft Fabric → plataforma unificada de análise.
- Azure Databricks → engenharia de dados e ciência de dados.
- Microsoft Purview → governança de dados.
- Arquitetura Medalhão → Bronze, Silver e Gold.

---

# 📚 Saiba mais

- https://learn.microsoft.com/training/paths/azure-data-fundamentals-explore-core-data-concepts/
- https://learn.microsoft.com/azure/databricks/
- https://learn.microsoft.com/fabric/
- https://learn.microsoft.com/purview/