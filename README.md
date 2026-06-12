# SISTEMA DE CONTROLE DE RESERVAS E ACOMODAÇÕES

---

## 1. VISÃO GERAL

Este projeto foi desenvolvido com o objetivo de facilitar a administração de quartos e reservas em estabelecimentos de hospedagem.

O sistema possibilita:

- Registro de quartos
- Consulta de acomodações cadastradas
- Realização de reservas
- Visualização das reservas existentes
- Remoção de registros quando necessário

A aplicação utiliza arquitetura cliente-servidor, garantindo a comunicação entre interface, API e banco de dados.

---

## 2. TECNOLOGIAS EMPREGADAS

### Interface Web
- HTML5
- CSS3
- JavaScript

### Camada Servidora
- Node.js
- Express.js
- Prisma ORM

### Sistema de Banco de Dados
- MySQL

### Ferramenta de Desenvolvimento
- Visual Studio Code (VS Code)

---

## 3. ORGANIZAÇÃO DO PROJETO

A aplicação foi dividida em três componentes principais:

### Front-end
Responsável pela exibição das informações e interação com o usuário.

### Back-end
Responsável pelo processamento das requisições e integração com o banco de dados.

### Banco de Dados
Responsável pelo armazenamento e gerenciamento das informações cadastradas.

---

## 4. ESTRUTURA DAS ENTIDADES

### Tabela: Quartos
- id
- numero
- tipo
- status

### Tabela: Reservas
- id
- hospede
- dataEntrada
- dataSaida
- quartoId

### Relacionamento

- Um quarto pode estar associado a várias reservas.
- Cada reserva pertence a um único quarto.

---

## 5. ENDPOINTS DA API

### Operações com Quartos

- POST /quartos/cadastrar
- GET /quartos/listar
- GET /quartos/:id
- PUT /quartos/:id
- DELETE /quartos/:id

### Operações com Reservas

- POST /reservas/cadastrar
- GET /reservas/listar
- GET /reservas/:id
- PUT /reservas/:id
- DELETE /reservas/:id

---

## 6. FUNCIONALIDADES DAS PÁGINAS

### Página Inicial
- Exibição dos quartos disponíveis
- Consulta rápida dos registros
- Navegação para reservas

### Cadastro de Quartos
- Inserção do número do quarto
- Definição da categoria do quarto
- Salvamento das informações

### Página de Reservas
- Cadastro de hóspedes
- Definição das datas da hospedagem
- Listagem de reservas cadastradas

### Página Informativa
- Objetivo do projeto
- Tecnologias utilizadas
- Informações do desenvolvedor

---

## 7. RECURSOS IMPLEMENTADOS

- Cadastro de quartos
- Consulta de registros
- Criação de reservas
- Exclusão de dados
- Integração com MySQL
- Comunicação via API REST

---

## 8. IMAGENS DO SISTEMA

Inserir nesta seção:

- Tela principal
- Tela de cadastro de quartos
- Tela de gerenciamento de reservas
- Tela sobre o projeto

---

## 9. EXECUTANDO O PROJETO

### 1. Clonar o repositório

git clone https://github.com/lais01-hub/hotelreservas.git

### 2. Instalar as dependências

npm install

### 3. Criar o banco de dados

CREATE DATABASE hotel_db;

### 4. Configurar o arquivo .env

DATABASE_URL="mysql://root:@localhost:3306/hotel_db"
PORT_APP=3000

### 5. Aplicar as migrations

npx prisma migrate dev

### 6. Gerar o Prisma Client

npx prisma generate

### 7. Iniciar o servidor

node server.js

### 8. Abrir o sistema

Executar o arquivo index.html ou utilizar a extensão Live Server do VS Code.

---

## 10. CONSIDERAÇÕES FINAIS

O Sistema de Controle de Reservas e Acomodações foi desenvolvido para oferecer uma solução simples e eficiente para o gerenciamento de hospedagens. A estrutura adotada permite manutenção facilitada, organização dos dados e possibilidade de implementação de novas funcionalidades futuramente.
