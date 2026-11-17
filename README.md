# MAKE MY TOUR — GitHub Pages starter

A responsive, multi-page static travel website built with HTML, CSS and vanilla JavaScript. It uses JSON files for tour and editorial content and is designed to deploy on GitHub Pages.

## Included
- Homepage with destination discovery, categories, sample packages and editorial cards
- Tour listing with search, category filtering and price sorting
- Reusable tour detail page driven by `assets/tours.json`
- Travel journal and article template driven by `assets/articles.json`
- About and contact/enquiry pages
- Responsive mobile navigation and GitHub Actions deployment workflow

## Run locally
Because the site loads JSON with `fetch`, run it through a local web server (not by opening the HTML file directly).

```bash
python -m http.server 8000
```
Open http://localhost:8000.

## Deploy to GitHub Pages
1. Create a GitHub repository named `make-my-tour` (or change the Vite-free static workflow paths if you choose a different publishing method).
2. Upload the contents of this folder to the repository root.
3. In GitHub, open **Settings → Pages** and set the source to **GitHub Actions**.
4. Push to the `main` branch. The workflow publishes the site automatically.
5. Your site URL will be shown under Settings → Pages.

The workflow copies this static site into the Pages artifact. No build step or package manager is required.

## Add or edit tour packages
Edit `assets/tours.json`. Each tour needs a unique `id`, `title`, `destination`, `type`, `duration`, numeric `price`, `departure`, `image`, `description`, `route`, and `itinerary` array. The price and itinerary values currently included are illustrative demo content and must be verified/replaced before publication.

## Add or edit travel articles
Edit `assets/articles.json`. Each article needs a unique `id`, `category`, `title`, `excerpt`, `author`, `date`, `reading`, `image`, and `body` array. Article copy is sample editorial content and should be fact-checked and edited before publication.

## Enquiry form — important
The contact form is deliberately in demo mode. It validates fields in the browser but **does not send or store personal information**. Before accepting real enquiries, connect it to a trusted form provider or your own secure backend. Configure spam protection, privacy notice, retention and access controls. Never put private API keys or passwords in this public repository.

## Production checklist
- Replace demo package prices, departures, itineraries and imagery with licensed, accurate material.
- Add genuine customer reviews only with permission and supporting records.
- Supply verified business address, phone, email, legal entity details and policies.
- Configure a working enquiry endpoint and test delivery.
- Add a domain-specific canonical URL, sitemap URLs, robots rules, Open Graph image and structured data after the final domain is known.
- Add privacy, terms, cancellation and refund policies reviewed for your business.
- Check all links, accessibility and performance on real devices before launch.

## Architecture limitation
GitHub Pages is static hosting. It does not provide a database, secure admin login, server-side authentication, booking engine or payment processing. For a secure admin dashboard and live booking/payment features, use a separate backend or a Git-based CMS with proper authentication and a server-side integration.
