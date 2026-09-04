---
description: Turn this fresh copy of the template into a real Lakeview Labs app
---

Walk Casey through turning this fresh copy of the template into a real app. Casey is usually on a phone, so ask one short question at a time and keep replies brief.

## 1. Work out what the app is

Ask what the app should do and who it is for. Skip the question if that was already described in the message that triggered this command.

Ask follow ups only where the answer changes what gets built:
- What data does it need, and is that data on the Chicago Data Portal?
- Is there one number or one view that matters more than the rest?

If the app needs an API key or any other secret, stop and say so before writing code. No keys in the HTML.

## 2. Set the repo identity

- Read this repo's name from `git remote get-url origin`. Lowercase it and turn anything that is not a letter, number or hyphen into a hyphen, because Worker names allow nothing else. Set `name` in `wrangler.jsonc` to that.
- If the result differs from the repo name, say so plainly. The address follows the Worker name, not the repo name, and renaming the repo on github.com is the tidier fix if Cloudflare is not connected yet.
- Replace the `<title>`, meta description, `<h1>` and lede in `public/index.html`.
- Rewrite the top of `README.md`: the heading becomes the app name, followed by two sentences on what it does and who it is for. Leave the rest of the README as it is.

## 3. Build it

Follow `CLAUDE.md`. Everything inline in `public/index.html`, no build step and no packages. Lay it out for a 390px phone screen before anything else. Pick a palette and typeface that suit this particular app.

## 4. Ship it

- Commit with a clear message and push to `main`. Workers Builds deploys it. Never run `wrangler deploy`.
- Give Casey the live address: the Worker name followed by `.caseymhudetz.workers.dev`. Say that the first build takes a minute or two.
- Offer to draft the entry for the index page in the `lakeview-labs` repo.
