<div align="center">

# 🔔 SyncGuard

### Make sense of delayed notifications.

**A privacy-first Android assistant for checking notification settings and following safe, device-specific troubleshooting guidance.**

[![Android 8.0+](https://img.shields.io/badge/Android-8.0%2B-3DDC84?logo=android&logoColor=white)](https://www.android.com/)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.2.10-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)](https://developer.android.com/compose)
[![Version](https://img.shields.io/badge/version-2.0.1-245CFF)](#about)

**Built by [Shahariar Nawous](https://github.com/N4ous)**

### [⬇️ Download SyncGuard 2.0.1 APK](https://github.com/N4ous/SyncGuard/releases/download/v2.0.1-testing/SyncGuard-2.0.1-debug-testing.apk)

[View release notes and changelog](https://github.com/N4ous/SyncGuard/releases/tag/v2.0.1-testing)

</div>

---

> [!WARNING]
> **The available APK is a debug-signed testing build, not a production release.** It is signed with Android's standard debug certificate; a future production-signed build may not install as an upgrade over it. Review the release notes and APK checksum before installing. Android does not allow a regular app to guarantee instant notifications from other apps.

## 👋 What is SyncGuard?

Some Android devices and manufacturer software apply battery and background limits that can affect how apps run. SyncGuard helps you inspect settings Android exposes, find relevant system screens, and follow OEM-specific steps—without claiming to force third-party apps to sync.

## ✨ Features

| Feature | What it does |
| --- | --- |
| **Device dashboard** | Shows device/ROM details, a readiness summary, notification permission, SyncGuard battery optimization, optional Notification Access, and Google Play Services availability. |
| **App selection** | Search launchable installed apps, choose apps to troubleshoot, and see Android statuses where available. |
| **Resync Assistant** | Open the selected app or Android settings, follow repair guidance, run a local SyncGuard test, and record an outcome. |
| **OEM repair guides** | Guidance for Xiaomi/Redmi/POCO, Huawei, Honor, Vivo/iQOO, OPPO/Realme, OnePlus, Samsung, and generic Android. |
| **Local test notification** | Check SyncGuard's own notification path; this does not test another app's push delivery. |
| **Optional timing history** | If you explicitly enable Notification Access in Android Settings, timing/package/screen-state metadata is recorded without message content. |
| **Local settings and history** | Light/dark/system themes, test and resync history, diagnostic export, and confirmed clear/reset controls. |
| **Update checker** | Designed to check GitHub releases when configured. It never silently downloads or installs APKs. |

Suggested apps include WhatsApp, Outlook, Facebook, Gmail, Telegram, Slack, and other launchable apps.

## 🧭 Who is it for?

Android users who experience late or inconsistent notifications, especially on phones with aggressive battery management, and want clear diagnostics and practical manual steps. SyncGuard is also for privacy-conscious users who want to keep diagnostics local and control sensitive access themselves.

## 📥 Download and install

### [Download the SyncGuard 2.0.1 APK directly](https://github.com/N4ous/SyncGuard/releases/download/v2.0.1-testing/SyncGuard-2.0.1-debug-testing.apk)

This is a **debug-signed testing build**, not a production release. See the [release notes, changelog, and checksums](https://github.com/N4ous/SyncGuard/releases/tag/v2.0.1-testing) before installing.

The current build is **version 2.0.1 (version code 2)**. Minimum Android version is 8.0 (API 26); target SDK is 35.

To install, download the APK on your Android device and open it. Android may ask you to permit installation from the browser or file manager. Only install APKs you trust. If a production-signed SyncGuard build is already installed, the debug-signed test build may not update it in place; Android signing rules can require uninstalling the other build first, which can remove its app data.

### Source availability

The Android project source is **not yet included in this GitHub repository**. This repository currently hosts the README and testing release asset. A build-from-source guide will be added when the source project is published here.

## 📸 Screenshots

Screenshots are not included yet. When available, this section will show genuine app captures from the dashboard, app selection, Resync Assistant, settings, and history—not mockups.

## 🔐 Privacy

- SyncGuard does not read or store notification text, message bodies, attachments, or conversations.
- Notification Access is optional and only enabled by the user in Android Settings. The monitor stores timing/package/screen-state metadata only.
- Preferences and diagnostic history are stored locally by default; no SyncGuard account or backend is used.
- Diagnostic reports are exported only when requested.
- The release checker contacts GitHub only when the user requests an update check. It does not download or install APKs.

## ⚠️ Limitations

- Android does not let a normal app guarantee instant notification delivery from WhatsApp, Outlook, or any other app.
- The local notification test checks SyncGuard only; it cannot test a remote server or another app's push path.
- Timing history compares Android's notification post time with when SyncGuard observes it; it cannot know when a remote server sent the notification.
- Android/OEM software does not reliably expose all third-party autostart, background activity/data, and battery controls. Some checks are unsupported, and manual steps may be needed.
- The readiness score summarizes only the checks named in the app; it is not a delivery guarantee.
- Scan frequency is a stored preference; this version does not run scheduled background scans or reminders.
- The in-app GitHub update checker still requires repository configuration in the Android project source.

## 🛠️ Technology

The Android app is implemented in Kotlin with Jetpack Compose, Material 3, MVVM, `StateFlow`, Compose Navigation, Room, DataStore, and coroutines. This GitHub repository does not yet contain those project source files.

## 🗺️ Future ideas

These are future possibilities, not features promised or shipped:

- Publish Android project source and a production-signed release when ready.
- Add real screenshots and test across more device brands, screen sizes, and Android versions.
- Continue refining OEM guidance and explanations for unsupported checks.
- Explore transparent, user-controlled reminders if they can be implemented reliably.
- Improve accessibility and small-screen testing.

## 💡 Developer vision

Help people understand notification problems without compromising message privacy or making exaggerated promises. Make device-specific settings easier to find, clearly explain what Android does and does not expose, and keep sensitive choices in the user's hands.

## 👨‍💻 About

| | |
| --- | --- |
| **App** | SyncGuard |
| **Current version** | 2.0.1 testing build |
| **Developer** | [Shahariar Nawous](https://github.com/N4ous) |
| **Platform** | Android 8.0+ (API 26+) |
| **Application ID** | `com.syncguard.app` |

## 🤝 Feedback

When reporting an issue, include your device manufacturer/model, Android or ROM version, affected app, and steps tried. Do not post private messages, notification contents, credentials, or other sensitive information.