# NLW Agents - Web

<p align="center">
<img src="https://img.shields.io/badge/Projeto-NLW%20Agents%20Web-573dff?style=for-the-badge&logo=react&logoColor=white" />
<img src="https://img.shields.io/badge/Evento-Rocketseat-E82D92?style=for-the-badge&logo=rocket&logoColor=white" />
</p>

Frontend da aplicação **NLW Agents** desenvolvido durante um evento da **Rocketseat**. O projeto utiliza React com TypeScript, Vite como bundler e TailwindCSS para estilização.

## 🧩 Tecnologias Utilizadas

### Frontend

- **React 19** - Biblioteca para interfaces de usuário
- **TypeScript** - Tipagem estática para JavaScript
- **Vite** - Build tool rápida para desenvolvimento
- **React Router DOM** - Roteamento para aplicações React
- **TailwindCSS 4** - Framework CSS utility-first
- **Lucide React** - Ícones para React
- **Shadcn/UI** - Componentes de UI acessíveis
- **TanStack React Query** - Gerenciamento de estado de servidor
- **React Hook Form** - Gerenciamento de formulários performático
- **Zod** - Validação de esquemas TypeScript-first
- **Day.js** - Biblioteca para manipulação de datas
- **Biome** - Linter e formatter para JavaScript/TypeScript
- **Web Speech API** - Reconhecimento de voz nativo do browser

## 📁 Estrutura do Projeto

```
src/
├── components/
│   ├── ui/
│   │   ├── button.tsx          # Componente de botão reutilizável
│   │   ├── card.tsx            # Componente de card
│   │   ├── form.tsx            # Componentes de formulário
│   │   ├── input.tsx           # Componente de input
│   │   ├── label.tsx           # Componente de label
│   │   ├── textarea.tsx        # Componente de textarea
│   │   ├── badge.tsx           # Componente de badge
│   │   └── skeleton.tsx        # Componente de loading skeleton
│   ├── create-room-form.tsx    # Formulário de criação de salas
│   ├── room-list.tsx           # Lista de salas disponíveis
│   ├── question-form.tsx       # Formulário de perguntas
│   ├── question-item.tsx       # Item individual de pergunta
│   └── question-list.tsx       # Lista de perguntas da sala
├── http/
│   ├── types/
│   │   ├── create-room-*.ts    # Tipos para criação de salas
│   │   ├── create-question-*.ts # Tipos para criação de perguntas
│   │   └── get-room-*.ts       # Tipos para busca de dados da sala
│   ├── use-create-room.ts      # Hook para criação de salas
│   ├── use-create-question.ts  # Hook para criação de perguntas
│   ├── use-room-questions.ts   # Hook para buscar perguntas da sala
│   └── use-rooms.ts            # Hook para buscar salas
├── lib/
│   ├── utils.ts               # Utilitários e helpers
│   └── dayjs.ts               # Configuração do Day.js
├── pages/
│   ├── create-room.tsx        # Página de criação/listagem de salas
│   ├── room.tsx               # Página da sala de chat
│   └── record-room-audio.tsx  # Página de gravação de áudio
├── app.tsx                    # Componente principal da aplicação
├── main.tsx                   # Ponto de entrada da aplicação
├── index.css                  # Estilos globais com TailwindCSS
└── vite-env.d.ts              # Definições de tipos do Vite
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
- `npm run build` - Compila TypeScript e gera build otimizada para produção
- `npm run preview` - Visualiza a build de produção localmente

## 🔗 Funcionalidades

### Páginas

- **Página Inicial** (`/`) - Listagem de salas disponíveis e criação de novas salas
- **Sala** (`/room/:roomId`) - Interface da sala de chat com perguntas e respostas
- **Gravação de Áudio** (`/room/:roomId/audio`) - Interface para gravação de áudio usando Web Speech API

### Recursos Principais

- **Criação de Salas** - Formulário para criar novas salas de chat
- **Listagem de Salas** - Visualização de todas as salas disponíveis
- **Sistema de Perguntas** - Criação e listagem de perguntas em tempo real
- **Respostas Automáticas** - Integração com IA para geração de respostas
- **Gravação de Áudio** - Suporte a reconhecimento de voz nativo do browser
- **Interface Responsiva** - Design adaptável para diferentes dispositivos

### Componentes Reutilizáveis

- **Formulários** - Componentes de formulário com validação usando React Hook Form + Zod
- **Cards** - Componentes de card para organização de conteúdo
- **Botões** - Componentes de botão customizáveis com variantes
- **Inputs** - Componentes de entrada de dados com validação
- **Loading States** - Skeleton components para estados de carregamento

## 🎨 Sistema de Design

O projeto utiliza **TailwindCSS 4** como framework de estilização, proporcionando:

- **Design System Consistente** - Paleta de cores e espaçamentos padronizados
- **Responsividade Mobile-First** - Design adaptável para todos os dispositivos
- **Componentes Reutilizáveis** - Baseados em **Radix UI** para acessibilidade
- **Ícones Modernos** - Biblioteca **Lucide React** para ícones consistentes
- **Animações Suaves** - Transições e estados visuais aprimorados
- **Tema Customizável** - Variáveis CSS para personalização fácil

### Padrões de Design

- **Atomic Design** - Componentes organizados em hierarquia reutilizável
- **Compound Components** - Padrão para componentes complexos
- **Variant API** - Sistema de variantes para componentes flexíveis

## 🔌 Integração com Backend

A aplicação se conecta com o backend através de:

- **TanStack React Query** para gerenciamento de estado de servidor e cache
- **Custom Hooks** para abstração das chamadas HTTP
- Requisições HTTP para `http://localhost:3333`
- **Endpoints utilizados:**
  - `GET /rooms` - Listagem de salas
  - `POST /rooms` - Criação de novas salas
  - `GET /rooms/:id/questions` - Busca perguntas de uma sala
  - `POST /rooms/:id/questions` - Criação de perguntas em salas
  - `POST /rooms/:id/questions/:id/answers` - Geração de respostas para perguntas

