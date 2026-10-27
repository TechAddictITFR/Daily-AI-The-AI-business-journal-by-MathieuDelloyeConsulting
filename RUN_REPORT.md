# Run report 27-10-2026
- template: daily-ai-journal_26-10-2026.html
- articles: 3, news: 3
- short post: 623 chars, long post: 2234 chars
- warnings: ['long post 2234 chars (target 2400-2700)']
- errors: none

## Human check (2 min): open SPOT_CHECK.md and compare the 3 figures with their source

## Files
- RUN_REPORT.md
- SPOT_CHECK.md
- daily-ai-journal_27-10-2026.html
- daily-ai-journal_27-10-2026.json
- index.html
- linkedin-drafts_27-10-2026.md

## After review (you push)
```
git checkout main && git pull && git checkout -b daily-ai-27-10-2026
cp /Users/techaddict/.hermes/skills/hermes-daily-ai/daily-ai-editor/work/27-10-2026/../out/27-10-2026/* .   # copy the files to the repo root
git add . && git commit -m "Daily AI — edition 27-10-2026"
git push -u origin daily-ai-27-10-2026
```