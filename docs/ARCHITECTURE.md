# Sarita POS — Architecture Overview

## Scope

This document describes the public demo and its boundary with the private production environment. It intentionally excludes credentials, private URLs, spreadsheet identifiers, employee information, and administrative implementation details.

## Public demo

```text
Visitor's browser
      |
      v
GitHub Pages
HTML + CSS + Vanilla JavaScript
      |
      +---- JSONP read request ----> Demo Apps Script
      |                                  |
      |                                  v
      |                           Sample catalog data
      |
      +---- Simulated sale ------> Browser localStorage
                                         |
                                         v
                                  Local daily summary
```

## Production boundary

```text
Sales users ---> Private production frontend ---> Protected Apps Script services
                                                     |
                                                     v
                                              Private Google Sheet

Owner --------> Private administrative dashboard
```

The public repository does not contain the production service URL. Production source code, data, access roles, and administrative functions remain separate and private.

## Components

### Web interface

- Built with HTML5, CSS3, and Vanilla JavaScript.
- Presents the catalog, order controls, payment selection, validations, confirmation dialog, and daily summary.
- Runs without a build tool or framework.

### Demo catalog service

- Uses Google Apps Script.
- Returns sample categories, products, prices, and flavors through JSONP.
- Does not provide production records or administrative data.

### Local demo state

- Uses browser `localStorage`.
- Keeps simulated daily sales in the visitor's browser.
- Supports the demo summary without registering real transactions.

### Versioning and deployment

- Git and GitHub provide version control.
- GitHub Pages publishes the public demo.
- The production frontend is deployed separately through Vercel.

## Main demo data flow

1. The browser loads the static interface from GitHub Pages.
2. The interface requests the sample catalog from the demo Apps Script endpoint.
3. The visitor creates an order and selects a payment method.
4. Client-side rules validate the order, selected user, flavor, and cash amount.
5. The confirmation dialog summarizes the transaction.
6. Demo mode stores the simulated sale locally and clears the active order.
7. The daily summary calculates totals from the browser's local demo data.

## Key design decisions

- **Separate environments:** public demonstration and daily production operation cannot share endpoints or data.
- **Mobile-first workflow:** the interface prioritizes quick use from a phone.
- **Low operational complexity:** the demo requires only a browser and static hosting.
- **Explicit confirmation:** a sale is reviewed before it is completed.
- **Local simulation:** recruiters can test the workflow without creating business records.

## Current limitations

- The public frontend is contained in a single HTML file.
- Automated tests are not yet configured.
- The demo summary belongs only to the current browser.
- Accessibility and keyboard navigation require further review.

These limitations are suitable candidates for the project's public roadmap and GitHub Issues.
