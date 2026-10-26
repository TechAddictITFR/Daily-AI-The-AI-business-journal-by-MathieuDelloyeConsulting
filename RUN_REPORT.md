# Run report 26-10-2026
- template: daily-ai-journal_23-10-2026.html
- articles: 3, news: 3
- short post: 408 chars, long post: 1699 chars
- warnings: ['long post 1699 chars (target 2400-2700)', 'short post 408 chars (target ~700)']
- errors: none

## Human check (2 min): open SPOT_CHECK.md and compare the 3 figures with their source

## Files
- daily-ai-journal_26-10-2026.html
- daily-ai-journal_26-10-2026.json
- index.html
- linkedin-drafts_26-10-2026.md

## After review (you push)
```
git checkout main && git pull && git checkout -b daily-ai-26-10-2026
cp /Users/techaddict/.hermes/skills/hermes-daily-ai/daily-ai-editor/work/26-10-2026/../out/26-10-2026/* .   # copy the files to the repo root
git add . && git commit -m "Daily AI — edition 26-10-2026"
git push -u origin daily-ai-26-10-2026
```