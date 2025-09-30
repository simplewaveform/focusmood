# State Diagrams — FocusMood

## 1. Login Screen States
States: `Not Authenticated` → `Authenticating` → `Authenticated` / `Authentication Failed`  
Transitions:
- "Log In" clicked → Authenticating
- Valid credentials → Authenticated
- Invalid credentials → Authentication Failed → back to Not Authenticated

## 2. Focus Session States
States: `Mood Selection` → `Timer Running` → `Final Mood Selection` → `Result Displayed`  
Transitions:
- Mood selected → Timer Running
- Timer ends → Final Mood Selection
- Final mood submitted → Result Displayed
![](https://github.com/simplewaveform/focusmood/blob/main/docs/Diagrams/State_FocusSession.png)

## 3. Profile/History States
States: `Dashboard Idle` → `Loading Calendar` → `Session Details View`  
Transitions:
- Open profile → Loading Calendar
- Click date → Session Details View
- Back button → Dashboard Idle
