# Contributing

Thanks for helping keep this list current! AI × fusion research moves fast, and community additions are very welcome.

## Adding an entry

1. Pick the section that best fits (see the [Table of Contents](README.md#-table-of-contents)). If it spans two sections, add the full entry to the primary section and a short "See [Section](#anchor)" cross-reference to the other.
2. Use this format for a paper:

   ```markdown
   - **[Title](url)** — Author et al., Institution · *Venue* · Year. One or two sentence description of what it does and why it's notable.
   ```

3. For a dataset, tool, or framework, add a row to the relevant table, matching its existing columns.
4. Sort entries within a section newest-first by year.

## Requirements for a PR to be merged

- **Link works.** Please check the URL resolves before submitting (paywalled or bot-blocked-but-otherwise-real links, e.g. some publisher sites, are fine — just note it in the PR if you weren't able to check with `curl`).
- **Real citation.** Include the actual arXiv ID / DOI / URL — no placeholders (`xxxxx`) or guessed identifiers.
- **On-topic.** The item should sit at the intersection of AI/ML and nuclear fusion (magnetic or inertial confinement) — not general plasma physics or general ML with no fusion connection.
- **One sentence on why it's notable**, not just a restatement of the title.

## Reporting a broken link or outdated entry

Open an issue, or submit a PR that fixes the link/description directly. Please include what you checked and (if you found one) the corrected URL.
