# Code Craft

Este é um projeto de exemplo que utiliza Fastify, Drizzle ORM, Redis e PostgreSQL para gerenciar assinaturas e rankings de referência.

## Configuração

### Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```
PORT=3333

# URL
WEB_URL="http://localhost:3000"

# Database
POSTGRES_URL="postgresql://docker:docker@localhost:5433/codecraft"
REDIS_URL="redis://localhost:6379"
```

### Docker

Utilize o Docker Compose para iniciar os serviços do PostgreSQL e Redis:

```sh
docker-compose up -d
```

### Instalação

Instale as dependências do projeto:

```sh
npm install
```

### Execução

Para iniciar o servidor em modo de desenvolvimento:

```sh
npm run dev
```

Para construir o projeto:

```sh
npm run build
```

## Endpoints

### Assinaturas

- **POST /subscriptions**: Inscreve um usuário em um evento.

### Convites

- **GET /invites/:subscriberId**: Acessa o link de convite e redireciona o usuário.

### Ranking

- **GET /ranking**: Obtém o ranking de referências.
- **GET /subscribers/:subscriberId/ranking/count**: Obtém a posição do assinante no ranking.
- **GET /subscribers/:subscriberId/ranking/clicks**: Obtém o número de cliques no link de convite do assinante.

## Documentação da API

A documentação da API está disponível em `/docs` após iniciar o servidor.

## Licença

Este projeto está licenciado sob a licença ISC.
```