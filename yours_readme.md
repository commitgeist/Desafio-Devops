# Desafio DevOps – Deploy Django + PostgreSQL com Docker

Este repositório contém a solução para o desafio DevOps, cujo objetivo é provisionar e disponibilizar uma aplicação Django com banco de dados PostgreSQL, utilizando Docker, Docker Compose, NGINX e CI/CD com GitHub Actions.

---

##  Tecnologias Utilizadas

- [x] Python + Django
- [x] PostgreSQL 17
- [x] Docker e Docker Compose
- [x] NGINX (Proxy reverso)
- [x] GitHub Actions (CI)
- [x] `.env` para variáveis de ambiente

---

## 📦 Estrutura do Projeto

├── Dockerfile
├── docker-compose.yml
├── nginx/
│ └── default.conf
├── .env
├── manage.py
├── requirements.txt
└── <código do projeto Django>



---

## ⚙️ Como Executar Localmente

### 1. Clone o projeto

```bash
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
```

Crie um arquivo .env na raiz com o seguinte conteúdo:

2. Configure o arquivo .env
```bash
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

3. Suba os containers

```bash
docker-compose up --build
```