### Tipos TypeScript

O projeto utiliza tipagem forte com interfaces específicas para:

- Requisições e respostas da API
- Estados dos componentes
- Validação de formulários com Zod schemas

## 🏗️ Arquitetura

### Padrões Utilizados

- **Custom Hooks** - Abstrações para lógica reutilizável de API
- **Compound Components** - Componentes complexos com múltiplas partes
- **Render Props** - Padrão para compartilhamento de lógica entre componentes
- **Server State Management** - Gerenciamento otimizado de dados do servidor

### Estrutura de Dados

- **Optimistic Updates** - Atualizações otimistas para melhor UX
- **Cache Invalidation** - Estratégias inteligentes de invalidação de cache
- **Error Boundaries** - Tratamento robusto de erros em componentes

## 🔧 Requisitos do Sistema

### Navegadores Suportados

- Chrome/Edge 88+
- Firefox 85+
- Safari 14+

### APIs Necessárias

- **Web Speech API** (para funcionalidade de gravação de áudio)
- **MediaRecorder API** (para captura de áudio)
- **getUserMedia API** (para acesso ao microfone)

### Permissões

A aplicação pode solicitar permissão para:

- Acesso ao microfone (para gravação de áudio)

## 🐛 Troubleshooting

### Problemas Comuns

**Erro de CORS:**

```
Verifique se o backend está rodando em http://localhost:3333
```

**Funcionalidade de áudio não funciona:**

```
Verifique se o navegador suporta Web Speech API
Certifique-se de que as permissões de microfone estão concedidas
```

**Build falha:**

```
npm run build
# Se houver erro de TypeScript, execute:
npx tsc --noEmit
```

---

Desenvolvido durante o evento **NLW Agents** da [Rocketseat](https://rocketseat.com.br) 🚀
