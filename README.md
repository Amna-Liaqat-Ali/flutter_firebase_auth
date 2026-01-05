# Flutter Firebase Authentication App

A clean and modern Flutter app demonstrating **Email/Password Authentication** with **Firebase Authentication** and **Cloud Firestore** integration.  
The app includes **Signup, Login, and Profile screens** with **form validation**.

---

## Features

- Firebase Email/Password Authentication
- Store and retrieve user details in Firestore
- Form validation for email and password
---

## Setup Instructions

1.  Clone the Repository
   ```bash
   git clone https://github.com/Amna-Liaqat-Ali/flutter_firebase_auth.git
   cd flutter_firebase_auth
   ```

2. Install Dependencies
   ```bash
   flutter pub get
   ```

3. Configure Firebase
	1.	Go to Firebase Console
	2.	Create a new project
	3.	Add Android/iOS app to the project
	4.	Download google-services.json (for Android) or GoogleService-Info.plist (for iOS)
	5.	Place these files in your Flutter project:
	•	android/app/google-services.json
	•	ios/Runner/GoogleService-Info.plist
	6.	Enable Email/Password Authentication:
	•	Firebase Console → Authentication → Sign-in method → Email/Password → Enable
	7.	Create a Firestore database:
	•	Mode: Test Mode (for development)
  •	Rules:
```bash
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null;
    }
  }
}
```
8. Run the app
   ```bash
   flutter run
   ```
---   
   
### Note
•	This app uses Firebase Test Mode for development.  
•	Before production, update Firestore rules for proper security.

