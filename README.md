# 📚 ABC Book — Online Bookstore

A full-featured **online bookstore** web application built with **Symfony 7.1**, allowing users to browse books by category, search by author or publisher, add books to a cart, and place orders — with a complete admin panel for back-office management.

---

## 🖥️ Screenshot

![Home Page](public/images/Capture.png)

---

## ✨ Features

### 🛍️ Customer Side
- **Home page** with a hero banner carousel showcasing featured books
- **Browse & Search** — find books by author or publisher via the search bar
- **Categories** — filter the catalogue by book category
- **Book detail pages** — title, cover image, price, number of pages, edition date, publisher, and authors
- **Shopping Cart** — add books, update quantities, and review the cart before checkout
- **Checkout & Orders** — place orders and receive confirmation
- **User Registration & Login** — secure authentication with email verification
- **User Profile** — view and update personal information
- **Contact page** — get in touch with the store
- **About page** — information about the bookstore

### 🔧 Admin Back-Office (EasyAdmin)
- Full CRUD management for **Books** (with cover image upload)
- Full CRUD management for **Authors**, **Publishers**, **Categories**
- **Order management** — view and process customer orders
- **User management** — manage registered accounts
- **PDF export** — generate PDF documents via DomPDF

### 📧 Email & Notifications
- Transactional emails via **Symfony Mailer** with **Google Mailer** integration
- Email verification on registration via **SymfonyCasts Verify Email Bundle**

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Symfony 7.1 |
| Language | PHP 8.2+ |
| ORM | Doctrine ORM 3 + Doctrine Migrations |
| Templating | Twig |
| Admin Panel | EasyAdmin Bundle 4 |
| Frontend | Symfony AssetMapper + Stimulus + Turbo |
| File Uploads | VichUploaderBundle |
| PDF Generation | DomPDF |
| Authentication | Symfony Security Bundle |
| Email | Symfony Mailer + Google Mailer |
| Database | MySQL |
| Testing | PHPUnit + Zenstruck Foundry |

---

## 🗂️ Data Model

| Entity | Description |
|---|---|
| `Livre` | Book — title, price, pages, edition date, copies, cover image |
| `Auteur` | Author — linked to books (many-to-many) |
| `Editeur` | Publisher — linked to books |
| `Categories` | Book category |
| `User` | Registered customer with roles |
| `Cart` / `CartItem` | Shopping cart and its line items |
| `Commande` / `CommandeItem` | Order and its line items |
| `Ouvrier` | Store staff / worker entity |

---

## 🏗️ Project Structure

```
livre2/
├── src/
│   ├── Controller/        # All route controllers (Home, Livre, Cart, Checkout, Auth…)
│   ├── Entity/            # Doctrine entities
│   ├── Form/              # Symfony form types
│   ├── Repository/        # Doctrine repositories
│   ├── Security/          # Authentication handlers
│   └── services/          # Custom service classes
├── templates/             # Twig templates
├── public/
│   └── images/            # Uploaded book cover images
├── migrations/            # Doctrine database migrations
├── assets/                # JS and CSS assets
├── config/                # Symfony configuration
├── tests/                 # PHPUnit tests
└── compose.yaml           # Docker Compose setup
```

---

## 🚀 Getting Started

### Prerequisites

- PHP 8.2+
- Composer
- Symfony CLI
- MySQL
- Node.js (for asset management)

### Installation

1. Clone the repository and install dependencies with Composer
2. Copy `.env` to `.env.local` and configure your database URL and mailer DSN
3. Create the database and run migrations
4. Install JavaScript dependencies and compile assets
5. Start the Symfony local server

> A Docker Compose file (`compose.yaml`) is included for containerized setup.

---

## 👨‍💻 Author

**Wassim Hamdi**
