# 🚀 AI Coding Agent

A fully-featured **cloud-based AI-powered IDE** built with modern web technologies.

AI Coding Agent is a browser-based development environment inspired by modern AI-native code editors, featuring real-time collaboration, AI-assisted editing, and full-stack project management.

---

## ✨ Features

### 🧠 AI Capabilities

* Real-time code suggestions with ghost text
* Quick Edit (Cmd + K style natural language editing)
* Conversation-based AI assistant
* Context-aware code improvements

### 💻 Code Editor

* Multi-language syntax highlighting (JS, TS, CSS, HTML, JSON, Markdown, Python)
* Line numbers & code folding
* Minimap overview
* Bracket matching & indentation guides
* Multi-cursor editing
* Tab-based file navigation

### 📁 File Management

* File explorer with folder hierarchy
* Create, rename, delete files and folders
* VSCode-style file icons
* Auto-save with debouncing

### ⚡ Real-Time Architecture

* Instant updates powered by Convex
* Optimistic UI updates
* Background job processing via Inngest

---

# 🏗 Tech Stack

| Category                | Technologies                                           |
| ----------------------- | ------------------------------------------------------ |
| **Frontend**            | Next.js 16, React 19, TypeScript, Tailwind CSS 4       |
| **Editor**              | CodeMirror 6, Custom Extensions                        |
| **Backend**             | Convex (Real-time Database), Inngest (Background Jobs) |
| **AI**                  | Claude Sonnet 4 or Gemini 2.0 Flash                    |
| **Auth**                | Clerk (with GitHub OAuth)                              |
| **UI**                  | shadcn/ui, Radix UI                                    |
| **Execution (Planned)** | WebContainer API, xterm.js                             |

---

# 📂 Project Structure

```
src/
├── app/
│   ├── api/
│   │   ├── messages/
│   │   ├── suggestion/
│   │   └── quick-edit/
│   └── projects/
├── components/
│   ├── ui/
│   └── ai-elements/
├── features/
│   ├── auth/
│   ├── conversations/
│   ├── editor/
│   ├── preview/
│   └── projects/
├── inngest/
└── lib/

convex/
├── schema.ts
├── projects.ts
├── files.ts
├── conversations.ts
└── system.ts
```

---

# 🛠 Getting Started

## Prerequisites

* Node.js 20+
* npm or pnpm
* Accounts required:

  * Clerk (Authentication)
  * Convex (Database)
  * Inngest (Background jobs)
  * Anthropic or Google AI Studio (AI API)

---

## Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Coding-Agent.git
cd AI-Coding-Agent
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Setup Environment Variables

```bash
cp .env.example .env.local
```

Add:

```env
# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

# Convex
NEXT_PUBLIC_CONVEX_URL=
CONVEX_DEPLOYMENT=
POLARIS_CONVEX_INTERNAL_KEY=

# AI Provider (Choose one)
ANTHROPIC_API_KEY=
GOOGLE_GENERATIVE_AI_API_KEY=
```

---

### 4️⃣ Start Development Servers

Terminal 1:

```bash
npx convex dev
```

Terminal 2:

```bash
npm run dev
```

Terminal 3:

```bash
npx inngest-cli@latest dev
```

---

### 5️⃣ Open in Browser

```
http://localhost:3000
```

---

# 📜 Scripts

```bash
npm run dev       # Development server
npm run build     # Production build
npm run start     # Start production
npm run lint      # ESLint
```

---
