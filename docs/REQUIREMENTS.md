# Sarita POS — Functional Requirements

## Purpose

Sarita POS supports a simple and consistent sales workflow for a small retail kiosk. The public demo reproduces the main checkout experience with sample data while remaining completely separated from the production environment.

## Actors

- **Sales user:** creates and confirms a sale in the production system.
- **Owner:** reviews business information through the private administrative environment.
- **Demo visitor:** explores the public workflow without accessing or changing production data.

## Public demo scope

| ID | Requirement | Acceptance criteria |
|---|---|---|
| FR-01 | Load the demo product catalog. | The available categories appear after the page loads. |
| FR-02 | Filter products by category. | Selecting a category displays only its related products. |
| FR-03 | Require a flavor when the selected category uses flavors. | A product that requires a flavor cannot be added until one is selected. |
| FR-04 | Build and edit an order. | The visitor can add products and increase or decrease each quantity. |
| FR-05 | Display the current order total. | The total remains visible and updates whenever the order changes. |
| FR-06 | Support the available payment methods. | The visitor can select Cash, Card, or Pedidos Ya. |
| FR-07 | Calculate cash change. | For cash payments, the interface calculates the difference between the amount received and the order total. |
| FR-08 | Require a sales user. | The confirmation dialog cannot open until a user is selected. |
| FR-09 | Validate cash payments. | A cash sale cannot continue when the amount received is lower than the order total. |
| FR-10 | Confirm the order before registration. | The interface displays the selected items and payment method before completing the simulated sale. |
| FR-11 | Simulate a sale without writing to production. | Confirming a demo sale shows a success message and clears the current order without calling the production system. |
| FR-12 | Display a local daily summary. | The summary shows transaction count and totals grouped by payment method for the current browser session. |
| FR-13 | Cancel an active order. | The visitor can discard the current order after confirming the cancellation. |

## Business rules

- A sale must contain at least one product.
- A sales user must be selected.
- Products in flavor-based categories require a flavor.
- Cash received must be equal to or greater than the order total.
- Card and Pedidos Ya sales do not require a cash amount.
- The public demo must never register data in production.
- Demo information must use fictional users and sample catalog data.

## Non-functional requirements

| ID | Requirement |
|---|---|
| NFR-01 | The interface must remain usable on a mobile screen. |
| NFR-02 | Validation messages must explain the action required from the user. |
| NFR-03 | The public demo must not expose production URLs, credentials, spreadsheets, or administrative access. |
| NFR-04 | The demo must run without a build step or local installation. |
| NFR-05 | The sales workflow must remain understandable to a first-time visitor. |

## Out of scope for the public demo

- Production authentication and employee access.
- Real sales registration.
- Administrative dashboard access.
- Production spreadsheet access.
- Inventory management.
- Real payment processing.

## Traceability

The requirements above are covered by the manual scenarios in [TEST_CASES.md](TEST_CASES.md). The technical boundaries are documented in [ARCHITECTURE.md](ARCHITECTURE.md).
