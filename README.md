# Date question for Lina 💛

A little one-page site that asks Lina on a date. She can't click "No"
(it grows the Yes button instead), then she picks the date, the activity, and the food — and
the final screen lets her send the whole plan straight to your WhatsApp,
or copy it. It also invites her to follow you on Instagram.

## Before you deploy — 2 things to do

1. **Add the photo.** Drop the picture into the `images/` folder and
   name it exactly `lina.jpg` (if it's missing, the photo frame is hidden).

2. **Add your WhatsApp number.** Open `script.js` and edit the first line:
   ```js
   const MY_WHATSAPP = "27000000000";
   ```
   Use full international format, digits only (no `+`, spaces or `0` at the
   start). South African `082 123 4567` → `27821234567`.

## Test it locally first

From this folder:
```bash
python -m http.server 8080
```
Then open http://localhost:8080 and click through it.

## Deploy on Coolify

1. Push this folder to a Git repo (GitHub/GitLab) **or** zip it — Coolify
   supports both.
2. In Coolify: **+ New → Application**, pick your repo.
3. Set **Build Pack = Dockerfile** (the included `Dockerfile` serves the
   site with nginx on port **80**).
4. Add a domain, deploy, and send Lina the link. Done.

> The plan is also auto-saved in her browser (localStorage) as a backup,
> but the WhatsApp / copy button is how it gets to you.
