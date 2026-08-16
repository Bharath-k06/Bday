# Niveditha's Birthday Celebration Web Project ✨

A production-ready, zero-cost, zero-credential birthday website featuring AES-256 client-side encrypted assets, 3D envelope animation, canvas image shielding, real-time Discord visitor telemetry, and an in-app guest pass generator.

---

## 📁 Project Structure

```text
bday-project/
├── index.html       # Public website (3D envelope, AES-256 decryptor, Canvas protection, Discord alerts)
├── encryptor.html   # Private offline encryption tool (runs locally in your browser)
├── vault.json       # Generated encrypted data file (downloaded from encryptor.html)
└── README.md        # Setup & deployment instructions
```

---

## 🚀 Quick Setup & Deployment Guide

### Step 1: Encrypt Your Photos & Letter Offline
1. Double-click `encryptor.html` to open it in your browser.
2. Set your **Master Passphrase** (e.g. `niveditha_love_2026`).
3. Select your photos from your laptop.
4. Customize your personal birthday letter text.
5. Click **"🔒 Encrypt & Create vault.json File"**.
6. Click **"📥 Download vault.json"** and place the `vault.json` file inside your `bday-project/` folder next to `index.html`.

*(No manual copy-pasting of long ciphertext strings is needed—`index.html` automatically loads `vault.json`!)*

---

### Step 2: Configure Webhook in `index.html`
1. Open `index.html` in VS Code or your text editor.
2. In the `<script>` section near line 450:
   - Paste your Discord Webhook URL into `DISCORD_WEBHOOK_URL`.
   - Ensure `MASTER_KEY_DEFAULT` matches the passphrase you entered in `encryptor.html`.
3. Save the file.

---

### Step 3: Test Locally on Kali WSL / Windows
In your Kali terminal:
```bash
cd bday-project
python3 -m http.server 8000
```
Open your browser to:
- **Locked Test**: `http://localhost:8000` (Verifies uninvited visitors see the locked gatekeeper).
- **VIP Unlock Test**: `http://localhost:8000/?key=niveditha_love_2026` (Unlocks full experience, decrypts photos in RAM, and triggers Discord alert).

---

### Step 4: Free 1-Click Deployment (Netlify Drop)
1. Go to [Netlify Drop](https://app.netlify.com/drop).
2. Drag and drop the `bday-project` folder containing `index.html` and `vault.json`.
3. Netlify will provide your live HTTPS URL (e.g. `https://special-delivery-niveditha.netlify.app`).

---

### 💌 Sending the Magic Link
Send Niveditha her personal VIP link:
```text
https://your-site-name.netlify.app/?key=niveditha_love_2026
```
