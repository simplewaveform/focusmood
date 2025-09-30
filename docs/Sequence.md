# Sequence Diagrams — FocusMood

## 1. Log In
Objects: `LoginUI`, `AuthService`, `UserProfile`  
Flow:
- User → LoginUI: enter email/password
- LoginUI → AuthService: authenticate(email, password)
- AuthService → UserProfile: loadUserData()
- UserProfile → LoginUI: displayDashboard()

## 2. Start Focus Session
Objects: `MoodSelector`, `TimerService`, `ResultScreen`  
Flow:
- User → MoodSelector: selectMood("happy")
- MoodSelector → TimerService: startTimer(25)
- TimerService → ResultScreen: onComplete()
- ResultScreen → MoodSelector: requestFinalMood()

## 3. Save Session
Objects: `ResultScreen`, `SessionManager`, `StorageService`  
Flow:
- ResultScreen → SessionManager: createSession(initial, final)
- SessionManager → StorageService: save(session)
- StorageService → SessionManager: confirmSave()
