# Software Requirements Specification (SRS) — FocusMood

## 1. Introduction

### 1.1 Purpose
This document defines functional and non-functional requirements for “FocusMood” — a web-based application that enables users to track their emotional state before and after focused work sessions, with optional user accounts and history tracking.

### 1.2 Business Goals
- Promote self-reflection on emotional-productivity correlation.
- Reduce burnout by encouraging mindful work intervals.
- Provide personalized insights through saved session history.

## 2. Overall Description

### 2.1 Product Perspective
Web application with optional user accounts (for persistent data). Can be used anonymously, but full features require login.

### 2.2 Product Functions
- User selects initial mood before starting timer.
- 25-minute focus timer runs (Pomodoro standard).
- Upon completion, user selects final mood.
- System displays mood transition feedback.
- Optional: Save session history locally or in cloud.
- Optional: Login / Sign up for persistent data.
- Optional: Choose background music for focus.

### 2.3 User Characteristics
- Target audience: students, freelancers, remote workers.
- Technical level: basic computer literacy.
- May use app anonymously or create account.

### 2.4 Constraints
- Must function in modern browsers without plugins.
- No backend required for anonymous mode; optional Firebase/Auth0 for logged-in users.
- localStorage used for local history if no account.

### 2.5 Implementation Technology (Planned)
- Frontend: HTML5, CSS3, Vanilla JavaScript (or React/Vue)
- Storage: localStorage (anonymous), Firebase (logged-in)
- Hosting: GitHub Pages (static) or Vercel (with auth)

## 3. Functional Requirements

| ID  | Description                                  |
|-----|----------------------------------------------|
| FR1 | User selects initial mood (via emoji or 1–5 scale) |
| FR2 | User starts 25-minute focus timer            |
| FR3 | On timer completion, user selects final mood |
| FR4 | System displays mood change feedback (e.g., “😩 → 😊 Improvement!”) |
| FR5 | (Optional) Store session history locally     |
| FR6 | User can log in via email/password           |
| FR7 | User can sign up for new account             |
| FR8 | Logged-in user sees dashboard with stats     |
| FR9 | User can choose background music/sound       |

## 4. Non-Functional Requirements

| Type               | Requirement                                  |
|--------------------|----------------------------------------------|
| Usability          | Minimalist, intuitive interface              |
| Performance        | Timer accuracy ±1 second                     |
| Compatibility      | Supports Chrome, Firefox, Edge               |
| Portability        | Runs directly in browser, no install         |
| Maintainability    | Code must be modular and commented           |
| Security           | Passwords stored encrypted (if backend used) |

## 5. UI Mockups
Mockups are provided in `/docs/mockups/`:

- `login.png` — User log-in page
- `main.png` — Initial screen: mood selection + “Start” button
- `music.png` — Background music selection
- `month.png` — Monthly calendar view of sessions
- `submit.png` — Post-session mood selection + feedback

## 6. Glossary

- **Focus Session**: A 25-minute uninterrupted work interval.
- **Mood Rating**: Subjective emotional state represented via emoji or numeric scale.
- **Pomodoro**: Time management method using 25-min work + 5-min break cycles.
- **User Account**: Optional feature allowing persistent data across sessions.
