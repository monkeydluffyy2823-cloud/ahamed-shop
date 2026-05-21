# 🚀 Deploy AHAMED Shop to the Internet (FREE)

Follow these steps to get a **live public web domain** for your shop in ~5 minutes. No credit card needed.

You will get a domain like: **`https://ahamed-shop.onrender.com`**

---

## ✅ What You Need (all free)
1. A **GitHub** account → https://github.com/signup
2. A **Render** account → https://render.com (sign up with GitHub — 1 click)
3. *(Optional)* A **Gmail App Password** for email notifications

---

## 📋 Step-by-Step Guide

### **STEP 1 — Put your code on GitHub**

#### Option A: Use the GitHub website (easiest, no commands)
1. Go to https://github.com/new
2. Repository name: `ahamed-shop`
3. Set as **Public** → click **Create repository**
4. On the next page, click **"uploading an existing file"**
5. Drag and drop these files from your `ahamed-shop` folder:
   - `index.html`
   - `server.js`
   - `package.json`
   - `package-lock.json`
   - `render.yaml`
   - `.gitignore`
   - `README.md`
   - `DEPLOY.md`
   - ⚠️ **DO NOT upload** `node_modules/` or `orders.json`
6. Click **Commit changes**

#### Option B: Using Git commands (if you know git)
```bash
cd ahamed-shop
git init
git add .
git commit -m "Initial AHAMED Shop"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/ahamed-shop.git
git push -u origin main
```

---

### **STEP 2 — Deploy to Render**

1. Go to https://dashboard.render.com
2. Click **"New +"** → **"Web Service"**
3. Click **"Connect GitHub"** → authorize Render
4. Find your **`ahamed-shop`** repo → click **Connect**
5. Render will auto-fill from `render.yaml`. Just verify:
   - **Name:** `ahamed-shop` (or any name — this becomes your domain!)
   - **Runtime:** Node
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`
   - **Plan:** Free
6. Click **"Create Web Service"** at the bottom

⏳ Wait 2–3 minutes for the first deploy…

🎉 **You're LIVE!** Your shop is now at:
```
https://ahamed-shop.onrender.com
```
(or whatever name you chose)

Admin dashboard: `https://ahamed-shop.onrender.com/admin`

---

### **STEP 3 (Optional) — Enable Email Notifications**

If you want order emails sent to **monkeydluffy2823@gmail.com**:

#### 3a. Get a Gmail App Password
1. Go to https://myaccount.google.com/security
2. Enable **2-Step Verification** (required by Google)
3. Go to https://myaccount.google.com/apppasswords
4. App name: `AHAMED Shop` → click **Create**
5. **Copy the 16-character password** (looks like: `abcd efgh ijkl mnop`)

#### 3b. Add it to Render
1. In Render Dashboard → click your `ahamed-shop` service
2. Left sidebar → **Environment**
3. Click **"Add Environment Variable"**:
   - Key: `GMAIL_PASS`
   - Value: paste your 16-char password (remove spaces)
4. Click **Save Changes** — Render will auto-redeploy

Now every order will email you the full invoice! 📧

---

## 🌐 Want a Custom Domain (like `ahamedshop.com`)?

Render supports free custom domains:
1. Buy a domain from **Namecheap** (~₹700/year) or **GoDaddy**
2. In Render → your service → **Settings** → **Custom Domain**
3. Add your domain → Render gives you DNS records
4. Paste those in your domain registrar's DNS settings
5. Done! HTTPS is free & automatic

---

## ⚠️ Important Notes about Render Free Tier

| Limitation | What it means |
|---|---|
| 💤 **Sleeps after 15 min idle** | First request after sleep takes ~30 sec to wake up. Subsequent requests are instant. |
| 🔄 **750 hours/month free** | Plenty for a normal shop |
| 💾 **Orders stored in file** | Orders.json resets on redeploy. For permanent storage, upgrade later to use a database (free tier available too) |

For a small shop this is **perfectly fine**.

---

## 🆘 Troubleshooting

**Site shows "Application failed to respond"**
→ Check Render logs (Dashboard → your service → Logs). Usually a missing dependency.

**Email not sending**
→ Make sure `GMAIL_PASS` is set in Environment and you used an **App Password**, not your regular Gmail password.

**Orders not saving after redeploy**
→ This is normal on free tier (filesystem is ephemeral). Need a database for permanence — ask me and I'll upgrade the code to use Render's free PostgreSQL.

---

## 🎯 Quick Summary

| Step | Time | Result |
|------|------|--------|
| 1. Upload to GitHub | 2 min | Code online |
| 2. Connect to Render | 3 min | **🌐 LIVE WEBSITE** |
| 3. Add Gmail password | 2 min | 📧 Email working |

**Total: ~7 minutes to a live shop on the internet!** 🚀
