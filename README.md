# Red Sox News — High Recall Update

This patch changes discovery to **scan broadly, process narrowly**.

- Google News RSS entries inspected per search: **25**
- Fresh unseen Google articles processed per search: **max 6 total**
- GDELT results requested per search: **15**
- Fresh unseen GDELT articles processed per search: **max 6**
- Rolling window: **3 hours**
- Duplicate comparison window: **24 hours**
- Title similarity: **0.80**
- Token overlap: **0.68**
- Body-lead similarity: **0.75**

The existing batch rotation is preserved.

Replace `main.py`, `config.json`, and `README.md`.
Do not replace your existing `data/articles.json`, `data/state.json`, or `docs/`.
