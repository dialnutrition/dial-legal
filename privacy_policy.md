# DIAL Nutrition — Privacy Policy

**Effective date:** 2026-07-20
**Version:** 1.0

DIAL Nutrition ("the App") is developed and operated by Rohail Naqvi ("the Developer"). This policy explains what data the App handles, where it lives, and where it goes. It is written to be read, not skimmed — it is short because the App's data practices are simple.

## 1. The short version

- Your data lives **on your phone**, in an encrypted database. In this version, the Developer operates **no server** and cannot see, access, or recover your data.
- The App sends data to **Google** only when you use Addie (the AI assistant), only under **your own Google API key**, and only after you have consented.
- Meal photos are sent to Google **once** for analysis and are **not stored** by the App.
- Backups are created only when you choose, encrypted with a passphrase **only you know**, and saved **where you choose**. The Developer never receives them.

## 2. Data stored on your device

The App stores the following locally, in a database encrypted with a key held in your device's secure hardware (Android Keystore):

- Profile: name, date of birth, gender, height, activity level, units preference
- Goals: goal type, target weight, calorie/macro/water targets and their history
- Logs: meals (including AI-estimated macros), water, weight and vitals entries
- Saved recipes, including any you add manually
- Your last 3 days of conversation with Addie (older messages are deleted automatically)
- App settings and state, including Health Connect connection status
- A log of API request metadata (timestamps, success/failure — never message content beyond what is described above)

This data never leaves your device except as described in sections 4 and 5.

## 3. Data read from Health Connect (optional)

If you connect Health Connect, the App currently **reads only** (it does not write): active calories burned, steps, and sleep sessions. If a future version adds writing (for example, saving workouts you log), the App will request the additional permission and update this policy. These values are displayed in the App and, if you use Addie, included in messages to Google as described below. The App does not store Health Connect history; it reads current values when needed. You can disconnect at any time in Settings; full permission revocation is available in your device's Health Connect settings.

## 4. Data sent to Google (only when you use Addie)

Addie is powered by Google's Gemini API using **your own API key**. When and only when you send Addie a message, the App transmits to Google:

- Your profile: name, age, gender, height, activity level
- Your goal and target weight; dietary restrictions, allergies, and dietary notes; units preference
- Your current calorie/macro/water targets and today's meal and water totals
- If Health Connect is connected: calories burned, steps, and last night's sleep
- Your latest weight and its timestamp
- Your timezone and current local time
- Up to 3 days of your conversation history with Addie
- Any meal photos you attach (each photo is uploaded once for analysis; the App deletes its temporary copy immediately after reading it and does not store your photos)

**This data is handled under your agreement with Google, not the Developer's.** If you use a free-tier API key, Google's terms permit Google to use submitted content to improve its products and services. If you do not want this, do not connect an API key or use Addie — every other feature of the App works fully without it.

The Developer receives none of this data.

## 5. Backups

Backups are created only when you tap "Back up now." The backup file contains your full database, encrypted (AES-256-GCM, key derived from your passphrase). You choose where it goes via the Android share sheet. **If you forget your passphrase, the backup cannot be recovered by anyone, including the Developer.** Automatic Android cloud backup of the App's data is disabled by design; the encrypted backup file you create is the only backup path.

## 6. What the Developer collects

Nothing, in this version. The App contains no analytics, telemetry, crash reporting, or tracking; the Developer operates no server, receives no data from the App, and cannot identify who uses it. If a future version introduces any such feature, this policy will be updated and your renewed consent requested first.

## 7. Data retention and deletion

All data is retained on your device until you delete it. Deleting a log entry removes it from your view immediately (the underlying record is marked deleted). Uninstalling the App permanently destroys the database and its encryption key. Conversation history with Addie is automatically deleted after 3 days. Data you sent to Google via Addie is thereafter governed by Google's retention practices, not the App's.

## 8. Children

The App is not directed at, and must not be used by, anyone under 18. This is a condition of Google's Gemini API terms and of the App's own Terms of Use.

## 9. Changes

If this policy changes materially, the App will present the updated policy and ask for your consent again before continuing to use Addie.

## 10. Contact

Questions: dial.nutrition.app@gmail.com
