
<div align="center" id="top"> 
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/65/RIHAPPY_Logo.svg" alt="Loja de Brinquedos API" width="200" />
  <h1 align="center">Loja de Brinquedos API</h1>
</div>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/CharCarvalho/CP4-Brinquedos?color=56BEB8">
  <img alt="Github language count" src="https://img.shields.io/github/languages/count/CharCarvalho/CP4-Brinquedos?color=56BEB8">
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/CharCarvalho/CP4-Brinquedos?color=56BEB8">
  <img alt="License" src="https://img.shields.io/github/license/CharCarvalho/CP4-Brinquedos?color=56BEB8">
</p>

<p align="center">
  <a href="#Sobre">Sobre</a> &#xa0; | &#xa0; 
  <a href="#Funcionalidades">Funcionalidades</a> &#xa0; | &#xa0;
  <a href="#Tecnologias">Tecnologias</a> &#xa0; | &#xa0;
  <a href="#Requisitos">Requisitos</a> &#xa0; | &#xa0;
  <a href="#Começando">Começando</a> &#xa0; | &#xa0;
  <a href="https://github.com/CharCarvalho" target="_blank">Autor</a>
</p>

<br>

## 📝 Sobre

Este projeto é uma API para uma loja de brinquedos, criada para gerenciar operações CRUD de brinquedos em um banco de dados. A API foi desenvolvida usando Java Spring Boot e utiliza o Azure SQL Database para armazenar informações.

## ✨ Funcionalidades

- ✅ Listar Brinquedos
- ✅ Adicionar Novo Brinquedo
- ✅ Atualizar Brinquedo Existente
- ✅ Remover Brinquedo
- ✅ Consultar Brinquedo por ID

## 🚀 Tecnologias

As seguintes ferramentas foram utilizadas neste projeto:

- [Java Spring Boot](https://spring.io/projects/spring-boot)
- [Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)
- [Eclipse IDE](https://www.eclipse.org/)

## ✔️ Requisitos

Antes de começar, certifique-se de ter [Git](https://git-scm.com) e [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) instalados.

## 🏁 Começando

```bash
# Clone este projeto
$ git clone https://github.com/CharCarvalho/CP4-Brinquedos

# Acesse o diretório
$ cd CP4-Brinquedos

# Compile e execute o projeto
$ ./mvnw spring-boot:run

# A API estará disponível em http://localhost:8080/brinquedos

## 📂 Endpoints

Aqui estão alguns exemplos de como você pode interagir com a API:

### POST /brinquedos

Cria um novo brinquedo.

**Request:**

```json
{
  "nm_brinquedo": "Carrinho de Controle Remoto",
  "tipo_brinquedo": "Eletrônico",
  "classificacao_brinquedo": "4+",
  "tamanho_brinquedo": "Médio",
  "preco_brinquedo": 129.99
}
```

![POST](https://github.com/user-attachments/assets/1b5db55e-3fff-4ae4-8213-57903149aa9e)

### PUT /brinquedos/1

Atualiza um brinquedo existente.

**Request:**

```json
{
  "nm_brinquedo": "Boneca Barbie",
  "tipo_brinquedo": "Eletrônico",
  "classificacao_brinquedo": "100+",
  "tamanho_brinquedo": "Gigante",
  "preco_brinquedo": 129.99
}
```

![PUT](https://github.com/user-attachments/assets/86fe2e58-d056-4f9b-9941-449258e7228d)

### PATCH /brinquedos/1

Atualiza parcialmente um brinquedo.

**Request:**

```json
{
  "nm_brinquedo": "Carrinho de Controle Remoto Turbo",
  "preco_brinquedo": 149.99
}
```

![PATCH](https://github.com/user-attachments/assets/8a225243-4066-4602-9f74-b59da41772d9)

### DELETE /brinquedos/1

Remove um brinquedo.

**Response:**

Status 204 No Content

![DELETE](https://github.com/user-attachments/assets/b45d42fa-33d5-4e46-bb52-62c97eedb2bc)

### GET /brinquedos

Lista todos os brinquedos.

**Response:**

```json
[
  {
    "id": 1,
    "nm_brinquedo": "Carrinho de Controle Remoto",
    "tipo_brinquedo": "Eletrônico",
    "classificacao_brinquedo": "4+",
    "tamanho_brinquedo": "Médio",
    "preco_brinquedo": 129.99
  },
  {
    "id": 2,
    "nm_brinquedo": "Boneca Barbie",
    "tipo_brinquedo": "Boneca",
    "classificacao_brinquedo": "3+",
    "tamanho_brinquedo": "Pequeno",
    "preco_brinquedo": 89.90
  }
  // outros brinquedos
]
```

![GET](https://github.com/user-attachments/assets/b3045e28-bcfc-453f-a196-952dfeef797c)

### GET /brinquedos/{id}

Obtém detalhes de um brinquedo específico.

**Response:**

```json
{
  "id": 1,
  "nm_brinquedo": "Carrinho de Controle Remoto",
  "tipo_brinquedo": "Eletrônico",
  "classificacao_brinquedo": "4+",
  "tamanho_brinquedo": "Médio",
  "preco_brinquedo": 129.99
}
```

![GetById](https://github.com/user-attachments/assets/0fe26fc7-2862-4aea-ba83-0eaa09462347)

### PUT /brinquedos/{id}

Atualiza um brinquedo específico.

**Request:**

```json
{
  "nm_brinquedo": "Novo Nome do Brinquedo",
  "tipo_brinquedo": "Novo Tipo",
  "classificacao_brinquedo": "Nova Classificação",
  "tamanho_brinquedo": "Novo Tamanho",
  "preco_brinquedo": 199.99
}
```

**Response:**

```json
{
  "id": 1,
  "nm_brinquedo": "Novo Nome do Brinquedo",
  "tipo_brinquedo": "Novo Tipo",
  "classificacao_brinquedo": "Nova Classificação",
  "tamanho_brinquedo": "Novo Tamanho",
  "preco_brinquedo": 199.99
}
```

![PUT](https://github.com/user-attachments/assets/86fe2e58-d056-4f9b-9941-449258e7228d)

### PATCH /brinquedos/{id}

Atualiza parcialmente um brinquedo específico.

**Request:**

```json
{
  "nm_brinquedo": "Nome Atualizado",
  "preco_brinquedo": 159.99
}
```

**Response:**

```json
{
  "id": 1,
  "nm_brinquedo": "Nome Atualizado",
  "tipo_brinquedo": "Tipo Atual",
  "classificacao_brinquedo": "Classificação Atual",
  "tamanho_brinquedo": "Tamanho Atual",
  "preco_brinquedo": 159.99
}
```

![PATCH](https://github.com/user-attachments/assets/8a225243-4066-4602-9f74-b59da41772d9)

---

**Link para o deploy:** [Loja de Brinquedos API na Azure](https://cp4-brinquedos-b6gnfqh5djhxh7f3.eastus-01.azurewebsites.net/br
