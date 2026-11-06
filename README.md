# AEGIS AI — Mobile prototype

## Included working features
- Link risk analysis using explainable local URL-pattern rules.
- Reasons for each warning and recommended next steps.
- Visual alert overlay, flashing warning light, and two-tone sound.
- Privacy scanner for common email, phone, payment-card-like, password/OTP-label, and identity-number patterns.
- Masked text preview and copy button.
- Built-in safety Q&A guidance.
- Installable Progressive Web App (PWA) with offline cache after first visit.

## Important limitations
This is a functional educational MVP, not a certified antivirus product or a full large-language-model system. The assistant uses a local rule engine and built-in responses. It does not contact Google Safe Browsing, VirusTotal, urlscan, or another live threat-intelligence service. A low-risk result does not mean a website is safe. No submitted text or URL is sent to a server by this prototype. Do not paste passwords, OTPs, full card data, or confidential documents.

## Install on your Android phone (recommended)
PWA installation needs HTTPS. Easiest free route:
1. On a computer or phone browser, create a GitHub account at https://github.com.
2. Create a new public repository named `aegis-ai`.
3. Upload every file in this folder to the repository root.
4. Open repository **Settings → Pages**.
5. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
6. Wait for the HTTPS website address, usually `https://YOUR-USERNAME.github.io/aegis-ai/`.
7. Open that address in Chrome on Android.
8. Tap Chrome menu (⋮) → **Install app** or **Add to Home screen**.
9. Open AEGIS from the new icon. Tap the page once before testing the sound; browsers block automatic audio until user interaction.

## Test on a computer
Install Python 3, open a terminal in this folder, and run:
`python -m http.server 8000`
Then visit `http://localhost:8000`.

## Files
- `index.html` — interface
- `styles.css` — responsive design
- `app.js` — local analysis, warning, and assistant logic
- `manifest.json` — PWA metadata
- `service-worker.js` — offline cache
- `icon.svg` — app icon

## Advanced production upgrades
To become a stronger real-world security product, add a protected backend and a reputable live URL reputation API. Keep API keys server-side, add authentication/rate limits, use a privacy-preserving real language model, threat-model the system, test false positives/negatives, and obtain a security review. Never claim complete protection.
