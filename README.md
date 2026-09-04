# CHANGE-ME

One sentence about what this does. Second sentence about who it is for.

Part of [Lakeview Labs](https://lakeview-labs.caseymhudetz.workers.dev).

## Starting a new app from this template
1. On github.com open `caseyhudetz/lab-template`, choose **Use this template**, then **Create a new repository**. Name it, make it public.
2. In the Cloudflare dashboard: **Workers & Pages**, **Create**, **Import an existing Git repository**, pick the new repo, **Deploy**. That connects Workers Builds so every later push deploys itself. You only do this once per app.
3. Open the new repo at [claude.ai/code](https://claude.ai/code) and run `/new-app`. It asks what you are building and handles the rest.
4. Add the finished app to the index page in the `lakeview-labs` repo.

The address follows the repo name. A repo called `ward-44-trash` lands at `ward-44-trash.caseymhudetz.workers.dev`.

## How it works
Single standalone `public/index.html`, no backend. Deployed to Cloudflare Workers as static assets. Every push to `main` deploys automatically.
