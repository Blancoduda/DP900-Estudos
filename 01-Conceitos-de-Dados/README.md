# 📊 01 - Conceitos de Dados

## 🎯 Objetivo

Compreender os principais conceitos de dados, conhecer os diferentes tipos de dados utilizados pelas organizações, entender como eles são armazenados e identificar os formatos de arquivos mais utilizados em soluções modernas de dados.

---

# O que são dados?

Dados são uma coleção de fatos, como números, descrições e observações utilizados para registrar informações.

As estruturas de dados normalmente representam entidades importantes para uma organização.

Exemplos de entidades:

- Cliente
- Produto
- Pedido
- Funcionário

Cada entidade possui atributos (características).

### Exemplo

| Entidade | Atributos |
|----------|-----------|
| Cliente | Nome, Endereço, Telefone, E-mail |
| Produto | Código, Nome, Preço |
| Pedido | Número, Data, Valor |

---

# Tipos de Dados

Os dados podem ser classificados em três categorias principais.

## Dados Estruturados

Dados estruturados seguem um esquema fixo.

Todos os registros possuem exatamente os mesmos campos.

Normalmente são armazenados em tabelas compostas por linhas e colunas.

### Exemplo

| ID | Nome | Cidade |
|----|-------|---------|
|1|Eduarda|Porto Alegre|
|2|João|São Paulo|

### Exemplos de uso

- Bancos relacionais
- SQL Server
- Azure SQL Database
- PostgreSQL
- MySQL

---

## Dados Semiestruturados

Possuem uma estrutura flexível.

Nem todos os registros precisam possuir exatamente os mesmos campos.

O formato mais comum é o **JSON (JavaScript Object Notation)**.

### Exemplo

```json
{
  "cliente":"Eduarda",
  "cidade":"Porto Alegre",
  "emails":[
      "eduarda@email.com",
      "contato@email.com"
  ]
}
```

### Exemplos de uso

- APIs REST
- Azure Cosmos DB
- MongoDB

---

## Dados Não Estruturados

Não possuem uma estrutura definida.

Exemplos:

- Imagens
- Vídeos
- Áudios
- PDFs
- Documentos Word

As organizações também trabalham cada vez mais com **dados vetoriais (Embeddings)** utilizados por aplicações de Inteligência Artificial.

---

# Armazenamento de Dados

Os dados podem ser armazenados para registrar:

- Clientes
- Produtos
- Vendas
- Documentos
- Imagens
- Logs
- Vídeos

Posteriormente, esses dados podem ser utilizados para:

- Relatórios
- Dashboards
- Business Intelligence
- Machine Learning
- Inteligência Artificial

---

# Categorias de Armazenamento

Existem duas categorias principais.

## Armazenamento em Arquivos

Exemplos:

- CSV
- JSON
- XML
- Parquet
- Avro
- Imagens
- Vídeos

---

## Bancos de Dados

Utilizados para organizar, consultar e manter os dados.

Exemplos:

- Bancos Relacionais
- Bancos NoSQL
- Data Warehouse
- Lakehouse

---

# Como escolher um formato?

A escolha depende de fatores como:

- Tipo de dado
- Aplicações que irão consumir os dados
- Necessidade de leitura humana
- Eficiência de armazenamento
- Performance

---

# Arquivos Delimitados

O formato mais comum é o **CSV (Comma Separated Values)**.

Os campos são separados por vírgulas.

### Exemplo

```csv
id,nome,cidade
1,Eduarda,Porto Alegre
2,João,São Paulo
```

Outros formatos:

- TSV (Tab Separated Values)
- Delimitado por espaço
- Largura fixa

---

# JSON (JavaScript Object Notation)

JSON representa informações utilizando objetos e atributos.

É um formato extremamente utilizado por APIs.

### Exemplo

```json
{
    "id":1,
    "nome":"Eduarda",
    "cidade":"Porto Alegre"
}
```

Muito utilizado em:

- APIs
- Azure Cosmos DB
- Aplicações Web

---

# XML (Extensible Markup Language)

Formato bastante utilizado em sistemas legados.

Utiliza tags para representar informações.

### Exemplo

```xml
<cliente>
    <nome>Eduarda</nome>
    <cidade>Porto Alegre</cidade>
</cliente>
```

---

# BLOB (Binary Large Object)

BLOB representa arquivos armazenados em formato binário.

Exemplos:

- Imagens
- Vídeos
- Áudios
- PDFs

No Azure esse tipo de armazenamento é representado pelo **Azure Blob Storage**.

---

# Formatos Otimizados

Para grandes volumes de dados existem formatos especializados.

## Parquet

Formato colunar otimizado para consultas analíticas.

Características:

- Alta compressão
- Alta performance
- Muito utilizado em Data Lakes
- Muito utilizado no Microsoft Fabric
- Muito utilizado no Azure Databricks

---

## Avro

Formato baseado em linhas.

Características:

- Compactação eficiente
- Muito utilizado em Big Data
- Excelente para transmissão de dados

---

## Delta Lake

Formato baseado em Parquet.

Adiciona:

- Transações ACID
- Controle de versão
- Atualizações confiáveis

Muito utilizado em:

- Azure Databricks
- Microsoft Fabric

---

# Comparação

| Formato | Melhor utilização |
|----------|-------------------|
| CSV | Dados simples |
| JSON | APIs |
| XML | Sistemas legados |
| BLOB | Arquivos binários |
| Parquet | Analytics |
| Avro | Streaming |
| Delta Lake | Lakehouse |

---

# Resumo

- Dados podem ser estruturados, semiestruturados ou não estruturados.
- CSV é simples e legível.
- JSON é flexível.
- XML ainda aparece em sistemas antigos.
- BLOB armazena arquivos binários.
- Parquet é colunar.
- Avro é baseado em linhas.
- Delta Lake adiciona ACID ao Parquet.

---

# 🎯 O que costuma cair na DP-900

✅ Diferença entre:

- Dados estruturados
- Dados semiestruturados
- Dados não estruturados

✅ Saber reconhecer:

- CSV
- JSON
- XML
- Parquet
- Avro
- Delta Lake

✅ Relacionar os formatos com seus casos de uso.

---

# 📚 Saiba mais

- https://learn.microsoft.com/training/paths/azure-data-fundamentals-explore-core-data-concepts/
- https://learn.microsoft.com/azure/storage/blobs/
- https://learn.microsoft.com/azure/databricks/
- https://learn.microsoft.com/fabric/
- https://learn.microsoft.com/azure/storage/blobs/data-lake-storage-introduction

---

## 📌 Próximo módulo

➡️ **02 - Tipos de Bancos de Dados**