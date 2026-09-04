# House rules for Lakeview Labs projects

This repo was created from caseyhudetz/lab-template. Follow these rules for every change.

## Shape of the project
- One standalone file: `public/index.html`. All CSS and JS inline. No build step, no framework, no npm packages, no bundler.
- No Worker script and no `main` entry in `wrangler.jsonc`. Cloudflare serves `public/` as static assets. Only add a Worker script if the app truly needs a server (secrets, cron, writes).
- No secrets in the HTML. If a key is needed, stop and say so before writing any code.
- Deploys happen automatically on push to `main` via Cloudflare Workers Builds. Never run `wrangler deploy` manually.

## First task on a fresh repo
1. Set `name` in `wrangler.jsonc` to the repo name.
2. Replace the placeholder title, description and content in `public/index.html`.
3. Update `README.md` with a two sentence description of what the app does.
4. Remind Casey to add the new app to the Lakeview Labs index page (lakeview-labs repo).

## Data
- Chicago open data comes from the Chicago Data Portal (Socrata SODA API). Filter to East Lakeview / Ward 44 where relevant. Call it directly from the browser and cache in `localStorage` where it helps.
- Handle empty results and fetch failures with a plain sentence that says what happened and what to do.

## Design
- Mobile first. Casey often opens these on a phone. Test the layout at 390px wide before anything else.
- Pick a palette and typeface that fit the subject of this specific app. Avoid the generic defaults: cream background with serif headline and terracotta accent, near-black with one neon accent, identical rounded cards with soft grey shadows, all-caps eyebrow labels, arrows appended to button text.
- One memorable element, everything else quiet.
- Respect `prefers-reduced-motion`. Visible focus states. Real contrast.

## Writing
- Plain, conversational, sentence case. No em dashes. No Oxford comma.
- Buttons say what they do. Errors say what went wrong and how to fix it.
- Empty states invite an action.

## Workflow
- Small commits with a clear message. Push to `main` when the change is ready to ship.
- Do not create extra files unless the app genuinely needs them. One HTML file is the goal.
