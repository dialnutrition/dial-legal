# DIAL Nutrition — Privacy Policy

**Effective date:** 2026-09-06
**Version:** 1.1

DIAL Nutrition ("the App") is developed and operated by Rohail Naqvi ("the Developer"). This policy explains what data the App handles, where it lives, and where it goes. It is written to be read, not skimmed — it is short because the App's data practices are simple.

The App runs on Android and iOS. Where the two platforms differ — and on health data they differ in substance, not just in naming — this policy says so rather than picking one and hoping.

## 1. The short version

- Your data lives **on your phone**, in an encrypted database. In this version, the Developer operates **no server** and cannot see, access, or recover your data.
- The App sends data to **Google** only when you use Addie (the AI assistant), only under **your own Google API key**, and only after you have consented. Saving a key also sends one small test message to check the key works — no data of yours in it.
- Meal photos you send to Addie are transmitted to Google **once** for analysis and are **not stored** by the App.
- Recipe cover photos you choose are the one image the App does keep: they stay **on your phone**, are never sent anywhere, and are not included in backups.
- Backups are created only when you choose, encrypted with a passphrase **only you know**, and saved **where you choose**. The Developer never receives them.

## 2. Data stored on your device

The App stores the following locally, in a database encrypted with a key held in your phone's secure key store — the **Android Keystore** on Android, the **iOS Keychain** on iOS. On both platforms the key is marked so that it cannot travel to another device: it is not synced to any cloud, and it is not carried into a device-to-device transfer or an encrypted device backup.

- **Profile:** name, date of birth, gender, height, activity level, units preference
- **Dietary information:** dietary restrictions, allergies, and any dietary notes you write
- **Goals:** goal type, target weight, calorie/macro/water targets and their history
- **Logs:** meals (including AI-estimated macros), water, weight and vitals entries
- **Saved recipes**, including any you add manually
- **Recipe cover photos** you choose, stored as image files in the App's private storage (see below)
- **A daily activity record:** one number per day — the calories your health app says you burned — kept only if you connect a health app (see section 3)
- **Your recent conversation with Addie**, and a short note of logging actions you take elsewhere in the App (see below). Both are deleted automatically after 3 days
- **App settings and state**, including whether a health app is connected and when you last backed up
- **A log of API requests** to Google: the time, the type of request, how long it took, how many tokens it used, whether it succeeded, and — when it failed — the HTTP status code or the name of the error. **Never the content of your messages, and never any text returned by Google.** Kept for 90 days, then deleted automatically

Two of those entries deserve more than a line.

**Recipe cover photos** are the one exception to the database: they are saved as ordinary image files in the App's private storage area, which other apps cannot read, rather than inside the encrypted database. They are downscaled on save and never transmitted.

**The notes about logging you do elsewhere in the App.** When you log a meal, add or remove water, delete a meal, or mark a recipe as cooked using the ordinary screens — not by talking to Addie — the App writes a short line into the same place it keeps your conversation, for example: `logged meal "chicken and rice" (610 cal) via the Today tab.` This exists so that Addie's memory matches your actual records instead of going stale, and it is written whether or not you have an API key and whether or not you have ever opened Addie. These lines are not shown in the chat, so you will not see them on screen. They are deleted on the same 3-day schedule as the rest of the conversation, they are sent to Google if and when you next message Addie (section 4), and they are included in a backup (section 5). We would rather tell you they exist than have you find them in a backup file.

This data never leaves your device except as described in sections 4 and 5.

## 3. Data read from your health app (optional)

The App can read from **Health Connect** on Android and **Apple Health (HealthKit)** on iOS. It **reads only — it never writes**, on either platform. What it asks for is not the same on both, because the two platforms do not offer the same things:

| | Android (Health Connect) | iOS (Apple Health) |
|---|---|---|
| Total calories burned | read | not available on iOS |
| Active calories burned | read | read |
| Resting/basal calories | not requested | read |
| Steps | read | read |
| Sleep | read | **not read — see below** |

**Sleep is not read on iOS.** The App does not request sleep permission there and does not display a sleep figure; the underlying library does not yet support Apple Health's sleep format, and rather than ship a guess the feature is simply absent on iOS. If a future version adds it, the App will ask for the permission then and this policy will be updated. Sleep works as described on Android.

If a future version adds writing (for example, saving workouts you log), the App will request the additional permission and update this policy.

**One piece of health data is stored, and this is a correction to earlier versions of this policy.** Each day you open the App or pull to refresh, it records **one number** — that day's burned-calorie total as your health app reports it — against that date. Nothing else from your health app is kept: not steps, not sleep, not sessions, not history.

That single number exists because your own history would otherwise be wrong. If your calorie target follows your activity, then the target you had last Tuesday depended on what you actually burned last Tuesday — and health platforms do not reliably let an app go back and ask. Without the record, your past reports would quietly show a formula estimate in place of what really happened.

**It is kept until you uninstall.** There is no automatic expiry and no button to clear it, and that is a deliberate decision rather than an oversight: it is one small number per day, and deleting it would silently break the accuracy of your own past reports. It is not included in backups, because it can simply be read again. Uninstalling the App removes it with everything else.

