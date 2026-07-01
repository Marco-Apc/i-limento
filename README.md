# i-limento 🍕🍔🍣

> **i-limento** (lê-se como *alimento*) é uma plataforma moderna de cardápio digital e delivery que conecta clientes famintos a estabelecimentos e restaurantes locais.

O projeto está estruturado em dois ambientes independentes: **frontend** (React + Vite) e **backend** (Node.js + Express + MongoDB).

---

## 🛠️ Tecnologias Utilizadas

### Backend
- **Node.js** com **Express** (API RESTful)
- **MongoDB** com **Mongoose** (Banco de dados de documentos)
- **JWT (JSON Web Tokens)** & **Bcrypt.js** (Autenticação e segurança)
- **Dotenv** & **Cors**

### Frontend
- **React.js** (com **Vite** para inicialização ultrarrápida)
- **Vanilla CSS** (Estilização premium, limpa e responsiva)
- **LocalStorage** (Usado como banco de dados simulado no modo de demonstração)

---

## 📂 Estrutura do Projeto

```text
i-limento/
├── backend/                  # Servidor API e banco de dados
│   ├── src/
│   │   ├── config/           # Conexão com o MongoDB
│   │   ├── controllers/      # Lógica de controle de rotas
│   │   ├── middlewares/      # Proteção de rotas com JWT
│   │   ├── models/           # Schemas do Mongoose (Usuário, Estabelecimento, Item)
│   │   ├── routes/           # Rotas da API
│   │   └── scripts/          # Script de semeadura de dados (seed)
│   └── .env                  # Configurações do servidor (.gitignore instalado)
│
└── frontend/                 # Interface do usuário (React)
    ├── src/
    │   ├── App.jsx           # Componente principal e fluxo de navegação
    │   ├── App.css           # Estilização premium da interface
    │   └── index.css         # Reset global e variáveis CSS
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
- **Node.js** instalado.
- **MongoDB** rodando localmente (opcional, pois o frontend possui um **Modo Demonstrativo** com banco local integrado via `LocalStorage`).

---

### Passo 1: Configurar e Rodar o Backend

1. Navegue até a pasta do backend:
   ```bash
   cd backend
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Crie e configure o arquivo `.env` (já criamos um modelo padrão para você):
   ```env
   PORT=5000
   MONGO_URI=mongodb://127.0.0.1:27017/i-limento
   JWT_SECRET=sua_chave_secreta_aqui
   ```
4. *(Opcional)* Popule o banco de dados MongoDB local com dados fictícios de teste:
   ```bash
   npm run seed
   ```
5. Inicie o servidor:
   ```bash
   npm run dev
   ```

O backend estará ativo em: **http://localhost:5000**

---

### Passo 2: Configurar e Rodar o Frontend

1. Abra outro terminal e navegue até a pasta do frontend:
   ```bash
   cd ../frontend
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

O frontend estará ativo em: **http://localhost:5173** (ou a porta padrão exibida no terminal).

---

## 💡 Informações Importantes & Contas de Teste

Se você estiver rodando sem o MongoDB ativo, o frontend entrará automaticamente no **Modo Demonstrativo (Mock)**.

Você pode fazer login utilizando as seguintes credenciais de teste já semeadas:
- **Dono de Restaurante (Luigi)**: `luigi@pizza.com` (senha: `password123`)
- **Cliente Comum (Maria)**: `maria@cliente.com` (senha: `password123`)