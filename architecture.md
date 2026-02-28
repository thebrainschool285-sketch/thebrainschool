# The Brain School - Project Architecture

## 1. High-Level System Architecture

The Brain School platform is built using a modern, scalable, and high-performance tech stack following a Jamstack/Client-Server hybrid architecture.

### 1.1 Frontend (Client-Side)
- **Framework:** Next.js 14 (App Router)
- **Library:** React 18
- **Styling:** Tailwind CSS (utility-first, responsive design, dark mode)
- **Animations:** Framer Motion (page transitions, micro-interactions), Three.js (3D Hero elements), GSAP (complex scroll sequences if needed)
- **State Management:** Zustand or React Context API
- **Deployment:** Vercel (for edge caching, serverless functions, and global CDN)

### 1.2 Backend (Server-Side)
- **Platform:** Supabase (PostgreSQL-based backend-as-a-service) or Next.js API Routes (Node.js) backed by Firebase. *Recommendation: Supabase for relational data handling which is superior for LMS (users, courses, enrollments, etc.)*
- **Authentication:** Supabase Auth (JWT-based, supports email/password, OAuth)
- **Storage:** Supabase Storage or AWS S3 (for lecture videos, assignment documents, user avatars)
- **Payment Gateway:** Stripe API (for credit cards, wallets) integrated via Next.js Server Actions/API routes.

## 2. Core Modules & Data Flow

### 2.1 User Roles & Authentication Flow
- **Authentication:** Unified login/signup portal. Role-Based Access Control (RBAC) determines post-login redirection.
- **Roles:** `Admin`, `Student`, `Teacher`, `Parent`.

### 2.2 Learning Management System (LMS)
- **Content Delivery:** Videos streamed via optimized CDN.
- **Live Classes:** Integration with Zoom API or Google Meet API to inject meeting links into student dashboards.
- **Assignments:** Real-time database updates for assignment submissions, utilizing Supabase Storage for drag-and-drop document uploads.

### 2.3 Tuition Marketplace
- **Search Engine:** Algolia or Supabase Full-Text Search for fast, typo-tolerant tutor searching.
- **Scheduling:** Integration with Calendly API or a custom time-slot booking system stored in the database.

## 3. Aesthetic & UI/UX Principles
- **Design System:** "Apple-style" minimalism, extensive use of white space, SF Pro/Inter typography.
- **Glassmorphism:** Frosted glass effects (`backdrop-blur` in Tailwind) for sticky headers, floating navigation, and modal backgrounds.
- **Bento Grid Layouts:** Dashboard widgets and feature highlights presented in a masonry/grid style with varying card sizes, soft shadows, and rounded corners (`rounded-2xl` to `rounded-3xl`).
- **Theming:** CSS Variables handling color palettes (Deep Blue: `#0A192F`, Electric Blue: `#00D8FF`, Neon Purple: `#B026FF`) with a strict Dark Mode toggle mapped via `next-themes`.

---

*This architecture ensures The Brain School is incredibly fast, visually stunning, fully responsive, and highly scalable for thousands of concurrent users.*
