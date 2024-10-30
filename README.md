# DSList - Projeto de Lista de Jogos

Este repositório contém o projeto **DSList**, desenvolvido em **Java** com **Spring Boot**. O objetivo do projeto é criar uma API REST para gerenciar uma lista de jogos, com funcionalidades que permitem listar, ordenar e organizar jogos em listas personalizadas.

## Tecnologias Utilizadas

- **Java** 17
- **Spring Boot** 3+
- **JPA/Hibernate**
- **H2 Database** (para ambiente de desenvolvimento)
- **PostgreSQL** (para ambiente de produção)
- **Maven** (gerenciador de dependências)

## Funcionalidades

- **Listagem de Jogos**: Exibe jogos cadastrados no sistema.
- **Listagem por Categorias**: Possibilidade de listar jogos por diferentes categorias.
- **Reordenação de Jogos**: Organize os jogos em listas personalizadas, com possibilidade de reordenar os jogos na lista.
  
## Estrutura do Projeto

O projeto segue uma arquitetura organizada em camadas:

- **Entities**: Classes que representam as tabelas no banco de dados.
- **Repositories**: Interfaces para o acesso aos dados, implementadas pelo Spring Data JPA.
- **Services**: Contêm a lógica de negócios da aplicação.
- **Controllers**: Exposição dos endpoints da API REST.

## Como Executar o Projeto

### Pré-requisitos

- **Java 17** ou superior.
- **Maven** instalado para gerenciamento de dependências.

### Passo a Passo

1. Clone o repositório:

   ```bash
   git clone https://github.com/KauanOliveira1/dslist.git
   cd dslist

2. Compile e execute o projeto usando o Maven:

   ```bash
   mvn spring-boot:run
   
3. Acesse a aplicação na URL: http://localhost:8080

   ```bash
   mvn spring-boot:run

## Endpoints Principal

- GET /games: Lista todos os jogos cadastrados.
- GET /games/{id}: Retorna as informações de um jogo específico.
- GET /lists: Lista todas as listas de jogos.
- POST /lists: Cria uma nova lista de jogos.
- POST /lists/{listId}/games: Adiciona um jogo a uma lista específica.
- PUT /lists/{listId}/games/reorder: Reordena a posição dos jogos em uma lista.

## Estrutura de Dados

### Exemplo de JSON para **Jogo**

```json
{
  "title": "The Legend of Zelda",
  "genre": "Aventura",
  "platform": "Nintendo Switch",
  "score": 9.8
}
```

### Exemplo de JSON para **Lista de Jogos**

```json
{
  "name": "Favoritos",
  "games": [
    { "id": 1, "title": "The Legend of Zelda" },
    { "id": 2, "title": "Super Mario Odyssey" }
  ]
}
```
## Banco de Dados
O projeto usa o H2 Database para ambiente de desenvolvimento e PostgreSQL para produção. As configurações de cada banco de dados podem ser ajustadas no arquivo application.properties conforme o ambiente.

