# DIAL Nutrition — Data Ownership Statement

**Effective date:** 2026-09-06
**Version:** 1.1

This statement is a plain-language commitment about who owns and controls your data. It supplements the Privacy Policy and describes the App as currently shipped, on Android and on iOS.

## Your data is yours

Everything you record in DIAL Nutrition — your profile, goals, meals, water, weight, recipes (including any cover photos you choose), and conversations with Addie — belongs to you.

## It lives with you

Your data is stored in an encrypted database on your device. The encryption key is generated on your device and held in your phone's secure key store — the Android Keystore on Android, the iOS Keychain on iOS. It is marked so that it cannot travel to another device: it is not synced to any cloud, and it is not carried into a device-to-device transfer or an encrypted device backup.

In this version of the App, the Developer operates no server and the App contains no accounts, analytics, or tracking. The Developer cannot see, access, alter, or recover your data. If a future version introduces features that change this (for example, optional accounts or sync), the Privacy Policy will be updated and your renewed consent requested before those features apply to you.

## It moves only when you move it

- **Backups:** you decide when to create one and where it goes. Backups are encrypted with a passphrase only you know.
- **Addie:** when you choose to use the AI assistant, the specific data listed in the Privacy Policy is sent to Google under your own API key. That is the App's only network destination.
- **Your health app:** Health Connect on Android, Apple Health on iOS. Read-only on both, with your permission, revocable at any time. The App keeps one number per day from it — the calories you burned — so that your own past reports stay accurate; the Privacy Policy, section 3, explains why.

**If you never use Addie, your data never leaves your device.** One honest asterisk on that: when you save an API key, the App sends a single test message to Google to check that the key works, before you have chatted at all. That message contains no data of yours — the body is the literal word "Hi". If you never add a key, the App makes no network requests whatsoever.

## Deleting, uninstalling, and restoring

- Deleting an entry removes it from your records and from every total the App shows.
- Your conversation with Addie is deleted automatically after 3 days, and you can clear it immediately with "Clear chat history" in Addie's ⋯ menu.
- Uninstalling the App deletes the on-device database and any recipe cover photos you saved. On Android it also deletes the encryption key. On iOS the key is held in the Keychain, and Keychain entries are not guaranteed to be removed when an app is deleted — a key left behind opens nothing, since the database is gone, and it cannot travel to another device. The Privacy Policy, section 7, says how to be certain.
- **Your own backups are unaffected by uninstalling.** If you have a backup file saved (in Google Drive, in Files or iCloud Drive, or anywhere else you put it), reinstalling the App and choosing "Restore from backup" with your passphrase brings your records back — on the same phone or a new one.
- Three things do not come back with a restore. **Recipe cover photos** are image files rather than records, are not part of a backup, and those recipes return with generated cover art. **Your Gemini API key** lives in your phone's secure key store rather than the database, so you will be asked to enter it again. **Your health-app connection** belongs to a device rather than to your data, so you reconnect it in two taps.
- The Developer holds no copy at any point.

## Ownership and responsibility

Because no one else holds your data, no one else can restore it. Backups are encrypted end-to-end with your passphrase: without it, a backup file cannot be decrypted — by design, and by anyone. Two habits keep your data safe: back up regularly (the App shows the date of your last backup in Settings), and keep your passphrase somewhere you trust.

One thing worth knowing before you share a backup file with anyone: it is a complete copy of your records at that moment. That includes entries you deleted (the App marks records deleted rather than erasing them) and whatever was in your Addie conversation when you exported it, even though the App itself deletes that after 3 days. The file is strongly encrypted and useless without your passphrase — but it is a fuller picture of you than the screens show, and that is worth knowing before you hand one over.

— Rohail Naqvi, Developer
