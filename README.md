
# Welcome to the Cookmaster Project Repository!

This app was developed as part of the backend module in the Trybe Web Development course.

The project utilizes the MSC architecture and includes user registration and login functionality. Only registered users can access, modify, and delete the recipes they have created.

The goal was to enhance understanding of authentication tokens, file uploads, route authentication, and saving files on the server 🚀


# Boas vindas ao repositório do projeto Cookmaster!

App desenvolvido no módulo de backend do curso de Desenvolvimento Web da Trybe. 

Este projeto utiliza a arquitetura MSC e inclui funcionalidade de cadastro e login de pessoas usuárias, onde apenas essas pessoas poderão acessar, modificar e deletar as receitas que cadastraram. 

O objetivo foi desenvolver o entendimento acerca de tokens de autenticação, upload de arquivos, autenticação de rotas, salvamento de arquivos no servidor 🚀

---
# Table of Contents

- [Welcome to the Cookmaster Project Repository!] (#welcome-to-the-cookmaster-project-repository)
- [Skills](#skills)
- [Development](#development)
- [Submission Date](#submission-date)
- [Database Connection](#database-connection)
- [Collections](#collections)
- [Project Requirements](#project-requirements)
- [Mandatory Requirements](#mandatory-requirements)
  - [1 - Create an endpoint for user registration](#1---create-an-endpoint-for-user-registration)
  - [2 - Create an endpoint for user login](#2---create-an-endpoint-for-user-login)
  - [3 - Create an endpoint for recipe creation](#3---create-an-endpoint-for-recipe-creation)
  - [4 - Create an endpoint for recipe listing](#4---create-an-endpoint-for-recipe-listing)
  - [5 - Create an endpoint for viewing a specific recipe](#5---create-an-endpoint-for-viewing-a-specific-recipe)
  - [6 - Create a Mongo query to insert an admin user](#6---create-a-mongo-query-to-insert-an-admin-user)
  - [7 - Create an endpoint for editing a recipe](#7---create-an-endpoint-for-editing-a-recipe)
  - [8 - Create an endpoint for deleting a recipe](#8---create-an-endpoint-for-deleting-a-recipe)
  - [9 - Create an endpoint for adding an image to a recipe](#9---create-an-endpoint-for-adding-an-image-to-a-recipe)
  - [10 - Create an endpoint for accessing a recipe’s image](#10---create-an-endpoint-for-accessing-a-recipes-image)
  - [11 - Create integration tests that cover at least 30% of files in src, with a minimum of 50 lines covered](#11---create-integration-tests-that-cover-at-least-30-of-files-in-src-within-a-minimum-of-50-lines-covered)
- [Bonus Requirements](#bonus-requirements)
- [12 - Create an endpoint for registering admin users](#12---create-an-endpoint-for-registering-admin-users)
- [13 - Create integration tests that cover at least 60% of files in src, with a minimum of 100 lines covered](#13---create-integration-tests-that-cover-at-least-60-of-files-in-src-with-a-minimum-of-100-lines-covered)
- [14 - Create integration tests that cover at least 90% of files in src, with a minimum of 150 lines covered](#14---create-integration-tests-that-cover-at-least-90-of-files-in-src-with-a-minimum-of-150-lines-covered)


# Sumário

- [Boas vindas ao repositório do projeto Cookmaster!](#boas-vindas-ao-repositório-do-projeto-cookmaster)
- [Habilidades](#habilidades)
- [Desenvolvimento](#desenvolvimento)
- [Data de Entrega](#data-de-entrega)
- [Conexão com o Banco](#conexão-com-o-banco)
- [Coleções](#coleções)
- [Requisitos do projeto](#requisitos-do-projeto)
  - [Requisitos Obrigatórios](#requisitos-obrigatórios)
    - [1 - Crie um endpoint para o cadastro de usuários](#1---crie-um-endpoint-para-o-cadastro-de-usuários)
    - [2 - Crie um endpoint para o login de usuários](#2---crie-um-endpoint-para-o-login-de-usuários)
    - [3 - Crie um endpoint para o cadastro de receitas](#3---crie-um-endpoint-para-o-cadastro-de-receitas)
    - [4 - Crie um endpoint para a listagem de receitas](#4---crie-um-endpoint-para-a-listagem-de-receitas)
    - [5 - Crie um endpoint para visualizar uma receita específica](#5---crie-um-endpoint-para-visualizar-uma-receita-específica)
    - [6 - Crie uma query em mongo que insira uma pessoa usuária com permissões de admin](#6---crie-uma-query-em-mongo-que-insira-uma-pessoa-usuária-com-permissões-de-admin)
    - [7 - Crie um endpoint para a edição de uma receita](#7---crie-um-endpoint-para-a-edição-de-uma-receita)
    - [8 - Crie um endpoint para a exclusão de uma receita](#8---crie-um-endpoint-para-a-exclusão-de-uma-receita)
    - [9 - Crie um endpoint para a adição de uma imagem a uma receita](#9---crie-um-endpoint-para-a-adição-de-uma-imagem-a-uma-receita)
    - [10 - Crie um endpoint para acessar a imagem de uma receita](#10---crie-um-endpoint-para-acessar-a-imagem-de-uma-receita)
    - [11 - Crie testes de integração que cubram no mínimo 30% dos arquivos em `src`, com um mínimo de 50 linhas cobertas](#11---crie-testes-de-integração-que-cubram-no-mínimo-30-dos-arquivos-em-src-com-um-mínimo-de-50-linhas-cobertas)
  - [Requisitos Bônus](#requisitos-bônus)
    - [12 - Crie um endpoint para cadastro de pessoas administradoras](#12---crie-um-endpoint-para-cadastro-de-pessoas-administradoras)
    - [13 - Crie testes de integração que cubram no mínimo 60% dos arquivos em `src`, com um mínimo de 100 linhas cobertas](#13---crie-testes-de-integração-que-cubram-no-mínimo-60-dos-arquivos-em-src-com-um-mínimo-de-100-linhas-cobertas)
    - [14 - Crie testes de integração que cubram no mínimo 90% dos arquivos em `src`, com um mínimo de 150 linhas cobertas](#14---crie-testes-de-integração-que-cubram-no-mínimo-90-dos-arquivos-em-src-com-um-mínimo-de-150-linhas-cobertas)

---

# Skills

In this project, the following skills were developed:

- Understanding the inner workings of an authentication token.
  
- Token generation using login and password information.
  
- Route authentication in Express using JWT tokens.
  
- File uploads in REST APIs.
  
- Saving files on the server via a REST API.
  
- Accessing server files via a REST API.
  
- Writing integration tests.


# Habilidades

Neste projeto, foram desenvolvidas as seguintes habilidades:

- Entendimento acerca do que há por dentro de um token de autenticação.

- Geração de tokens a partir de informações como login e senha.

- Autenticação de rotas do Express, usando o token JWT.

- Upload de arquivos em APIs REST.

- Salvamento de arquivos no servidor através de uma API REST.

- Consulta aos arquivos do servidor através de uma API REST.

- Realização de testes de integração

---

# Development

All layers of the application were developed (Models, Service, and Controllers).

Through this application, it is possible to perform basic CRUD operations (Create, Read, Update, Delete) in a database.

To perform any kind of data modification (such as recipe creation, editing, or deletion), authentication is required.

Authentication is handled via `JWT`.

Images can be added to recipes using file uploads powered by `multer`.


# Desenvolvimento

Desenvolvimento de todas as camadas da aplicação (Models, Service e Controllers).

Através dessa aplicação, é possível realizar as operações básicas de CRUD que se pode fazer em um banco de dados: Criação, Leitura, Atualização e Exclusão.

Para realizar qualquer tipo de alteração no banco de dados (como cadastro, edição ou exclusão de receitas) é necessário autenticar-se.

A autenticação é feita via `JWT`.

É possível adicionar imagem à uma receita, utilizando o upload de arquivos fornecido pelo `multer`.

---
# Submission Date

- As specified by Trybe, this was a `3`-day project.
- Final project submission date: `09/30/2021 - 14:00h`.


# Data de Entrega

    - Por especificação da Trybe, foram `3` dias de projeto.
    - Data de entrega para avaliação final do projeto: `30/09/2021 - 14:00h`.

---

# Database Connection

The local database connection must use the following parameters:

```javascript
Copiar código
const MONGO_DB_URL = 'mongodb://localhost:27017/Cookmaster';
const DB_NAME = 'Cookmaster';
```


# Conexão com o Banco

A conexão do banco local deverá conter os seguintes parâmetros:

```javascript
const MONGO_DB_URL = 'mongodb://localhost:27017/Cookmaster';
const DB_NAME = 'Cookmaster';
```

# Collections

The database contains two collections: users and recipes.

The users collection is named `users`.

The fields in the `users` collection have the following format:

```json
{ "name" : "Erick Jacquin", "email" : "erickjacquin@gmail.com", "password" : "12345678", "role" : "user" }
```

The response for a successful insert operation is as follows:

```json
{ "_id" : ObjectId("5f46914677df66035f61a355"), "name" : "Erick Jacquin", "email" : "erickjacquin@gmail.com", "password" : "12345678", "role" : "user" }
```

(The _id will be automatically generated by MongoDB)

The recipes collection is named `recipes`.

The fields in the `recipes` collection have the following format:

```json
{ "name" : "Receita do Jacquin", "ingredients" : "Frango", "preparation" : "10 minutos no forno" }
```

The response for a successful insert operation is as follows:

```json
{ "_id" : ObjectId("5f46919477df66035f61a356"), "name" : "string", "ingredients" : "string", "preparation" : "string", "userId" : ObjectId("5f46914677df66035f61a355") }
```

(The _id will be automatically generated by MongoDB, and the userId will be generated with the ID of the user who created the recipe)



# Coleções

O banco tem duas coleções: usuários e receitas.

A coleção de usuários tem o seguinte nome: `users`.

Os campos da coleção `users` tem este formato:

```json
{ "name" : "Erick Jacquin", "email" : "erickjacquin@gmail.com", "password" : "12345678", "role" : "user" }
```

A resposta do insert para ser retornada após a criação é esta:

```json
{ "_id" : ObjectId("5f46914677df66035f61a355"), "name" : "Erick Jacquin", "email" : "erickjacquin@gmail.com", "password" : "12345678", "role" : "user" }
```
(O _id será gerado automaticamente pelo mongodb)

A coleção de receitas deverá tem o seguinte nome: `recipes`.

Os campos da coleção `recipes` tem este formato:

```json
{ "name" : "Receita do Jacquin", "ingredients" : "Frango", "preparation" : "10 minutos no forno" }
```

A resposta do insert para ser retornada após a criação é esta:

```json
{ "_id" : ObjectId("5f46919477df66035f61a356"), "name" : "string", "ingredients" : "string", "preparation" : "string", "userId" : ObjectId("5f46914677df66035f61a355") }
```
(O _id será gerado automaticamente pelo mongodb, e o userId será gerado com o id do usuário que criou a receita)

---

# Project Requirements

### Mandatory Requirements

### 1 - Create an endpoint for user registration

- The route should be (/users).

- In the database, a user must have the following fields: Email, Password, Name, and Role.

- To create a user via the API, all fields are required except for Role.

- The Email field must be unique.

- Users created through this endpoint should have the Role field set to user, meaning they are regular users and not admins.

- The request body should be formatted as follows:

  
  ```json
  {
    "name": "string",
    "email": "string",
    "password": "string"
  }
  ```

  Do not use bcrypt or other libraries to encrypt the password, to ensure compatibility with the evaluator.

  ### Additionally, the following checks will be performed:

- **[It will be validated that the "name" field is required]**

If the user does not provide the "name" field, the returned result should be as shown below, with an HTTP status of `400`:

![User without Name](./public/usuariosemnome.png)

- **[It will be validated that the "email" field is required]**

If the user does not provide the "email" field, the returned result should be as shown below, with an HTTP status of `400`:

![User without Email](./public/usuariosememail.png)

- **[It will be validated that it is not possible to register a user with an invalid email]**

If the user provides an invalid email, the returned result should be as shown below, with an HTTP status of `400`:

![Invalid Email](./public/campoemailinvalido.png)

- **[It will be validated that the "password" field is required]**

If the user does not provide the "password" field, the returned result should be as shown below, with an HTTP status of `400`:

![User without Password](./public/usuariosemsenha.png)

- **[It will be validated that the "email" field is unique]**

If the user registers an email that already exists, the returned result should be as shown below, with an HTTP status of `409`:

![Email already Used](./public/emailjausado.png)

- **[It will be validated that it is possible to register a user successfully]**

If the user is successfully registered, the returned result should be as shown below, with an HTTP status of `201`:

![User Created](./public/usuariocriadocomsucesso.png)

- **[It will be validated that when registering a user, the "role" field has the value "user"]**

If the user is created successfully, the returned result should be as shown below, with an HTTP status of `201`:

![Validate Role](./public/validarrole.png)

### 2 - Create an endpoint for user login

- The route should be (`/login`).

- The route should receive the Email and Password fields, and these fields must be validated in the database.

- In the `JWT` configuration, **do not use environment variables** to avoid conflicts with the evaluator.

- A `JWT` token should be generated and returned if the login is successful. The payload must contain the user's id, email, and role.

- The request body should have the following format:

  ```json
  {
    "email": "string",
    "password": "string"
  }
  ```
  
**Additionally, the following checks will be performed:**

- **[It will be validated that the "email" field is required]**

If the login does not provide the "email" field, the returned result should be as shown below, with an HTTP status of `401`:

![User without Email](./public/loginsememail.png)

- **[It will be validated that the "password" field is required]**

If the login does not provide the "password" field, the returned result should be as shown below, with an HTTP status of `401`:

![User without Password](./public/loginsemsenha.png)

- **[It will be validated that it is not possible to log in with an invalid email]**

If the login provides an invalid email, the returned result should be as shown below, with an HTTP status of `401`:

![Invalid Email](./public/loginemailinvalido.png)

- **[It will be validated that it is not possible to log in with an invalid password]**

If the login provides an invalid password, the returned result should be as shown below, with an HTTP status of `401`:

![Invalid Password](./public/loginsenhainvalida.png)

- **[It will be validated that it is possible to log in successfully]**

If the login is successful, the returned result should be as shown below, with an HTTP status of `200`:

![Successful Login](./public/logincomsucesso.png)

### 3 - Create an endpoint for recipe registration

- The route must be (`/recipes`).

- A recipe can only be created if the user is logged in and the `JWT` token is validated.

- In the database, the recipe should have the fields Name, Ingredients, Preparation Method, Image URL, and Author ID.

- Name, ingredients, and preparation method must be received in the request body in the following format:

  ```json
  {
    "name": "string",
    "ingredients": "string",
    "preparation": "string"
  }
  ```


---

# Requisitos do projeto

## Requisitos Obrigatórios

### 1 - Crie um endpoint para o cadastro de usuários

- A rota deve ser (`/users`).

- No banco um usuário precisa ter os campos Email, Senha, Nome e Role.

- Para criar um usuário através da API, todos os campos são obrigatórios, com exceção do Role.

- O campo Email deve ser único.

- Usuários criados através desse endpoint devem ter seu campo Role com o atributo _user_, ou seja, devem ser usuários comuns, e não admins.

- O body da requisição deve conter o seguinte formato:

  ```json
  {
    "name": "string",
    "email": "string",
    "password": "string"
  }
  ```
- Não use `bcrypt` ou outra biblioteca para encriptar a senha, para que o avaliador funcione corretamente.

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o campo "name" é obrigatório]**

Se o usuário não tiver o campo "name" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Usuário sem Nome](./public/usuariosemnome.png)

- **[Será validado que o campo "email" é obrigatório]**

Se o usuário não tiver o campo "email" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Usuário sem Email](./public/usuariosememail.png)

- **[Será validado que não é possível cadastrar usuário com o campo email inválido]**

Se o usuário tiver o campo email inválido o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Email Inválido](./public/campoemailinvalido.png)

- **[Será validado que o campo "senha" é obrigatório]**

Se o usuário não tiver o campo "senha" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Usuário sem Senha](./public/usuariosemsenha.png)

- **[Será validado que o campo "email" é único]**

Se o usuário cadastrar o campo "email" com um email que já existe, o resultado retornado deverá ser conforme exibido abaixo, com um status http `409`:

![Email já Usado](./public/emailjausado.png)

- **[Será validado que é possível cadastrar usuário com sucesso]**

Se o usuário for cadastrado com sucesso o resultado retornado deverá ser conforme exibido abaixo, com um status http `201`:

![Usuário Cadastrado](./public/usuariocriadocomsucesso.png)

- **[Será validado que é possível ao cadastrar usuário, o valor do campo "role" tenha o valor "user"]**

Se o usuário for criado com sucesso o resultado retornado deverá ser conforme exibido abaixo, com um status http `201`:

![Campo Role](./public/validarrole.png)

### 2 - Crie um endpoint para o login de usuários

- A rota deve ser (`/login`).

- A rota deve receber os campos Email e Senha e esses campos devem ser validados no banco de dados.

- Na configuração do `JWT` **não use variáveis de ambientes** para não ter conflito com o avaliador.

- Um token `JWT` deve ser gerado e retornado caso haja sucesso no login. No seu payload deve estar presente o id, email e role do usuário.

- O body da requisição deve conter o seguinte formato:

  ```json
  {
    "email": "string",
    "password": "string"
  }
  ```

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o campo "email" é obrigatório]**

Se o login não tiver o campo "email" o resultado retornado deverá ser conforme exibido abaixo, com um status http `401`:

![Usuário sem Senha](./public/loginsememail.png)

- **[Será validado que o campo "password" é obrigatório]**

Se o login não tiver o campo "password" o resultado retornado deverá ser conforme exibido abaixo, com um status http `401`:

![Usuário sem Senha](./public/loginsemsenha.png)

- **[Será validado que não é possível fazer login com um email inválido]**

Se o login tiver o email inválido o resultado retornado deverá ser conforme exibido abaixo, com um status http `401`:

![Email Inválido](./public/loginemailinvalido.png)

- **[Será validado que não é possível fazer login com uma senha inválida]**

Se o login tiver a senha inválida o resultado retornado deverá ser conforme exibido abaixo, com um status http `401`:

![Senha Inválida](./public/loginsenhainvalida.png)

- **[Será validado que é possível fazer login com sucesso]**

Se foi feito login com sucesso o resultado retornado deverá ser conforme exibido abaixo, com um status http `200`:

![Login com Sucesso](./public/logincomsucesso.png)

### 3 - Crie um endpoint para o cadastro de receitas

- A rota deve ser (`/recipes`).

- A receita só pode ser criada caso o usuário esteja logado e o token `JWT` validado.

- No banco, a receita deve ter os campos Nome, Ingredientes, Modo de preparo, URL da imagem e Id do Autor.

- Nome, ingredientes e modo de preparo devem ser recebidos no corpo da requisição, com o seguinte formato:

  ```json
  {
    "name": "string",
    "ingredients": "string",
    "preparation": "string"
  }
  ```

- O campo dos ingredientes pode ser um campo de texto aberto.

- O campo ID do autor, deve ser preenchido automaticamente com o ID do usuário logado, que deve ser extraído do token JWT.

- A URL da imagem será preenchida através de outro endpoint

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que não é possível cadastrar receita sem o campo "name"]**

Se a receita não tiver o campo "name" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Receita sem nome](./public/receitasemnome.png)

- **[Será validado que não é possível cadastrar receita sem o campo "ingredients"]**

Se a receita não tiver o campo "ingredients" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Receita sem ingrediente](./public/receitasemingrediente.png)

- **[Será validado que não é possível cadastrar receita sem o campo "preparation"]**

Se a receita não tiver o campo "preparation" o resultado retornado deverá ser conforme exibido abaixo, com um status http `400`:

![Receita sem preparo](./public/receitasempreparo.png)

- **[Será validado que não é possível cadastrar uma receita com token invalido]**

Se a receita não tiver o token válido o resultado retornado deverá ser conforme exibido abaixo, com um status http `401`:

![Receita com token inválido](./public/tokeninvalidoreq3.png)

- **[Será validado que é possível cadastrar uma receita com sucesso]**

O resultado retornado para cadastrar a receita com sucesso deverá ser conforme exibido abaixo, com um status http `201`:

![Receita com Sucesso](./public/receitacomsucesso.png)

### 4 - Crie um endpoint para a listagem de receitas

- A rota deve ser (`/recipes`).

- A rota pode ser acessada por usuários logados ou não

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que é possível listar todas as receitas sem estar autenticado]**

O resultado retornado para listar receitas com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Receita com Sucesso](./public/listarreceitas.png)

- **[Será validado que é possível listar todas as receitas estando autenticado]**

O resultado retornado para listar receitas com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Receita com Sucesso](./public/listarreceitas.png)

### 5 - Crie um endpoint para visualizar uma receita específica

- A rota deve ser (`/recipes/:id`).

- A rota pode ser acessada por usuários logados ou não

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que é possível listar uma receita específica sem estar autenticado]**

O resultado retornado para listar uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Listar uma Receita](./public/listarumareceita.png)

- **[Será validado que é possível listar uma receita específica estando autenticado]**

O resultado retornado para listar uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Listar uma Receita](./public/listarumareceita.png)

- **[Será validado que não é possível listar uma receita que não existe]**

O resultado retornado para listar uma receita que não existe deverá ser conforme exibido abaixo, com um status http `404`:

![Listar uma Receita inexistente](./public/receitanaoencontrada.png)

### 6 - Crie uma query em mongo que insira uma pessoa usuária com permissões de admin

Crie um arquivo `seed.js` na raiz do projeto com uma query do Mongo DB capaz de inserir um usuário na coleção _users_ com os seguintes valores:

`{ name: 'admin', email: 'root@email.com', password: 'admin', role: 'admin' }`

**Obs.:** Esse usuário tem o poder de criar, deletar, atualizar ou remover qualquer receita, independente de quem a cadastrou. Isso será solicitado ao longo dos próximos requisitos.

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o projeto tem um arquivo de seed, com um comando para inserir um usuário root e verifico que é possível fazer login]**    

Será validado no arquivo `seed.js` existe a query para criar um usuário root

### 7 - Crie um endpoint para a edição de uma receita

- A rota deve ser (`/recipes/:id`).

- A receita só pode ser atualizada caso o usuário esteja logado e o token `JWT` validado.

- A receita só pode ser atualizada caso pertença ao usuário logado, ou caso esse usuário seja um admin.

- O corpo da requisição deve receber o seguinte formato:

  ```json
  {
    "name": "string",
    "ingredients": "string",
    "preparation": "string"
  }
  ```

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que não é possível editar receita sem estar autenticado]**

O resultado retornado para editar receita sem autenticação deverá ser conforme exibido abaixo, com um status http `401`:

![Editar uma Receita sem autenticação](./public/editarsemautenticacao.png)

- **[Será validado que não é possível editar receita com token inválido]**

O resultado retornado para editar receita com token inválido deverá ser conforme exibido abaixo, com um status http `401`:

![Editar uma Receita com token inválido](./public/editartokeninvalido.png)

- **[Será validado que é possível editar receita estando autenticado]**

O resultado retornado para editar uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Editar uma Receita](./public/editarcomsucesso.png)

- **[Será validado que é possível editar receita com usuário admin]**

O resultado retornado para editar uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Editar uma Receita](./public/editarcomsucesso.png)

### 8 - Crie um endpoint para a exclusão de uma receita

- A rota deve ser (`/recipes/:id`).

- A receita só pode ser excluída caso o usuário esteja logado e o token `JWT` validado.

- A receita só pode ser excluída caso pertença ao usuário logado, ou caso o usuário logado seja um admin.

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que não é possível excluir receita sem estar autenticado]**

O resultado retornado para excluir uma receita sem autenticação deverá ser conforme exibido abaixo, com um status http `401`:

![Excluir uma Receita sem autenticação](./public/excluirsemautenticacao.png)

- **[Será validado que é possível excluir receita estando autenticado]**

O resultado retornado para excluir uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `204`:

![Excluir uma Receita](./public/excluircomsucesso.png)

- **[Será validado que é possível excluir receita com usuário admin]**

O resultado retornado para excluir uma receita com sucesso deverá ser conforme exibido abaixo, com um status http `204`:

![Excluir uma Receita](./public/excluircomsucesso.png)

### 9 - Crie um endpoint para a adição de uma imagem a uma receita

- A rota deve ser (`/recipes/:id/image/`).

- A imagem deve ser lida do campo `image`.

- O endpoint deve aceitar requisições no formato `multipart/form-data`.

- A receita só pode ser atualizada caso o usuário esteja logado e o token `JWT` validado.

- A receita só pode ser atualizada caso pertença ao usuário logado ou caso o usuário logado seja admin.

- O upload da imagem deverá ser feito utilizando o `Multer`.

- O nome do arquivo deve ser o ID da receita, e sua extensão `.jpeg`.

- A URL completa para acessar a imagem através da API deve ser gravada no banco de dados, junto com os dados da receita.

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que é possível enviar foto com usuário autenticado]**

O resultado retornado para adicionar uma foto na receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Foto Autenticada](./public/fotocomsucesso.png)

- **[Será validado que ao enviar foto, o nome da imagem é alterada para o id da receita]**

O resultado retornado para adicionar uma foto na receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Foto Autenticada](./public/fotocomsucesso.png)

- **[Será validado que não é possível enviar foto sem estar autenticado]**

O resultado retornado para adicionar uma foto na receita com sucesso deverá ser conforme exibido abaixo, com um status http `401`:

![Excluir uma Receita](./public/fotonaoautenticada.png)

- **[Será validado que é possível enviar foto com usuário admin]**

O resultado retornado para adicionar uma foto na receita com sucesso deverá ser conforme exibido abaixo, com um status http `200`:

![Foto Autenticada](./public/fotocomsucesso.png)

### 10 - Crie um endpoint para acessar a imagem de uma receita

- As imagens devem estar disponíveis através da rota `/images/<id-da-receita>.jpeg` na API.

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que é retornada uma imagem como resposta]**

O resultado retornado deverá ser do tipo imagem, com um status http `200`:

![Foto Autenticada](./public/imagemrecetornada.png)

### 11 - Crie testes de integração que cubram no mínimo 30% dos arquivos em `src`, com um mínimo de 50 linhas cobertas

- Os testes de integração devem ser criados na pasta `./src/integration-tests`, essa pasta **não pode ser renomeada ou removida**;

- O arquivo `change.me.test.js` pode ser alterado, renomeado ou removido;

- Os testes devem ser criados usando o instrumental e boas práticas apresentado nos conteúdos de testes do course;

- Para rodar os testes, utilize o comando `npm run dev:test`;

- Para visualizar a cobertura, utilize o comando `npm run dev:test:coverage`;

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o teste cobre o valor esperado]**

Nenhum teste pode ser pulado;
O resultado do percentual total de cobertura deve ser igual ou maior que `30`;
O resultado do numero total de linhas cobertas deve ser igual ou maior que `50`.

## Requisitos Bônus

### 12 - Crie um endpoint para cadastro de pessoas administradoras

- A rota deve ser (`/users/admin`).

- Só será possível adicionar um admin caso esta ação esteja sendo feita por outro admin, portanto, deve ser validado se há um admin logado.

- Por padrão, as requisições pra esse endpoint devem adicionar um usuário com a role _admin_.

- O corpo da requisição deve ter o seguinte formato:

  ```json
  {
    "name": "string",
    "email": "string",
    "password": "string"
  }
  ```

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que não é possível cadastrar um usuário admin, sem estar autenticado como um usuário admin]**

Se o usuário admin não é criado com sucesso o resultado retornado deverá ser conforme exibido abaixo, com um status http `403`:

![Criar usuário sem ser admin](./public/soadmincria.png)

- **[Será validado que é possível cadastrar um usuário admin]**

Se o usuário admin é criado com sucesso o resultado retornado deverá ser conforme exibido abaixo, com um status http `201`:

![Criar admin](./public/criaradmin.png)

### 13 - Crie testes de integração que cubram no mínimo 60% dos arquivos em `src`, com um mínimo de 100 linhas cobertas

- Os testes de integração devem ser criados na pasta `./src/integration-tests`, essa pasta **não pode ser renomeada ou removida**;

- O arquivo `change.me.test.js` pode ser alterado, renomeado ou removido;

- Os testes devem ser criados usando o instrumental e boas práticas apresentado nos conteúdos de testes do course;

- Para rodar os testes, utilize o comando `npm run dev:test`;

- Para visualizar a cobertura, utilize o comando `npm run dev:test:coverage`;

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o teste cobre o valor esperado]**

Nenhum teste pode ser pulado;
O resultado do percentual total de cobertura deve ser igual ou maior que `60`;
O resultado do numero total de linhas cobertas deve ser igual ou maior que `100`.

### 14 - Crie testes de integração que cubram no mínimo 90% dos arquivos em `src`, com um mínimo de 150 linhas cobertas

- Os testes de integração devem ser criados na pasta `./src/integration-tests`, essa pasta **não pode ser renomeada ou removida**;

- O arquivo `change.me.test.js` pode ser alterado, renomeado ou removido;

- Os testes devem ser criados usando o instrumental e boas práticas apresentado nos conteúdos de testes do course;

- Para rodar os testes, utilize o comando `npm run dev:test`;

- Para visualizar a cobertura, utilize o comando `npm run dev:test:coverage`;

**Além disso, as seguintes verificações serão feitas:**

- **[Será validado que o teste cobre o valor esperado]**

Nenhum teste pode ser pulado;
O resultado do percentual total de cobertura deve ser igual ou maior que `90`;
O resultado do numero total de linhas cobertas deve ser igual ou maior que `150`.
