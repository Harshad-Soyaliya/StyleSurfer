<!-- Banner -->
<p align="center">
  <img src="https://img.shields.io/badge/StyleSurfer-Eco%20Fashion%20Rental-8d6748?style=for-the-badge&logo=python&logoColor=white" alt="StyleSurfer Banner"/>
</p>

<h1 align="center">StyleSurfer</h1>

<p align="center">
  <b>Bringing affordable & sustainable fashion to everyone</b><br/>
  Rent, buy, resell & customize premium outfits with an eco-friendly approach.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Backend-Python%20%7C%20Django-8d6748?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS%20%7C%20Bootstrap%20%7C%20JS-b08968?style=flat-square&logo=bootstrap&logoColor=white"/>
  <img src="https://img.shields.io/badge/Database-SQLite3-8d6748?style=flat-square&logo=sqlite&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Academic%20Project%202024--25-b08968?style=flat-square"/>
</p>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Core Features](#-core-features)
  - [Customer Experience](#customer-experience)
  - [Seller Experience](#seller-experience)
  - [Delivery Partner Experience](#delivery-partner-experience)
  - [Admin Panel](#admin-panel)
- [Architecture & Diagrams](#-architecture--diagrams)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Project](#running-the-project)
- [Key User Flows](#-key-user-flows)
- [Security, Safety & Quality](#-security-safety--quality)
- [Results & Outcomes](#-results--outcomes)
- [Roadmap & Future Plans](#-roadmap--future-plans)
- [Contributing](#-contributing)
- [Authors](#-authors)
- [Acknowledgements](#-acknowledgements)
- [License / Usage](#-license--usage)

---

## 🌍 Overview

**StyleSurfer** is a fashion rental web platform that enables users to rent, buy, resell and customize premium outfits instead of purchasing them outright. It focuses on **affordability**, **sustainability**, and a **real e-commerce experience** through role-based portals for customers, sellers, delivery partners, and admins.

By reusing garments and offering options like reselling and buy-back, StyleSurfer promotes **circular fashion**, helping reduce textile waste while making designer and occasion-wear more accessible. :contentReference[oaicite:0]{index=0}

---

## ✨ Core Features

### Customer Experience

- 🛒 **Smart Product Browsing & Filters**
  - Browse outfits by **category, brand, size, color and price**.
  - Detailed product pages with images, description, rent price, deposit and rental duration.

- 🧺 **Cart & Rental Management**
  - Add outfits to cart and configure:
    - Rental period
    - Delivery date
    - Size and color (if applicable)
  - See rent breakdown: rent, security deposit, shipping, discounts, final total.

- 🎰 **Spin-to-Win Rewards**
  - Monthly spins to earn **coins**.
  - Redeem coins for **discount vouchers** on a dedicated voucher page.

- 🔁 **Reselling Section**
  - Explore **pre-rented outfits at discounted prices**.
  - Category-wise reselling pages for Men and Women.

- 🔄 **Buy-Back Option**
  - Request **customized outfits** (e.g., embroidery, stone work, alterations).
  - Use the outfit and optionally **return it within a fixed period (e.g., 20 days)** for a guaranteed buy-back amount.

- 🧾 **Orders, Reviews & Help**
  - Order history with status tracking.
  - Rate and review products after rental.
  - Help Center for FAQs and support requests.

---

### Seller Experience

- 📊 **Seller Dashboard**
  - Overview of:
    - Total rental products
    - Total resell products
    - Orders
    - Pending payments

- 🧵 **Product Management**
  - Add, edit, and manage:
    - Rental products
    - Resell products
  - Control price, rental price, stock, sizes, colors, images and categories.

- 💸 **Resell & Inventory Optimization**
  - Convert outfits that have been rented multiple times into **resell products** at discounted prices.

- 💼 **Buy-Back Management**
  - View & act on customer **buy-back customization requests**.
  - Approve / reject requests and manage related listings.

---

### Delivery Partner Experience

- 🚚 **Delivery Partner Dashboard**
  - View assigned orders with:
    - Customer details
    - Delivery address
    - Pickup/return schedules

- 📦 **Order Lifecycle Management**
  - Update status:
    - Assigned → Picked up → Out for Delivery → Delivered
    - Return pickup → Returned
  - Track completed deliveries and earnings.

---

### Admin Panel

- 🛂 **User & Role Management**
  - Manage **customers, sellers and delivery partners**.
  - Approve, verify or suspend accounts.

- 🧾 **Order, Payment & Dispute Management**
  - Monitor rentals, resell orders and payments.
  - Handle refunds, penalties and disputes (e.g., damage, late return).

- 🧩 **Content & Configuration**
  - Manage FAQs, rules & regulations, penalties and system-wide settings.

---

## 🧠 Architecture & Diagrams

All diagrams are stored in the [`diagrams/`](diagrams/) directory:

- **Use Case Diagram** – overall interaction of Customers, Sellers, DPs & Admins.  
- **ER Diagram** – database schema including Customer, Seller, Product, Resell_Product, Cart, Order, SpinToWin, Voucher, BuyBack and more.
- **Activity Diagrams** – for each role:
  - `activity_customer.png`
  - `activity_seller.png`
  - `activity_dp.png`
  - `activity_admin.png`
- **Sequence Diagrams** – request/response flows for major operations.
- **DFD (Level 0, 1, 2)** – data movement between entities and processes.
- **Flowchart Diagrams** – end-to-end flows for each role.
- **Class Diagram** – Django model/class relationships.

> 🔗 Update the filenames above to match your actual diagram file names if they differ.

---

## 🛠 Tech Stack

**Backend**

- Python
- Django (MVT architecture)
- SQLite3 (RDBMS)

**Frontend**

- HTML5
- CSS3
- Bootstrap
- JavaScript (with small helper libraries where needed)

**Infrastructure & Integrations**

- SMTP for:
  - Email OTP verification
  - Account and order notifications
- Stripe (or similar gateway) for secure online payments
- HTTP/HTTPS based communication

---

## 📁 Project Structure

> Example structure assuming you have `code/`, `documentation/`, and `diagrams/` folders. Adjust if your names differ.

```bash
StyleSurfer/
├── code/                      # Django project & apps
│   ├── manage.py
│   ├── stylesurfer/           # Project settings, URLs, WSGI
│   └── apps/                  # Core apps: accounts, products, orders, spin, etc.
│
├── diagrams/                  # All UML, DFD, flowchart, class & architecture diagrams
│   ├── usecase.png
│   ├── er_diagram.png
│   ├── dfd_level0.png
│   └── ...
│
├── documentation/             # PDFs, SRS, user manual, presentations
│   ├── StyleSurfer_Project_Report.pdf
│   └── User_Manual.pdf
│
├── README.md
└── requirements.txt
