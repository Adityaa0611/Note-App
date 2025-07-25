# 📓 App-Notes

A user-friendly Android Notes application built with Kotlin and Firebase.

## ✨ Features

### 🔐 Authentication
- User *Sign Up* with username, email, and password.
- Validates email format and password strength during registration.
- Sends a *welcome email* after successful account creation.
- *Login* using username and password.
- *Forgot Password* using only the *username*.
- Uses *Firebase Authentication* + *Firebase Realtime Database*.

### 🗒 Notes Management
- Create, update, and delete notes.
- Notes are stored under each individual user's Firebase UID.
- Notes displayed in card layout using RecyclerView.

### 🔁 Persistent Login
- Login session stored using SharedPreferences.
- App skips login screen if already logged in.

### 🧭 Navigation Drawer
- Side drawer shows username.
- Logout option clears session and redirects to *LoginActivity*.

---

## ✅ Changes We Made During Development

- 🔄 *Replaced Firebase email-based login* with *username-based login*.
- 🔐 *Forgot Password* functionality updated:
  - Now uses username to look up the registered email.
  - Sends a reset email using Firebase Authentication.
- 📩 *Welcome email* is sent upon signup instead of verification email.
- 🧠 *Persistent login session* using SharedPreferences.
- 📝 *Notes now saved per user* using their UID to isolate notes.
- 🔄 *Logout flow fixed: After logout, user is returned to **LoginActivity*, not MainActivity.
- 🔧 Fixed multiple runtime and Firebase-related bugs:
  - AlertDialog reference issues.
  - Incorrect Firebase rules and structure.
  - Password update bug resolved by syncing both Auth and Database.

---

## 🛠 Tech Stack
- Kotlin
- Android SDK
- Firebase Authentication
- Firebase Realtime Database

