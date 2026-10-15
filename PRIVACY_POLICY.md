# Privacy Policy — Timelapse: Adaptive Blocking

**Developer:** Alvaro Kim  
**Contact:** kingprogramming150+t@gmail.com<br>
**Effective date:** Jun 2, 2026  
**Last updated:** October 14, 2026

> **Public URL:** `https://kingkim150m.github.io/timelapse-selfaccountability-android-legal/`

---

## What this app is

Timelapse: Adaptive Blocking is a personal productivity tool you run for yourself. It creates a time-lapse recording of your own screen so you can review how you spent your time and hold yourself accountable. Capture files, detailed session records, schedules, and settings stay on your phone unless you deliberately export or share them. Optional Analytics signals are sent to Google only if you grant Analytics consent. Website access separately sends permitted domain lookups over an encrypted connection to Cloudflare's public DNS resolver.

This app is **not** a parental-control tool, an employee-monitoring tool, or a hidden surveillance tool. Screen-capture sessions are started manually by you, are visible on your screen at all times, and require your explicit approval before they begin.

---

## Summary

- **You start every recording.** The app never captures your screen silently or in the background without your action.
- **Your detailed records stay on your phone.** Captures, MP4 timelapses, PDF reports, schedules, and detailed usage history are stored locally. Optional Analytics sends limited product-measurement events and technical metadata to Google only after you grant consent.
- **No app-operated backend.** The developer does not operate a server for app data. Separate external flows are described below: optional Analytics to Google, permitted Website access DNS queries to Cloudflare, Google Play billing, and information you choose to send for support.
- **No advertising feature.** The app does not display ads. Its Analytics consent settings deny advertising storage, ad user-data, and ad-personalization consent; see “Optional Analytics and diagnostics” for the remaining identifier review.
- **No camera, no microphone.** The app does not use your camera or record audio of any kind.
- **Google Play handles billing.** Subscription payments go through Google Play; the developer never receives your payment card details.

---

## What the app records and stores

### Screen capture sessions

When you start a recording session, Android displays a screen-capture permission prompt. Your screen is only captured after you approve that prompt. The app saves individual frames at regular intervals and can build them into an MP4 timelapse when you choose to export. Frames are automatically deleted from app-private storage after 7 days. Exported MP4 and PDF files are written to your phone's shared storage when you explicitly request an export.

**Screen captures may contain sensitive information.** Anything visible on your screen during a session — messages, emails, websites, financial information, health information, or other personal content — may appear in your captures and exported files. Some protected content (certain banking apps, DRM-protected video, or other system-protected surfaces) may appear as a blank or black frame depending on Android's own content protections.

### Automatic sensitive-app capture exclusions

The app can automatically add a supported banking app, wallet, or password manager to Capture
exclusions. This uses a small curated list of exact, case-sensitive package IDs and only checks
launchable apps that Android already makes visible to the app. It does not infer a sensitive app from
an app name, icon, category, screen content, or a partial package-name match. Matching happens
entirely on your device: the app does not send an app list, the matched app's package name, or screen
content to the developer or any outside service, and it does not request broad access to every app
installed on your phone.

This is a limited privacy safeguard, not a claim that the app can identify every financial app. When
a supported app is detected, future capture sessions black out the whole frame while that app is in
the foreground. You can remove any automatically protected app in Capture exclusions; that choice is
kept locally as an opt-out so it is not silently added again. Changes affect future sessions only;
an active session keeps the exclusions it had when it started. Google Play services is not treated as
a password-manager exclusion because it performs unrelated system functions.

### Local Insights (optional feature)

If you use Local Insights, the app periodically checks your on-device session history, usage patterns, and streak data and generates a short observation. This feature's processing happens entirely on the phone using simple rule-based logic — no AI model or server request is used for the insight itself. Generated insights are stored locally and are discarded when you dismiss them or when a new day's insights replace them. Separately, if you grant Analytics consent, the app may send the limited product-measurement events described below; those events do not contain your insight text or detailed session history.

### Onboarding data

During the initial setup flow, the app collects a daily focus goal, a sleep and wake time for the Night Lock preset, and a list of apps you identify as distracting. These values and app choices are stored locally on your phone and used to pre-configure your schedules and warning settings. They are not included in Analytics event parameters. If you grant Analytics consent, limited onboarding progress and completion events may be sent as described below; actions from before consent are not stored for later Analytics delivery.

