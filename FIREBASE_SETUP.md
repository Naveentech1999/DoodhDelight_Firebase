# Firebase setup
1. Create a Firebase project and register a Web App.
2. Enable Authentication → Sign-in method → Email/Password.
3. Create Cloud Firestore.
4. Publish `firestore.rules` in the Firestore Rules tab.
5. Copy `firebase-config.example.js` to `firebase-config.js` and add the Web App config.
6. Keep `firebase-config.js` beside `index.html` in the deployed site.

Never add Firebase Admin service-account JSON/private keys to this browser repository. Each signed-in user owns `milk_app_state/{uid}`. Its `payload` stores the app state: customers, milk products, date-wise attendance, prices and monthly charges. Local browser storage remains active.

Export a JSON backup from the original app, import it into this app on the master device, sign in, then upload device data once. Keep the export until a second device confirms the records.
