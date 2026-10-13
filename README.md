# Marryatt Accounting

One-page client guide for https://marryatt.ca, using HTML and CSS. No dependencies, installation, or build required.

## Before launch

Contact links include email, WhatsApp, and Instagram. Payments direct clients to the link on their QuickBooks invoice or Interac e-Transfer to `ar@marryatt.ca`. QuickBooks options depend on what is enabled on the invoice. Review the descriptions and payment instructions before publishing.

Document submission, booking links, and checklists can be added as new sections when available. No inactive resource buttons are shown.

## Deploy through Cloudflare Pages

In Cloudflare, open Workers & Pages, create a Pages project, and import the GitHub repository `mike0000000001/marryatt-accounting`.

| Setting | Value |
| --- | --- |
| Production branch | `main` |
| Framework preset | None |
| Build command | `exit 0` |
| Build output directory | `public` |
| Root directory | Leave blank |

Save and deploy. Open the supplied `pages.dev` address to check the page. Future pushes to the production branch deploy automatically.

Then open the Pages project's Custom domains settings and add `marryatt.ca`. Follow Cloudflare's domain instructions. Add `www.marryatt.ca` separately if wanted. Preserve the existing Microsoft 365 MX, TXT, and email CNAME records. Only adjust website-related DNS records as instructed. Review any existing website A/AAAA records for conflicts.

Official guides:
- https://developers.cloudflare.com/pages/framework-guides/deploy-anything/
- https://developers.cloudflare.com/pages/configuration/custom-domains/

## Edit

- `public/index.html`: page text, contact details, navigation, metadata.
- `public/styles.css`: colours, layout, and mobile styles.
- `public/assets/`: supplied logo and favicon variants, copied unchanged.

The logo has generous white margins; CSS displays the relevant area without changing the original image. Dark assets are retained for later use. No contact form, analytics, external fonts, or cookies are included in the source.
