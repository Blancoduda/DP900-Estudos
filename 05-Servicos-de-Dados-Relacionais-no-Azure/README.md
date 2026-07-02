# 🗄️ 05 - Serviços de Dados Relacionais no Azure

## 🎯 Objetivo

Conhecer os principais serviços de banco de dados relacionais oferecidos pelo Microsoft Azure, entender suas características, diferenças e identificar quando utilizar cada solução.

---

# O que são Serviços de Dados Relacionais?

Os serviços de dados relacionais do Azure permitem armazenar dados estruturados utilizando tabelas, relacionamentos e SQL.

Eles são indicados para aplicações que necessitam de:

- Integridade dos dados
- Alta disponibilidade
- Escalabilidade
- Segurança
- Transações ACID

Todos seguem o modelo relacional baseado em tabelas.

---

# Azure SQL Database

O **Azure SQL Database** é um serviço de banco de dados totalmente gerenciado (PaaS).

É baseado no Microsoft SQL Server, porém sem a necessidade de administrar servidores físicos ou máquinas virtuais.

---

## Principais características

- Serviço totalmente gerenciado
- Atualizações automáticas
- Backups automáticos
- Alta disponibilidade
- Escalabilidade automática
- Segurança integrada

---

## Quando utilizar?

Ideal para:

- Aplicações Web
- Sistemas corporativos
- APIs
- Sistemas financeiros
- ERP
- CRM

---

# Azure SQL Managed Instance

O **Azure SQL Managed Instance** oferece quase 100% de compatibilidade com o SQL Server tradicional.

Foi criado para facilitar migrações de aplicações existentes para a nuvem.

---

## Principais características

- Compatibilidade elevada com SQL Server
- Recursos avançados de administração
- Menor necessidade de alterações nas aplicações
- Ambiente gerenciado pela Microsoft

---

## Quando utilizar?

- Migração de bancos SQL Server existentes
- Aplicações legadas
- Sistemas corporativos complexos

---

# SQL Server em Máquina Virtual (IaaS)

Também é possível executar o SQL Server dentro de uma Máquina Virtual no Azure.

Nesse modelo o cliente continua responsável por:

- Sistema Operacional
- Atualizações
- Backup
- Segurança
- Administração do banco

---

## Quando utilizar?

Quando existe necessidade de controle total do ambiente.

---

# Comparação

| Serviço | Modelo |
|---------|---------|
| Azure SQL Database | PaaS |
| Azure SQL Managed Instance | PaaS |
| SQL Server em Máquina Virtual | IaaS |

---

# PaaS x IaaS

## PaaS (Platform as a Service)

A Microsoft administra:

- Infraestrutura
- Sistema Operacional
- Atualizações
- Banco de Dados

O cliente administra apenas:

- Dados
- Aplicação

---

## IaaS (Infrastructure as a Service)

O cliente administra:

- Máquina Virtual
- Sistema Operacional
- SQL Server
- Backups
- Atualizações

A Microsoft administra apenas a infraestrutura física.

---

# Escalabilidade

Os serviços relacionais do Azure permitem aumentar ou reduzir recursos conforme a necessidade.

É possível alterar:

- CPU
- Memória
- Armazenamento

Sem necessidade de substituir servidores físicos.

---

# Alta Disponibilidade

Todos os serviços oferecem mecanismos para minimizar indisponibilidades.

Exemplos:

- Replicação
- Failover automático
- Backups automáticos

---

# Segurança

Os bancos relacionais do Azure oferecem recursos integrados de segurança.

Entre eles:

- Criptografia
- Firewall
- Autenticação Azure AD
- Controle de acesso
- Auditoria

---

# Comparação Geral

| Característica | Azure SQL Database | Managed Instance | SQL VM |
|----------------|-------------------|------------------|--------|
| Gerenciado | ✅ | ✅ | ❌ |
| Compatibilidade SQL Server | Alta | Muito Alta | Total |
| Administração | Baixa | Média | Alta |
| Modelo | PaaS | PaaS | IaaS |

---

# Resumo

- Azure SQL Database é totalmente gerenciado.
- Managed Instance facilita migrações.
- SQL Server em VM oferece maior controle.
- Azure administra praticamente tudo em PaaS.
- No modelo IaaS a administração é responsabilidade do cliente.

---

# 🎯 O que costuma cair na DP-900

✅ Azure SQL Database

✅ Azure SQL Managed Instance

✅ SQL Server em Máquina Virtual

✅ Diferença entre PaaS e IaaS

✅ Compatibilidade com SQL Server

---

# 📚 Saiba mais

- https://learn.microsoft.com/azure/azure-sql/
- https://learn.microsoft.com/azure/azure-sql/database/
- https://learn.microsoft.com/azure/azure-sql/managed-instance/
- https://learn.microsoft.com/azure/azure-sql/virtual-machines/

---

## 📌 Próximo módulo

➡️ **06 - Serviços de Dados Não Relacionais no Azure**