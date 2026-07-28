# Sarita POS — Manual Test Cases

## Test objective

Validate the public demo's main sales workflow, user feedback, calculations, and separation from production.

## Test environment

- Application: [Sarita POS public demo](https://c-sorto.github.io/sarita-pos/)
- Test type: manual functional testing
- Data: sample catalog and fictional user
- Production writes: disabled

## Test cases

| ID | Scenario | Steps | Expected result |
|---|---|---|---|
| TC-01 | Load the catalog | Open the demo and wait for the catalog to load. | All available categories appear without a connection error. |
| TC-02 | Filter products | Select `Pasteles`. | Only products from the selected category are displayed. |
| TC-03 | Require a flavor | Select `Conos` and try to add `Cono Simple` without choosing a flavor. | The product is not added and the message `Seleccioná un sabor primero` appears. |
| TC-04 | Add a flavored product | Select a flavor and add `Cono Simple`. | The order displays the product, selected flavor, quantity, and total. |
| TC-05 | Update quantity | Use the `+` and `−` controls on an order item. | Quantity and order total update; reducing the quantity below one removes the item. |
| TC-06 | Require a sales user | Add a product and try to register the sale without selecting a user. | The confirmation dialog does not open and the user field is highlighted. |
| TC-07 | Reject insufficient cash | Add a product, select the demo user, and enter less cash than the order total. | The confirmation dialog does not open and the interface reports that the cash amount is lower than the total. |
| TC-08 | Use a non-cash payment | Add a product, select `Tarjeta`, select the demo user, and register the sale. | Cash controls are hidden and the confirmation dialog opens. |
| TC-09 | Confirm a demo sale | Confirm a valid order from the confirmation dialog. | A demo success message appears and the active order is cleared. |
| TC-10 | Review the daily summary | Complete a demo sale and open `Hoy`. | Transaction count and totals by payment method include the completed sale. |
| TC-11 | Cancel an order | Add a product, select `Cancelar`, and approve the browser confirmation. | The order is cleared and its total returns to `$0.00`. |
| TC-12 | Protect production | Review the public source and complete a demo sale. | No production endpoint is present and no real sale is registered. |

## Execution record

| Date | Version | Result | Notes |
|---|---|---|---|
| 2026-07-28 | `3d289dc` | Core flow passed | TC-01 through TC-10 and TC-12 were manually verified. Total visibility and validation-order defects found during testing were corrected and regression-tested. TC-11 remains available for the next full regression cycle. |

## Defect handling

Defects and improvements that remain open are tracked in [GitHub Issues](https://github.com/C-Sorto/sarita-pos/issues). Each future change should be retested against the relevant cases in this document.
