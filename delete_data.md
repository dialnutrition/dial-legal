<!--
  NOT DISPLAYED IN THE APP.

  This file is the maintained source for the publicly hosted delete-data
  page (github.com/dialnutrition/dial-legal), which the Play Console and
  App Store Connect both link to. It lives here so that it is versioned
  and reviewed alongside the three documents the App actually shows, and
  so that a session changing what the App stores changes this in the same
  pass instead of leaving the hosted copy to drift.

  It is deliberately absent from LegalDoc / LegalDocuments.docs — adding
  it there would put it in Settings and on the consent screen, which is
  not what it is for.

  WHEN YOU EDIT THIS: copy it to the hosted repo in the same session, or
  the two are out of step and the hosted one is what a reviewer reads.
  Last synced to hosted: 2026-09-10
-->

# DIAL Nutrition — Deleting Your Data

**Effective date:** 2026-09-06
**Version:** 1.1

DIAL Nutrition stores your data **on your phone**, not on a server. There is no account to close and no request to send: deleting your data is something you do on the device, and it takes effect immediately. The Developer holds no copy and could not delete anything on your behalf even if asked.

This page applies to DIAL Nutrition on **Android and iOS**.

## Deleting individual entries

Inside the App you can delete any meal, water entry, weight entry or recipe from the screen it appears on. A deleted entry disappears from every screen and every total straight away.

To be precise about what happens underneath: the record is **marked deleted** rather than erased from the database. It is gone from the App as far as anything you can see or count is concerned, but it is still present in the database file, and it is included if you export a backup. Uninstalling the App destroys it along with everything else.

## Deleting your conversation with Addie

Your conversation with Addie is deleted automatically after **3 days**. To delete it immediately, open Addie, tap the **⋯** menu and choose **Clear chat history**. That erases the messages outright.

This also clears something you cannot see on screen: when you log a meal, add or remove water, delete a meal, or mark a recipe as cooked from the ordinary screens, the App records a short line about it — for example `logged meal "chicken and rice" (610 cal) via the Today tab.` — so that Addie's memory matches your records. Those lines live with the conversation, expire on the same 3-day schedule, and are erased by "Clear chat history" too.

## Deleting everything

**Uninstall the App.** That permanently destroys:

- The encrypted database and everything in it — profile, dietary information, goals and their history, meals, water, weight, recipes, and any entries you had previously deleted
- Your recipe cover photos
- **The daily activity record** — one number per day, the calories your health app reported, kept so that your past reports stay accurate. It has no separate delete control and no expiry; uninstalling is what removes it
- The log of API requests to Google (which in any case deletes itself after 90 days)
- Your conversation with Addie and the logging notes described above

**On Android**, uninstalling also destroys the database encryption key.

**On iOS**, the encryption key is held in the iOS Keychain, and Keychain entries are **not guaranteed** to be removed when an app is deleted. A key left behind opens nothing — the database it decrypts is gone — and it cannot travel to another device. If you want certainty that nothing remains, erase the device (Settings → General → Transfer or Reset iPhone → Erase All Content and Settings). We would rather state this than claim a deletion we have not confirmed.

## What uninstalling does not reach

**Backups you made.** A `.dialb` backup file is yours and lives wherever you put it — Google Drive, Files, iCloud Drive, a computer, a chat thread. Uninstalling the App does not touch it. If you want your data gone, **delete your backup files too.** They are strongly encrypted and unreadable without your passphrase, but they are a complete copy of your records at the moment you exported them.

**Data already sent to Google.** If you used Addie, the messages and photos you sent went to Google under **your own API key**, and Google's retention practices govern them from that point — not the App's, and not the Developer's. Deleting the App does not reach them. Manage that data through your own Google account: **[myactivity.google.com](https://myactivity.google.com)**, and the Gemini API settings for the key you created. You can also delete or restrict the API key itself at **[aistudio.google.com/apikey](https://aistudio.google.com/apikey)**.

**Health data.** DIAL never writes to Health Connect or Apple Health, so there is nothing of DIAL's to delete there. The permissions you granted are revoked in your device's Health Connect settings on Android, or in the Health app's Privacy settings on iOS. Doing so stops future reads; the one-number-per-day record already inside DIAL is removed by uninstalling.

## Questions

dial.nutrition.app@gmail.com
