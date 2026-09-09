# How to publish this profile

GitHub shows the `README.md` from a repo **named exactly like your username** on your
profile page. So:

## 1. Create the special repo on GitHub

- Repo name: **`us-urvin`** (must match your username exactly)
- Visibility: **Public**
- Do **not** add a README/licence/gitignore (this folder already has everything)

## 2. Push this folder

```bash
cd /var/www/html/us-urvin
git add .
git commit -m "Add animated profile README"
git remote add origin git@github.com:us-urvin/us-urvin.git   # or the https URL
git push -u origin main
```

Open `https://github.com/us-urvin` — the README renders on your profile.

## 3. Turn on the contribution snake 🐍

The README points at `snake.svg` / `snake-dark.svg` on an `output` branch that
doesn't exist yet, so those images 404 until the action runs once:

1. On GitHub go to the repo's **Actions** tab → enable workflows if prompted.
2. Open **"Generate contribution snake"** → **Run workflow** on `main`.
3. It creates the `output` branch with the SVGs. After that it self-updates every 6h.

## 4. Things you may want to edit in `README.md`

| Where | What to check |
| --- | --- |
| `$urvin['currently']` | Employer line — I inferred **ViitorCloud Technologies** from public data. Fix if wrong. |
| `$urvin` array | Motto, focus, "off the clock" — make them yours. |
| Projects table | **RR Group** and **DevNest** have no links (from urvin.space). Add repo/demo links if they're public. |
| Typing SVG `lines=` | The rotating headline sentences. |
| Theme | Every card uses `tokyonight` / purple-pink gradients. Swap `theme=` and the `color=` hex values to re-skin. |

## 5. Pin your best repos

Profile page → **"Customize your pins"** → pick `laravel-host-manager` (and any
others). Pins sit right under the README.
