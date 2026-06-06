# 🌾 Fair Trade Agri-Portal

Empowering Farmers with Better Market Rates — A digital platform that connects farmers directly with buyers, promotes fair trade, and enhances agricultural transparency.

---

## 🖼️ Live Preview

Here's a look at the homepage of the Fair Trade Agri-Portal:

<p align="center">
  <img src="images/Home.png.png" alt="Fair Trade Agri-Portal Homepage" width="700"/>
</p>

## 📌 Project Summary

This repository contains an early-stage Fair Trade Agri-Portal project setup. It currently includes only tooling metadata and MySQL database artifacts.

### What is present

- `package.json` and `package-lock.json` for Tailwind CSS tooling
- `tailwind.config.js` for Tailwind CSS content scanning
- `data/` directory with MySQL database files for `admin_database` and `database`

### What is missing

- PHP backend source files
- HTML views for buyer, farmer, and admin panels
- CSS/JS page assets
- route/controller logic and authentication code

> The core application source is not currently included. To fully realize the portal, add application code under a clear project structure such as `src/`, `public/`, or the repository root.

---

## 🚀 Expected Portal Features

The intended portal should ideally support:

- 👨‍🌾 Farmer portal
  - register/login
  - manage products with price, quantity, and description
  - view pending orders and update shipment status
  - mark items as shipped

- 🛒 Buyer portal
  - register/login
  - browse fresh agricultural products
  - add products to cart and place orders
  - view order status and delivery progress

- 📦 Order management
  - display status values such as Pending, Shipped, Delivered
  - update order fulfillment from farmer/admin side
  - show detailed shipping address fields

- ⚙️ Admin dashboard
  - manage users, orders, and products
  - view market insights and sales metrics
  - moderate marketplace activity

- 📊 Market insights
  - track product pricing trends over time
  - display educational content about fair pricing

---

## 📂 Repository Contents

- `package.json` — npm dependency manifest
- `package-lock.json` — exact dependency tree
- `tailwind.config.js` — Tailwind CSS configuration
- `data/` — MySQL database artifacts
  - `admin_database/` — admin-related tables and schema files
  - `database/` — core application tables such as users, products, orders, cart, and profile management

---

## 🛠️ Tech Stack

| Layer | Technology |
|------|------------|
| Styling | Tailwind CSS 4 |
| Tooling | Node.js / npm |
| Database | MySQL |
| Server | Apache / XAMPP |
| Admin UI | phpMyAdmin |

---

## ✅ Installed Dependencies

The current npm dependencies are:

- `tailwindcss` ^4.0.12
- `@tailwindcss/cli` ^4.0.12

There are no npm scripts currently defined in `package.json`.

---

## ⚙️ Local Development Setup

### 1. Install dependencies

```bash
npm install
```

### 2. Build Tailwind CSS

If you choose to add a Tailwind input file, use a command like:

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

Update the `-i` and `-o` paths to match your actual asset folders.

### 3. Run local server

- Copy or link your application files to your XAMPP `htdocs` folder
- Start Apache and MySQL
- Open the application in your browser at `http://localhost/`

### 4. Import database files

The `data/` directory contains MySQL table files, not a SQL dump. To use the database locally:

- If you already have the MySQL data directory imported, place the `admin_database/` and `database/` folders under your MySQL data folder
- Otherwise, export the database from a working MySQL instance and import via phpMyAdmin or MySQL Workbench once you have SQL dumps available

---

## 🔧 Tailwind CSS Details

The `tailwind.config.js` file currently sets:

```js
export default {
  content: ["*"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

This means Tailwind will scan all files in the repository. When you add real templates, restrict the `content` paths to those folders for better performance, for example:

```js
content: ["./src/**/*.{html,php,js}", "./public/**/*.{html,php,js}"]
```

---

## 💡 Recommendations

- Add a `src/` or `public/` directory to host HTML, PHP, CSS, and JS files
- Create a `db.sql` export or a script to rebuild the database schema
- Add npm scripts such as `build`, `watch`, and `dev` once you have assets
- Document any PHP configuration, database credentials, and environment setup

---

## 📌 Suggested Project Structure

A useful structure might be:

```
/ public/
  index.php
  login.php
  buyer-dashboard.php
  farmer-dashboard.php
  admin-dashboard.php
/ src/
  assets/
    css/
    js/
  components/
/ data/
  admin_database/
  database/
/ tailwind.config.js
/ package.json
```

---

## 📚 Notes

- This README is intentionally detailed to help orient future development.
- The current workspace is incomplete and needs source code to function as a full portal.
- Back up your MySQL database files before making local changes.



