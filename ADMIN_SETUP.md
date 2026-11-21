# Firebase Admin Setup (required before moderation)

1. Create a Firebase project and register a Web App.
2. Enable **Authentication → Email/Password** and create your admin user.
3. Create Cloud Firestore in production mode.
4. Publish `firestore.rules` from this folder.
5. Assign the admin user's custom claim `admin: true` from a trusted server or local one-time Admin SDK script. Never expose a service-account key or Admin SDK in the website.
6. Set the Firebase Web App values in `.env` using `.env.example`.

The website only permits public creation of `pending` reviews. Public visitors can read approved reviews. An authenticated account can moderate reviews only when its verified ID token contains `admin: true`.
