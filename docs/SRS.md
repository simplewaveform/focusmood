# Software Requirements Specification (SRS) — FocusMood

## 1. Introduction

### 1.1 Purpose
This document defines functional and non-functional requirements for “FocusMood” — a web-based application that enables users to track their emotional state before and after a focused work session.

### 1.2 Business Goals
- Promote self-reflection on emotional-productivity correlation.
- Reduce burnout by encouraging mindful work intervals.
- Provide a zero-friction tool for students and remote workers seeking better focus habits.

## 2. Overall Description

### 2.1 Product Perspective
Standalone client-side web application. No server, authentication, or external dependencies.

### 2.2 Product Functions
- User selects initial mood before starting timer.
- 25-minute focus timer runs (Pomodoro standard).
- Upon completion, user selects final mood.
- System displays mood transition feedback.

### 2.3 User Characteristics
- Target audience: students, freelancers, remote workers.
- Technical level: basic computer literacy.
- No setup or installation required.

### 2.4 Constraints
- Must function in modern browsers without plugins.
- No persistent storage required (localStorage optional).
- No backend or user accounts.

### 2.5 Implementation Technology (Planned)
- Frontend: HTML5, CSS3, Vanilla JavaScript
- Storage: localStorage (optional, for session history)
- Hosting: GitHub Pages

## 3. Functional Requirements

| ID  | Description                                  |
|-----|----------------------------------------------|
| FR1 | User selects initial mood (via emoji or 1–5 scale) |
| FR2 | User starts 25-minute focus timer            |
| FR3 | On timer completion, user selects final mood |
| FR4 | System displays mood change feedback (e.g., “😩 → 😊 Improvement!”) |
| FR5 | (Optional) Store session history locally     |

## 4. Non-Functional Requirements

| Type               | Requirement                                  |
|--------------------|----------------------------------------------|
| Usability          | Minimalist, intuitive interface              |
| Performance        | Timer accuracy ±1 second                     |
| Compatibility      | Supports Chrome, Firefox, Edge               |
| Portability        | Runs directly in browser, no install         |
| Maintainability    | Code must be modular and commented           |

## 5. UI Mockups
Mockups are provided in `/docs/mockups/`:

- `main-screen.png` — Initial screen: mood selection + “Start” button
- `result-screen.png` — Post-session screen: mood re-selection + feedback

## 6. Glossary

- **Focus Session**: A 25-minute uninterrupted work interval.
- **Mood Rating**: Subjective emotional state represented via emoji or numeric scale.
- **Pomodoro**: Time management method using 25-min work + 5-min break cycles.
