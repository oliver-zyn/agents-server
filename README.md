# NLW Agents - Server

Servidor backend do projeto NLW Agents, desenvolvido durante um evento da Rocketseat.

## Tecnologias Utilizadas

- **Node.js** - Runtime JavaScript
- **TypeScript** - Tipagem estática
- **Fastify** - Framework web rápido e eficiente
- **Drizzle ORM** - ORM type-safe para TypeScript
- **PostgreSQL** - Banco de dados relacional com extensão pgvector
- **Zod** - Validação de schemas
- **Biome** - Linter e formatter

## Setup e Configuração

### Pré-requisitos

- Node.js 18+
- Docker e Docker Compose

### Instalação

1. Instale as dependências:

```bash
npm install
```

2. Configure as variáveis de ambiente:

```bash
cp .env.example .env
```

3. Inicie o banco de dados PostgreSQL:

```bash
docker compose up -d
```

4. Execute as migrations:

```bash
npx drizzle-kit migrate
```

5. Popule o banco com dados iniciais:

```bash
npm run db:seed
```

### Desenvolvimento

```bash
npm run dev
```

### Produção

```bash
npm start
```

## Estrutura do Projeto

```
src/
├── db/              # Configuração do banco de dados
│   ├── schema/      # Schemas do Drizzle ORM
│   └── migrations/  # Arquivos de migração
├── http/            # Rotas HTTP
│   └── routes/      # Definição das rotas
├── env.ts           # Validação de variáveis de ambiente
└── server.ts        # Configuração do servidor
```

## Scripts Disponíveis

- `npm run dev` - Executa em modo desenvolvimento com watch
- `npm start` - Executa em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais
