# Profile repo — status & maintenance

✅ **Published** to https://github.com/us-urvin — the `README.md` renders on your
GitHub profile page automatically (repo name matches your username).

## What's automated

`.github/workflows/profile.yml` runs every 6 hours (and on demand from the
**Actions** tab) and does two things:

| Job | Output | Shows up as |
| --- | --- | --- |
| `metrics` | commits `github/metrics.svg` to `main` | the big stats panel (activity, languages, habits) |
| `snake`   | pushes SVGs to the `output` branch | the contribution-snake animation |

Everything else in the README is a live badge/image from a public service
(shields.io, skillicons.dev, readme-typing-svg, capsule-render, streak-stats,
komarev, quotes) — nothing to maintain.

> ℹ️ The old `github-readme-stats` / `github-profile-trophy` /
> `github-readme-activity-graph` cards were dropped — those public instances are
> currently offline. `lowlighter/metrics` runs inside your own repo instead, so it
> can't break the same way.

## One thing left for you to do manually

**Pin your repos**: profile page → *"Customize your pins"* → pick
`laravel-host-manager`. (GitHub has no API for this.)

## Things to personalize in `README.md`

| Where | What |
| --- | --- |
| `$urvin['currently']` | Employer line — I put **ViitorCloud Technologies** from public data. Fix if wrong. |
| `$urvin` array | Motto / focus / "off the clock" — make them yours. |
| Projects table | **RR Group** and **DevNest** have no links. Add repo/demo URLs if public. |
| Typing SVG `lines=` | The rotating headline sentences. |
| Theme | Everything uses `tokyonight` + purple→pink. Change `theme=` / `color=` hex to reskin. |

## Re-run the automation after editing

```bash
cd /var/www/html/us-urvin
git add . && git commit -m "Update profile" && git push
```

Push triggers `profile.yml`; or trigger it from the repo's **Actions** tab →
*Build profile assets* → **Run workflow**.
