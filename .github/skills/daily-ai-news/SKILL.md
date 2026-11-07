---
name: daily-ai-news
description: "Research, draft, update, and validate the Daily AI Breaking News edition and its LinkedIn copy and image. Use for daily or special-edition AI news deliverables, article research, HTML edition updates, or LinkedIn drafts."
argument-hint: "Edition date and news period, e.g. 2026-11-04"
user-invocable: true
---

# Daily AI News

Produce a sourced Daily AI Breaking News edition and its companion LinkedIn draft and publication image. Preserve the existing site and publication workflow; never publish or push without the user's explicit instruction.

## Workflow

1. **Establish the edition and scope.** Use the date supplied by the user or today's date. Confirm the news period when it is ambiguous; use the user's requested start and end dates exactly. Identify the existing HTML edition, LinkedIn draft template, and image assets before editing. Check `git status` and do not overwrite or include unrelated worktree changes.
2. **Research before drafting.** Aim to find ten significant AI-related stories from the requested period. Prefer original announcements, research institutions, regulators, and primary documents; use established journalism for independent reporting and subjects without a useful primary source. For each candidate, record its publication date, headline, publisher, canonical URL, factual summary, and relevance. Verify the article and date from its source page or clearly disclose when date verification relies on a secondary index. Never pad the list with older, duplicate, or unverified articles; if fewer than ten qualify, report the verified count and ask whether to proceed with fewer or wait.
3. **Request editorial approval.** Present the verified candidates in French for the user's review, with source links and concise summaries. Do not edit the edition contents or prepare publication copy until the user validates the selection and count. Incorporate requested substitutions and seek approval for a revised list as needed.
4. **Update the HTML after approval.** Replace the old stories with the approved stories while preserving the page's structure and rendering contract. Keep localized data consistent across all existing languages. Preserve CSS, fonts, themes, buttons, and JavaScript behavior. If an anomaly is discovered in these areas, explain the impact and get explicit permission before changing it. Keep facts, analysis, uncertainty, and hypotheses distinct; do not present unverified claims as fact.
5. **Prepare the LinkedIn draft and image.** Write both short and long post versions in English unless instructed otherwise. The preferred opening, when requested, is exactly: `Good Evening Network, here are the news from Daily AI Breaking news special edition from the week.` Include a source-list first comment and a link to the edition. Create a separate LinkedIn image (1200x630 PNG) that reflects the approved edition. Never overwrite `og-image.png` or a user-supplied image without explicit approval. Link the generated image from the draft.
6. **Validate.** Parse the embedded edition JSON; verify ten unique approved stories, dates and source URLs; check each language's story counts and required render fields; preview each language in a browser; check the image dimensions and draft opening; and run `git diff --check`. Report inaccessible sources or unverified publication dates transparently.
7. **Deliver and stop.** Summarize the HTML, LinkedIn draft, image, and validation status. Do not stage, commit, push, publish, or deploy unless the user explicitly asks. If asked to push, stage only the deliverables for this edition, check the staged diff, commit with the repository's required co-author trailer, push the current branch, and verify the resulting commit and clean state for those files.

## Repository conventions

- Edition HTML: follow the repository's existing filename pattern, such as `daily-ai-journal_YYYY-MM-DD.html`.
- LinkedIn copy: `linkedin-drafts_DD-MM-YYYY.md`.
- LinkedIn publication image: `linkedin-image_DD-MM-YYYY.png`.
- Match the established page data model and localization pattern; inspect the current edition rather than assuming an older schema.
- Avoid unrelated edits, including changes to the index page, site styling, analytics, or other editions.
