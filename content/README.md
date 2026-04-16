# Content Source Documents

Drop any documents here that Claude should use to populate and update the CV pages.

## What to put here

- Work experience descriptions (current or past roles)
- Project portfolios or case studies
- Client-facing bio or profile documents from your employer
- Notes about recent work, skills, or accomplishments
- Any loosely structured text about your professional background

## Formats accepted

Any plain text format: `.md`, `.txt`, `.html`. No special structure required — Claude will parse them and extract relevant information.

## How to trigger a refresh

After dropping documents here, open Claude Code in this repo and run:

```
/refresh-site
```

Claude will read everything in this directory, search for new public information (new articles at thenatureofcities.com, etc.), and regenerate all CV pages.
