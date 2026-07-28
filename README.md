# Sarita POS

Sarita POS is a sales system created for an ice cream kiosk. The private production version is used every day and continues to evolve around the needs of the owner and sales staff.

**[Open the public demo](https://c-sorto.github.io/sarita-pos/)**

> The public version uses sample data and a fictional user. It does not store sales in production or provide access to real business information.

## The problem

The kiosk needed a simple way to register sales from a phone, reduce mistakes during checkout, and review daily results without introducing a complex or expensive system.

Sarita POS turns that process into a short and consistent workflow: select products, prepare the order, choose the payment method, calculate change, validate the information, and confirm the sale.

## Main features

- Product catalog organized by category.
- Product, flavor, and quantity selection.
- Order editing and cancellation.
- Cash, card, and Pedidos Ya payment methods.
- Automatic change calculation.
- Checkout validations and confirmation.
- Daily sales summary by payment method.
- Mobile-friendly interface.
- Separate demo and production environments.

## My role and ownership

I guide the functional development and continuous improvement of Sarita POS:

- Gather requirements from the owner and sales staff.
- Translate daily operations into clear workflows and business rules.
- Define validations and expected behavior for each stage of a sale.
- Organize the catalog and the information required by the system.
- Test complete user journeys and edge cases.
- Validate changes with real users before daily operation.
- Identify defects, document findings, and follow improvements.
- Support the live system and maintain its operational continuity.
- Manage documentation and version control with Git and GitHub.

Sarita POS demonstrates my ability to take ownership of a real operational problem, turn it into a working system, and improve it responsibly through testing and user feedback.

## Technology

Sarita POS was built with:

- HTML5.
- CSS3.
- Vanilla JavaScript.
- Google Apps Script for backend services.
- Google Sheets for operational data storage.
- JSONP for communication between the web interface and Apps Script.
- Browser `localStorage` for demo data and local state.
- Git and GitHub for version control.
- GitHub Pages for the public demo.
- Vercel for the private production frontend.

## Demo architecture

```text
Visitor
  |
  v
Web interface on GitHub Pages
  |
  +--> Demo product catalog
  |
  +--> Simulated sale and local daily summary

Production: separate private repository, data, and access controls
```

Simulated sales remain in the visitor's browser. The public demo does not include the production spreadsheet, administrative dashboard, or employee application.

## Screenshots

<img width="424" height="518" alt="Product selection in Sarita POS" src="https://github.com/user-attachments/assets/9354f71b-2f39-41e7-ad8d-181d5ed537b3" />
<img width="429" height="395" alt="Checkout workflow in Sarita POS" src="https://github.com/user-attachments/assets/dfd8db58-3163-4bd2-9509-22eced1123a1" />

## Run locally

No build tools are required.

```bash
git clone https://github.com/C-Sorto/sarita-pos.git
cd sarita-pos
```

Then open `index.html` in a browser.

## Roadmap

- Document complete test cases.
- Add a visual walkthrough of the sales flow.
- Improve accessibility and validation messages.
- Track enhancements and defects through GitHub Issues.

## Author

**Christian Sorto**

Systems Engineering student

[LinkedIn](https://www.linkedin.com/in/christian-sorto-cortez/)
