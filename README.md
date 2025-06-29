# 🏡 Airbnb Clone – Scalable Booking Platform

A full-stack, production-grade Airbnb Clone built to simulate the architecture, workflows, and engineering practices behind a real-world booking platform.

This project goes beyond simple CRUD, it’s a deep dive into backend systems, database design, secure APIs, team collaboration, and CI/CD, giving me hands-on experience with scalable software architecture.

---

## 🎯 Project Goals

- Model real-world software development workflows (SDLC, GitHub team collaboration)
- Design scalable backend systems using Django and MySQL
- Implement secure, well-documented APIs (REST/GraphQL)
- Build CI/CD pipelines with tools like Docker and GitHub Actions
- Explore architectural planning, feature-driven development, and database normalization

---

## 🧰 Technology Stack

- **Backend:** Django, Django REST Framework, GraphQL
- **Database:** MySQL
- **CI/CD & DevOps:** Docker, GitHub Actions
- **Version Control & Team Workflow:** Git, GitHub
- **Others:** Markdown, API security best practices, system design principles

---

## 🔍 Key Highlights

- 📁 Structured GitHub repo following best practices  
- 👥 Team roles and collaborative documentation  
- 🛡️ Secure API integration with access control & validation  
- 🗃️ Relational DB design for real-world booking logic  
- 🚀 Automated deployments with CI/CD pipelines  
- 📌 Feature breakdown with user-first functionality

---

## 👫🏾 Team Roles.

- 👨🏽‍💻 Backend Developer Role
The backend developer is responsible for designing and implementing the server-side logic of the application. This includes building secure and scalable APIs using Django, modeling the relational database in MySQL, and integrating authentication and authorization mechanisms. The role also involves collaborating on system architecture, ensuring data integrity, and setting up CI/CD pipelines for smooth deployment. A strong focus is placed on performance, security, and maintainability.

---

## 🗃️ Database Design

This project models a real-world booking platform, with entities that reflect key user and business interactions. Below are the primary entities and their relationships:

### 🔹 Users
Represents platform users (guests and hosts).
- `id` – Unique identifier
- `name` – Full name of the user
- `email` – Used for login and communication
- `role` – Either "guest" or "host"
- `created_at` – Account creation timestamp

### 🔹 Properties
Represents the listings that users can book.
- `id` – Unique identifier
- `title` – Name or headline of the property
- `description` – Detailed property overview
- `location` – City or region
- `host_id` – References the user who owns the property

**Relationship:** A user (host) can own multiple properties.

### 🔹 Bookings
Represents reservations made by guests.
- `id` – Unique identifier
- `property_id` – References the booked property
- `user_id` – References the guest making the booking
- `start_date` – Booking start date
- `end_date` – Booking end date

**Relationship:** A booking belongs to one user and one property.

### 🔹 Reviews
Represents feedback left by guests after a stay.
- `id` – Unique identifier
- `user_id` – Reviewer (guest)
- `property_id` – Property being reviewed
- `rating` – Numeric score
- `comment` – Optional written feedback

**Relationship:** A user can leave many reviews; a property can have many reviews.

### 🔹 Payments
Represents completed booking payments.
- `id` – Unique identifier
- `booking_id` – References the booking
- `amount` – Total amount paid
- `payment_method` – e.g., card, PayPal
- `status` – e.g., success, failed

**Relationship:** Each payment is linked to a single booking.

---

### 🔗 Entity Relationships Overview

- One **user** can be both a **guest** and a **host**.
- One **user** (host) can own many **properties**.
- One **property** can have many **bookings** and **reviews**.
- One **booking** is made by one **guest** and linked to one **property**.
- One **review** is tied to one **user** and one **property**.
- One **payment** is tied to one **booking**.




