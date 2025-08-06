# 🚀 Desafio DevOps – Deploy Django + PostgreSQL com Docker

Este repositório apresenta a solução para um desafio DevOps com foco em provisionamento de uma aplicação Django com banco de dados PostgreSQL, utilizando Docker, Docker Compose, NGINX e CI com GitHub Actions.

---

## 🧰 Tecnologias Utilizadas

- Python + Django
- PostgreSQL 17
- Docker e Docker Compose
- NGINX (proxy reverso)
- GitHub Actions (CI)
- `.env` para gerenciamento de variáveis de ambiente

---

## 📁 Estrutura do Projeto

```
├── Dockerfile
├── docker-compose.yml
├── nginx/
│   └── default.conf
├── .env
├── manage.py
├── requirements.txt
└── <código da aplicação Django>
```

---

## ⚙️ Como Executar Localmente

### 1. Clone o projeto

```bash
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
```

---

### 2. Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
# Variáveis do banco
DATABASE_ENGINE=django.db.backends.postgresql
DATABASE_NAME=appdb
DATABASE_USERNAME=admin
DATABASE_PASSWORD=admin
DATABASE_HOST=postgres
DATABASE_PORT=5432

# Variáveis do Django
DJANGO_SECRET_KEY=sua-chave-secreta
DEBUG=True
DJANGO_LOGLEVEL=info
DJANGO_ALLOWED_HOSTS=localhost 127.0.0.1
```

---

### 3. Suba os containers

```bash
docker-compose up --build
```

Acesse a aplicação no navegador via:

📍 http://localhost

---

## ✅ Funcionalidades do Projeto

- Django rodando via Gunicorn/DevServer
- PostgreSQL isolado em container
- NGINX expondo a aplicação na porta 80
- CI com GitHub Actions para build e push de imagem Docker
- Variáveis sensíveis isoladas no `.env`

---

## 👨‍💻 Autor

Desenvolvido por [Seu Nome](https://github.com/seu-usuario) como parte de um desafio técnico DevOps.
