# TaskFlow — A Fast, Flexible Kanban Board for Modern Workflows

TaskFlow is a modern Kanban-style task management application focused on speed,
clarity, and real-world usability. It helps individuals organize work visually
without unnecessary complexity.

---

## Live Demo & Links

🔗 Live Demo: https://taskflow.vercel.app  
📦 GitHub Repository: https://github.com/your-username/taskflow  

---

## Why TaskFlow?

Most task management tools are either too simple to scale
or too complex for everyday use.

TaskFlow was built to strike a balance — a clean Kanban system that stays fast,
flexible, and intuitive while handling real workflows like drag-and-drop,
task updates, and filtering.

The focus of this project was not feature quantity,
but solid architecture, clean UX, and maintainable code.

---

## Core Features

- Create and manage multiple boards
- Custom columns for flexible workflows
- Drag-and-drop tasks between columns
- Edit tasks (title, description, priority, due date)
- Filter tasks by priority and due date
- Responsive design for desktop and mobile
- Secure authentication and data isolation
- Realtime-ready backend architecture

---

## Tech Stack

- **Next.js (App Router)** — modern routing, performance, SEO-friendly
- **React + TypeScript** — predictable UI logic and type safety
- **Supabase (PostgreSQL)** — relational database with Row Level Security
- **Clerk** — secure authentication and user management
- **dnd-kit** — accessible, predictable drag-and-drop
- **Tailwind CSS + shadcn/ui** — fast, consistent UI development

---

## Architecture Overview

TaskFlow follows a layered architecture to keep UI clean
and business logic centralized.

UI Components
↓
Custom Hooks (useBoard, useBoards)
↓
Service Layer (taskService, boardService)
↓
Supabase (PostgreSQL + RLS)


- UI components focus only on rendering
- Hooks manage state and orchestration
- Services handle all database interactions
- This separation improves scalability and maintainability

---

## Key Engineering Decisions

- Scoped the app as a **single-user system** to focus on execution quality
- Centralized task logic in hooks to avoid prop drilling
- Used optimistic UI updates for smooth drag-and-drop experience
- Avoided premature features like collaboration until core UX was solid
- Designed the backend to be realtime-ready without overengineering

---

## Data & Security

- PostgreSQL database managed by Supabase
- Row Level Security (RLS) ensures users can only access their own data
- All reads and writes go through a controlled service layer
- Authentication handled securely via Clerk

---

## Limitations & Future Improvements

Current limitations:
- Designed for single-user workflows
- No real-time collaboration between users
- No activity logs or task history

Planned / possible improvements:
- Multi-user board collaboration
- Realtime presence indicators
- Activity logs and audit history
- Performance optimizations for large boards

---

## What I Learned

- Designing scalable frontend architecture using hooks and services
- Managing complex UI state with drag-and-drop interactions
- Making product trade-offs instead of overbuilding features
- Writing cleaner, more maintainable React + TypeScript code
- Thinking beyond “just making it work” toward real usability

---

## Running the Project Locally

```bash
# Clone the repository
git clone https://github.com/your-username/taskflow.git

# Install dependencies
npm install

# Add environment variables
cp .env.example .env.local

# Start the development server
npm run dev


Built with ❤️ by  Ved