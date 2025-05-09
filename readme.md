# Aplicação para Agendamento de salas 

O projeto consiste em uma aplicação web que permite aos usuários visualizar e realizar reservas de salas disponíveis em uma instituição de ensino. A plataforma exibe informações detalhadas sobre cada sala, como localização, capacidade e horários de funcionamento, além de indicar quais estão disponíveis ou já reservadas. Também é possível ao usuário acessar o histórico e o status atual de suas reservas. Com uma interface intuitiva e foco na usabilidade, a aplicação visa facilitar a dinâmica de agendamento, reduzir erros manuais, economizar tempo e proporcionar uma visão clara e atualizada da ocupação dos espaços da instituição.

## Requisitos

- Node.js (versão 24.0.1)
- PostgreSQL (versão 17.3)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/carolm.paz/agendamento-salas.git
   cd seu-projeto
```

2. **Instalar as dependências:**
    
```bash
npm install
```
    
3. **Configurar o arquivo `.env`:**
    
Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.
    

Configuração do Banco de Dados
------------------------------

1. **Criar banco de dados:**
    
    Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.
    
2. **Executar o script SQL de inicialização:**
    
```bash
npm run init-db
```
    
Isso criará a tabela `users` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.
    

Funcionalidades
---------------

* **Padrão MVC:** Estrutura organizada em Model, View e Controller.
* **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
* **UUID:** Utilização de UUID como chave primária na tabela `users`.
* **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
* **Testes:** Inclui estrutura básica para testes automatizados.

Scripts Disponíveis
-------------------

* `npm start`: Inicia o servidor Node.js.
* `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
* `npm run test`: Executa os testes automatizados.
* `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

Estrutura de Diretórios
-----------------------

* **`config/`**: Configurações do banco de dados e outras configurações do projeto.
* **`controllers/`**: Controladores da aplicação (lógica de negócio).
* **`models/`**: Modelos da aplicação (definições de dados e interações com o banco de dados).
* **`routes/`**: Rotas da aplicação.
* **`tests/`**: Testes automatizados.

Estrutura de pastas 
-----------------------

```
agendamento-salas/
│
├── config/                
│   └── db.js
├── controllers/           
│   └── UserController.js
├── models/                
│   └── UserModel.js
├── routes/                
│   └── frontRoutes.js
│   └── frontRoutes.js
├── services/              
│   └── userService.js
├── migrations/             
│   └── fisico.js
├── assets/                
├── scripts/               
├── styles/                
├── .gitignore             
├── .env.example           
├── package-lock.json      
├── package.json           
├── readme.md              
├── server.js             
└── runMigration.js

```