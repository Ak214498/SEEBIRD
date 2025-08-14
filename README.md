
SEEBIRDEARN — Static frontend (GitHub Pages ready)
=================================================

What this package contains
- A single-page static frontend (index.html, styles.css, app.js) that implements:
  - Balance, earning records (LocalStorage)
  - Daily check-in (+1 point)
  - Telegram join tasks (2 links)
  - Ads task (4 rotating links, 100 clicks/day)
  - Withdraw form (demo, client-side)
  - Telegram Login Widget integration (frontend only): shows Telegram profile picture and name when user logs in via Telegram

Important notes about Telegram login security
- The Telegram Login Widget returns user data and a `hash` parameter. **You MUST verify this `hash` on a server** using your bot token to ensure the user data wasn't tampered with.
- This static demo accepts the widget data client-side so you can see the profile picture and name. For any production usage (authentication, payouts, referrals), implement server-side verification:
  1. Receive the login data on your server.
  2. Use your bot token to compute the HMAC-SHA256 as per Telegram docs and compare with the `hash`.
  3. Create/issue a secure session token for the user.

How to deploy to GitHub Pages
1. Create a new GitHub repository (e.g., `seebirdearn`).
2. Upload the three files (index.html, styles.css, app.js) to the repo root.
3. In the repo settings -> Pages, choose the main branch root as source and save.
4. Your site will be published at `https://<your-username>.github.io/<repo-name>/`

How to set the Telegram bot username (important)
- Open `index.html` and replace `__BOT_USERNAME__` (in the script tag) with your bot's username (without @).
  Example: data-telegram-login="MySeebirdBot"
- Make sure your bot is configured and its domain is allowed in bot settings for the Login Widget.

Files included:
- index.html
- styles.css
- app.js
- README (this file)

Generated on: 2025-08-14T01:52:28.935746 UTC