### Focus (optional feature)

If you turn on Master Focus, a background service runs continuously and monitors which app is in the foreground. It enforces the focus schedules and Quick Locks you have configured by displaying a blocking overlay over restricted apps. Your detailed schedules, lock settings, app identities, and usage history are stored locally and are not included in Analytics event parameters. If enabled, Analytics may receive coarse first-configuration, activation, or blocking milestones, as described below; it does not receive the detailed records used for enforcement.

Three optional switches can extend a lock; each is off unless you turn it on for that lock:

- **Do Not Disturb.** If you turn on Do not disturb for a Night Lock, Focus Block, or Quick Lock,
  the app asks Android to use its Priority Do Not Disturb mode while that lock is active and
  restores your previous interruption mode when the last active lock ends. This uses Android's
  notification policy access, which you grant yourself in Android Settings. The app only changes
  the interruption mode; it does not read your notifications, calls, or messages through this access.
- **Force Stop protection (Device Admin).** You can optionally make Android ask for an extra
  confirmation before this app can be force-stopped or uninstalled. This uses Android's Device Admin
  feature with **no device-management policies requested**: the app cannot lock your screen, change
  or read your password, wipe your device, or manage it in any other way. To remove it, deactivate
  the app under Device admin apps in Android Settings; Force Stop and Uninstall then work normally.
- **Restart recovery.** Focus enforcement can resume after a restart without you reopening the app
  (see "Restart recovery — Accessibility Service" under Permissions).

### Built-in protections (Social Cooldown, Adaptive Protection, Strict Mode, Emergency pass)

The protection decisions and detailed state are handled on your phone. If you grant Analytics consent,
limited first-configuration, activation, or first-block milestones may be sent for product measurement
as described below. Detailed protection records and app identities are not included in those event
parameters.

- **Social Cooldown** is a built-in minimum standard you agree to during setup. It uses Usage Access
  to count how long a fixed list of social and video apps (TikTok, Instagram, Facebook, X, Reddit,
  Snapchat, and YouTube) has been in the foreground, so it can start a break when the shared
  allowance is used up. It can keep monitoring while Master Focus is off, which is why its
  persistent notification can read "Social monitoring is active". The timing state stays on your phone.
- **Adaptive Protection** can automatically add stronger protection on your phone, such as a
  late-night time limit or a temporary block of additional distracting apps after a block. It decides
  using only local signals such as which app is in the foreground and when. It does not use screen
  content, typed text, web addresses, keystrokes, media, or notification contents. Any record of its
  actions is minimal, kept only for a limited time, and stays on your phone.
- **Strict Mode** (optional) protects certain actions with a 10-digit passcode that you and a trusted
  contact choose. The app stores the passcode only on your phone as a one-way hash, and optionally
  the trusted contact's name you typed. The app does not contact your trusted contact and keeps no
  server copy of the passcode.
- **Emergency pass** use and the other events above are recorded locally in the Protection Log.

### Website access (optional premium feature)

If you configure Website access on a Night Lock, Focus Block, or Quick Lock, you can either
block selected domains or allow selected domains only. The app uses Android's local VPN mechanism
to enforce those domain rules. When a DNS lookup is permitted, the app sends the request over
encrypted DNS-over-TLS to Cloudflare's public resolver at `1.1.1.1` or `1.0.0.1`, verifying the TLS
hostname `one.one.one.one`. Cloudflare receives the requested domain name and related DNS query
details, as well as the network source address needed to return the response. TLS encrypts the
request in transit to Cloudflare; Cloudflare can read the requested domain name. Cloudflare says
its Public Resolver Logs, which can include query names and related DNS details, are deleted within
25 hours. It says source IP addresses are not retained in non-volatile storage except in limited
randomly sampled packets for troubleshooting and denial of service mitigation, and truncated client
IP addresses are deleted within 25 hours. Cloudflare may retain aggregate resolver data indefinitely
and gives APNIC limited access to anonymized resolver log data for non-profit operational research.
See Cloudflare's DNS-over-TLS documentation (`https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-tls/`)
and public resolver privacy commitments (`https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/`).

