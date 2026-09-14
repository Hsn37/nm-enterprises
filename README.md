# NM Enterprises Static Website

A responsive single-page supplier website for nmenterprises.net. Built with HTML, CSS and a small navigation script; no build step or external fonts required.

## Preview locally

Open `index.html` directly, or run:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Then visit http://127.0.0.1:4173.

## Image licensing and contact details

1. **Replace the two denim stock previews with licensed downloads.** The exact sources and license status are recorded in [assets/SOURCES.md](assets/SOURCES.md). No stock images have been purchased. The laser-machine and cutwork photographs are free Pexels stock.
2. The contact details supplied by the owner are `naeem@nmenterprises.net` and `+92 321 3543761` (local format: `03213543761`). All email links use this address, and the phone link uses `tel:+923213543761`.

## Hosting

Repository: https://github.com/Hsn37/nm-enterprises

GitHub Pages publishes the root of the `main` branch. `.nojekyll` serves these files directly, with no site generator. Push changes to `main` to deploy updates.

Custom domain: `nmenterprises.net`. See [DEPLOYMENT.md](DEPLOYMENT.md) for the DNS configuration and verification steps.

## Design

Restrained navy, white and light grey; readable type; straightforward service descriptions; garment-focused photography; direct email enquiries. Mobile navigation supports keyboard dismissal, closes after navigation and remains available when JavaScript is disabled.
