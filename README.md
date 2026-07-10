# TDrive

TDrive is a private cloud drive for Android that saves your files through your own Telegram account.

Think of it like a personal Google Drive, but the storage is connected to Telegram. Your files are encrypted on your phone before they are uploaded, then saved inside private Telegram storage that belongs to your Telegram account.

TDrive is not an official Telegram app. It uses Telegram's API through TDLib.

## Download

Latest version: **1.0.3**

[Download TDrive.apk](https://raw.githubusercontent.com/anandmoon/TDrive-releases/main/releases/v1.0.3/TDrive.apk)

This app currently supports Android phones with **arm64-v8a** support. Most modern Android phones are arm64.

## What TDrive Does

| Feature | What it means |
|---|---|
| Upload files | Pick files from your phone and save them to your private TDrive. |
| Multi-device sync | Log in on another Android phone and find the same TDrive vault. |
| Photos, videos, docs, music tabs | Files are grouped automatically so they are easier to find. |
| Saved Messages folder | Files from Telegram Saved Messages appear inside TDrive under `Saved`. |
| File preview/open | Tap a file to open it with a compatible app on your phone. |
| Share | Share decrypted files to WhatsApp, Telegram, Quick Share, email, or other compatible apps. |
| Download | Save files back to your phone. Multiple files or folders can be downloaded as a zip where supported. |
| Trash | Restore deleted items or delete them permanently. |
| App updates | TDrive can check this public release feed and ask Android to install updates. |

## How To Install

1. Tap [Download TDrive.apk](https://raw.githubusercontent.com/anandmoon/TDrive-releases/main/releases/v1.0.3/TDrive.apk).
2. Open the downloaded APK.
3. If Android asks, allow installation from your browser or file manager.
4. Tap **Install**.
5. Open **TDrive**.

If Android warns you because the app was downloaded outside the Play Store, only continue if you downloaded it from this repository.

## First-Time Setup

### 1. Enter your Telegram phone number

Use the same phone number you use for Telegram.

TDrive does not use the developer's Telegram account. It logs into your own Telegram account.

### 2. Enter the Telegram code

Telegram may send the code to:

- Your Telegram app on another device
- SMS
- Email, if Telegram asks for email verification

Enter that code in TDrive.

### 3. Enter Telegram password if asked

If your Telegram account has two-step verification enabled, TDrive will ask for your Telegram password.

You can tap the eye icon to show or hide the password before continuing.

### 4. Set up your private drive

If this is your first TDrive device, tap **Create new drive**.

TDrive will create private Telegram storage for you:

| Telegram item | Why it exists |
|---|---|
| `TDrive Storage 001` | Stores encrypted file blobs. |
| `TDrive Index` | Stores the encrypted map of your folders and files. |

Please do not delete these Telegram channels. If they are deleted, TDrive may need to create new ones and sync whatever it can still find.

## Using TDrive On A New Phone

1. Install TDrive on the new phone.
2. Log in with the same Telegram account.
3. Choose **Find existing drive**.
4. Select your TDrive vault.
5. Wait for sync to finish.

Do not create a new drive if you want to use the files from your old phone. Use **Find existing drive**.

## What Telegram Can See

TDrive uploads encrypted files to Telegram. The readable file names and folder details are stored inside encrypted TDrive metadata.

Telegram may still show private TDrive channels in your account, but the uploaded file blobs are not meant to be opened directly from Telegram.

Simple version:

| Question | Answer |
|---|---|
| Are files uploaded to my Telegram account? | Yes. |
| Are they uploaded to the developer's Telegram account? | No. |
| Are files encrypted before upload? | Yes. |
| Should I delete the TDrive Telegram channels? | No. |
| Can I use the same vault on many phones? | Yes, when you log in with the same Telegram account. |

## Saved Messages

TDrive shows Telegram Saved Messages as a folder named **Saved**.

This helps if you already saved files in Telegram and want to see them in TDrive.

Saved Messages files are not automatically moved into your encrypted TDrive vault. If you want one of those files inside TDrive, use the **Add to TDrive** action.

After a Saved Messages file is added, the action changes to **Added**.

## Updates

TDrive checks this file for app updates:

[update.json](https://raw.githubusercontent.com/anandmoon/TDrive-releases/main/update.json)

When an update is available:

1. Open TDrive.
2. Go to **Settings**.
3. Tap **Check for updates**.
4. Android will ask you to confirm installation.

Important: if you previously installed a debug APK, Android may not update it with the public signed APK. In that case, uninstall the debug APK once, then install the public APK from this repo.

## Common Problems

| Problem | What to try |
|---|---|
| I do not see my old files on a new phone. | Make sure you logged in with the same Telegram account, then choose **Find existing drive** and tap the sync button. |
| TDrive asks me to create storage again. | Your saved TDrive Telegram channels may be missing or inaccessible. Use the setup screen to find existing storage or create replacement channels. |
| Telegram code does not arrive. | Check your Telegram app on another device first. Telegram may also use SMS or email. |
| A file will not open. | Install an app that supports that file type, then try again. |
| Sharing to WhatsApp changes quality. | Some apps compress media by default. Use document/file sharing in the receiving app when original quality matters. |
| Update install fails. | If you installed an old debug APK, uninstall it once and install the public release APK. |

## Fair Use

TDrive depends on Telegram's API. Please use it for personal storage and avoid spam, bulk abuse, or anything that violates Telegram's rules.

Very heavy uploads may be limited by Telegram, your internet connection, or your device.
