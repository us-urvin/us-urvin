# Profile repo — status & maintenance

✅ **Published** to https://github.com/us-urvin — the `README.md` renders on your
GitHub profile page automatically (repo name matches your username).

## What's automated

`.github/workflows/snake.yml` runs every 6 hours (and on demand from the
**Actions** tab). It generates the contribution-snake animation and pushes the
SVGs to the `output` branch. Nothing else needs maintenance — every other image
in the README is a live badge from a public service (shields.io, skillicons.dev,
readme-typing-svg, capsule-render, komarev, quotes-github-readme).

## One thing left for you to do manually

**Pin your repos**: profile page → *"Customize your pins"* → pick
`laravel-host-manager`. (GitHub has no API for this.)

## Things you may still want to personalize in `README.md`

| Where | What |
| --- | --- |
| `$urvin` array | Motto / focus / "off the clock" — make them yours. |
| Projects table | **RR Group** and **DevNest** have no links. Add repo/demo URLs if public. |
| Typing SVG `lines=` | The rotating headline sentences. |
| Theme | Everything uses `tokyonight` + purple→pink. Change `theme=` / `color=` hex to reskin. |

## Re-run the automation after editing

```bash
cd /var/www/html/us-urvin
git add . && git commit -m "Update profile" && git push
```

Push triggers the snake workflow; or run it from the repo's **Actions** tab →
*Generate contribution snake* → **Run workflow**.
