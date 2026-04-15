# 🍦 Sarita POS — Point of Sale System

A lightweight, mobile-first point of sale (POS) web application built for **Kiosco Sarita**, a small ice cream retail kiosk in El Salvador. Designed to run entirely on a smartphone with no installation required.

**Live app:** [c-sorto.github.io/sarita-pos](https://c-sorto.github.io/sarita-pos)

---

## 📋 Overview

Kiosco Sarita needed a simple, reliable way to register sales, track inventory, and visualize daily metrics — without expensive POS hardware or complex software. This system replaces manual paper tracking with a real-time digital solution built on free tools.

**The result:** A fully functional POS app that works offline, syncs automatically, and feeds data into a live business dashboard.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, JavaScript (Vanilla) |
| Hosting | GitHub Pages |
| Backend / API | Google Apps Script (doGet) |
| Database | Google Sheets |
| Dashboard | Looker Studio |
| Communication | JSONP (CORS-safe) |

---

## ✨ Features

- **Dynamic product catalog** — loads products and prices from Google Sheets in real time
- **Category-based navigation** — quick selection across 8 product categories
- **Sale registration** — records product, quantity, price, payment method, and cashier
- **Change calculator** — real-time change calculation with quick bill buttons ($1, $5, $10, $20, $50)
- **Offline mode** — saves sales locally when there's no internet connection
- **Auto-sync** — automatically sends pending sales when connectivity is restored
- **Daily summary** — shows total sales, transaction count, and breakdown by payment method
- **PWA support** — installable on Android as a home screen app
- **Confirmation modal** — shows order summary before registering each sale

---

## 🗂️ Data Architecture

All business data lives in Google Sheets with the following structure:

| Sheet | Purpose |
|-------|---------|
| `RAW_DATA` | All sales records (main data source) |
| `CATALOGO_PRODUCTOS` | Active products with SKU, category, and price |
| `CATALOGO_INSUMOS` | Supplies and costs |
| `INVENTARIO_MAESTRO` | Stock control |
| `TABLA_RECETAS` | Product recipes |
| `VENTAS_CONSOLIDADAS` | Daily sales summary |
| `COSTOS_MARGENES` | Cost and margin analysis |
| `RAW_RECEPCION` | Inventory entries |
| `RAW_MERMAS` | Waste/loss records |

---

## 🚀 How It Works

```
Cashier (mobile app)
       ↓
   GitHub Pages (Frontend)
       ↓ JSONP GET request
   Google Apps Script (API)
       ↓
   Google Sheets (Database)
       ↓
   Looker Studio (Dashboard)
```

1. The app loads the product catalog from Google Sheets via Apps Script
2. The cashier selects products, enters payment, and confirms the sale
3. The sale is sent as a GET request to the Apps Script endpoint
4. Data is written to `RAW_DATA` in Google Sheets
5. Looker Studio reads from the Sheet and updates the dashboard in real time

---

## 📱 Screenshots

<img width="264" height="290" alt="image" src="https://github.com/user-attachments/assets/1d27ce28-4c8c-4457-92d9-c0d7f245b8fb" />
<img width="240" height="297" alt="image" src="https://github.com/user-attachments/assets/86bd6aac-66df-466e-be88-4b6fcab90d6a" />

---

## 🔧 Local Development

No build tools required. Clone the repo and open `index.html` in your browser.

```bash
git clone https://github.com/C-Sorto/sarita-pos.git
cd sarita-pos
# Open index.html in your browser
```

To connect your own Google Sheets backend:
1. Copy the Apps Script code to your own Google Apps Script project
2. Deploy it as a web app (execute as: me, access: anyone)
3. Replace the `SCRIPT_URL` constant in `index.html` with your deployment URL

---

## 📈 Business Impact

- Eliminated manual paper-based sales tracking
- Real-time inventory and revenue visibility for the owner
- Offline-capable — works even with unstable internet
- Zero hardware cost — runs on any smartphone

---

## 👨‍💻 Author

**Christian Sorto** — Systems Engineering Student & Backend Developer in training  
[linkedin.com/in/christian-sorto-cortez](https://linkedin.com/in/christian-sorto-cortez)

---

## 📄 License

This project was built for a specific business use case. Feel free to use it as inspiration for your own POS system.
