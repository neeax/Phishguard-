# 🛡️ PhishGuard Mobile

A mobile-friendly cybersecurity awareness app that checks URLs for common phishing warning signs. PhishGuard is designed
offline use after the app has been loaded once.

## 🔎 1. Check a suspicious URL

1. Open PhishGuard.
2. Paste a website URL into the input box.
3. Tap **ANALYZE URL**.
4. Review the risk level, score, and warning signs.

PhishGuard can display three levels:

- **LOWER RISK** — few common warning signs were detected.
- **SUSPICIOUS** — some warning signs were detected.
- **HIGH RISK** — several warning signs were detected.

> A low score does **not** prove that a website is safe. This demo uses simple URL heuristics and does not query a live phishing database.


## 📲 3. Install it like an app

- **Android (Chrome):** Open the published HTTPS website, tap the ⋮ menu, then choose **Install app** or **Add to Home screen**.
- **iPhone (Safari):** Open the website, tap **Share → Add to Home Screen**.
- **Desktop (Chrome/Edge):** Use the install icon in the address bar if it appears.

The exact menu wording may vary by browser and device.

## 📴 How offline works

- `sw.js` caches the app files so the interface can load offline after the first successful visit.
- URL checks run locally in your browser.
- PhishGuard does not need to contact the URL being analyzed.
- The first visit and app updates require an internet connection.

## 🧠 What the checker looks for

Depending on the URL, the demo may flag:

- URLs that do not use HTTPS.
- IP addresses used in place of ordinary domain names.
- Unusually long URLs or many subdomains.
- Username/password text placed before the host.
- Punycode domains that deserve extra scrutiny.
- Words often used in login, account, payment, or prize lures.

These are clues, not proof. Legitimate sites can trigger warnings, and phishing sites can avoid them.

## ⚠️ Things to know

- **Not a live threat scanner.** It does not use a reputation feed or verify a domain against a phishing database.
- **No website is opened.** The checker only analyzes the text of the URL you paste.
- **False positives and misses are possible.** Never rely on the score alone.
- **HTTPS is not a trust guarantee.** It encrypts the connection but does not prove that a website is legitimate.
- **Stay cautious.** Do not enter passwords, verification codes, payment details, or personal information on a suspicious site.

## 📁 Files

| File | Purpose |
|---|---|
| `index.html` | Mobile interface, URL analysis logic, and risk indicator |
| `manifest.json` | App name, display settings, and installable-app metadata |
| `sw.js` | Service worker that caches app files for offline use |
| `icon.svg` | Vector app icon |
| `icon-192.png` | Small app icon for supported Android launchers |
| `icon-512.png` | Large app icon for installation and launchers |
| `README.md` | Project instructions and documentation |

## 👨‍💻 Credits

**PHISHGUARD — OFFLINE DEMO · DEVELOPED BY NEEAX* 
