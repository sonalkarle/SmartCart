#  🚀 SmartCart

# 🛒 E-Commerce Platform — Angular + .NET Core + Azure

A full-fledged, scalable, and secure e-commerce platform built with Angular (frontend), ASP.NET Core Web API (backend), and Microsoft SQL Server (SSMS). Designed for real-world business scenarios, it features advanced user role management, UPI payment integration, CI/CD deployment on Azure, and secure modern authentication.

---

## 🚀 Project Overview

This platform is designed to simulate an end-to-end commercial e-commerce system, complete with:

- Multiple user types (buyers, admins, purchasers)
- Role-based access control
- Product & category management
- Cart, wishlist, and order management
- Payment gateway integration (UPI)
- Multi-address management
- Azure-based deployment with CI/CD pipelines

It is built with clean architecture principles for maintainability, scalability, and real-world adaptability.

---

## 🛠 Tech Stack

| Layer           | Technology                                       |
|----------------|--------------------------------------------------|
| Frontend        | Angular (TypeScript, RxJS, Angular Router)       |
| Backend         | ASP.NET Core Web API (C#), Clean Architecture     |
| Database        | SQL Server (SSMS)                                |
| Authentication  | Azure AD B2C or Auth0 (OTP, UPI login)           |
| Payment Gateway | Razorpay / PhonePe API (UPI support)             |
| DevOps          | GitHub → Azure CI/CD Pipelines                   |
| Deployment      | Azure App Service + Azure SQL                    |
| Docs            | Swagger, Postman                                 |

---

## 🎯 Core Features

### 👥 User & Role Management
- Super Admin: Full control of the platform
- Category Admin: Manages specific product categories
- Buyer: Regular customer who browses and purchases
- Purchaser: Special customer who can bulk order
- Anonymous: Can browse, add to wishlist, register

### 🛒 E-Commerce Functionalities
- Product listing, search, filters, sorting
- Cart and wishlist (session-based for guests, persistent for users)
- Multi-address support per user
- Order tracking and order history
- UPI-based payment through Razorpay/PhonePe
- Admin dashboards for product and user management

### 🛡️ Security & Authentication
- Azure AD B2C or Auth0 (OTP-based login instead of JWT)
- Role-based API authorization and Angular route guards

### 🧾 Orders & Payments
- Order placement with real-time payment integration
- UPI payment using external APIs
- Webhook handling for payment confirmation

---

## 🧱 System Architecture

### 🏗️ Backend (Clean Architecture)
Presentation Layer → ASP.NET Controllers
Application Layer → Services, DTOs, Use Cases
Domain Layer → Business Entities, Interfaces
Infrastructure Layer → DB, Payment, Auth, Email, External APIs
- Loose coupling, dependency injection, testable
- FluentValidation, AutoMapper, and MediatR integration

### 🧩 Frontend (Angular Structure)
/src/app/
│
├── modules/
│ ├── admin/
│ ├── buyer/
│ └── shared/
│
├── services/
├── guards/
├── interceptors/
└── components/

### Main Entities:
- **Users** → with RoleID
- **Roles** → Super Admin, Category Admin, Buyer, etc.
- **Products** → linked with categories
- **Categories** → hierarchical
- **Orders** → linked with payments and users
- **OrderItems** → product, quantity, subtotal
- **Cart** → per user/session
- **Wishlist** → per user
- **Addresses** → multiple per user
- **Payments** → linked with UPI transaction IDs
- 
### GitHub + Azure App Service Flow:
- CI:
  - Lint, Test, Build Angular & .NET apps
  - Create artifacts
- CD:
  - Auto deploy to Azure App Service via GitHub Actions or Azure Pipelines
  - Azure SQL for database hosting
  - Optional: Blue-Green deployment with deployment slots

---

## 🧠 Learning Roadmap for You

| Area                     | What to Learn                                               |
|--------------------------|-------------------------------------------------------------|
| 🔧 Backend Dev           | ASP.NET Core Web API, Clean Architecture, EF Core           |
| 🧱 DB Design             | SSMS, Foreign Keys, Indexing, Normalization, ERD tools      |
| 💳 Payment Integration   | Razorpay UPI APIs, webhook listeners                        |
| 🔐 Authentication        | Azure AD B2C, OAuth2, OTP Login without JWT                 |
| 🧠 Angular               | Routing, Guards, Interceptors, State Management             |
| ☁️ DevOps + Azure        | GitHub Actions, Azure Pipelines, App Service Deployment     |

---


### ✅ Prerequisites:
- Node.js + Angular CLI
- .NET 7 SDK
- SQL Server Management Studio (SSMS)
- Razorpay/PhonePe developer account (for testing UPI)


### Covering Things in table 

🔹 Core Commerce Flows
Users, products, orders, carts, wishlists, payments, addresses, etc.

🔹 Admin & Role Management
Super admin, category admin, RBAC (Role-Based Access Control)

🔹 Behavioral Analytics
Search history, product views, abandoned carts, product analytics

🔹 Customer Experience
Reviews, multiple addresses, refunds, help desk, loyalty/gift cards (if added later)

🔹 Payments & Security
UPI, payment attempts, refunds, logs, optional 2FA

🔹 Scalability Readiness
Warehousing, scheduled tasks, marketing campaigns, tax & invoices


