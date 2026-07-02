# 🌌 06 - Serviços de Dados Não Relacionais no Azure

## 🎯 Objetivo

Conhecer os principais serviços de armazenamento de dados não relacionais do Microsoft Azure, entender suas características, diferenças e identificar quando utilizar cada solução.

---

# O que são Serviços de Dados Não Relacionais?

Os serviços de dados não relacionais permitem armazenar informações que não seguem necessariamente um esquema fixo de tabelas.

Esses serviços são ideais para aplicações que precisam de:

- Alta escalabilidade
- Flexibilidade
- Alta disponibilidade
- Grandes volumes de dados
- Diferentes formatos de armazenamento

No Azure, os principais serviços são:

- Azure Storage
- Azure Cosmos DB

---

# Azure Storage

O **Azure Storage** é um serviço de armazenamento altamente escalável, seguro e durável.

Ele permite armazenar diferentes tipos de dados utilizados por aplicações modernas.

---

## Tipos de armazenamento

O Azure Storage oferece quatro principais serviços.

### Azure Blob Storage

Armazena grandes quantidades de dados não estruturados.

Exemplos:

- Imagens
- Vídeos
- PDFs
- Arquivos
- Backups
- Logs

É um dos serviços mais utilizados em Data Lakes.

---

### Azure Files

Fornece compartilhamento de arquivos na nuvem.

Pode ser acessado por diferentes máquinas utilizando protocolos padrão como SMB.

Ideal para:

- Compartilhamento de arquivos
- Migração de File Servers
- Aplicações legadas

---

### Azure Queue Storage

Serviço utilizado para troca de mensagens entre aplicações.

Permite desacoplar sistemas.

Muito utilizado em arquiteturas distribuídas.

---

### Azure Table Storage

Banco NoSQL baseado em chave-valor.

Armazena grandes volumes de dados estruturados sem exigir um esquema relacional.

---

# Azure Cosmos DB

O **Azure Cosmos DB** é o banco de dados NoSQL totalmente gerenciado da Microsoft.

Foi desenvolvido para aplicações distribuídas globalmente.

---

## Principais características

- Banco NoSQL
- Distribuição global
- Alta disponibilidade
- Escalabilidade automática
- Baixa latência
- Totalmente gerenciado

---

## Modelos suportados

O Azure Cosmos DB suporta diferentes APIs.

Entre elas:

- SQL API
- MongoDB
- Cassandra
- Gremlin (Grafos)
- Table API

---

# Quando utilizar o Cosmos DB?

Ideal para:

- Aplicações Web
- Jogos Online
- IoT
- Redes Sociais
- Aplicações Globais
- APIs

---

# Azure Storage x Azure Cosmos DB

| Azure Storage | Azure Cosmos DB |
|---------------|-----------------|
| Armazena arquivos | Banco NoSQL |
| Blob, Files, Queue e Table | Documentos, grafos e chave-valor |
| Muito utilizado em Data Lakes | Muito utilizado por aplicações distribuídas |
| Armazenamento | Banco de Dados |

---

# Blob Storage

O Blob Storage é o principal serviço para armazenamento de arquivos.

Pode armazenar:

- Fotos
- Vídeos
- Documentos
- Backups
- Dados de Data Lake

É altamente escalável e durável.

---

# Azure Data Lake Storage Gen2

O **Azure Data Lake Storage Gen2** é uma extensão do Azure Blob Storage.

Ele adiciona recursos específicos para análise de dados.

Entre eles:

- Hierarquia de diretórios
- Melhor desempenho
- Controle refinado de permissões
- Compatibilidade com Hadoop

É amplamente utilizado por:

- Microsoft Fabric
- Azure Databricks
- Azure Synapse Analytics

---

# Comparação Geral

| Serviço | Principal utilização |
|----------|----------------------|
| Azure Blob Storage | Arquivos não estruturados |
| Azure Files | Compartilhamento de arquivos |
| Azure Queue Storage | Mensageria |
| Azure Table Storage | Chave-Valor |
| Azure Cosmos DB | Banco NoSQL |
| Azure Data Lake Storage Gen2 | Data Lakes |

---

# Resumo

- Azure Storage oferece diferentes formas de armazenamento.
- Blob Storage armazena dados não estruturados.
- Azure Files compartilha arquivos.
- Queue Storage permite comunicação entre aplicações.
- Table Storage é um banco chave-valor.
- Azure Cosmos DB é o principal banco NoSQL do Azure.
- Azure Data Lake Storage Gen2 é otimizado para análises em larga escala.

---

# 🎯 O que costuma cair na DP-900

✅ Azure Blob Storage.

✅ Azure Files.

✅ Azure Queue Storage.

✅ Azure Table Storage.

✅ Azure Cosmos DB.

✅ Azure Data Lake Storage Gen2.

✅ Diferença entre Azure Storage e Cosmos DB.

---

# 📚 Saiba mais

- https://learn.microsoft.com/azure/storage/
- https://learn.microsoft.com/azure/storage/blobs/
- https://learn.microsoft.com/azure/storage/files/
- https://learn.microsoft.com/azure/storage/queues/
- https://learn.microsoft.com/azure/storage/tables/
- https://learn.microsoft.com/azure/cosmos-db/
- https://learn.microsoft.com/azure/storage/blobs/data-lake-storage-introduction

---

## 📌 Próximo módulo

➡️ **07 - Análise de Dados em Escala no Azure**