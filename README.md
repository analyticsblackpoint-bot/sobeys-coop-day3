# Day 4 class site (GitHub Pages)

One static folder: `index.html` (the landing page), `prompt-lab.html`, `dashboard.html` (Dashboard · Assistant · AGI vote; the vote saves in the browser of the computer that runs it, so run it on the projector laptop), `snack-bar-assistant.html`, `skills/`, `pack/Day4_students_2026-11-06.zip`. No build step, no accounts, nothing is sent anywhere.

## Put it on GitHub Pages (about 5 minutes)

1. On github.com: **New repository** → name `day4` → Public → Create repository.
2. **Add file → Upload files** → drag the *contents* of this folder (not the folder itself: `index.html` must sit at the top) → Commit changes. The zip is 5 MB; GitHub accepts it.
3. **Settings → Pages** → Build and deployment: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. Wait about a minute, refresh the Pages settings: the link is `https://<your-username>.github.io/day4/`.
5. Open the link on your phone: landing page, Prompt Lab, the zip downloads, the vote page opens on the AGI vote tab.
6. Write that one link on the board. Students need nothing else.

To change a page later: edit it in `_build\day4\site\`, upload again (replace), commit. The vote tally lives in the browser you use on the day; press Reset on the vote tab before class.
