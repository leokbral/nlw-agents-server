# NLW Agents

Projeto desenvolvido durante o evento **NLW Agents** da **Rocketseat**, focado na criação de um servidor backend com Node.js e PostgreSQL.

## 📋 Tecnologias Utilizadas

### Backend
- **Node.js** com TypeScript nativo (`--experimental-strip-types`)
- **Fastify** - Framework web rápido e eficiente
- **Zod** - Validação de schemas e tipagem
- **PostgreSQL** - Banco de dados relacional
- **pgvector** - Extensão do PostgreSQL para busca vetorial

### ORM e Banco de Dados
- **Drizzle ORM** - ORM moderno para TypeScript
- **postgres** - Driver PostgreSQL para Node.js
- **drizzle-kit** - Ferramentas de CLI para migrações
- **drizzle-seed** - Ferramenta para populir o banco

### Ferramentas de Desenvolvimento
- **Biome** - Linter e formatador de código
- **Docker** - Containerização do banco de dados
- **Ultracite** - Configuração pré-definida do Biome

## 🏗️ Padrões de Projeto

- **Clean Architecture** - Separação clara entre camadas
- **Dependency Injection** - Inversão de dependências
- **Schema Validation** - Validação de dados com Zod
- **Type Safety** - Tipagem forte em toda aplicação
- **RESTful API** - Padrão REST para endpoints

## 🚀 Setup e Configuração

### Pré-requisitos
- Node.js 18+
- Docker e Docker Compose
- Git

### 1. Clonar o repositório
```bash
git clone <url-do-repositorio>
cd server
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Iniciar o banco de dados
```bash
docker-compose up -d
```

### 5. Executar migrações
```bash
npx drizzle-kit migrate
```

### 6. Popular o banco (opcional)
```bash
npm run db:seed
```

### 7. Iniciar o servidor
```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## 📡 Endpoints

- `GET /health` - Verificação de saúde da aplicação
- `GET /rooms` - Listagem de salas

## 🐳 Docker

O projeto utiliza Docker para o banco de dados PostgreSQL com a extensão pgvector:

```bash
docker-compose up -d  # Iniciar banco
docker-compose down   # Parar banco
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento
- `npm start` - Inicia o servidor em modo produção
- `npm run db:seed` - Popula o banco com dados iniciais

---

Desenvolvido com ❤️ durante o **NLW Agents** da **Rocketseat**
