# CHU Android App

**Creative Humanity Universe** — Capacitor-wrapped Android project.

## Quickest way to get an APK (no Android Studio needed)

1. Push this folder to a **new GitHub repository** (see steps below)
2. GitHub Actions builds the APK automatically
3. Download `CHU-debug-apk` from the **Actions** tab

## Step-by-step: Push to GitHub & download APK

### One-time setup
Install Git if you don't have it: https://git-scm.com/downloads

### Commands (run in this folder)

```bash
git init
git add .
git commit -m "Initial CHU Android project"
```

Go to https://github.com/new and create a **blank** repo (no README, no .gitignore).
Copy the repo URL (e.g. `https://github.com/yourname/chu-android.git`), then:

```bash
git remote add origin https://github.com/yourname/chu-android.git
git branch -M main
git push -u origin main
```

### Get the APK
1. Open your repo on GitHub
2. Click the **Actions** tab
3. Click the running workflow **"Build CHU APK"**
4. Wait ~3 minutes for the build to finish
5. Under **Artifacts**, click **CHU-debug-apk** to download a ZIP
6. Unzip it — inside is `app-debug.apk`

### Install on your phone
1. On your Android phone: **Settings → Security → Install unknown apps** → allow your browser or file manager
2. Transfer `app-debug.apk` to your phone (USB, Google Drive, WhatsApp, email)
3. Tap the file to install

## Rebuild after updating CHU

In Replit's Shell, run:
```bash
pnpm run cap:sync   # (inside artifacts/chu-app/)
```
Then push the updated `android/` folder to GitHub — a new APK builds automatically.
