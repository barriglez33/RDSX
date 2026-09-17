# Red Sox News

GitHub-online-only RSS monitor for Boston Red Sox coverage.

Tracks 59 names from the supplied Red Sox list.

Features:
- multilingual discovery using GDELT + Google News
- Red Sox/MLB context filtering to reduce false positives
- automatic Spanish translation before RSS generation
- source included in every RSS title, e.g. `[ESPN] Roman Anthony...`
- smart duplicate detection across publishers/languages
- only the most complete repeated version is kept
- alternate repeated sources are preserved in `alternate_sources`
- master RSS plus individual RSS feeds per person
- GitHub Actions runs every hour at minute `:33`

Workflow:
`.github/workflows/update.yml`

Run manually:
**Actions → Update Red Sox News RSS → Run workflow**

Generated:
- `docs/feed.xml`
- `docs/people/*.xml`
- `docs/index.html`
- `data/articles.json`

For public GitHub Pages:
**Settings → Pages → Deploy from branch → main → /docs**
