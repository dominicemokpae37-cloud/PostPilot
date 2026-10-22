# PostPilot — Content Planner (frontend starter)

A responsive HTML/CSS/JavaScript content planner inspired by your screenshots.

## Included
- Monthly calendar with post cards
- Create/edit/clear posts, caption notes, platform and planned date
- Mark posts complete (✓) or incomplete (–); prompt to reschedule incomplete posts or clear completed ones
- Idea bank, upcoming posts, overview counts
- Light/dark theme saved in this browser
- Reminder notification scheduling while the app/browser is open
- Login screen with a preview mode and a clearly marked Google-auth integration point
- Footer credit: Dominic Emokpae and dominemokpae6@gmail.com

## Run it
Open `index.html` in a browser, or use VS Code Live Server.

## Important setup notes
**Google login:** The included Google button is a setup placeholder, not real authentication. To implement real sign-in, create a Firebase project, enable Authentication → Google, register your web app, add Firebase's web SDK and project config, then call Firebase `signInWithPopup` (or redirect) from the button. Keep protected user data behind Firebase rules or your own backend. Do not ask users to type their Gmail password into your app.

**Phone reminders:** Browser notifications require permission and are not a dependable alarm when the browser is closed, the device is asleep, or the browser restricts background timers. For reliable scheduled reminders, implement a backend scheduler/push notifications (e.g. Firebase Cloud Messaging plus a server/cloud function) or a native app. The current version schedules reminders in-page.

**Data:** This starter stores posts/ideas in localStorage on the same browser/device. It is not cloud sync or secure multi-user storage yet.

## Suggested next step
Configure Firebase Auth + Firestore, then store each user's posts under their authenticated UID and secure them with Firestore Security Rules.
