# Fórum Hub - Challenge Alura

![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Java](https://img.shields.io/badge/Java-17-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-green)

## 📖 Sobre o Projeto

O **Fórum Hub** é uma API REST completa e funcional desenvolvida como solução para o Challenge do programa Oracle Next Education (ONE) em parceria com a Alura. A aplicação simula um fórum de discussão, permitindo que usuários criem, leiam, atualizem e deletem tópicos, garantindo a segurança das rotas com autenticação e autorização.

Este projeto foi construído para aplicar e solidificar os conhecimentos em desenvolvimento back-end com **Java e Spring Boot**, seguindo as melhores práticas de mercado, como arquitetura RESTful, validações, tratamento de erros e segurança.

## 🚀 Funcionalidades Principais

-   **Autenticação e Autorização:** Controle de acesso via tokens JWT (JSON Web Tokens). Endpoints protegidos que exigem autenticação.
-   **CRUD Completo de Tópicos:**
    -   `POST /topicos`: Criação de um novo tópico (requer autenticação).
    -   `GET /topicos`: Listagem de todos os tópicos.
    -   `GET /topicos/{id}`: Detalhamento de um tópico específico.
    -   `PUT /topicos/{id}`: Atualização de um tópico existente (requer autenticação e autorização do autor).
    -   `DELETE /topicos/{id}`: Exclusão de um tópico (requer autenticação e autorização do autor).
-   **Validações:** Validações de dados de entrada conforme as regras de negócio (ex: não permitir tópicos duplicados).
-   **Banco de Dados:** Persistência de dados utilizando o Spring Data JPA.
-   **Migrações:** Gerenciamento e versionamento do schema do banco de dados com Flyway.
-   **Documentação:** Documentação interativa dos endpoints com Swagger (OpenAPI).

## 🛠️ Tecnologias Utilizadas

Abaixo estão as principais tecnologias e ferramentas usadas na construção da API:

-   **Linguagem:** Java 17
-   **Framework:** Spring Boot 3
-   **Segurança:** Spring Security, JWT (JSON Web Token)
-   **Persistência:** Spring Data JPA / Hibernate
-   **Banco de Dados:** MySQL (ou H2 para ambiente de teste)
-   **Gerenciador de Dependências:** Maven
-   **Migrações de Banco:** Flyway
-   **Documentação:** SpringDoc (Swagger/OpenAPI)
-   **Utilitários:** Lombok

## 📄 Documentação da API

A documentação completa de todos os endpoints disponíveis, incluindo modelos de `request` e `response`, pode ser acessada de forma interativa através do Swagger UI.

Após iniciar a aplicação, acesse a seguinte URL no seu navegador:
[http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

## ⚙️ Como Executar o Projeto

Siga os passos abaixo para rodar o projeto em seu ambiente local.

### Pré-requisitos

-   JDK 17 ou superior
-   Maven 3.8 ou superior
-   Git
-   Um cliente de API (Postman, Insomnia, etc.)
-   MySQL (ou outro banco de dados relacional de sua preferência)

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/meu-forum-hub.git](https://github.com/seu-usuario/meu-forum-hub.git)
    cd meu-forum-hub
    ```

2.  **Configure o Banco de Dados:**
    -   Abra o arquivo `src/main/resources/application.properties`.
    -   Altere as propriedades `spring.datasource.url`, `spring.datasource.username` e `spring.datasource.password` com as credenciais do seu banco de dados local.
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/forumhub
    spring.datasource.username=seu_usuario_mysql
    spring.datasource.password=sua_senha_mysql
    ```

3.  **Execute a aplicação:**
    -   Você pode executar a aplicação diretamente pela sua IDE (Eclipse, IntelliJ) ou pelo terminal usando o Maven.
    ```bash
    mvn spring-boot:run
    ```

4.  **Acesse os endpoints:**
    -   A API estará disponível em `http://localhost:8080`.
    -   Use o Postman ou similar para testar os endpoints, como `POST /login` para obter um token e `GET /topicos` para listar os tópicos.

## ✒️ Autor

Projeto desenvolvido por **[Seu Nome Completo]**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/seu-usuario-linkedin/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/seu-usuario/)

## 🙏 Agradecimentos

Agradeço à **Alura** e à **Oracle** pelo desafio proposto no programa ONE, que proporcionou uma excelente oportunidade para aplicar e aprimorar minhas habilidades em desenvolvimento back-end.
