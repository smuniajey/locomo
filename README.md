# EV Buggy Subscription App

A modern, mobile-responsive web app for EV Buggy campus transport subscription — built as a single `index.html` with no build step required.

---

## 🚀 Run in VS Code

### Option 1 — Live Server (recommended)

1. **Install VS Code** — [download](https://code.visualstudio.com/)
2. **Open the project folder** in VS Code (`File → Open Folder`)
3. VS Code will prompt: *"Do you want to install the recommended extensions?"* — click **Install**
   - This installs **Live Server** by Ritwick Dey
4. Right-click `index.html` in the Explorer panel → **"Open with Live Server"**
5. The app opens at **http://127.0.0.1:5501/index.html**

### Option 2 — Open directly in browser

Double-click `index.html` on your computer — it opens straight in your default browser.
> ⚠️ Google login (Firebase) won't work from a `file://` URL; use Live Server for full functionality.

### Option 3 — VS Code Launch Config (F5)

1. Install the **Debugger for Chrome** extension
2. Press `F5` → select **"Open index.html in Chrome"**

---

## ⚙️ Configuration

Before going live, edit these three values at the top of the `<script>` block in `index.html`:

| Constant | Where to get it |
|---|---|
| `FIREBASE_CONFIG` | [Firebase Console](https://console.firebase.google.com/) → Project Settings → Your apps |
| `RAZORPAY_KEY_ID` | [Razorpay Dashboard](https://dashboard.razorpay.com/) → Settings → API Keys |
| `ADMIN_PASSWORD` | Change `admin@123` to a secure password |

The app runs in **demo mode** when these are not configured — all flows work with simulated data stored in `localStorage`.

---

## 📱 Pages

| Page | Description |
|---|---|
| **Landing** | Hero, About, Pricing, Safety, Contact |
| **Login** | Google sign-in via Firebase |
| **Registration** | Name · Phone · Apartment · Block |
| **Subscription** | Choose plan: 1mo / 3mo / 6mo (3% off) / 12mo (5% off) |
| **Payment** | Razorpay checkout |
| **Success** | Confirmation + subscription details |
| **Admin** | `/index.html#admin` — password-protected user list |

---

## 🛠️ Tech Stack

- **Tailwind CSS** (CDN) — utility-first styling
- **Firebase** (Auth + Firestore) — Google login & data persistence
- **Razorpay** — payment gateway
- **Vanilla JS** — no framework, no build step
