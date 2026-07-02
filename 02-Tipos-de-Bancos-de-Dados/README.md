# 🗄️ 02 - Tipos de Bancos de Dados

## 🎯 Objetivo

Compreender os principais tipos de bancos de dados utilizados atualmente, conhecer as diferenças entre bancos de dados relacionais e não relacionais (NoSQL), identificar seus principais modelos e entender quando utilizar cada um deles.

---

# O que é um Banco de Dados?

Um banco de dados é um sistema utilizado para armazenar, organizar, consultar e gerenciar informações de forma estruturada.

Seu principal objetivo é armazenar dados de maneira segura, organizada e eficiente, permitindo que aplicações consultem e atualizem essas informações.

Exemplos de utilização:

- Cadastro de clientes
- Produtos
- Pedidos
- Contas bancárias
- Redes sociais
- Sensores IoT

---

# Bancos de Dados Relacionais

Os bancos de dados relacionais são comumente utilizados para armazenar e consultar **dados estruturados**.

Os dados são organizados em tabelas que representam entidades, como:

- Clientes
- Produtos
- Pedidos
- Funcionários

Cada linha representa um registro e cada coluna representa um atributo da entidade.

## Exemplo

### Clientes

| ClienteID | Nome | Cidade |
|------------|--------|-----------|
| 1 | Eduarda | Porto Alegre |
| 2 | João | São Paulo |

### Pedidos

| PedidoID | ClienteID | Valor |
|------------|------------|---------|
| 1001 | 1 | R$ 250,00 |
| 1002 | 2 | R$ 89,90 |

Observe que a tabela **Pedidos** não armazena novamente o nome do cliente.

Ela apenas referencia o **ClienteID**.

---

# Chave Primária (Primary Key)

Cada registro possui uma identificação única chamada **Chave Primária**.

Ela garante que dois registros nunca tenham o mesmo identificador.

Exemplo:

| ClienteID | Nome |
|------------|---------|
| 1 | Eduarda |
| 2 | João |

Neste caso:

```
ClienteID
```

é a chave primária.

---

# Chave Estrangeira (Foreign Key)

A chave estrangeira é utilizada para relacionar tabelas.

Ela faz referência à chave primária de outra tabela.

Exemplo:

Pedidos

| PedidoID | ClienteID |
|------------|------------|
|1001|1|

O valor **1** faz referência ao cliente Eduarda.

---

# Normalização

Os bancos relacionais utilizam um processo chamado **Normalização**.

Seu objetivo é:

- Eliminar dados duplicados
- Reduzir redundância
- Garantir consistência
- Facilitar manutenção

Por exemplo, os dados do cliente são armazenados apenas uma vez, mesmo que ele realize vários pedidos.

---

# SQL (Structured Query Language)

Os bancos relacionais utilizam a linguagem SQL para gerenciar os dados.

Com SQL é possível:

- Criar tabelas
- Inserir registros
- Atualizar registros
- Excluir registros
- Consultar informações

### Exemplo

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

Os bancos de dados não relacionais **não exigem um esquema fixo**.

Também são conhecidos como **NoSQL (Not Only SQL)**.

São indicados para aplicações que precisam de:

- Escalabilidade
- Flexibilidade
- Alto volume de dados
- Alta disponibilidade

Alguns bancos NoSQL oferecem suporte a uma variante da linguagem SQL.

---

# Tipos de Bancos NoSQL

Existem quatro modelos principais.

---

## 🔑 Banco de Dados Chave-Valor

Cada registro é composto por:

```
Chave → Valor
```

Exemplo

```
usuario123

↓

{
   "nome":"Eduarda"
}
```

Ideal para:

- Cache
- Sessões de usuários
- Configurações

---

## 📄 Banco de Dados de Documentos

É uma evolução do modelo chave-valor.

O valor armazenado normalmente é um documento JSON.

Exemplo

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

## 📊 Banco de Dados Família de Colunas

Armazena dados em linhas e colunas.

As colunas podem ser agrupadas em famílias de colunas relacionadas.

Exemplo

| Cliente | Dados Pessoais | Compras |
|----------|----------------|----------|

Muito utilizado em soluções Big Data.

---

## 🕸️ Banco de Dados em Grafo

Armazena entidades como **nós** conectados por **relacionamentos**.

Exemplo

```text
Eduarda
    │
 segue
    │
João
```

Muito utilizado em:

- Redes sociais
- Sistemas de recomendação
- Detecção de fraudes
- Mapas de relacionamento

---

# Comparação

| Banco Relacional | Banco Não Relacional |
|-----------------|----------------------|
| Dados estruturados | Dados estruturados e semiestruturados |
| Esquema fixo | Esquema flexível |
| Utiliza SQL | Utiliza NoSQL |
| Tabelas | Documentos, Grafos, Chave-Valor e Colunas |
| Alta consistência | Alta escalabilidade |
| Ideal para transações | Ideal para grandes volumes de dados |

---

# Serviços Azure

| Serviço | Tipo |
|----------|------|
| Azure SQL Database | Relacional |
| Azure Database for PostgreSQL | Relacional |
| Azure Database for MySQL | Relacional |
| Azure Cosmos DB | Não Relacional |

---

# Resumo

- Bancos relacionais armazenam dados em tabelas.
- Utilizam chaves primárias e estrangeiras.
- Utilizam SQL.
- São altamente normalizados.

Já os bancos NoSQL:

- Não exigem esquema fixo.
- São altamente escaláveis.
- Possuem quatro modelos principais:
  - Chave-Valor
  - Documento
  - Família de Colunas
  - Grafo

---

# 🎯 O que costuma cair na DP-900

✅ Diferença entre SQL e NoSQL.

✅ Identificar quando utilizar bancos relacionais.

✅ Identificar quando utilizar bancos NoSQL.

✅ Conhecer os quatro modelos NoSQL.

✅ Saber que:

- Azure SQL Database → Banco Relacional
- Azure Cosmos DB → Banco Não Relacional

---

# 📚 Saiba mais

- https://learn.microsoft.com/training/modules/explore-relational-data-offerings/
- https://learn.microsoft.com/training/modules/explore-non-relational-data-offerings/
- https://learn.microsoft.com/azure/azure-sql/
- https://learn.microsoft.com/azure/cosmos-db/introduction

---

## 📌 Próximo módulo

➡️ **03 - Processamento Transacional e Analítico**