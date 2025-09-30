# Sequence Diagrams — FocusMood

## 1. Log In
Objects: `LoginUI`, `AuthService`, `UserProfile`  
Flow:
- User → LoginUI: enter email/password
- LoginUI → AuthService: authenticate(email, password)
- AuthService → UserProfile: loadUserData()
- UserProfile → LoginUI: displayDashboard()
![](https://github.com/simplewaveform/focusmood/blob/main/docs/Diagrams/Sequence_LogIn.png)

## 2. Start Focus Session
Objects: `MoodSelector`, `TimerService`, `ResultScreen`  
Flow:
- User → MoodSelector: selectMood("happy")
- MoodSelector → TimerService: startTimer(25)
- TimerService → ResultScreen: onComplete()
- ResultScreen → MoodSelector: requestFinalMood()
![](https://github.com/simplewaveform/focusmood/blob/main/docs/Diagrams/Sequence_StartFocusSession.png)

## 3. View User Stats
Objects: `User`, `DashboardUI`, `StorageService`
Flow:
- User → DashboardUI: openDashboard()
- DashboardUI → StorageService: loadUserStats()
- StorageService → DashboardUI: return statsData
- DashboardUI → User: displayStats()
![](https://github.com/simplewaveform/focusmood/blob/main/docs/Diagrams/Sequence_ViewUserStats.png)
