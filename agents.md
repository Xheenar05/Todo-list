# AGENTS.md — AI Engineering Directives & Project Structure

This document establishes the architecture, agent roles, and execution workflows for building and maintaining the **AI Todo Studio** repository.

---

## 1. Project Purpose & Architecture
- **Objective:** Provide a fast, responsive, single-page application (SPA) todo list with integrated AI breakdown and natural-language capabilities.
- **Tech Stack:**
  - **HTML5:** Semantic SPA structure.
  - **Tailwind CSS:** Utility-first dark modern design system.
  - **JavaScript (Vanilla ES6+):** Client-side application state, LocalStorage, and AI heuristic algorithms.
- **Hosting Target:** GitHub Pages (Static Web Hosting).

---

## 2. AI Agent Roles & Directives

When AI coding assistants or developers operate on this codebase, they must follow these role specifications:

### 🏗️ `@architect-agent`
- **Responsibility:** Codebase structure, scalability, performance.
- **Rules:**
  - Maintain zero-dependency static execution (runs strictly in browser without custom server builds).
  - Use `localStorage` as the source of truth for task persistence.

### 🎨 `@frontend-agent`
- **Responsibility:** Design aesthetics, UI components, responsiveness.
- **Rules:**
  - Stick to the modern dark glassmorphism palette (`bg-slate-900`, `indigo`, `purple`, `emerald`).
  - Guarantee full responsiveness across mobile, tablet, and desktop screens.

### 🧠 `@ai-logic-agent`
- **Responsibility:** Natural language parsing, AI goal decomposition, and task prioritization heuristics.
- **Rules:**
  - Ensure fallback client-side heuristics work without external API keys.
  - Keep task input parsing secure against script injection (sanitize inputs).

### 🧪 `@qa-agent`
- **Responsibility:** Code verification and reliability.
- **Rules:**
  - Validate state persistence across browser refreshes.
  - Test edge cases (empty inputs, rapid submissions, long task titles).

---

## 3. Workflow & Development Lifecycle

1. **Feature Planning:** Break tasks down using `@architect-agent` guidelines.
2. **Implementation:** Write clean code conforming to `@frontend-agent` and `@ai-logic-agent` standards.
3. **Commit Guidelines:** Use standard commit formatting:
   - `feat: add task filtering system`
   - `fix: prevent empty task submission`
   - `docs: update AGENTS.md workflow directives`

---

## 4. Feature Roadmap

- [x] Responsive Dark Mode UI
- [x] Full CRUD operations with LocalStorage support
- [x] Natural language hashtag parsing (`#high`, `#low`)
- [x] AI Goal Breakdown engine
- [x] Automated productivity insights
- [ ] Export/Import task backups (JSON)
