<div align="center">

# 🔔 SyncGuard

### Make sense of delayed notifications.

**A privacy-first Android assistant that helps you check notification settings, understand phone-specific background restrictions, and follow safer troubleshooting steps.**

[![Android 8.0+](https://img.shields.io/badge/Android-8.0%2B-3DDC84?logo=android&logoColor=white)](https://www.android.com/)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.2.10-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)](https://developer.android.com/compose)
[![Material 3](https://img.shields.io/badge/Material%203-14264B?logo=materialdesign&logoColor=white)](https://m3.material.io/)
[![Version](https://img.shields.io/badge/version-2.0.1-245CFF)](#about)

**Built by [Shahariar Nawous](https://github.com/N4ous)**

</div>

---

## 👋 Welcome

Late notifications can make a phone feel unreliable. Some Android devices and manufacturer software apply battery and background limits that affect how apps run. SyncGuard helps you **inspect the settings Android exposes, find relevant system screens, and follow device-specific guidance**—without pretending it can control another app's push service.

> [!IMPORTANT]
> **SyncGuard cannot guarantee instant notifications.** Android does not let a regular app force WhatsApp, Outlook, or another app to sync. SyncGuard diagnoses and guides; it does not bypass Android restrictions or change another app's policies.

## ✨ What SyncGuard can do

| Feature | What it does |
| --- | --- |
| **Device health dashboard** | Summarizes notification permission, SyncGuard's battery-optimization status, optional notification access, and Google Play Services availability. |
| **Device and ROM overview** | Shows device manufacturer/model, Android version, and an OEM/ROM identification when available. |
| **App selection** | Search launchable installed apps, choose apps to troubleshoot, and review available per-app notification and battery status. |
| **OEM repair guidance** | Offers practical steps for Xiaomi/Redmi/POCO, Huawei, Honor, Vivo/iQOO, OPPO/Realme, OnePlus, Samsung, and generic Android. |
| **Safe Resync Assistant** | Open a selected app or its Android settings, review repair steps, run a SyncGuard test, and record whether the result improved. |
| **Local test notification** | Sends a notification from SyncGuard so you can check SyncGuard's own notification path. |
| **Optional timing history** | With Notification Access enabled by you in Android Settings, records notification timing metadata and screen state—not message text. |
| **Test and resync history** | Keeps local history of tests and user-reported outcomes. |
| **Light, dark, and system themes** | Choose an appearance and save it locally. |
| **Privacy and data controls** | Review sensitive access, export a diagnostic report on demand, clear history, or reset app preferences with confirmation. |
| **GitHub release checker** | Checks for a release when configured. It never silently downloads or installs an update. |

### Suggested apps

WhatsApp · Outlook · Facebook · Gmail · Telegram · Slack · Other launchable installed apps

## 🧭 Who is SyncGuard for?

SyncGuard is for Android users who:

- Notice notifications arriving late or inconsistently.
- Use phones from Xiaomi, Redmi, POCO, Huawei, Honor, Vivo, iQOO, OPPO, Realme, OnePlus, or Samsung.
- Want understandable instructions for notification, battery, and background settings.
- Prefer local diagnostics and want control over optional Notification Access.
- Understand that third-party app delivery depends on Android, the app, network conditions, and remote services.

## 📸 Screenshots

Screenshots are **not yet included in this repository**. I want the gallery to show real app screens rather than mockups. Device screenshots can be added here as they become available, ideally covering the dashboard, app selection, repair guide, resync result, settings, and history.

## 📥 Install or build

### Current repository contents

This GitHub repository currently contains the README only. **The Android project source and an installable APK have not been uploaded here yet**, so you cannot build or install SyncGuard from this repository at this time. I will update this section when the project source or a signed release is published.

### Build requirements (when source is available)

- Android Studio
- Android SDK Platform 35
- An Android device or emulator running Android 8.0 (API 26) or newer
- A JDK supported by the project's Android Gradle Plugin

Once the Android project is available, the debug APK can be built from its project folder with `:app:assembleDebug` using the Gradle wrapper. A debug build is for development and testing, not a signed production release.

## 🚀 Getting started

When an installable build is available:

1. Open **Home** and review the access and device status card.
2. Select the apps you want to troubleshoot.
3. Use **Repair guide** or **Resync Assistant** to open available Android settings and read your device's OEM guidance.
4. Allow SyncGuard notifications if you want to run its local notification test. Android 13 and later asks for notification permission.
5. If you want timing history, enable **Notification Access** yourself in Android Settings. This is optional.
6. Follow the local-test instructions and record your result. For comparison, test the third-party app separately while the phone is locked.

## 🔐 Privacy and permissions

- **No message content:** SyncGuard does not read or store notification text, message bodies, attachments, conversations, passwords, or credentials.
- **Notification Access is optional:** Monitoring starts only after you explicitly enable it in Android Settings. SyncGuard records timing/package/screen-state metadata only.
- **Local by default:** Preferences and diagnostic/test history are stored on your device.
- **No SyncGuard account or backend:** This MVP does not send your diagnostic history to a SyncGuard server.
- **Report export is user initiated:** A diagnostic report is created only when you request an export.
- **Internet access is for update checks:** The optional checker contacts GitHub's Releases API when you request a check. It does not fetch or install APKs.
- **Notification permission:** Needed for SyncGuard's own local test notification on Android 13 and newer.

Review Android's permission/access screens before granting access. You can revoke Notification Access in Android Settings.

## ⚠️ Important limitations

- A normal Android app cannot guarantee or force instant notifications from another app.
- Android and OEMs do not expose every app-specific autostart, background activity, background-data, or battery restriction in a consistent way. Some statuses are informational or unsupported; manual instructions are the fallback.
- The local notification test checks **SyncGuard only**. It does not send a message through WhatsApp or test another app's push delivery.
- Timing history records Android's notification post time and when SyncGuard observes the event. It does not reveal when a remote server sent a notification.
- The readiness score summarizes only the checks named in the app; it is not a delivery prediction.
- Scan frequency is a saved preference. This version does not schedule background scans or reminders.
- GitHub update checking remains unavailable until the repository owner and repository name are configured in `GitHubUpdateConfig.kt`.

## 🛠️ Technology

The Android app is built with Kotlin, Coroutines, Jetpack Compose, Material 3, MVVM, `StateFlow`, Compose Navigation, Room, DataStore, and Android notification/system-settings APIs. Project source is not yet present in this GitHub repository.

## 🗺️ Future updates

These are **ideas for future work, not promises or features available in the current version**:

- Publish the Android project source and, when ready, a signed installable release.
- Add a gallery of real screenshots from supported screen sizes and Android/OEM versions.
- Expand device testing and refine OEM instructions from verified user reports.
- Improve diagnostic report readability and add clearer explanations for unknown/unsupported checks.
- Explore optional, user-controlled reminders or scan scheduling if they can be implemented reliably and transparently.
- Improve accessibility and continue testing navigation and layouts on small screens.
- Configure GitHub Releases and the in-app update checker after release ownership and distribution are ready.

## 💡 Developer's vision

SyncGuard is being built around a simple idea: **help people understand notification problems without asking them to surrender message privacy or trust exaggerated promises**. The goal is to make Android's device-specific settings easier to find, explain what can and cannot be checked, and leave decisions and sensitive access in the user's hands.

## 👨‍💻 About

| | |
| --- | --- |
| **App** | SyncGuard |
| **Current version** | 2.0.1 |
| **Developer** | [Shahariar Nawous](https://github.com/N4ous) |
| **Platform** | Android 8.0+ (API 26+) |
| **Application ID** | `com.syncguard.app` |

## 🤝 Feedback and contributions

Bug reports and focused contributions are welcome. When reporting a problem, include your device manufacturer/model, Android or ROM version, affected app, and the steps you tried.

**Please do not post private messages, notification contents, credentials, or other sensitive information in issues.**