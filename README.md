# 🏡 Airbnb Clone – Scalable Booking Platform

A full-stack, production-grade Airbnb Clone built to simulate the architecture, workflows, and engineering practices behind a real-world booking platform.

This project goes beyond simple CRUD, it’s a deep dive into backend systems, database design, secure APIs, team collaboration, and CI/CD, giving me hands-on experience with scalable software architecture.

---

## 🎯 Project Overview & Goals

This project aims to:

- Simulate real world software development workflows (GitHub collaboration, SDLC)
- Design scalable backend systems using Django and MySQL
- Implement secure, well-documented APIs (REST/GraphQL)
- Build CI/CD pipelines with tools like Docker and GitHub Actions
- Strengthen planning, documentation, and feature-driven development skills

---

## 🧰 Technology Stack

A breakdown of the core technologies and their roles:

| Technology        | Purpose                                                                 |
|-------------------|-------------------------------------------------------------------------|
| **Django**        | Backend framework to build APIs and manage business logic               |
| **Django REST Framework** | Handles RESTful API development and serialization                |
| **GraphQL**       | Enables flexible, efficient querying between frontend and backend        |
| **MySQL**         | Relational database to store and manage platform data                   |
| **Docker**        | Containerizes the application for consistent development and deployment |
| **GitHub Actions**| Automates testing and deployment pipelines                              |
| **Markdown**      | Used for documentation (`README.md`, planning, and team workflows)      |
| **Git + GitHub**  | Version control and collaborative team development platform             |

---

## 👥 Team Roles

This project simulates a real-world collaborative team setup:

### 👨🏽‍💻 Backend Developer
Designs and implements APIs using Django and GraphQL. Handles authentication, business logic, and backend integrations.

### 🗃️ Database Administrator (DBA)
Manages schema design, indexing, normalization, and relational integrity using MySQL. Works closely with the backend developer.

### 🧪 QA Engineer
Develops automated and manual tests to validate system functionality and prevent regressions. Ensures system reliability.

### 🐳 DevOps Engineer
Sets up and manages CI/CD pipelines using Docker and GitHub Actions. Automates testing and deployment processes.

### 🧑🏽‍🎨 Frontend Developer *(Optional/Future Scope)*
Responsible for the user interface, integrating with APIs and improving user experience.

---

## 🗃️ Database Design

The application models real-world booking logic using the following entities:

### 🔹 Users
- `id` – Unique identifier
- `name` – User’s full name
- `email` – Login identifier
- `role` – “host” or “guest”
- `password` – Encrypted for secure login

### 🔹 Properties
- `id` – Unique listing ID
- `title` – Property name
- `description` – Details about the property
- `location` – Address or city
- `host_id` – Linked to Users (host)

**A user (host) can own multiple properties.**

### 🔹 Bookings
- `id` – Unique booking reference
- `user_id` – Guest who booked
- `property_id` – Booked property
- `start_date` – Check-in
- `end_date` – Check-out

**A booking belongs to one user and one property.**

### 🔹 Reviews
- `id` – Review ID
- `user_id` – Reviewer
- `property_id` – Property reviewed
- `rating` – Numerical rating
- `comment` – Text feedback

**Users can review multiple properties. Properties can have many reviews.**

### 🔹 Payments
- `id` – Payment record ID
- `booking_id` – Related booking
- `amount` – Payment amount
- `method` – Payment method
- `status` – Transaction status

**Each payment is linked to one booking.**

---

## 🔗 Entity Relationships

- One **user** can act as both **host** and **guest**
- One **host** can own many **properties**
- One **guest** can create many **bookings**
- One **property** can have many **reviews** and **bookings**
- Each **booking** links one user to one property
- Each **payment** is tied to one booking

---

## ✨ Feature Breakdown

### 👤 User Management
Handles sign up, login, and role-based actions. Guests can book properties; hosts can manage listings.

### 🏠 Property Management
Hosts can create, update, and remove listings. Guests can browse available properties by location and details.

### 📆 Booking System
Allows guests to book available properties and view reservation history. Prevents double-bookings via validation.

### 💳 Payment Integration
Captures payment information and tracks transaction success/failure. Prepares for future gateway integration.

### ⭐ Reviews & Ratings
Guests can leave ratings and comments post-stay. Reviews help other users assess property quality.

### 🔐 API Security
Secures all data through authentication, role-based access, input validation, and rate limiting.

### 🚀 CI/CD Automation
Deployments and test suites are automated via GitHub Actions and Docker, ensuring consistent delivery.

---

## 🔐 API Security

### ✅ Authentication
Token-based user verification (e.g., JWT) ensures secure access to protected routes.

### 🔒 Authorization
Enforces role-based access, e.g., only hosts can manage properties.

### 📉 Rate Limiting
Prevents API abuse and brute-force attempts by capping request frequency.

### 🧼 Input Validation
Cleans and verifies user inputs to prevent SQL injection and XSS.

### 🛑 Error Handling
Fails securely and logs meaningful server-side errors for developer visibility.

---

## 🚀 CI/CD Pipeline

CI/CD automates testing, builds, and deployment. It enables developers to ship faster and with fewer bugs.

### 📦 Benefits:
- Catches bugs early through automated tests
- Enables quick and safe deployments
- Supports a smoother developer workflow

### 🛠️ Tools Used:
- **GitHub Actions** – Triggers build/test on every push or PR
- **Docker** – Containers ensure consistent environments
- **(Optional)** – Integration with cloud platforms for deployment

---
