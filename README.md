# ⬡ VaultX — Password Manager

A secure, zero-dependency password manager that runs entirely in your browser. One HTML file. No server. No accounts. No tracking.

---

## ✨ Features

- 🔐 **AES-256-GCM encryption** with PBKDF2 key derivation (310,000 iterations)
- 🧠 **Master password** — never stored anywhere, only used to derive the encryption key
- 📂 **7 categories** — Social Media, Email, Gaming, Crypto Wallets, Finance, Work, Other
- 🪙 **Crypto wallet support** — wallet address, seed phrase, private key, network/chain
- ⚡ **Password generator** — configurable length, uppercase, lowercase, numbers, symbols
- 💪 **Password strength meter** on all password fields
- 👁 **Show/hide toggle** on all sensitive fields
- 📋 **One-click copy** on every field
- 📤 **Export encrypted backup** — safe to store in cloud or USB
- 📄 **Export plain JSON** — for migration to other managers
- 📥 **Import & merge** — supports both encrypted and plain backup formats
- 🔒 **Lock vault** — clears memory and returns to login instantly
- 🔍 **Search + category filter** sidebar
- ⌨️ **Keyboard shortcut** — `Escape` closes any open modal

---

## 🚀 Getting Started

### Option 1 — Open Locally
Download `vaultx.html` and open it directly in any modern browser. No installation needed.

### Option 2 — Deploy to Vercel
1. Create a new GitHub repository
2. Add `vaultx.html` to the root of the repo
3. Connect the repo to [Vercel](https://vercel.com)
4. Set **Framework Preset** to `Other`
5. Set **Output Directory** to `.` (root)
6. Deploy — done ✅

### Option 3 — Deploy to GitHub Pages
1. Push `vaultx.html` to a repo (rename to `index.html`)
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your vault is live at `https://yourusername.github.io/repo-name`

### Option 4 — Any Static Host
Upload `vaultx.html` to Netlify, Cloudflare Pages, or any static file host. It works anywhere.

---

## 🔒 Security Model

| Property | Detail |
|---|---|
| Encryption | AES-256-GCM |
| Key derivation | PBKDF2-SHA256, 310,000 iterations |
| Salt | 16 bytes, randomly generated per save |
| IV | 12 bytes, randomly generated per save |
| Master password | Never stored — used only in memory during session |
| Storage | `localStorage` (encrypted blob only) |
| Network | Zero — fully offline capable |
| Dependencies | None — uses only Web Crypto API |

> **Important:** If you forget your master password, your vault **cannot be recovered**. Always keep an exported backup in a safe place.

---

## 📁 Entry Fields

### All Categories
| Field | Description |
|---|---|
| Title | Name of the service (required) |
| Username | Login username |
| Email | Account email address |
| URL | Website URL |
| Password | Account password |
| Notes | Any extra information |

### Crypto Wallets (additional fields)
| Field | Description |
|---|---|
| Wallet Address | Public address (0x…, bc1…, etc.) |
| Seed Phrase | 12 or 24-word mnemonic recovery phrase |
| Private Key | Raw private key in hex or WIF format |
| Network / Chain | Ethereum, Bitcoin, Solana, BNB, etc. |

---

## 💾 Backup & Import

### Export Encrypted Backup
Exports the raw encrypted vault blob as a `.json` file. Safe to store anywhere — it cannot be read without your master password.

```
vaultx_backup_2025-01-01.json
```

### Export Plain JSON
Exports all entries in plain readable JSON. Use only for migrating to another manager. **Keep this file secure.**

### Import
Supports importing both encrypted backups and plain JSON exports. Duplicate entries (matched by ID) are skipped automatically — merging is safe to run multiple times.

---

## 🛠️ Tech Stack

- Pure **HTML + CSS + JavaScript** — no frameworks, no build tools
- **Web Crypto API** — native browser encryption
- **Google Fonts** — Syne, JetBrains Mono, Instrument Sans
- **localStorage** — encrypted vault persistence

---

## 📋 Keyboard Shortcuts

| Key | Action |
|---|---|
| `Escape` | Close any open modal |
| `Enter` | Submit login / setup form |

---

## 🗂️ File Structure

```
vaultx.html     ← The entire app (single file)
README.md       ← This file
```

---

## ⚠️ Disclaimer

VaultX is a personal-use password manager. While it uses industry-standard encryption, it has not undergone a formal third-party security audit. For high-stakes use, consider auditing the source code or using a professionally audited solution alongside it.

---

## 📜 License

MIT — free to use, modify, and distribute.
