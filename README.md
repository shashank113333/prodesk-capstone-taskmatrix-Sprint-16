# 🚀 TaskMatrix — Sprint 16: The AI Injection & Polish (Commercial SaaS Deliverable)

![Sprint 16 Status](https://img.shields.io/badge/Sprint-16_AI_&_Polish-emerald?style=for-the-badge)
![Track](https://img.shields.io/badge/Track-A:_Frontend_Specialist-blue?style=for-the-badge)
![Next.js 14](https://img.shields.io/badge/Next.js-14_App_Router-black?style=for-the-badge)
![Google Gemini AI](https://img.shields.io/badge/AI_Engine-Google_Gemini_1.5_Flash-purple?style=for-the-badge)

## 📌 Executive Summary
Sprint 16 elevates **TaskMatrix** from a student project into a commercial-grade, SaaS-level Agile Task Management System. Under strict **Code Freeze** protocols, client-side UX/UI responsiveness has been perfected for mobile viewports, non-blocking toast notifications integrated, branded empty state fallbacks implemented, and a server-side **Google Gemini AI Microservice** deployed for 1-click automated subtask generation.

---

## 🌐 Live Application & Links
- 🚀 **Live Website (Vercel)**: [https://prodesk-capstone-taskmatrix-sprint-inky.vercel.app](https://prodesk-capstone-taskmatrix-sprint-inky.vercel.app)
- 📦 **GitHub Repository**: [https://github.com/shashank113333/prodesk-capstone-taskmatrix-Sprint-16](https://github.com/shashank113333/prodesk-capstone-taskmatrix-Sprint-16)
- 📝 **AI Compliance Log**: Refer to [`Prompts.md`](./Prompts.md) for complete LLM system prompts and engineering rationale logs.

---

## 🔑 Evaluator & System Administrator Credentials

Below are pre-seeded credentials for evaluators to audit mobile responsiveness, RBAC security guards, and Gemini AI subtask generation:

| Role Name | Agile Designation | Email Address | Default Password | Permissions & Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **System Administrator** | Master System Admin | `shashankv@gmail.com` | `1234` | Full Admin Control: AI Subtask Generator, BaaS CRUD, Accounts DB Directory, Timed Account Suspensions, Role Editor |
| **Scrum Lead** | Project Lead / Scrum Master | `scrumlead@prodesk.io` | `1234` | Project Lead Control: AI Subtask Generator, CRUD Operations, Task Deletion with Confirmation Modal |
| **Developer** | Frontend Specialist | `developer@prodesk.io` | `1234` | Developer Access: AI Subtask Generator, Create/View/Edit tasks (Restricted from Delete & Accounts DB) |

---

## 🏗️ Technical Architecture & Tech Stack

| Layer | Technology / Tool | Operational Rationale |
| :--- | :--- | :--- |
| **Framework** | Next.js 14 (App Router) | Server-driven routing, edge API microservices & static optimization |
| **AI Microservice** | Google Gemini 1.5 Flash API | Server-side LLM call via `/api/ai/generate-subtasks` with strict JSON schema |
| **Language** | TypeScript | Strict typing for Task entities, stores, and API payloads |
| **Styling** | Tailwind CSS | Responsive utility-first dark mode design & mobile drawer UI |
| **State Management** | Zustand | Global auth & task state persistence with localStorage hydration |
| **Analytics Engine** | Recharts | Dynamic Bar and Distribution charts driven by `.reduce()` metrics |
| **Icons** | Lucide React | Enterprise UI iconography (`Menu`, `Sparkles`, `Inbox`, `ShieldAlert`) |

---

## 🔑 Key Features Implemented (Sprint 16 Deliverables)

### 📱 1. Viewport Responsiveness (Phase 1 - P0 Mandatory)
- **Mobile Hamburger Drawer**: Responsive navbar drawer integrated (`Menu` icon toggle) on mobile viewports (`<768px`) ensuring full access to Profile details, Accounts DB, and Logout buttons.
- **Layout & Overflow Isolation**: Grid container optimization and overflow control across mobile device sizes (e.g. iPhone 14 Pro, 375px–430px).

### 🤖 2. Client-Side AI Injection (Phase 2 - P1 Priority)
- **Server-Side AI Endpoint**: Dedicated API Route (`POST /api/ai/generate-subtasks`) executing Google Gemini 1.5 Flash LLM calls securely with environment variable keys.
- **Auto-Generate Task Sub-steps**: Task Modal features a **`✨ Auto-generate Sub-tasks`** button that parses Task Titles/Descriptions and auto-populates formatted actionable sub-step bullet points.
- **Prompts Documentation**: All system prompts, regex JSON fallbacks, and security rationales logged in `Prompts.md`.

### ✨ 3. Micro-Interactions & Fallback States (Phase 3 - P2 Advanced)
- **Toast Notifications**: Replaced browser `alert()` popups with non-blocking toast notifications (`Access Control Notice`) for RBAC authorization guards.
- **Asynchronous Loading UX**: Integrated smooth CSS animated spinners (`Loader2 animate-spin`) during AI payload generation and hydration.
- **Branded Empty States**: Kanban columns with zero tasks render branded empty state cards with `<Inbox />` icons and helpful action prompts.

---

## 🛠️ Local Development Setup

```bash
# 1. Clone the repository
git clone https://github.com/shashank113333/prodesk-capstone-taskmatrix-Sprint-16.git

# 2. Navigate to project directory
cd prodesk-capstone-taskmatrix-Sprint-16

# 3. Install dependencies
npm install

# 4. Set up environment variables (.env.local)
# GEMINI_API_KEY=your_google_gemini_api_key

# 5. Launch development server
npm run dev
```
