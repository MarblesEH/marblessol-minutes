# MarblesSol Minutes

A lightweight, dependency-free meeting minutes app. Create meetings, enter categorized points, and record an assignee and due date. All fields save automatically in the **current browser's localStorage**.

## Deploy to Cloudflare Pages

1. In Cloudflare dashboard open **Workers & Pages → Create application → Pages → Connect to Git**.
2. Authorize GitHub and select `MarblesEH/marblessol-minutes` (grant repository access in the GitHub app if needed).
3. Set the production branch to `main`, framework preset to **None**, leave build command empty, and set build output directory to `/` (repository root).
4. Deploy, check the `*.pages.dev` URL, then add the custom domain `minutes.marblessol.com` in the Pages project's **Custom domains** settings.
5. Configure **Cloudflare Access** for the app before using it for confidential meetings. The current repository is public, so code is public but browser meeting contents are not committed to GitHub.

## Data safety

This is *not cloud synchronization*. Each browser and website origin has separate local data. Moving from a downloaded HTML file to a Cloudflare-hosted site does not transfer meetings. Use **Export backup** from the old app and **Import backup** in the hosted app to move data. Do not assume Cloudflare Access encrypts or backs up localStorage. Clearing browser storage may delete meeting contents. Back up regularly.