The app reads each DNS domain to decide whether it matches a website rule you chose or the app's
built-in blocklist (described below). It does not inspect or record page paths, search terms, query
strings, cookies, page content, account data, or ordinary non-DNS traffic. Your blocked-domain list
and blocked attempts stay on your device and are not sent to Cloudflare or the developer, or
included in Support Reports. The permitted DNS queries described above do leave the device.

If an encrypted connection to Cloudflare cannot be established or verified, a valid DNS question
fails with a local DNS `SERVFAIL` response. The app does not fall back to unencrypted DNS. A network
that blocks DNS-over-TLS may therefore prevent domain lookups while a Website access rule is active.

Whenever a Website access rule is active, in either mode, the app also blocks a built-in list of
well-known adult-content websites and public encrypted-DNS providers, whether or not you added them.
That list is bundled inside the app, cannot be edited or turned off separately, is not downloaded
from or updated by a server, and is not sent anywhere.

Allow-only rules apply to domain names and their subdomains only. A page may require separate CDN,
sign-in, or embedded-content domains; IP-address access, page paths, and already-resolved tabs are
outside DNS-only enforcement. Android permits only one active VPN at a time. Enabling Website access can disconnect another
personal or work VPN, and connecting another VPN can stop Website access. Some browsers' default
encrypted-DNS behavior is handled locally; a manually configured private resolver outside the app's
curated public-resolver list can still bypass domain blocking.

### Short-form feeds (optional premium feature)

If you turn on Short-form feeds for a Night Lock, Focus Block, or Quick Lock — YouTube Shorts
and Instagram Reels are the two supported providers, independently selectable per lock — Android's
Accessibility API lets the app read the accessible on-screen structure of the YouTube and/or
Instagram app only, never any other app, so it can recognize when the Shorts or Reels screen you
turned on is open while that lock is active and show this app's own Focus block screen over it.
This is best-effort recognition of an on-screen layout, not a guarantee, and it never edits, hides,
or otherwise modifies YouTube's or Instagram's own interface — normal use of either app (Home,
Search, subscriptions, long-form videos, DMs, Stories, posting) is unaffected.

