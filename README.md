# Detail Haus — Website Hosting & Setup Guide

Welcome, Reece. This guide walks you through getting your new website live, start to finish. No coding required — everything happens in your web browser, all on accounts you'll own and control.

**Total time:** 60–90 minutes the first time through. You can pause between stages — each one ends with a checkpoint.

**What you'll need:**
- A GitHub account (you'll create this in Stage 1)
- Your GoDaddy login
- A working email — recommend **DetailHaus.or@gmail.com** for everything
- Your phone (2FA codes)

**If you get stuck:** Ryan can help with code-related issues (bugs in the site itself). For account, billing, or setup questions on the services below, refer to each service's support docs.

---

## How this works

You'll be standing up the website yourself across five free services. Every account is created in your name and email, so you own all of it — no shared logins, no monthly fees, no dependencies on anyone else.

| # | Service | What it does | Cost |
|---|---|---|---|
| 1 | GitHub | Stores the website's code (private repo) | Free |
| 2 | Vercel | Hosts the live website | Free (Hobby) |
| 3 | Formspark | Receives contact form submissions | Free (250 submissions/month) |
| 4 | UploadThing | Stores customer vehicle photos | Free tier |
| 5 | GoDaddy | Points your domain at the new site | Already paid |

The order matters — each stage builds on the one before it. Don't skip ahead.

> 💡 Use **DetailHaus.or@gmail.com** for all four new accounts so everything lands in one inbox.

---

## Stage 1 — Create a GitHub account & accept the repo transfer

GitHub stores your website's code. You won't ever need to read or edit it — but Vercel (next stage) needs to pull the code from somewhere, and GitHub is that somewhere. Ryan already has the code in his GitHub account and will transfer the repository to yours.

### Step A — Sign up for GitHub

1. Go to **https://github.com**
2. Click **Sign up** in the top-right corner.
3. Enter **DetailHaus.or@gmail.com**. Click **Continue**.
4. Create a password (at least 15 chars, OR 8+ chars with a number and lowercase letter). Click **Continue**.
5. Choose a username. Something like `detail-haus` or `reece-detailhaus` works.
   - ⚠️ Usernames are public and permanent. Don't use anything you wouldn't want a customer to see.
6. Answer the email-updates question. Click **Continue**.
7. Complete the puzzle/CAPTCHA.
8. GitHub will email a launch code. Open Gmail, find the email from GitHub, copy the code, paste it into GitHub.
9. Setup questions — **Just me**, pick any features, any role.
10. When asked to choose a plan, select **Continue for free**.
11. You'll land on the GitHub dashboard.

### Step B — Send Ryan your GitHub username

1. Your username is shown in the top-right corner of github.com when you're logged in. Click your profile icon → username is at the top of the dropdown.
2. Send it to Ryan along with confirming your account email is **DetailHaus.or@gmail.com**. He needs both to transfer the repository.

### Step C — Accept the repository transfer

Once Ryan initiates the transfer, GitHub will email you.

1. Check **DetailHaus.or@gmail.com** for an email from **GitHub** titled something like *"A repository has been transferred to you"* or *"@ryan would like to transfer a repository to you"*.
2. Click the **Accept this transfer** button in the email (or the link to GitHub).
3. GitHub may ask you to confirm by typing the repository name. Type it exactly as shown and click **I understand, transfer this repository**.
4. The repository now appears under your GitHub account at `github.com/<your-username>/detail-haus-website`.
5. Click into the repository to confirm you see files like `app/`, `components/`, `public/`, `package.json`, `next.config.js`, etc.
   - ⚠️ The repository is private — only you (and anyone you explicitly invite) can see it. Don't change it to public.

✅ **Checkpoint:** You can see the Detail Haus repository under your GitHub account, with all the code files inside it.

---

## Stage 2 — Create a Vercel account & deploy the site

Vercel hosts your website on the internet. Free for your usage.

### Step A — Sign up

1. Go to **https://vercel.com**
2. Click **Sign Up** in the top-right.
3. Click **Continue with GitHub**.
4. Log into GitHub if prompted (use the account from Stage 1).
5. On the **Authorize Vercel** screen, scroll down and click **Authorize Vercel**.
6. Setup questions:
   - **What's your name?** → Your name.
   - **For what purpose will you use Vercel?** → **Personal**.
   - Team name → `detail-haus` or your own name (internal label only).
7. You'll land on the Vercel dashboard.

### Step B — Import your repository

1. Click **Add New...** (top-right) → **Project**.
2. Find `detail-haus-website` in the **Import Git Repository** list.
   - ⚠️ If you don't see it, click **Adjust GitHub App Permissions**. GitHub opens in a new tab — find Vercel, grant it access to the repo, save, return to Vercel.
3. Click **Import**.
4. On the **Configure Project** screen, leave everything at default:
   - **Project Name:** leave as-is or rename to `detail-haus`.
   - **Framework Preset:** should already say **Next.js**. Don't change.
   - **Root Directory:** leave as-is.
   - Ignore **Environment Variables** for now.
5. Click **Deploy**.
6. Vercel builds the site. Takes 2–4 minutes.
   - ⚠️ The first deploy may show warnings about missing environment variables — expected. The site will still go live; the contact form and photo uploads won't work yet.
7. When done, click **Continue to Dashboard**.
8. You'll see a temporary URL like `detail-haus-abc123.vercel.app`. Click it to confirm the site loads.

✅ **Checkpoint:** The site loads at the `.vercel.app` URL and looks correct visually.

---

## Stage 3 — Set up Formspark (contact form)

### Step A — Create your account

1. Go to **https://formspark.io**
2. Click **Sign up**.
3. Use **DetailHaus.or@gmail.com** and create a password.
4. Verify your email if Formspark sends a confirmation.

### Step B — Create the form & grab the Form ID

1. From your dashboard, click **+ New form** (or **Create form**).
2. Name it `Detail Haus Contact Form`. Click **Create**.
3. On the form's page, find the **Form ID** or a code snippet like `https://submit-form.com/XXXXXXXXXX`.
4. **Copy the random string at the end** (the `XXXXXXXXXX` — 10–12 characters). That's your Form ID.
5. Save it somewhere you can find again (notes app, sticky note, doc). You'll need it in Stage 5.
   - ⚠️ Copy ONLY the ID, not the full URL.

### Step C — Set the notification email

1. On the same form's page, find **Settings** or **Notifications**.
2. Confirm **DetailHaus.or@gmail.com** is the notification email.

✅ **Checkpoint:** You have a Formspark Form ID saved, and notification emails point at your Gmail.

---

## Stage 4 — Set up UploadThing (photo uploads)

### Step A — Create your account

1. Go to **https://uploadthing.com**
2. Click **Sign in** or **Get Started**.
3. Click **Continue with GitHub** — use the same account from Stage 1.
4. Authorize UploadThing.

### Step B — Create the app

1. From the dashboard, click **Create a new app** (or **+ New App**).
2. Name it `detail-haus`. Click **Create App**.

### Step C — Grab your token

1. Inside the app, find **API Keys** in the left sidebar (or **Keys** / **Settings → API Keys**).
2. Look for **Token** or **V7 Token** — a long string of characters.
3. Click the **Copy** button.
4. Save it in the same safe place as your Formspark Form ID.
   - ⚠️ **The UploadThing token IS sensitive — treat it like a password.** Don't share publicly, post on social media, or email anywhere insecure.

✅ **Checkpoint:** You have both the UploadThing token AND the Formspark Form ID saved.

---

## Stage 5 — Plug the IDs into Vercel & redeploy

### Step A — Add the environment variables

1. Go to **https://vercel.com** and open your project dashboard.
2. Click **Settings** → **Environment Variables** (left sidebar).
3. Add the **first variable**:
   - **Key:** `NEXT_PUBLIC_FORMSPARK_FORM_ID`
   - **Value:** paste your Formspark Form ID.
   - **Environments:** check **Production**, **Preview**, AND **Development**.
   - Click **Save**.
4. Add the **second variable**:
   - **Key:** `UPLOADTHING_TOKEN`
   - **Value:** paste your UploadThing token.
   - **Environments:** all three checked.
   - Click **Save**.
   - ⚠️ Type the keys EXACTLY as shown — capitalization and underscores matter. Easiest is to copy-paste from this guide.

### Step B — Redeploy

1. Click **Deployments** at the top.
2. Find the most recent deployment. Click the **⋯** (three dots) → **Redeploy**.
3. Leave **Use existing Build Cache** UNchecked. Click **Redeploy**.
4. Wait 2–4 minutes (green checkmark when done).

✅ **Checkpoint:** Both env variables show in Vercel settings, and a fresh deployment finished successfully.

---

## Stage 6 — Connect your GoDaddy domain

### Step A — Add the domain in Vercel

1. In Vercel: **Settings** → **Domains**.
2. In the **Add Domain** box, type `detail-haus.com` (no `https://`, no `www`). Click **Add**.
3. Choose the option to add `detail-haus.com` and redirect `www.detail-haus.com` to it.
4. Vercel will show DNS records:

| Type | Name | Value |
|---|---|---|
| A | `@` | an IP (something like `76.76.21.21`) |
| CNAME | `www` | `cname.vercel-dns.com` |

   - ⚠️ **Leave this Vercel page open.** Write down the exact values — don't use the example IP above.

### Step B — Add the records at GoDaddy

1. Go to **https://godaddy.com**. Log in.
2. Profile icon → **My Products**.
3. Find `detail-haus.com` → click **DNS** (or **Manage DNS**).
4. You'll see a table of DNS records.
   - ⚠️ **Don't delete MX, TXT, or any records you don't recognize.** Those are for email. Only touch A and CNAME records below.
5. Find existing **A record** with Name `@`:
   - Edit it: change **Value** to Vercel's IP, save.
   - If none exists: **Add New Record** → Type `A` → Name `@` → Value = Vercel's IP → save.
6. Find existing **CNAME record** with Name `www`:
   - Edit it: Name `www`, Value `cname.vercel-dns.com.`
   - If none exists, add it as a new CNAME.
7. Save all changes.
   - ⚠️ GoDaddy may say "up to 48 hours." In practice, 5–30 minutes.

### Step C — Wait and verify

1. Go back to Vercel. Refresh.
2. Domain will show **Invalid Configuration** or **Pending** at first — normal.
3. Wait 10–15 minutes, refresh. Should change to **Valid Configuration** (green checkmark).
   - ⚠️ If after an hour still **Invalid Configuration**, double-check the A record and CNAME values at GoDaddy match EXACTLY what Vercel showed.
4. Once green, open a new tab → type `https://detail-haus.com`. Site should load.
   - ⚠️ If you see a security warning, wait another 5–10 minutes for SSL to provision.

✅ **Checkpoint:** `detail-haus.com` loads with a 🔒 lock icon.

---

## Stage 7 — Final verification

1. Open `https://detail-haus.com` on your phone AND a computer.
2. Click through every section.

### Test the contact form

1. Scroll to contact section.
2. Fill it out with your own info and a test message.
3. Attach a photo (any photo).
4. Click **Submit**.
5. Should see a success message.
6. Within a minute or two, check **DetailHaus.or@gmail.com** — new email from Formspark with form contents and photo link.
   - ⚠️ If no email arrives: check Gmail **Spam** folder. If there, mark **Not Spam**.
   - ⚠️ If nowhere: open Formspark → form settings → confirm notification email is `DetailHaus.or@gmail.com`.

### Test the photo upload

1. Log into UploadThing.
2. Open your `detail-haus` app → **Files**.
3. Your test photo should be there.
   - ⚠️ If not, the `UPLOADTHING_TOKEN` may be wrong in Vercel. Re-check it, redeploy.

✅ **Checkpoint — You're done:** Domain loads, contact form sends emails, photos appear in UploadThing.

---

## What to do going forward

**Form submissions** come to `DetailHaus.or@gmail.com`. Reply directly — the reply-to is auto-set to the customer's email.

**Your dashboards:**

| Service | URL | For |
|---|---|---|
| GitHub | github.com | Code storage. Won't visit often. |
| Vercel | vercel.com/dashboard | Hosting, deploys, domain, env variables. |
| Formspark | formspark.io | Submissions history, form settings. |
| UploadThing | uploadthing.com/dashboard | Photo storage. |
| GoDaddy | godaddy.com | Domain renewal, DNS. |

**Renewals & limits:**
- GoDaddy domain renews annually — keep your card current.
- Formspark free tier: 250 submissions/month.
- UploadThing free tier: storage and bandwidth limits in the dashboard.
- Vercel Hobby tier: plenty for a small business site.

**If the site itself breaks** (broken layout, missing section, button not working): contact Ryan at Fathom. That's a code issue. Have a screenshot ready.

**If contact form / photo upload / domain stops working:** check the relevant service's dashboard first (Formspark, UploadThing, GoDaddy/Vercel). Each has its own support docs.

**Future site changes** (new services, pricing updates, photos): contact Ryan. He'll update the code; changes auto-deploy.

---

## 🛠️ Or: skip all of this with the maintenance plan

If reading through the above made your eyes glaze over, the **$150/month maintenance plan** is still on the table. Here's exactly what changes:

> 💡 **Everything above gets handled for you.** Ryan does the GitHub, Vercel, Formspark, UploadThing, and GoDaddy setup. He keeps it running. You never log into a dashboard unless you want to.

### What's included

- **All the setup in this guide, done by Ryan** — zero of the 60–90 minutes above, zero of the friction
- **Ryan covers the paid plans** — Vercel Pro and Formspark Pro (if you ever outgrow the free tier) come out of the $150, not your pocket
- **Monthly content updates** — send new before/after photos, pricing changes, seasonal banners, copy tweaks. Ryan pushes them live. *(This is the one that matters most for a detailing business — your portfolio stays fresh without you doing anything.)*
- **Uptime monitoring** — Ryan gets alerted if the site goes down before you do, and fixes it. You're running a one-person business; you can't be watching your own website at 11pm.
- **Spam filtering on the contact form** — bot protection and junk filtering so only real leads hit your inbox
- **Local SEO maintenance** — keeping your Google Business listing, sitemap, and structured data tuned so customers in your service area actually find you
- **Photo optimization** — every new portfolio shot gets compressed and formatted so the site stays fast on mobile
- **Domain & DNS babysitting** — if GoDaddy ever does something weird, Ryan handles it. You don't touch DNS again.
- **Annual design refresh** — small tune-ups each year so the site doesn't look dated two years from now
- **Backups & disaster recovery** — if something catastrophic happens, Ryan can restore everything

### How the math works out

- $150/month ≈ **one extra Refresh detail per month** covers it
- vs. a few hours of your time every time something breaks or needs updating
- vs. ~$120/year just for the paid tier upgrades if you ever need them

### Cancel anytime

No lock-in. If you decide it's not worth it, just say so and Ryan hands the keys over to you using the guide above.

Just let Ryan know if you want to switch over — he can have everything stood up within a few days and you'd never have to read the rest of this guide.

---

*Setup guide prepared by Fathom (fathom.services) for Detail Haus.*
