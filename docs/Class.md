# Class Diagram — FocusMood

## 1. User
- id: string
- email: string
- password: string
- sessions: Session[]

Methods:
- login(): boolean
- logout(): void

## 2. Session
- startTime: Date
- endTime: Date
- initialMood: string
- finalMood: string
- duration: number = 25

Methods:
- calculateMoodChange(): string  // e.g., "Improved", "Worsened"

## 3. TimerService
- timeLeft: number
- isRunning: boolean

Methods:
- start(duration: number): void
- stop(): void
- onTick(callback: Function): void

## 4. MoodSelector
- selectedMood: string

Methods:
- submitMood(): void

## 5. StorageService
Methods:
- saveSession(session: Session): void
- loadSessions(): Session[]
