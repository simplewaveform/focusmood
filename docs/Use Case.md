# Use Cases — FocusMood

## 1. Select Initial Mood
**Actor**: User  
**Description**: User selects emotional state before starting a focus session.  
**Main Flow**:
1. User opens the application.
2. Sees 6 mood emojis (Happy, Sad, Angry, Anxious, Neutral, Excited).
3. Clicks one mood.
4. Clicks "Submit Mood".
5. System stores initial mood.

**Alternative Flows**:
- 3a. No mood selected → "Submit" button remains disabled.
- 4a. User cancels → returns to mood selection.

---

## 2. Start Focus Timer
**Actor**: User  
**Description**: Launch 25-minute Pomodoro timer.  
**Main Flow**:
1. After mood selection, "Start Focus" button appears.
2. User clicks it.
3. Timer starts counting down from 25:00.
4. On completion, audio alert plays and user is redirected to final mood selection.

---

## 3. Log In
**Actor**: Registered User  
**Description**: Authenticate to access personal history.  
**Main Flow**:
1. User clicks "Log In".
2. Enters email and password.
3. Clicks "Log In".
4. System validates credentials → redirects to dashboard.

**Alternative Flows**:
- 2a. Invalid credentials → shows "Invalid email or password".
- 2b. Forgot password → link to password reset.

---

## 4. View Session History
**Actor**: Registered User  
**Description**: Review past focus sessions in calendar view.  
**Main Flow**:
1. User navigates to profile/dashboard.
2. Sees monthly calendar with color-coded session indicators.
3. Clicks a date → views session details (initial/final mood, duration).

---
