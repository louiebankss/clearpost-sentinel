# ClearPost Sentinel — Prototype v0.3

A free, installable web-app prototype for a future voice-first personal security assistant.

## What's in this version
- Tap-to-talk speech input when supported by the browser; typed input is always available.
- Browser speech synthesis for spoken responses.
- Local, rules-based warning-sign checks for suspicious text and links.
- Basic security guidance for lost phones, compromised accounts, and privacy settings.
- Progressive Web App (PWA) manifest and an offline app-shell cache.

## Important limitations
This is **not** antivirus, a live AI model, a certified phishing detector, a phone-monitoring tool, an emergency service, or a smart-home camera integration. Rule-based checks can miss malicious content and can flag benign content. A “no obvious flags” result does not mean a message or link is safe.

The scanner and chat do not intentionally transmit the text you enter to a ClearPost server; this prototype has no ClearPost backend. Browser speech recognition may use services provided by the browser/platform. Do not paste passwords, one-time codes, financial account details, or other secrets.

## Run locally
Open `index.html` in a browser. Some browser voice features and PWA/offline behavior require HTTPS or localhost.

## Free deployment using GitHub Pages
1. Create/sign in to a GitHub account.
2. Create a **public** repository named `clearpost-sentinel` (public repositories are generally needed for free GitHub Pages on the free plan; verify current GitHub terms before relying on this).
3. Upload `index.html`, `manifest.json`, `icon.svg`, and `sw.js` to the repository root.
4. In repository **Settings → Pages**, select deployment from the `main` branch and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the HTTPS URL shown in that settings page.
6. Open that URL on the iPhone in Safari. Use **Share → Add to Home Screen** to install it.

A public repository means the source code is public. Do not put secrets, API keys, personal data, or credentials in the repository. This project currently contains no API key.

## Next development milestone
Before connecting a real language model, define a threat model and data policy. A real AI integration usually requires a backend to protect API credentials; never embed a secret API key in browser JavaScript. Keep user content out of logs by default and require explicit consent before any external analysis. Smart-home integrations should use supported vendor APIs, least-privilege permissions, and user confirmation for sensitive actions.
