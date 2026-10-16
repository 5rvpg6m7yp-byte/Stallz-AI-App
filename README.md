# STALLZ AI — three-file starter

**One AI. Endless possibilities.**

This repository is intentionally kept to three main files:
- `index.html` — responsive single-page AI workspace and browser features.
- `README.md` — this guide.
- `.github/workflows/build-apk.yml` — creates an Android debug APK in GitHub Actions.

## Build an APK
1. Push these files to the `main` branch.
2. Open **Actions** in your GitHub repository.
3. Choose **Build STALLZ AI APK** and run it, or wait for a push-triggered run.
4. When successful, open the run and download the `STALLZ-AI-debug-APK` artifact.
5. Extract the artifact ZIP to find `app-debug.apk`.

## What works in this three-file version
- Responsive dark STALLZ AI interface.
- Local conversation history in the current browser/device.
- Compatible OpenAI-style chat-completions API connection, if you supply a valid endpoint, model, and API key in Settings.
- Image/video prompt builders (they prepare prompts; they do not render images or videos).
- Browser speech recognition and text-to-speech when supported by the device/browser.
- Local settings and history controls.

## Honest limitations
No three-file static project can include every AI model or guarantee it is better than every AI worldwide. Actual AI answers require a provider and credentials. Actual image/video generation needs a provider with those capabilities and suitable API access. The simple browser-based API configuration is for personal testing only: the key is stored in local browser storage and may be exposed to browser tools. **Do not use it for a public production app.** For a public app, add a secure server-side backend that keeps API keys private. Accounts, cross-device sync, payments/subscriptions, and real video/image rendering are not included.

## GitHub Actions
The workflow creates a minimal Capacitor Android wrapper during the build, so you do not need to commit extra Android project files. It uses GitHub-hosted runners and GitHub Actions artifact storage; usage is subject to GitHub's current account limits.
