# Oráculo Brasileiro - App de Astrologia e Espiritualidade

Um aplicativo móvel que combina astrologia ocidental com sabedorias das religiões afro-brasileiras (candomblé, umbanda), oferecendo horóscopos personalizados, leituras de tarô e conexão com orixás.

## 🌟 Funcionalidades

### Core Features
- **Autenticação**: Sistema de cadastro e login com JWT
- **Mapa Astral**: Criação e análise de mapas astrais personalizados
- **Horóscopos Diários**: Horóscopos com influências dos orixás
- **Leituras de Tarô**: Sistema de tiragem de cartas com interpretações culturais
- **Orixás**: Base de dados com informações sobre orixás e suas correspondências
- **Sistema Premium**: Planos gratuito e premium com diferentes benefícios

### Características Técnicas
- **Backend**: Node.js + Express + PostgreSQL
- **Frontend**: React + TypeScript + Tailwind CSS
- **Autenticação**: JWT com refresh tokens
- **Database**: PostgreSQL com Drizzle ORM
- **UI**: Shadcn/ui components
- **Styling**: Tailwind CSS com cores místicas personalizadas

## 🚀 Como Executar

### Pré-requisitos
- Node.js 18+
- PostgreSQL database
- Variáveis de ambiente configuradas

### Variáveis de Ambiente Necessárias
```env
DATABASE_URL=postgresql://username:password@localhost:5432/oraculo_brasileiro
JWT_SECRET=your-jwt-secret-key
