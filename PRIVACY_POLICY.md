# Privacy Policy — Timelapse - Self Accountability

**Developer:** Alvaro Kim  
**Contact:** kingkim150m@gmail.com  
**Effective date:** May 9, 2026  
**Last updated:** May 23, 2026

> **Public URL:** `[TO BE FILLED — paste the hosted URL here before Play Store submission]`

---

## What this app is

Timelapse - Self Accountability is a personal productivity tool you run for yourself. It creates a time-lapse recording of your own screen so you can review how you spent your time and hold yourself accountable. Everything stays on your phone unless you deliberately share something.

This app is **not** a parental-control tool, an employee-monitoring tool, or a hidden surveillance tool. Screen-capture sessions are started manually by you, are visible on your screen at all times, and require your explicit approval before they begin.

---

## Summary

- **You start every recording.** The app never captures your screen silently or in the background without your action.
- **Everything stays on your phone.** Captures, MP4 timelapses, PDF reports, schedules, and usage history are stored locally on your device.
- **No developer servers.** The developer does not operate any server that receives your screen captures, usage data, or personal information.
- **No advertising use.** Your captures and usage data are never used for advertising and are never sold to third parties.
- **No camera, no microphone.** The app does not use your camera or record audio of any kind.
- **Google Play handles billing.** Subscription payments go through Google Play; the developer never receives your payment card details.

---

## What the app records and stores

### Screen capture sessions

When you start a recording session, Android displays a screen-capture permission prompt. Your screen is only captured after you approve that prompt. The app saves individual frames at regular intervals and can build them into an MP4 timelapse when you choose to export. Frames are automatically deleted from app-private storage after 24 hours. Exported MP4 and PDF files are written to your phone's shared storage when you explicitly request an export.

**Screen captures may contain sensitive information.** Anything visible on your screen during a session — messages, emails, websites, financial information, health information, or other personal content — may appear in your captures and exported files. Some protected content (certain banking apps, DRM-protected video, or other system-protected surfaces) may appear as a blank or black frame depending on Android's own content protections.

### Local Insights (optional feature)

If you use Local Insights, the app periodically checks your on-device session history, usage patterns, and streak data and generates a short observation. This processing happens entirely on the phone using simple rule-based logic — no AI model, no server request, and no data is transmitted anywhere. Generated insights are stored locally and are discarded when you dismiss them or when a new day's insights replace them.

### Onboarding data

During the initial setup flow, the app collects a daily focus goal, a sleep and wake time for the Night Lock preset, and a list of apps you identify as distracting. This data is stored locally on your phone and is used only to pre-configure your schedules and warning settings. It is never transmitted to the developer or any external service.

### Focus Guard (optional feature)

If you enable Focus Guard, a background service runs continuously and monitors which app is in the foreground. It enforces the focus schedules and temporary locks you have configured by displaying a blocking overlay over restricted apps. All schedule, lock, and usage data is stored locally on your phone. The developer does not receive this data.

### What stays on your phone

The following data is stored on-device only and is never sent to the developer or any external server:

- Screen capture frames (auto-deleted after 24 hours)
- Assembled MP4 timelapse files
- Session summaries and analytics
- PDF session and snapshot reports
- App usage summaries
- App labels and warning preferences
- Focus schedules, break windows, and Temporary Lock settings
- Focus Guard settings and guardian state
- Integrity and audit logs
- Settings snapshot history
- Local Insights (generated and stored on-device; never transmitted)
- Onboarding preferences (daily goal, sleep time, distraction app list)
- Subscription status (read from Google Play and cached locally)

---

## What the app does NOT do

- Does not record audio
- Does not use the camera
- Does not capture your screen without your knowledge or explicit consent
- Does not run silent background recording — the foreground service notification is always visible while capture or monitoring is active
- Does not upload screen captures, MP4 files, PDF reports, or usage data to any server
- Does not sell your personal data to anyone
- Does not use your data for advertising or pass it to advertising networks
- Does not include third-party analytics or crash-reporting SDKs (no Firebase Analytics, no Crashlytics, no similar services are embedded in the app)
- Does not share your data with the developer

---

## Permissions

The app declares the following Android permissions. Each is used only for the specific feature it describes.

### Notifications — `POST_NOTIFICATIONS`
Used to send distraction warnings when a labeled app is open during a session, and to show the persistent notification required by Android whenever a foreground service is running (screen capture, guardian monitoring). You can manage notification delivery in Android Settings at any time.

