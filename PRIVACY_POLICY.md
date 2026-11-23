# Privacy Policy for ShortsAway

**Last Updated:** November 19, 2026

ShortsAway ("we", "our", or "the app") is a privacy-first, 100% offline digital wellbeing Android utility designed to help users curb compulsive scrolling by selectively blocking short-form video feeds.

We believe that your personal data belongs to you alone. This Privacy Policy details our strict zero-data collection architecture and our transparent use of system services.

---

## 1. 100% Offline Architecture (Zero Data Collection)

* **No Internet Permission:** ShortsAway does not declare, request, or possess the `android.permission.INTERNET` permission. The app is technically incapable of transmitting any data over the internet or establishing network connections.
* **Zero Analytics & Telemetry:** We do not include any analytics frameworks, crash reporters, tracking SDKs, or third-party advertising identifiers.
* **No Accounts or Logins:** You do not need to create an account, register, or provide an email address or phone number to use ShortsAway.

---

## 2. On-Device Data Storage

All data created or modified within ShortsAway is stored strictly in your device's private sandbox storage using local SQLite (Room Database) and Jetpack DataStore:
* **Daily Statistics:** Aggregated counts of short-form videos closed, daily minutes spent, and your focus streak.
* **User Preferences:** Your selected daily allowance duration, active focus schedule hours, and individual platform toggles.
* **PIN / Biometric Lock:** If enabled, your 4-digit PIN is cryptographically hashed with SHA-256 and stored exclusively on your device. Biometric authentication is handled securely by Android's BiometricPrompt API; biometric credentials never leave the Android Secure Enclave / Keystore.

*All local data is automatically and permanently deleted when you uninstall the app or clear app data in Android Settings.*

---

## 3. Use of the Android AccessibilityService API

ShortsAway uses Android's `AccessibilityService` API strictly to deliver its core digital wellbeing and impulse-control functionality.

### Purpose of Use:
To detect when supported short-form video player containers (e.g., YouTube Shorts, Instagram Reels, Facebook Reels, and X immersive video feeds) enter the active viewport, and to dispatch a system Back action (`GLOBAL_ACTION_BACK`) or display a calm mindful breathing pause.

### What the Accessibility Service Does:
* Inspects visible window view identifiers and content descriptions of user-selected apps solely to identify short-form video containers.
* Dispatches a single system Back navigation to return you to your standard feed, search, or home timeline.

### What the Accessibility Service NEVER Does:
* It **NEVER** reads, captures, stores, or logs your typed text, passwords, usernames, or keystrokes.
* It **NEVER** inspects personal messages, chats, emails, banking information, or photos.
* It **NEVER** transmits any captured screen content or metadata off your device (the app has zero internet access).
* It **NEVER** modifies device settings or interferes with other apps outside of short-form video feeds.

### Policy Compliance:
* Configured with `android:isAccessibilityTool="false"` in compliance with Google Play Store policies.
* A prominent, full-screen in-app disclosure is presented to the user prior to requesting accessibility permissions.
* Users can pause or disable the Accessibility Service at any time via the in-app toggle, the Quick Settings tile, or Android System Settings.

---

## 4. Children’s Privacy

ShortsAway does not collect personal data from anyone, including children under the age of 13. The app is completely safe for all age groups.

---

## 5. Changes to This Privacy Policy

If we update this Privacy Policy, the updated version will be posted at this URL and included in future app releases. Any modifications will uphold our core commitment to 100% offline privacy and zero data collection.

---

## 6. Contact Us

If you have any questions or feedback regarding this Privacy Policy, please contact:
* **Email:** labs@jaidroid.com
* **Website:** https://github.com/shortsaway (or your developer website)
