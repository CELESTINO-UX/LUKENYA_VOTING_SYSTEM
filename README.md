# Lukenya Voting System 2026

Live voting system with real-time sync for Lukenya School Student Council Elections.

## Features
- 🗳️ Multi-device live voting sync
- 📊 Real-time results dashboard
- 👥 Student and Staff voter management
- 📱 Device tracking for each vote
- 🔐 Admin panel with full CRUD
- 📈 PDF/DOCX export
- 🌐 GitHub Pages hosting ready

## Live Demo
[https://celestino-ux.github.io/LUKENYA_VOTING_SYSTEM/](https://celestino-ux.github.io/LUKENYA_VOTING_SYSTEM/)

## Firebase Setup (Required for Live Sync)

1. **Create Firebase Project**
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Click "Add project" and follow steps

2. **Enable Realtime Database**
   - In your project, click "Realtime Database"
   - Click "Create Database"
   - Choose "Start in test mode" (for development)
   - Copy your database URL

3. **Get Firebase Config**
   - Click the gear icon ⚙️ → Project settings
   - Scroll to "Your apps" → Click the web icon (</>)
   - Register app (name it "Lukenya Voting")
   - Copy the `firebaseConfig` object

4. **Update the Code**
   - Open `index.html`
   - Find the `firebaseConfig` object (line ~230)
   - Replace with your actual config values

5. **Update Database Rules** (Optional but recommended)
   - In Firebase Console → Realtime Database → Rules
   - Paste:
```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