You can disconnect at any time in Settings; full permission revocation is available in your device's Health Connect settings on Android, or in the Health app's Privacy settings on iOS.

## 4. Data sent to Google (only when you use Addie)

Addie is powered by Google's Gemini API using **your own API key**. When and only when you send Addie a message, the App transmits to Google:

- Your profile: name, age, gender, height, activity level
- Your goal and target weight; dietary restrictions, allergies, and dietary notes; units preference
- Your current calorie/macro/water targets and today's meal and water totals
- If a health app is connected: calories burned, steps, and — on Android only — last night's sleep
- Your latest weight and its timestamp
- Your timezone and current local time
- **Up to the last 24 messages from the past 3 days** of your conversation, whichever is the smaller amount. This includes the notes about logging you did elsewhere in the App, described in section 2
- **An assessment of whether your goal is self-consistent.** Before each message the App checks whether your goal type, your current weight and your target weight contradict one another — for instance a goal to lose weight with a target above your current weight. When and only when it finds a contradiction, it includes a line describing it, so that Addie does not coach you toward a goal your own settings rule out. This is the App's judgement about your settings, not a field you entered, which is why it is listed separately here
- Any meal photos you attach (each photo is uploaded once for analysis; the App deletes its temporary copy immediately after reading it and does not store your photos)

**One other moment the App contacts Google.** When you save an API key — in setup or in Settings — the App makes a single test request to check the key works. That request contains **no data of yours**: the message body is the literal word "Hi". It happens before you have ever chatted, so it is worth naming, even though nothing about you is in it.

**This data is handled under your agreement with Google, not the Developer's.** If you use a free-tier API key, Google's terms permit Google to use submitted content to improve its products and services. If you do not want this, do not connect an API key or use Addie — every other feature of the App works fully without it.

The Developer receives none of this data.

## 5. Backups

Backups are created only when you tap "Back up now." The backup file contains your full database, encrypted (AES-256-GCM, key derived from your passphrase). You choose where it goes via the **Android share sheet** or the **iOS share sheet**. **If you forget your passphrase, the backup cannot be recovered by anyone, including the Developer.**

Two things about what a backup contains are easy to get wrong, so they are spelled out:

- **A backup preserves what was in your conversation at the moment you exported it** — including the logging notes from section 2 — even though that conversation is deleted from the App itself after 3 days. Restoring an old backup restores those messages.
- **A backup also contains the API request log** described in section 2, and **entries you have deleted.** Deleting a log entry hides it from every screen and every total, but the underlying record is marked deleted rather than erased (section 7), and marked-deleted records travel in a backup.

**What a backup does not contain:** your Gemini API key (it lives in your phone's secure key store, not the database — a restored install will ask you to enter it again), your recipe cover photos (section 7), the daily activity record (section 3), and your health-app permissions, which belong to a device rather than to your data.

The App does not let the operating system make its own copy. On Android, automatic cloud backup of the App's data is disabled. On iOS, the database and your recipe cover photos are marked as excluded from iCloud and from device backups — a copy the OS made could otherwise be restored to a phone whose Keychain does not hold the key to open it. **The encrypted backup file you create is the only backup path**, on both platforms.

## 6. What the Developer collects

Nothing, in this version. The App contains no analytics, telemetry, crash reporting, or tracking; the Developer operates no server, receives no data from the App, and cannot identify who uses it. If a future version introduces any such feature, this policy will be updated and your renewed consent requested first.

## 7. Data retention and deletion

Most data is retained on your device until you delete it. What expires on its own:

- **Conversation with Addie, and the logging notes from section 2** — deleted automatically after 3 days. You can also delete all of it immediately with **"Clear chat history"** in Addie's ⋯ menu; that erases the messages outright rather than marking them deleted
- **The API request log** — deleted automatically after 90 days
- **The daily activity record** — kept until uninstall, by the deliberate decision explained in section 3

Deleting a log entry (a meal, a water entry, a weight) removes it from your view immediately and from every total; the underlying record is marked deleted rather than erased, which is why it can still appear in a backup file (section 5). A recipe's cover photo file is deleted outright when you remove it, replace it, or delete the recipe.

**Uninstalling.** On Android, uninstalling the App destroys the database, its encryption key, and your recipe cover photos. On iOS, uninstalling destroys the database and the cover photos; **the encryption key is held in the iOS Keychain, and Keychain entries are not guaranteed to be removed when an app is deleted.** A key left behind on its own opens nothing — the database it decrypts is gone — and it cannot travel to another device. We would rather state this plainly than claim a deletion we have not confirmed on an iOS device. If you want the key gone with certainty, erase the device or reset it to factory settings.

Conversation history is deleted as described above. Data you sent to Google via Addie is thereafter governed by Google's retention practices, not the App's.

## 8. Children

The App is not directed at, and must not be used by, anyone under 18. This is a condition of Google's Gemini API terms and of the App's own Terms of Use.

## 9. Changes

If this policy changes materially, the App will present the updated policy and ask for your consent again before continuing to use Addie.

## 10. Contact

Questions: dial.nutrition.app@gmail.com
