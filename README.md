# 🏦 Crypto Portfolio Management System

A **full-stack Laravel application** for managing cryptocurrency portfolios. This system enables users to **register, deposit cryptocurrency, invest in portfolios, track performance, and withdraw funds**, all through a secure web interface built with **Blade templates**.

---

## 📌 Table of Contents

- [🚀 Features](#-features)
- [🛠️ Tech Stack](#-tech-stack)
- [📋 Project Structure](#-project-structure)
- [🖥️ Installation & Setup](#-installation--setup)
- [📡 API Endpoints](#-api-endpoints)
- [🎨 Frontend (Blade) Implementation](#-frontend-blade-implementation)
- [🚧 Development Timeline](#-development-timeline)
- [📝 License](#-license)

---

## 🚀 Features

### 🧑‍💻 User Management
- **User Registration & Authentication**: Email-based sign-up with **Laravel Breeze (Sanctum)** for API token authentication.
- **Role-Based Access**: Admins can manage deposits, withdrawals, and portfolios.
- **Profile Management**: Users can update profile details and change passwords.
- **Security Enhancements**:
  ✅ **Strong password policy** (8+ characters, numbers, special characters)
  ✅ **Email verification** before login access
  ✅ **Brute-force protection** (Laravel Throttle Middleware)
  ✅ **Session & Token Management** (auto-expiry after inactivity)

### 💰 Crypto Deposit System
- **Multi-Network Wallets**: Generate deposit addresses for different cryptocurrencies.
- **Real-time Transaction Monitoring**: Fetch on-chain transactions every **15 minutes**.
- **Admin Verification for Deposits**: Prevents unauthorized fund credits.
- **Supported Networks**:
  ✅ Ethereum (ETH)
  ✅ Bitcoin (BTC)
  ✅ Solana (SOL)

### 📈 Portfolio Management
- **Predefined Investment Strategies**: Users can invest in system-generated portfolios.
- **Custom Portfolio Creation**: Users can define **3-20 crypto assets per portfolio**.
- **Balance Verification Before Purchase**.
- **Transaction History & Receipts**.

### 📊 Performance Tracking
- **Daily Portfolio Value Updates**: Based on live market data.
- **Profit/Loss Calculation**: Users can track investment growth.
- **Admin Performance Reports**.

### 💵 Withdrawal System
- **Users Can Request Payouts**.
- **Email Confirmation for Security**.
- **Admin Approval Before Processing**.
- **Minimum Withdrawal Amount**: $50 equivalent.
- **Processing Period**: 5 business days.

---

## 🛠️ Tech Stack

| **Technology** | **Usage** |
|---------------|-----------|
| **Laravel 10** | Backend Framework |
| **Laravel Breeze** | Authentication & Session Handling |
| **Blade Templates** | Frontend Templating |
| **Alpine.js** | Lightweight JS for UI Interactions |
| **Livewire (Optional)** | Real-time UI updates |
| **PostgreSQL** | Database |

---

## 📋 Project Structure

```
/crypto-portfolio-management
│── /app
│   │── /Http/Controllers   # API & Web Controllers
│   │── /Models             # Eloquent ORM Models
│   │── /Services           # Business Logic
│── /database
│   │── /migrations         # Database Migrations
│   │── /seeders            # Sample Data
│── /resources
│   │── /views              # Blade Template Files
│   │── /js                 # Alpine.js Scripts
│   │── /css                # Custom Styles
│── /routes
│   │── web.php             # Web Routes
│   │── api.php             # API Routes
│── /public                 # Frontend Assets
│── .env                    # Environment Variables
│── composer.json           # PHP Dependencies
│── package.json            # JavaScript Dependencies
│── README.md               # Documentation
```

---

## 🖥️ Installation & Setup

### 📌 Prerequisites
- **PHP 8.1+**
- **Composer**
- **Node.js & npm**
- **PostgreSQL**

### 📥 Clone Repository
```bash
git clone https://github.com/your-username/crypto-portfolio-management.git
cd crypto-portfolio-management
```

### 📦 Install Dependencies
```bash
composer install
npm install && npm run build
```

### ⚙️ Configure Environment
Copy the `.env.example` file:
```bash
cp .env.example .env
```
Update database & API credentials:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=crypto_portfolio
DB_USERNAME=root
DB_PASSWORD=yourpassword

APP_URL=http://localhost
JWT_SECRET=your-secret-key
```

### 🔄 Run Migrations & Seeders
```bash
php artisan migrate --seed
```

### 🚀 Start Local Server
```bash
php artisan serve
```

---

## 📡 API Endpoints

### 🧑‍💻 User Authentication
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/register` | Create a new account |
| POST | `/login` | Authenticate user |
| POST | `/logout` | Log out and clear session |
| GET | `/user` | Retrieve authenticated user profile |

### 🎨 Frontend (Blade) Implementation
- **Authentication**: Uses Laravel Breeze's Blade authentication system.
- **Dashboard UI**: Styled with **TailwindCSS + Alpine.js** for interactivity.
- **Real-time Updates**: **Livewire (optional)** can be used for dynamic updates.

---

## 🚧 Development Timeline

| Week | Task |
|------|------|
| 1 | Project setup, authentication system |
| 2 | User registration & login, email verification |
| 3 | Crypto deposit system, blockchain transaction monitoring |
| 4 | Portfolio management system (predefined & custom portfolios) |
| 5 | Withdrawal system, email verification workflow |

---

## 📝 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

