# API de Enquentes

## Descrição
Este projeto é um sistema de votação online simples que permite aos usuários criar e participar de enquetes. O sistema é construído com as seguintes tecnologias:

- Node.js: Backend do sistema
- PostgreSQL: Banco de dados
- Docker: Contêinerização
- WebSockets: Comunicação em tempo real
- Redis: Cache
- Prisma: ORM

## Forma de funcionamento do sistema:

- HTTP para CRUD de enquetes e votos
- Cache para armazenamento de sessão e controle de quantidade de votos
- WS Para ter ao vivo o resultados da votação
- PostgreSQL para gerenciar dados
- Redis para armazenar a quantidade de votos em cada opção


## Executar o projeto localmente

### Clone o repositório:
```
git clone https://github.com/caleul/polls.git
```

### Instale as dependências:
```
npm install
```

### Crie o arquivo de configuração do banco de dados:
Edite o arquivo .env e configure as credenciais do banco de dados.
```
DATABASE_URL="postgresql://docker:docker@localhost:5432/polls?schema=public"
```

### Inicie os containers
Na pasta do repositório
```
docker-compose up -d
```

### Inicie o servidor:
```
npm run dev
```

## Recursos

- Criar enquete: Crie enquetes com perguntas de múltipla escolha e defina a data de término.
- Votar: Participe de enquetes e vote nas suas opções preferidas.
- Resultados: Visualize os resultados das enquetes em tempo real.
