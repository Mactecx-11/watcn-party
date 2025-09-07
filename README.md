# Firebase Social Watch & Play MVP (Hybrid Firestore + Realtime DB)

This skeleton uses Firebase Auth, Firestore (for chat, rooms, video state) and Realtime Database (for presence & fast game state).

## Quickstart
1. Install Node.js and npm
2. Unzip project and `cd frontend`
3. `npm install`
4. Fill `frontend/src/firebaseConfig.js` with your Firebase web config
5. `npm run build`
6. `firebase login` and `firebase use --add <PROJECT_ID>`
7. `firebase deploy --only hosting` (after build)
8. Deploy Firestore rules: `firebase deploy --only firestore:rules`
9. Deploy RTDB rules: `firebase database:rules:set database.rules.json`

## Notes
- Presence stored at `/presence/{userId}` in Realtime Database
- Chat messages stored at `rooms/{roomId}/messages` in Firestore
- Watch sync state stored at `rooms/{roomId}` in Firestore
- Ensure you add your hosting domain to Firebase Authorized Domains for Google Sign-In
