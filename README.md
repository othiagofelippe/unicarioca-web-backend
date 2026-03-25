# Unicarioca Web Backend

Sistema web com frontend em React e backend em Python (Flask), usando MongoDB como banco de dados.

---

## O que você vai precisar ter instalado

Escolha uma das duas opções abaixo:

**Opção 1 — Docker (mais fácil, recomendada)**
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)

**Opção 2 — Rodar manualmente**
- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- [Python](https://www.python.org/) (versão 3.10 ou superior)
- [MongoDB](https://www.mongodb.com/try/download/community) rodando localmente

---

## Como rodar o projeto

### Opção 1 — Docker (sobe tudo de uma vez)

```bash
docker-compose up
```

Pronto. Aguarde os containers subirem e acesse:

- **Frontend:** http://localhost:3000
- **Backend (API):** http://localhost:5001
- **MongoDB:** localhost:27017

Para parar tudo:

```bash
docker-compose down
```

---

### Opção 2 — Rodar manualmente (sem Docker)

Você vai precisar de 2 terminais abertos ao mesmo tempo.

**Terminal 1 — Frontend**

```bash
cd frontend
npm install
npm start
```

Acesse em: http://localhost:3000

**Terminal 2 — Backend**

```bash
cd backend
pip install -r requirements.txt
python app.py
```

API disponível em: http://localhost:5000

> Lembre-se de ter o MongoDB rodando localmente na porta 27017.

---

## Estrutura do projeto

```
unicarioca-web-backend/
├── frontend/        # Interface web (React)
├── backend/         # API REST (Python + Flask)
└── docker-compose.yml
```

---

## Endpoints da API

| Método | Rota        | O que faz                  |
|--------|-------------|----------------------------|
| GET    | /projects   | Lista todos os projetos     |
| POST   | /projects   | Adiciona um novo projeto    |
