# Setup Guide — Activating Every Animated Element

This README uses several third-party widgets that need to live in the right place to work.
Follow these steps once and everything will render automatically after that.

## 1. Create your profile repository (if you haven't already)

GitHub only turns a README into your profile page if the repo is:
- **Public**
- **Named exactly the same as your username** → `Baadal891310`

If that repo doesn't exist yet, create it at github.com/new.

## 2. Add the files from this zip

Unzip this package and copy everything into that repo, keeping the folder structure:

```
Baadal891310/
├── README.md
├── SETUP.md
└── .github/
    └── workflows/
        └── snake.yml
```

The `.github/workflows/snake.yml` path matters — GitHub only picks up Actions from that exact location.

## 3. Push it

```bash
git add .
git commit -m "Add premium animated README"
git push
```

## 4. Turn on the snake animation

1. Go to your repo → **Actions** tab.
2. You should see "Generate Snake Animation" listed. Click it, then **Run workflow** to trigger it manually the first time (it also runs automatically once a day after that).
3. Wait ~30–60 seconds for it to finish. It will create (or update) an `output` branch containing the generated SVGs.
4. Refresh your profile page — the snake animation in the README will now render, since it points at:
   `https://raw.githubusercontent.com/Baadal891310/Baadal891310/output/github-contribution-grid-snake-dark.svg`

If it still doesn't show up, double check:
- The repo is public
- Actions are enabled for the repo (Settings → Actions → General → allow all actions)
- The workflow run finished with a green checkmark, not a red X

## 5. Fill in your personal links

In `README.md`, replace these placeholders:
- `YOUR_LINKEDIN_LINK` → your LinkedIn profile URL
- `YOUR_EMAIL_HERE` → your email address
- `YOUR_FACEBOOK_LINK` → your Facebook profile URL (or delete that badge if you don't want it)

## 6. Rename the pinned project repos

The "Featured Projects" section pulls live data from repos named:
- `Smart-Meal-Management-System`
- `Student-Management-System`
- `DSA-Practice`
- `Portfolio`

Each card only renders once a public repo with that exact name exists on your account. Either create/rename repos to match, or edit the `repo=` values in the README to point at your real repo names.

## 7. (Optional) Live Spotify widget

The README includes a commented-out placeholder for a live "Now Playing" Spotify badge, using
[kittinan/spotify-github-profile](https://github.com/kittinan/spotify-github-profile). This requires
connecting your Spotify account via that project's OAuth flow — it's optional, so skip it if you don't
want to set that up, or come back to it later.

---

Everything else (stats card, streak stats, trophies, activity graph, typing animation, progress bars,
capsule banners) works immediately with no setup — they're all generated live from public GitHub data
using your username, so they'll just work as soon as the README is on your profile.
