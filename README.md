# NLW Agents - Web

<p align="center">
<img src="https://img.shields.io/badge/Projeto-NLW%20Agents%20Web-573dff?style=for-the-badge&logo=react&logoColor=white" />
<img src="https://img.shields.io/badge/Evento-Rocketseat-E82D92?style=for-the-badge&logo=rocket&logoColor=white" />
</p>

Frontend da aplicação **NLW Agents** desenvolvido durante um evento da **Rocketseat**. O projeto utiliza React com TypeScript, Vite como bundler e TailwindCSS para estilização.

## 🧩 Tecnologias Utilizadas

### Frontend

- **React** - Biblioteca para interfaces de usuário
- **TypeScript** - Tipagem estática para JavaScript
- **Vite** - Build tool rápida para desenvolvimento
- **React Router DOM** - Roteamento para aplicações React
- **TailwindCSS** - Framework CSS utility-first
- **Lucide React** - Ícones para React
- **Shadcn/UI** - Componentes de UI acessíveis
- **TanStack React Query** - Gerenciamento de estado de servidor
- **Biome** - Linter e formatter para JavaScript/TypeScript

## 📁 Estrutura do Projeto

```
src/
├── components/
│   └── ui/
│       └── button.tsx      # Componente de botão reutilizável
├── lib/
│   └── utils.ts           # Utilitários e helpers
├── pages/
│   ├── create-room.tsx    # Página de criação/listagem de salas
│   └── room.tsx           # Página da sala de chat
├── app.tsx               # Componente principal da aplicação
├── main.tsx              # Ponto de entrada da aplicação
├── index.css             # Estilos globais
└── vite-env.d.ts         # Definições de tipos do Vite
```

## 🚀 Setup e Configuração

### Pré-requisitos

- Node.js (versão 18 ou superior)
- npm ou yarn
- Servidor backend rodando em `http://localhost:3333`

### 1. Instalação das Dependências

```bash
npm install
```

### 2. Executar a Aplicação

#### Desenvolvimento

```bash
npm run dev
```

A aplicação estará disponível em `http://localhost:5173`

#### Build para Produção

```bash
npm run build
```

#### Preview da Build

```bash
npm run preview
```

## 📋 Scripts Disponíveis

- `npm run dev` - Executa a aplicação em modo desenvolvimento
- `npm run build` - Gera build otimizada para produção
- `npm run preview` - Visualiza a build de produção localmente

## 🔗 Funcionalidades

### Páginas

- **Página Inicial** (`/`) - Listagem de salas disponíveis e criação de novas salas
- **Sala** (`/room/:roomId`) - Interface da sala de chat com agentes

### Componentes

- **Button** - Componente de botão customizável com variantes
- **Utilitários** - Funções helper para manipulação de classes CSS

## 🎨 Sistema de Design

O projeto utiliza **TailwindCSS** como framework de estilização, proporcionando:

- Design system consistente
- Responsividade mobile-first
- Componentes reutilizáveis com **Radix UI**
- Ícones com **Lucide React**

## 🔌 Integração com Backend

A aplicação se conecta com o backend através de:

- **TanStack React Query** para gerenciamento de estado de servidor
- Requisições HTTP para `http://localhost:3333`
- Endpoints utilizados:
  - `GET /rooms` - Listagem de salas

---

Desenvolvido durante o evento **NLW Agents** da [Rocketseat](https://rocketseat.com.br) 🚀