### Screen capture and foreground services — `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PROJECTION`, `FOREGROUND_SERVICE_SPECIAL_USE`
Required for Android to allow the capture session and the Focus Guard guardian service to remain running while you use other apps. Android requires apps to declare foreground-service permissions for any service that stays active in the background. These result in a visible status-bar notification at all times while the service is running — there is no silent background capture.

### Usage Access — `PACKAGE_USAGE_STATS`
Lets the app read which app is currently in the foreground so it can show you accurate session summaries, trigger distraction warnings, and enforce focus schedules. This is a special permission you must grant manually in Android Settings — it is not granted automatically on install. The data is read on-device only and is never sent anywhere outside the app.

### Display over other apps — `SYSTEM_ALERT_WINDOW`
Used for two features:

- **Focus Guard block overlays:** When a focus schedule or Temporary Lock is active, a full-screen blocking overlay appears over a restricted app. This is the core enforcement mechanism of Focus Guard.
- **Optional in-session warning overlay:** An optional chip can appear over other apps when a distraction app is detected during a recording session. This feature is off by default and can be permanently disabled in Settings.

### Vibration — `VIBRATE`
Used for the haptic feedback pattern in distraction warnings.

### Exact alarms — `SCHEDULE_EXACT_ALARM`
Used to fire focus schedule start and end events at the precise times you have configured. Without this, schedule boundaries could be delayed by Android's battery-optimization system.

### Boot receiver — `RECEIVE_BOOT_COMPLETED`
Allows the app to restart the Focus Guard guardian service after a device reboot, if the feature was enabled before the reboot. Without this, the service would not resume protecting your configured schedules after the phone restarts.

### Storage — `WRITE_EXTERNAL_STORAGE` (Android 8 and below only)
Used on Android 8 (API level 28) and below to save exported MP4 and PDF files to shared storage. This permission is not requested on Android 9 or higher, where scoped storage rules apply automatically.

---

## When you export or share a file

When you export an MP4 or PDF and share it using Android's share sheet, the file is sent to whichever app or service you choose — email, messaging, cloud storage, and so on. From that point, the receiving app or service controls that copy of the file under its own terms. The developer has no control over or visibility into what happens to the file after you share it.

---

## Google Play Billing

Monthly and annual subscriptions are processed by Google Play. When you subscribe:

- Google handles payment processing and collects your payment card details.
- The developer does not receive your full card number or any payment credentials.
- The app reads your subscription status from Google Play to unlock premium features and restore access after reinstallation or on a new device.
- Google's own privacy policy governs the payment transaction: https://policies.google.com/privacy

---

## Third-party analytics and crash reporting

This app does not currently include any third-party analytics SDK (such as Firebase Analytics) or crash-reporting SDK (such as Crashlytics). No behavioral data, crash logs, or usage statistics are automatically sent to the developer or any analytics provider.

---

## Children and minors

This app is intended for use by individuals who want to voluntarily monitor and improve their own screen-time habits. It is not designed as a parental monitoring or child-tracking tool and should not be used to monitor another person's device without their knowledge and consent.

The app does not knowingly collect personal information from children under 13. If you believe a child under 13 has used this app in a way that involves their personal information, please contact us at kingkim150m@gmail.com.

---

## Data retention and deletion

| Data | How long it is kept |
|------|---------------------|
| Screen capture frames | Auto-deleted from app storage after 24 hours |
| Session data and analytics | Retained on-device until you clear app data or uninstall |
| Exported MP4 and PDF files | Remain in your phone's shared storage until you delete them |
| App data overall | Removed when you uninstall the app |

**No account to delete.** The app does not use accounts or sign-in. There is no server-side profile to delete.

**Android "Clear app data."** Clears all app-private data immediately. The app detects this on the next launch and records an entry in the Integrity Log.

---

## Security

- All data produced by the app is stored locally on your device.
- The app does not operate a cloud backend or developer-run server.
- `android:allowBackup="false"` is set in the app manifest, preventing app-private data (including screen captures and session data) from being included in Android's automatic cloud backup to Google.
- Exported files written to shared storage are subject to Android's standard file-system protections.

---

## Changes to this policy

If this policy changes in a material way, the updated version will be posted at the URL shown in the app's Google Play Store listing. The "Last updated" date at the top of this document will be updated accordingly. Continued use of the app after a policy update constitutes acceptance of the revised terms.

---

## Contact

For questions about this privacy policy or about your data:

**Developer:** Alvaro Kim  
**Email:** kingkim150m@gmail.com
