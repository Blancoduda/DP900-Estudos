# 🗄️ 02 - Tipos de Bancos de Dados

## 🎯 Objetivo

Compreender as diferenças entre bancos de dados relacionais e não relacionais (NoSQL), conhecer seus principais tipos, características e casos de uso, além de entender quando utilizar cada abordagem no Azure.

---

# O que é um banco de dados?

Um banco de dados é um sistema utilizado para armazenar, organizar, consultar e gerenciar informações de forma estruturada.

Seu principal objetivo é permitir que aplicações armazenem dados com segurança, integridade e desempenho.

Exemplos:

- Cadastro de clientes
- Produtos
- Pedidos
- Transações bancárias
- Redes sociais
- Sensores IoT

---

# Bancos de Dados Relacionais

Os bancos de dados relacionais são utilizados para armazenar dados estruturados.

Os dados são organizados em tabelas compostas por:

- Linhas (registros)
- Colunas (atributos)

Cada tabela representa uma entidade do negócio.

Exemplo:

### Clientes

| ID | Nome | Cidade |
|----|-------|---------|
|1|Eduarda|Porto Alegre|
|2|João|São Paulo|

### Pedidos

| Pedido | ClienteID | Valor |
|---------|-----------|-------|
|1001|1|250,00|
|1002|2|89,90|

Observe que o pedido não repete todas as informações do cliente.

Ele apenas armazena o **ClienteID**, criando um relacionamento entre as tabelas.

---

# Chave Primária (Primary Key)

Cada registro possui uma identificação única chamada **Chave Primária (Primary Key)**.

Exemplo:

| ClienteID | Nome |
|-----------|------|
|1|Eduarda|
|2|João|

Nesse caso:

```
ClienteID
```

é a chave primária.

Ela garante que não existam dois clientes com o mesmo identificador.

---

# Chave Estrangeira (Foreign Key)

Uma chave estrangeira referencia a chave primária de outra tabela.

Exemplo:

Pedidos

| Pedido | ClienteID |
|---------|-----------|
|1001|1|

O valor **1** aponta para o cliente Eduarda.

Esse relacionamento evita duplicação de dados.

---

# Normalização

A normalização é um processo utilizado para organizar os dados e reduzir redundâncias.

Seu objetivo é:

- Evitar duplicação
- Melhorar consistência
- Facilitar manutenção

Em vez de repetir os dados do cliente em cada pedido, o banco armazena apenas a referência (ClienteID).

---

# SQL

Os bancos relacionais utilizam SQL (Structured Query Language).

SQL permite:

- Criar tabelas
- Inserir dados
- Atualizar registros
- Excluir registros
- Consultar informações

Exemplo:

```sql
SELECT Nome
FROM Clientes
WHERE Cidade = 'Porto Alegre';
```

---

# Exemplos de Bancos Relacionais

- Microsoft SQL Server
- Azure SQL Database
- PostgreSQL
- MySQL
- Oracle Database

---

# Bancos de Dados Não Relacionais (NoSQL)

Os bancos NoSQL não exigem um esquema fixo.

São ideais para grandes volumes de dados ou dados com estrutura variável.

Eles costumam oferecer:

- Alta escalabilidade
- Alta disponibilidade
- Flexibilidade

---

# Tipos de Bancos NoSQL

## 1. Chave-Valor

Cada informação é composta por:

```
Chave → Valor
```

Exemplo:

```
usuario123
↓

{
  "nome":"Eduarda"
}
```

Ideal para:

- Cache
- Sessões
- Configurações

---

## 2. Documentos

Armazenam documentos JSON completos.

Exemplo:

```json
{
   "cliente":"Eduarda",
   "cidade":"Porto Alegre",
   "idade":26
}
```

Muito utilizado por:

- APIs
- Aplicações Web
- Azure Cosmos DB

---

## 3. Família de Colunas

Organizam dados em grupos de colunas relacionadas.

Muito utilizados em Big Data.

Exemplo:

| Cliente | Dados Pessoais | Compras |
|----------|---------------|----------|

---

## 4. Grafo

Representam entidades como nós e seus relacionamentos.

Exemplo:

```
Eduarda
    │
    │ segue
    ▼
João
```

Muito utilizados em:

- Redes sociais
- Sistemas de recomendação
- Detecção de fraudes

---

# Comparação

| Relacional | Não Relacional |
|------------|----------------|
| Esquema fixo | Esquema flexível |
| SQL | NoSQL |
| Tabelas | Documentos, grafos, chave-valor |
| Integridade forte | Escalabilidade elevada |
| Ideal para transações | Ideal para grandes volumes |

---

# Azure

| Serviço | Tipo |
|----------|------|
| Azure SQL Database | Relacional |
| Azure Database for PostgreSQL | Relacional |
| Azure Cosmos DB | Não Relacional |

---

# Resumo

- Bancos relacionais utilizam tabelas.
- Possuem chave primária e chave estrangeira.
- Utilizam SQL.
- São altamente normalizados.

Já os bancos NoSQL:

- Não exigem esquema fixo.
- São escaláveis.
- Possuem quatro modelos principais:
  - Chave-valor
  - Documento
  - Família de colunas
  - Grafo

---

# 💡 Dicas para a DP-900

✅ Saber diferenciar SQL e NoSQL.

✅ Saber quando utilizar cada um.

✅ Conhecer os quatro tipos de bancos NoSQL.

✅ Saber que o Azure Cosmos DB é um banco NoSQL.

---

# 📚 Saiba mais

- https://learn.microsoft.com/training/modules/explore-relational-data-offerings/
- https://learn.microsoft.com/training/modules/explore-non-relational-data-offerings/
- https://learn.microsoft.com/azure/cosmos-db/introduction