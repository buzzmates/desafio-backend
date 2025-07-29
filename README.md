
# Desafio Técnico - Desenvolvedor Backend (NestJS)

## Visão Geral - O que é esperado?
O objetivo deste desafio é avaliar suas habilidades com NestJS na criação de uma aplicação simples, onde você vai gerenciar tarefas e categorias. Queremos ver como você organiza o código, implementa boas práticas e estrutura a aplicação.

## Descrição do Sistema:
O sistema a ser desenvolvido é uma **TODO list**, onde cada tarefa pode ser associada a uma categoria. O candidato deverá implementar uma API RESTful que permita criar, ler, atualizar e excluir tanto as tarefas quanto as categorias dessas tarefas.

O sistema deve permitir que o usuário crie uma tarefa com um título e descrição, podendo também associar essa tarefa a uma categoria específica. Cada tarefa terá um status que pode ser alterado entre "pendente" e "concluída". Além disso, o sistema deverá permitir a criação, atualização, listagem e exclusão de categorias, que podem ser usadas para organizar as tarefas.

## Estrutura do Projeto:
O candidato deverá criar um projeto utilizando o **NestJS** com as funcionalidades descritas a seguir:

### 1. Tarefas (TODOs):
Cada tarefa no sistema terá um título, uma descrição, um status (pendente ou concluída) e estará associada a uma categoria. A API deverá ser capaz de realizar as operações de CRUD para as tarefas. Quando o usuário criar uma nova tarefa, ele deverá fornecer um título, uma descrição e escolher a categoria à qual a tarefa será associada. O sistema deve validar se todos os campos obrigatórios estão preenchidos.

O status de cada tarefa pode ser alterado, permitindo que o usuário marque uma tarefa como concluída ou pendente. A API deverá permitir que o usuário recupere uma lista de todas as tarefas, consulte detalhes de uma tarefa específica, edite as informações de uma tarefa e exclua uma tarefa do sistema.

### 2. Categorias:
O sistema permitirá a criação de categorias que serão usadas para organizar as tarefas. Cada categoria terá um nome e uma descrição. As categorias devem ser capazes de ser manipuladas através da API, permitindo a criação de novas categorias, a listagem das categorias existentes, a atualização de informações e a exclusão de categorias.

Cada tarefa estará associada a uma categoria, portanto, ao criar ou atualizar uma tarefa, o usuário deverá selecionar a categoria à qual ela pertence. O sistema deve garantir que, ao listar as tarefas, a categoria associada a cada uma delas seja incluída nos resultados.

## Funcionalidades da API:
- **Tarefas:**
  - **POST /todos**: Criar uma nova tarefa com título, descrição, status e categoria.
  - **GET /todos**: Listar todas as tarefas, incluindo a categoria associada a cada tarefa.
  - **GET /todos/:id**: Recuperar os detalhes de uma tarefa específica.
  - **PUT /todos/:id**: Atualizar os detalhes de uma tarefa, incluindo título, descrição e status.
  - **DELETE /todos/:id**: Excluir uma tarefa do sistema.

- **Categorias:**
  - **POST /categories**: Criar uma nova categoria.
  - **GET /categories**: Listar todas as categorias.
  - **GET /categories/:id**: Recuperar os detalhes de uma categoria específica.
  - **PUT /categories/:id**: Atualizar o nome e a descrição de uma categoria.
  - **DELETE /categories/:id**: Excluir uma categoria do sistema.

## Requisitos Técnicos:
O candidato deve utilizar preferencialmente as ferramentas e bibliotecas oferecidas pelo [NestJS](https://nestjs.com/) para implementar a API. Entre elas, deve-se utilizar o **class-validator** para validar as entradas de dados nas requisições e o **class-transformer** para garantir a correta transformação dos dados entre as entidades e a resposta da API.

## Opcionais:
Como tarefa extra, o candidato pode:
- Adicionar a funcionalidade de pesquisa de tarefas, permitindo que os usuários filtrem as tarefas por categoria ou status.
- Implementar uma autenticação simples utilizando **BEARER TOKEN**, para garantir que apenas usuários autenticados possam realizar operações de criação, edição e exclusão de tarefas e categorias.

## Critérios de Avaliação:
A avaliação do desafio será baseada nos seguintes pontos:
- **Funcionalidade:** A API deve ser capaz de criar, listar, atualizar e excluir tanto as tarefas quanto as categorias de forma funcional e sem erros.
- **Qualidade do Código:** O código deve ser bem estruturado, modularizado e fácil de entender.
- **Uso do NestJS:** A implementação deve demonstrar o uso correto dos principais recursos do NestJS, como decorators, injeção de dependências e módulos.
- **Boas Práticas:** O código deve seguir boas práticas de programação, como a utilização de tipagem forte, nomes de variáveis claros e funções bem definidas.
- **Documentação:** A API deve ser bem documentada utilizando o **Swagger**, com exemplos de requisições e respostas para facilitar os testes da API.

## Entrega:
O candidato deve enviar o código-fonte completo em um repositório Git (preferencialmente GitHub ou GitLab), juntamente com instruções claras de como rodar o projeto localmente.
