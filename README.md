# Talking Daughter — Android App

A WebView-wrapped Talking Tom-style app starring your daughter's photo.
GitHub Actions builds the APK automatically — **no Android Studio, no SDK, no local setup needed**.

---

## How to get your APK (5 clicks, ~3 minutes)

### 1. Create a GitHub repo
- Go to github.com, log in (or sign up — 2 min)
- Click the **+** in the top-right → **New repository**
- Name it anything (e.g. `talking-daughter`)
- Keep it **Public** (GitHub Actions is free for public repos)
- Click **Create repository**

### 2. Upload everything in this folder
- On the new empty repo page, click **"uploading an existing file"**
- Drag the **entire contents** of this folder (not the folder itself — all the files and subfolders inside) onto the page
- Wait for all files to upload (you should see `app/`, `gradle/`, `.github/`, `build.gradle`, etc.)
- Scroll down, click **Commit changes**

### 3. Wait for the build
- Click the **Actions** tab at the top of your repo
- You'll see a workflow called "Build Talking Daughter APK" running (yellow circle → green check)
- It takes about 3 minutes the first time

### 4. Download the APK
- Once the workflow shows a green check, click into it
- Scroll to the bottom — you'll see **Artifacts** → **TalkingDaughter-APK**
- Click to download a zip. Unzip it → you have `app-debug.apk`

### 5. Install on the Fold 4
- Transfer the APK to the phone (email, Google Drive, USB cable)
- Open **My Files** on the phone → tap the APK
- It'll ask to allow "install unknown apps" from the file manager — toggle on
- Tap **Install**
- Launch "Talking Daughter" from the app drawer
- Upload your daughter's photo on first launch

---

## What you're getting

- Real installable Android APK
- Works on the Fold 4 cover screen AND inner screen
- Microphone recording with pitched-up playback (the Talking Tom voice)
- 5 interactions: Tap, Hug, Tickle, Spin, Dance
- Photo stored locally on device, persists between launches

## If the build fails

Click into the failed workflow run → expand the red step → look at the last few lines of the log.
Most common issue: a file didn't upload. Re-upload and commit again.

## Customization

- App name: edit `app/src/main/res/values/strings.xml`
- App icon: replace files in `app/src/main/res/mipmap-*` folders
- Web app itself: edit `app/src/main/assets/html/index.html`

Each commit triggers a fresh APK build.
