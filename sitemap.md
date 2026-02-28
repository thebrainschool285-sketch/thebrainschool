# The Brain School - Detailed Sitemap

## 1. Public Facing Pages (Marketing & Discovery)
- **`/` (Homepage)**
  - 3D Hero Section (Dynamic Counters: Students, Tutors, Success Stories)
  - Bento Grid Features Overview
  - Testimonials (Scroll-triggered animations)
  - Footer & Newsletter CTA
- **`/about` (About Us)**
  - Vision & Mission
  - Team/Founders
- **`/tutors` (Tuition Marketplace)**
  - Advanced Search & Filters (Subject, Grade, Language, Price)
  - **`/tutors/[id]` (Tutor Profile)**
    - Tutor Details & Intro Video
    - "Book a Demo Class" / Scheduling UI
    - Reviews & Ratings
- **`/courses` (Recorded/Structured Courses)**
  - Course Catalog
  - **`/courses/[slug]` (Course Detail)**
    - Syllabus, Pricing, Enrollment CTA
- **`/admissions` (Admissions & Onboarding)**
  - Enrollment Form (Drag-and-drop document upload)
  - Stripe Payment Integration checkout flow
- **`/contact` (Contact & Support)**
  - Help Center / FAQ
  - Support Form

## 2. Authentication
- **`/login`** (Unified Login with Role redirection)
- **`/register`** (Signup forms step-by-step)
- **`/forgot-password`**

## 3. Secure Dashboards (Requires Authentication)

### 3.1 Student Dashboard (`/student`)
- **`/student/dashboard`** (Overview: Upcoming Classes, Recent Grades, Progress)
- **`/student/courses`** (List of enrolled courses)
  - **`/student/courses/[id]/learn`** (Video player, Course curriculum sidebar)
- **`/student/assignments`**
  - Pending & Submitted (File upload area)
- **`/student/live-classes`** (Zoom/Meet links schedule)
- **`/student/results`** (Result cards and feedback)
- **`/student/settings`** (Profile, Password, Notification prefs)

### 3.2 Teacher Dashboard (`/teacher`)
- **`/teacher/dashboard`** (Overview: Today's Schedule, Pending Grading)
- **`/teacher/courses`** (Manage uploaded content/lectures)
- **`/teacher/assignments`** (Review and grade student submissions)
- **`/teacher/attendance`** (Marking tools for live classes)
- **`/teacher/calendar`** (Manage 1-on-1 bookings and demo classes)
- **`/teacher/earnings`** (Revenue tracking)

### 3.3 Parent Dashboard (`/parent`)
- **`/parent/dashboard`** (Overview of child's progress)
- **`/parent/academic-tracker`** (Detailed breakdown of grades, attendance)
- **`/parent/billing`** (Fee payment history, pending invoices, Payment Gateway link)
- **`/parent/messages`** (Direct messaging with Teachers/Admin)

## 4. Admin Dashboard (`/admin`)
- **`/admin/users`** (Manage all Students, Teachers, Parents)
- **`/admin/finance`** (Platform-wide revenue, payouts to teachers)
- **`/admin/platform-settings`** (Global config, Hero counters config)
