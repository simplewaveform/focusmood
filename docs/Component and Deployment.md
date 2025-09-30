# Component and Deployment Diagram — FocusMood

![](https://github.com/simplewaveform/focusmood/blob/main/docs/Diagrams/Deployment.png)

## Components
- **UI Layer**: Renders all screens (login, main, music, calendar).
- **Auth Module**: Handles login, signup, and session validation.
- **Session Manager**: Coordinates timer, mood selection, and session creation.
- **Storage Module**: Persists data using localStorage (anonymous) or Firebase (registered).
- **Music Player**: Manages background audio playback.

## Deployment
- **Node**: Web Browser (Client)
  - Hosts all components (UI, Auth, Session, Storage, Music)
  - Uses localStorage for anonymous users
- **Node**: Firebase Cloud (Optional)
  - Stores user accounts and session history for registered users
  - Accessed only when user is logged in

Note: No backend server is required for core functionality.
