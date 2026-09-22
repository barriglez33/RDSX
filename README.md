# Red Sox News

GitHub-online-only RSS monitor for Boston Red Sox coverage.

## Timeout-safe batching

The 59 tracked names are split into two alternating batches:

- Batch 1: 30 names
- Batch 2: 29 names

The workflow runs hourly and alternates batches after each successful run.

Rotation state is stored in:

`data/state.json`

## Rolling 2-hour window

Each run only considers stories from the previous 2 hours.

Google News dates are checked before redirect decoding and article extraction, which avoids spending time on old results.

## Features

- GDELT + Google News multilingual discovery
- Red Sox / Boston / MLB context filtering
- automatic translation
- source shown in each RSS title
- smart duplicate detection
- keeps the most complete version of duplicate coverage
- master RSS + individual feeds in `docs/people/`
- newly accepted stories translated first
- only 10 older incomplete translations retried per run

## Workflow

`.github/workflows/update.yml`

Runs every hour at minute `:33`.

## Generated files

- `docs/feed.xml`
- `docs/people/*.xml`
- `docs/index.html`
- `data/articles.json`
- `data/state.json`