While YouTube or Instagram is open, the Accessibility Service receives screen-change events from
those two apps only. For each event the app builds a temporary, in-memory copy of the screen's
accessible structure: each element's type, its Android view ID, whether it is visible, and its
content description (the label Android exposes for accessibility, which in these apps can include
text such as a video title). It does not copy on-screen text fields, typed text, or search terms.
Recognition uses only the structure and view IDs; the content descriptions are not used. This
happens whenever either app is open, even if no lock is active; when no lock with Short-form feeds
is active, the copy is discarded immediately and the app takes no action. The app does not store,
log, upload, sync, or transmit anything it reads — recognition happens entirely on this device. The
service does not take screenshots or analyze pixels or video, and does not tap, scroll, type, or
perform any action inside either app. It is off by default, scoped to the YouTube and Instagram
packages only, and only acts (shows this app's own block screen) while a lock that selected that
specific provider is active — turning on just one provider does not enable recognition for the
other. It requires you to separately enable it in Android's own Accessibility
Settings after an in-app disclosure explains what it reads and why; the app cannot enable it for
you. If you later turn the service off in
Android Settings, a lock's saved setting stays saved but cannot enforce until you turn the service
back on. This app is not an accessibility tool and is not parental-control or employee-monitoring
software.

### Detailed records stored on your phone

The following detailed app records are stored locally. They are not sent as Firebase Analytics event parameters. This list does not cover the limited optional Analytics signals described below, DNS queries sent to Cloudflare when Website access is active, Google Play billing, or information you choose to share:

- Screen capture frames (auto-deleted after 7 days)
- Assembled MP4 timelapse files
- Session summaries and detailed local session analytics
- PDF session and snapshot reports
- App usage summaries
- Weekly Rhythm's local hourly usage ledger, heatmap, and suggestion dismissals
- App labels and warning preferences
- Capture exclusions and automatic-exclusion opt-outs
- Focus schedules, break windows, and Quick Lock settings
- Focus settings and guardian state
- Protection Log and audit records
- Social Cooldown timing state, Adaptive Protection state and exceptions, and Emergency pass state
- Strict Mode settings: a one-way hash of the passcode and the trusted contact's name if you entered one
- Settings snapshot history
- Local Insights (generated and stored on-device)
- Onboarding preferences (daily goal, sleep time, distraction app list)
- Subscription status read from Google Play and cached locally, plus limited local validation metadata (product ID, validation times, and boot identity) used to enforce the bounded recovery window. This metadata is not sent to the developer.

---

## Optional Analytics and diagnostics

The app includes Firebase Analytics for product measurement. Analytics is off unless and until you grant the separate Analytics choice shown during onboarding. You can change this choice independently in Settings at any time. No feature or app access depends on granting it. If you decline or have not answered, Analytics collection remains disabled. The app does not queue actions from before consent or replay them after you opt in.

If you grant Analytics consent, the app can send coarse events about onboarding progress and completion; first restriction configuration or activation; the first block-enforcement milestone; paywall presentation; plan selection; and basic checkout launch and callback outcomes. These custom events use limited fields such as feature category, screen surface, plan type, and flow outcome. Their parameters do not include names, email addresses, screenshots, screen contents, detailed session histories, app inventories, the names of apps you use or block, website domains, prices, payment credentials, purchase tokens, or order IDs. Custom app events do not report purchase completion, entitlement grants, or restore results.

Firebase Analytics also automatically creates an app-instance identifier and may collect app/session lifecycle events (such as `first_open`, session events, and `user_engagement`) and app, device, and operating-system metadata. Network requests expose an IP address to Google's Analytics service. Google says it uses IP addresses for routing and coarse geographic derivation and discards the raw address before Analytics data is logged; the fields and available geographic detail can vary. The app does not configure an Analytics User-ID, and it does not request precise location for Analytics.

The app's Analytics consent settings deny advertising storage, ad user-data, and ad-personalization consent. The production manifest does not request the Android Advertising ID permission, but the Analytics dependency includes an Ads Identifier library. Whether an advertising identifier is collected in practice has not been confirmed and remains under review for this draft.

The current app manifest sets `google_analytics_automatic_screen_reporting_enabled=false`, which disables Firebase's automatic Activity-level screen reporting. The app's Compose destinations run inside one Activity, and there is no active custom route-level `screen_view` event under the current launch scope. Production event receipt has not been re-observed. Firebase Analytics can also automatically log Google Play `in_app_purchase` events when the Firebase app is linked to Google Play. Whether that link is enabled for this app, and whether any events are received, remains under confirmation; this draft does not claim that automatic purchase tracking is absent.

The Analytics property is currently configured for **2 months** of user-level and event-level data retention. This setting is not a deletion deadline for every aggregate report. When you turn Analytics off, the app stops future collection, clears the SDK's local Analytics state, and refreshes its local app-instance identifier. This setting change does **not** delete Analytics records that were already uploaded.

The app has a separate diagnostics choice, but the production release does not collect crash reports or diagnostic telemetry. Granting the diagnostics choice does not enable Analytics or start diagnostics collection in the production release. Crash reporting is not included in the production app build.

For Google's privacy information, see https://policies.google.com/privacy. Google Analytics data handling, legal roles, and transfer details are subject to the remaining review before this policy draft is finalized.

## What the app does NOT do

- Does not record audio
- Does not use the camera
- Does not capture your screen without your knowledge or explicit consent
- Does not run silent background recording — the foreground service notification is always visible while capture or monitoring is active
- Does not automatically upload screen captures, MP4 files, PDF reports, detailed local session histories, app inventories, or website lists to an app server or Analytics
- Does not sell your personal data to anyone
- Does not use detailed app records or optional Analytics events for its own advertising and does not display ads
- Does not collect Analytics unless you grant the separate Analytics choice
- Does not collect crash reports or diagnostic telemetry in the production release

---

## Permissions

The app declares the following Android permissions. Each is used only for the specific feature it describes.

### Notifications — `POST_NOTIFICATIONS`

Used to send distraction warnings when a labeled app is open during a session, to show the persistent notification required by Android whenever a foreground service is running (screen capture, guardian monitoring), and for local Wake-up Check reminders after a user solves an Extreme Alarm. Wake-up Check notifications are scheduled only from local schedule/alarm state and are not sent to the developer. You can manage notification delivery in Android Settings at any time.

### Screen capture and foreground services — `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PROJECTION`, `FOREGROUND_SERVICE_SPECIAL_USE`

Required for Android to allow the capture session and the Focus guardian service to remain running while you use other apps. Android requires apps to declare foreground-service permissions for any service that stays active in the background. These result in a visible status-bar notification at all times while the service is running — there is no silent background capture.

### Usage Access — `PACKAGE_USAGE_STATS`

Lets the app read bounded recent usage events and which app is currently in the foreground so it can show accurate session summaries, trigger distraction warnings, enforce focus schedules, and build the local Weekly Rhythm view. Weekly Rhythm uses only on-device hourly totals and user-assigned labels; it does not inspect screen content, typed text, browsing history, VPN traffic, or Accessibility data. Android does not guarantee a complete event history, so missing hours remain unavailable rather than being shown as zero use. This is a special permission you must grant manually in Android Settings — it is not granted automatically on install. The detailed usage-event records and app identities are read and stored locally, not included in Analytics event parameters. Optional coarse product milestones are described under “Optional Analytics and diagnostics.”

### Display over other apps — `SYSTEM_ALERT_WINDOW`

Used for two features:

- **Focus block overlays:** When a focus schedule or Quick Lock is active, a full-screen blocking overlay appears over a restricted app. This is the core enforcement mechanism of Focus.
- **Optional in-session warning overlay:** An optional chip can appear over other apps when a distraction app is detected during a recording session. This feature is off by default and can be permanently disabled in Settings.

### Do Not Disturb access — `ACCESS_NOTIFICATION_POLICY`

Optional. Used only when you turn on Do not disturb for a lock: it lets the app ask Android to use
Priority Do Not Disturb while that lock is active and restore your previous interruption mode
afterward. You grant it yourself in Android Settings; the app cannot grant it for you. If you decline
or later revoke it, locks still work but cannot apply Do Not Disturb. The app does not read your
notifications, calls, or messages with this access.

### Full-screen alerts and wake lock — `USE_FULL_SCREEN_INTENT`, `WAKE_LOCK`

Used only by the optional Extreme Alarm and Wake-up Check: the full-screen alert lets the alarm
screen appear over the lock screen at the time you set, and the app holds a temporary wake lock only
while that alarm screen is ringing, so the phone stays awake. Nothing about them is sent anywhere.

### Device Admin — `BIND_DEVICE_ADMIN` (optional)

Optional and off by default. Used only so Android asks for an extra confirmation before this app can
be force-stopped or uninstalled. The app declares **no device-administration policies**: it cannot
lock your screen, set or read your password, wipe your device, or control it in any other way. You
enable it yourself on Android's own consent screen and can remove it at any time by deactivating the
app under Device admin apps in Android Settings.

### Vibration — `VIBRATE`

Used for the haptic feedback pattern in distraction warnings.

### Exact alarms — `SCHEDULE_EXACT_ALARM`

Used to fire focus schedule start and end events and local Extreme Alarm/Wake-up Check deadlines at precise times. Without this, schedule boundaries and accountability alarms could be delayed by Android's battery-optimization system.

### Boot receiver — `RECEIVE_BOOT_COMPLETED`

Allows the app to restart the Focus guardian service after a normal device reboot, if you had already enabled eligible Focus protection. It does not restart screen capture, reuse a prior screen-capture permission, or resume a timelapse without your fresh consent.

### Local VPN website blocking — `INTERNET`

Required by Android for the optional local DNS-only VPN service. The service sends permitted DNS
queries to Cloudflare's public resolver over encrypted DNS-over-TLS, verifying the TLS hostname
`one.one.one.one`. Cloudflare receives the permitted domain names and related DNS query details;
see the Website access section for its published data-handling terms. The app does not operate a
developer-run DNS server or send your blocked-domain list to Cloudflare.

### Short-form feed recognition — Accessibility Service (`BIND_ACCESSIBILITY_SERVICE`)

This app has two separate Accessibility Services; this one is for Short-form feeds only.

Optional and off by default. Used only to recognize the YouTube Shorts and/or Instagram Reels
screen so the app can show its own Focus block screen over it, and acts only while a lock with that
provider enabled is active. Whenever either app is open it briefly reads that app's on-screen
structure in memory only, even if no lock is active. Scoped to the YouTube and Instagram apps only —
it does not read, and cannot read, the accessible content of any other app. You must enable it
yourself in Android's Accessibility Settings, after a separate in-app disclosure. See "Short-form feeds (optional premium feature)"
above for the full data boundary.

### Restart recovery — Accessibility Service (`BIND_ACCESSIBILITY_SERVICE`)

A second Accessibility Service, separate from Short-form feed recognition, called "Timelapse:
Restart recovery". It exists only so Android reconnects the app after a phone restart or after the
system stops its background service, so rules you already turned on can resume without you reopening
the app. On connect and about every five minutes while it stays connected, it checks the app's own
saved state and, if protection should be running but is not, restarts the app's own Focus service
and re-arms its own saved alarms. It is scoped to this app's own package only, so Android never
delivers events from any other app to it, and it is configured not to retrieve window content, so it
cannot read the screen of this app or any other app. It never makes a blocking decision, does not read or
store any screen content, and nothing it does leaves your phone. You enable it yourself in Android's
Accessibility Settings, and a lock cannot be turned on until the reliability checks, which include
auto-resume, pass. If you turn it off, the app can no longer resume your rules on its own after a restart
or after the system stops its service. This app is not an accessibility tool and is not
parental-control or employee-monitoring software.

### Storage — `WRITE_EXTERNAL_STORAGE` (Android 8 and below only)

Used on Android 8 (API level 28) and below to save exported MP4 and PDF files to shared storage. This permission is not requested on Android 9 or higher, where scoped storage rules apply automatically.

---

## When you export or share a file

When you export an MP4 or PDF and share it using Android's share sheet, the file is sent to whichever app or service you choose — email, messaging, cloud storage, and so on. From that point, the receiving app or service controls that copy of the file under its own terms. The developer has no control over or visibility into what happens to the file after you share it.

## Feedback and support email

If you choose `Send feedback`, the app opens your email app with a draft addressed to the developer. The app does not automatically send feedback or attach any device data. You decide whether to send the email and what information to include.

If you choose `Request support` (or `Send report` from a monitoring alert), the app generates an optional support report locally. Depending on what is available, it can include the app name, version, build and package details; install source; device maker, model, Android version and display details; permission and service status; plan and billing availability; capture and output settings; storage totals, session and frame counts, dates and recent session metadata; capture and service-heartbeat timelines; device-wide memory-pressure readings; Android process-exit diagnostics (including reason, status, time and memory values); Focus settings and protection/activity summaries; error details and recent failure history; and app configuration flags. Android process-exit data may include the app's package-qualified process name, process ID (PID), and a random per-process run ID. The generated filename includes this app's install ID when available (or `install-unknown`); the ID appears in the filename, not in the report text.

The report does not include screenshots, videos, user notes, recorded screen or session content, user-entered session names, an inventory of installed or running apps, the names of apps you allow or block, website names, browsing history, blocked attempts, account email, Google Play purchase or order IDs or tokens, raw stack traces, or personal files. The report is created in app-private storage on your device. When generating a report, the app attempts to limit its local report files to five; it does not apply a time-based expiry. Uninstalling or clearing app data removes these local copies. The report is not sent automatically. On the Contact Support screen, you can preview it before choosing whether to copy, save, share, or email it. From a monitoring-change alert, choosing `Send report` opens an email draft with the report attached; you decide whether to send it from the email app. A destination receives the report only after you choose to share it or send the email. The developer has not confirmed how long an email provider keeps a report after you send it.

---

## Google Play Billing

Monthly and annual subscriptions are processed by Google Play. When you subscribe:

- Google handles payment processing and collects your payment card details.
- The developer does not receive your full card number or any payment credentials.
- Normal functional access requires a current Google Play-verified subscription; the App does not offer a public free plan. A 7-day trial may apply to the monthly offer and a 14-day trial may apply to the annual offer only when Google Play returns that offer as eligible for your account. Current localized price, billing period, trial, and renewal terms come from the selected Play offer.
- The app checks subscription status and Restore through Google Play. If Play is unavailable, a prior successful active check may support access for less than 24 hours on the same device boot; access closes at the 24-hour boundary. Otherwise access pauses until verification succeeds. A successful inactive check removes Play-based access immediately.
- The app stores limited successful-active-check metadata on the device to enforce that recovery window. It does not include a purchase token and is not sent to the developer.
- Google's own privacy policy governs the payment transaction: https://policies.google.com/privacy

---

## Children and minors

This app is intended only for adults aged at least 18. If your country or region sets a higher age for independently agreeing to these Terms and purchasing a subscription without parental or guardian consent, that higher age applies. Anyone below the applicable age is not eligible to use the app. The app is not designed as a parental-monitoring or child-tracking tool and should not be used to monitor another person's device without their knowledge and consent.

If you believe someone below the applicable age has sent personal information directly to the developer, for example by contacting support, please contact us at kingprogramming150+t@gmail.com.

---

## Data retention and deletion

| Data                                      | How long it is kept                                                                                                  |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Screen capture frames                     | Auto-deleted from app storage after 7 days                                                                           |
| Session records and detailed local analytics | Up to 90 free or 365 premium sessions; older sessions are cleaned daily and the current session is protected. Remaining app-private records are removed when you clear app data or uninstall. |
| Optional Firebase Analytics data          | The Analytics property is configured for 2 months of user-level and event-level retention; aggregate reports may remain longer. Turning Analytics off clears local SDK state but does not delete records already uploaded. |
| Exported MP4 and PDF files                | Remain in your phone's shared storage until you delete them                                                          |
| Remaining app-private data                | Removed when you uninstall the app                                                                                   |

**No app account.** The app does not use accounts or sign-in and does not maintain an app-operated server-side profile. Optional Analytics records are separate from the local app account and data described above.

**Android "Clear app data."** Clears all app-private data immediately. The app detects this on the next launch and records an entry in the Protection Log.

---

## Security

- Detailed capture, session, and Focus records are stored locally. Optional Analytics signals and permitted Website access DNS queries follow the separate network paths described above.
- The app does not operate a cloud backend or developer-run server for app data.
- The app does not add file-level or end-to-end encryption to locally stored captures, session records, or support reports. These files are protected by Android's per-app storage sandbox; encryption at rest depends on the device's Android storage encryption and security settings, which the app does not independently verify. `android:allowBackup="false"` disables Android Auto Backup for app-private data but is not encryption. MP4 and PDF exports in shared storage are not encrypted by the app.
- Firebase states that its services encrypt data in transit using HTTPS. Website Access sends permitted DNS requests to Cloudflare over DNS-over-TLS. If you choose to share or email a support report, the receiving app or service controls protection after you hand it over.
- `android:allowBackup="false"` is set in the app manifest, preventing app-private data (including screen captures and session data) from being included in Android's automatic cloud backup to Google.
- Exported files written to shared storage are subject to Android's standard file-system protections.

---

## Your privacy rights and requests

The app has no sign-in or account, and the developer does not operate an app backend. If you grant Analytics consent, limited event and technical data is sent to Google's Analytics service as described above. The app does not expose an Analytics app-instance identifier lookup or an in-app export or deletion control for those records. Turning Analytics off, clearing app data, or uninstalling stops future app collection but does not by itself delete records already uploaded.

For a privacy question or request about information associated with the app, including Analytics, contact kingprogramming150+t@gmail.com. This mailbox is monitored. The app does not currently provide a user-facing way to identify Analytics records by app-instance identifier, and a request intake, verification, response, and deletion workflow has not yet been confirmed. Email and support-report retention schedules have not been confirmed. No immediate deletion or response-time guarantee is made in this draft. The operator's legal identity and roles, applicable rights and legal bases, and data-transfer details remain subject to review before this draft is finalized. You may also contact your local data protection authority.

---

## Website visitors

This policy and the Terms are hosted on GitHub Pages. GitHub, as the hosting provider, may process visitors' IP addresses and request data under its own privacy statement. Timelapse adds no analytics, cookies, web fonts or other third-party resources to these pages.

---

## Changes to this policy

If this policy changes in a material way, the updated version will be posted at the URL shown in the app's Google Play Store listing. The "Last updated" date at the top of this document will be updated accordingly. Continued use of the app after a policy update constitutes acceptance of the revised terms.

---

## Contact

For questions about this privacy policy or about your data:

**Developer:** Alvaro Kim  
**Email:** kingprogramming150+t@gmail.com
