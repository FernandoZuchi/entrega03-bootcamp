# Enunciado da Entrega 03 - Implementação de Banco de Dados no Sistema de Gerenciamento de Solicitações de Suporte e Problemas Técnicos (SGSSPT)

## Objetivo
O objetivo desta entrega prática é implementar um banco de dados relacional no projeto desenvolvido na Entrega 01, utilizando **SQL Server** e **Entity Framework 6** como ORM (Object-Relational Mapping). A integração com o banco de dados permitirá que as operações de criação, edição, visualização, e exclusão de tickets sejam persistidas no banco, elevando o nível de realismo do projeto e adicionando escalabilidade à aplicação.

---

## Descrição
Nesta entrega, os dados dos tickets, que anteriormente eram armazenados em uma lista estática, deverão ser persistidos em um banco de dados relacional. Para isso, será necessário criar um modelo de banco de dados que atenda aos requisitos do sistema e configurar a conexão com o **SQL Server** utilizando o **Entity Framework 6** em sua abordagem **Code First**.

Os tickets deverão ser armazenados em uma tabela no banco de dados, e o sistema deverá ser capaz de realizar todas as operações (CRUD) diretamente no banco.

---

## Requisitos do Projeto

### 1. Configuração do Banco de Dados:
- Criar e configurar um banco de dados no **SQL Server** para armazenar os tickets.
- Configurar a string de conexão no arquivo `Web.config`.

### 2. Modelagem de Dados:
- Criar uma classe de modelo chamada `Ticket` que represente os tickets do sistema.
- Incluir os seguintes campos na tabela de tickets:
  - **Id**: Identificador único (chave primária).
  - **Título**: Nome ou descrição breve do chamado.
  - **Descrição**: Detalhamento do chamado.
  - **Status**: Status do chamado (aberto, em andamento, fechado).
  - **Prioridade**: Nível de prioridade do chamado (alta, média, baixa).
  - **DataAbertura**: Data e hora de criação do chamado.

### 3. Migração do Banco de Dados (Code First):
- Configurar o **Entity Framework 6** para usar o banco de dados em modo **Code First**.
- Criar as migrações necessárias para gerar a tabela de tickets no banco.

### 4. Atualização dos Controladores e Views:
- Atualizar o controlador `TicketController` para que as operações de listagem, criação, edição, exclusão e visualização de tickets sejam feitas diretamente no banco de dados.
- Atualizar as **Views** para refletir as mudanças e garantir que os dados exibidos sejam provenientes do banco.

### 5. Validações e Boas Práticas:
- Adicionar validações apropriadas no modelo `Ticket`, como `[Required]`, `[StringLength]`, entre outras.
- Garantir que as operações sejam seguras, evitando possíveis falhas ou comportamentos inesperados.

---

## Entrega e Avaliação
A entrega deverá ser feita em um repositório Git com os commits claros e descritivos. O repositório deverá conter:
1. Código atualizado com a integração do banco de dados.
2. Instruções no arquivo `README.md` para configurar a string de conexão e executar o projeto.

OBS: Faça um tópico nesta própria documentação, indicando as instruções para conectar com o banco de dados criado por você

### **Pontos de Avaliação (10 pontos):**

#### 1. Configuração do Banco de Dados e Entity Framework (2 pontos):
- Configuração correta do SQL Server e string de conexão.
- Criação das migrações para a tabela de tickets.

#### 2. Modelagem de Dados (2 pontos):
- Definição do modelo `Ticket` com todos os campos necessários.
- Validações adequadas no modelo.

#### 3. Atualização do Código (3 pontos):
- Ajuste dos controladores para usar o banco de dados nas operações CRUD.
- Atualização das views para refletir as alterações.

#### 4. Boas Práticas e Organização (2 pontos):
- Código limpo e bem estruturado.
- Commit frequente e claro.

#### 5. Testes de Funcionalidade (1 ponto):
- Teste de todas as operações CRUD com persistência no banco.

---

## Checklist 🗒️
Use o checklist abaixo para garantir que todos os requisitos foram atendidos:

- [ ] Configuração do banco de dados no SQL Server.
- [ ] Configuração da string de conexão no `Web.config`.
- [ ] Implementação da classe de modelo `Ticket`.
- [ ] Migração do banco de dados com o **Entity Framework 6**.
- [ ] Atualização do controlador para usar o banco de dados.
- [ ] Atualização das views para refletir as mudanças.
- [ ] Validações no modelo de dados.
- [ ] Teste completo de todas as operações CRUD.

---

## Dicas
- Revise o conteúdo do módulo **T4: Banco de Dados no ASP.NET MVC** antes de iniciar a implementação.
- Utilize o `SQL Server Management Studio` para verificar as tabelas e dados diretamente no banco.
- Caso enfrente problemas com migrações, use o comando `Add-Migration` e `Update-Database` no console do Gerenciador de Pacotes.
- Siga as boas práticas aprendidas nos módulos anteriores para manter o código limpo e escalável.

Boa sorte e bom trabalho! 🚀

