# DinoStream Website

A static, informational website for DinoStream (Home, Privacy Policy, Terms,
Support, DinoReward, Premium), built for the sole purpose of satisfying
Google Auth Platform's branding requirements. Plain HTML/CSS/JS — no build
step, no backend, no database.

## Files

```
index.html       Homepage
privacy.html      Privacy Policy
terms.html        Terms of Service
support.html      Support
dinoreward.html    DinoReward info
premium.html       Premium (Coming Soon)
styles.css         Shared styling
nav.js             Mobile nav toggle
```

## Deploy for free with GitHub Pages (recommended, ₹0)

1. Create a **new GitHub repository** (public), e.g. named `dinostream-website`.
2. Upload all files in this folder to the root of that repository
   (`index.html`, `privacy.html`, etc. — not inside a subfolder).
3. In the repository, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`.
5. Set **Branch** to `main` (or `master`) and folder to `/ (root)`. Click **Save**.
6. Wait 1–2 minutes. GitHub will show your live URL, in the form:
   ```
   https://<your-github-username>.github.io/dinostream-website/
   ```
7. Visit that URL to confirm the site loads over HTTPS.

No domain purchase is required — `github.io` subdomains are provided free and
already use HTTPS.

### Alternative: Cloudflare Pages (also free)
1. Push this folder to a GitHub repo (same as above, steps 1–2).
2. In Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**.
3. Select the repo. Framework preset: **None**. Build command: *(leave blank)*.
   Output directory: `/`.
4. Deploy. Cloudflare gives you a URL like `https://dinostream-website.pages.dev`.

### Alternative: Vercel (also free)
1. Push this folder to a GitHub repo.
2. In Vercel dashboard → **Add New → Project → Import** the repo.
3. Framework preset: **Other**. Leave build command blank, output directory `.`.
4. Deploy. Vercel gives you a URL like `https://dinostream-website.vercel.app`.

Pick **one** of the three — GitHub Pages is simplest since it needs no
external account beyond GitHub itself.

## Exact URLs to enter into Google Auth Platform

Once deployed (using GitHub Pages as the example — substitute your actual
username/project name and the option you chose):

| Field                  | URL                                                              |
|-------------------------|-------------------------------------------------------------------|
| Application home page  | `https://<username>.github.io/dinostream-website/`               |
| Privacy policy link    | `https://<username>.github.io/dinostream-website/privacy.html`   |
| Terms of service link  | `https://<username>.github.io/dinostream-website/terms.html`     |
| Support (informational) | `https://<username>.github.io/dinostream-website/support.html`  |

## About "Authorized domains" in Google Auth Platform

Google Auth Platform's **Authorized domains** field on the Branding page
generally accepts `github.io`, `pages.dev`, and `vercel.app` as valid
registrable domains — these are on the public suffix list, so Google treats
`<username>.github.io` (etc.) as a domain you can use, similar to how it
treats `.web.app` or `.firebaseapp.com`.

That said: **this has not been verified against your specific project in the
Google Auth Platform console yet.** Google occasionally tightens verification
requirements (e.g., requiring Search Console domain ownership verification
for some domain types). Steps to actually confirm:

1. Deploy the site (above).
2. Go to Google Cloud Console → **APIs & Services → OAuth consent screen /
   Auth Platform → Branding**.
3. Enter the homepage, privacy, and terms URLs from the table above.
4. Try to save. If Google accepts it without asking for domain verification,
   you're done at ₹0.
5. If Google asks you to **verify domain ownership via Google Search
   Console**, that's still free (no purchase needed) — Search Console
   supports verifying a `github.io`/`pages.dev`/`vercel.app` URL-prefix
   property without owning the whole domain.
6. Only if Google explicitly rejects the free subdomain outright (rare, and
   not the common case) would a custom domain become necessary — don't buy
   one unless you hit that wall.

## Notes

- No secrets, API keys, or tokens are present anywhere in this site.
- No claims are made about DinoReward reward values or Premium pricing —
  both are explicitly marked "Coming Soon" / unfinalized per your instructions.
- This site does not touch, import, or depend on your Android app source code.
