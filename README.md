[README.md](https://github.com/user-attachments/files/33644676/README.md)
# Cetacea Circular — The Circular Economy Mega-Cycle (microsite)

Static, single-page data room. No build step, no dependencies beyond the Chart.js CDN.

## Publish to GitHub Pages (2 minutes)

1. Create a new GitHub repository, e.g. `cetacea-megacycle`.
2. Upload `index.html` (drag-and-drop via **Add file → Upload files** works fine).
3. **Settings → Pages → Source: Deploy from a branch → Branch: main, /(root) → Save.**
4. Site is live at `https://<your-username>.github.io/cetacea-megacycle/`.

## Registration gate — wire up lead capture

The gate works out of the box (stores registrations in the visitor's browser via localStorage).
To **receive leads by email**, do this once:

1. Create a free form at [formspree.io](https://formspree.io) (name/company/email fields).
2. Copy your form ID into `index.html` — search for `YOUR_FORM_ID` and replace.
3. Done. Every registration posts to your Formspree inbox AND stays in localStorage.

Alternatives: swap the fetch URL for a Google Apps Script webhook, Basin, or your CRM endpoint.

## Collecting leads you already captured

If you demoed the site in-person and collected registrations on a shared machine,
open the browser console on the site and run:
    copy(localStorage.getItem('cc_registrations'))
— that pastes the JSON lead list to your clipboard.

## Content sources
Demand/EoL base case: Cetacea forecast SOP (Oct 2026), validated against IEA NZE,
Arcane Capital and Circular Energy Storage. Prices: Oct 2026 market (Cu US$14,500/t,
Li2CO3 ~US$17.5k/t). Plant economics: 50 ktpa module, US$2,000/tpa capex benchmark.

## Gated download
A 'Download the speaker notes' button sits in the Insights section. It stays disabled until the visitor registers, then serves a print-ready A4 HTML notes file (Blob download, no server needed).
