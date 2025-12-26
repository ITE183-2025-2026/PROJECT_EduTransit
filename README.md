# EDUTRANSIT – School Bus Route Management System

<p align="center">
  <img src="logo schoolbus.png" alt="EDUTRANSIT Logo" width="180">
</p>

## Project Overview

**EDUTRANSIT** is a web-based School Bus Route Management and Simulation System developed as part of an undergraduate thesis. The system is designed to model, manage, and simulate school bus routes within **Iligan City**, addressing the lack of a dedicated school bus system by providing optimized routing solutions using graph theory and mapping technologies.

The system supports **two user roles**: **Admin** and **Regular User**, each with specific functionalities.

---

## Objectives of the Project

* To provide a centralized system for managing school bus routes
* To visualize bus stops and routes on an interactive map
* To simulate optimal routes using real road networks
* To apply graph theory concepts in real-world transportation problems
* To assist future school bus system implementation in Iligan City

---

## Technologies Used

### Frontend

* HTML5, CSS3, JavaScript
* Leaflet.js (Interactive Maps)
* OpenStreetMap

### Backend

* PHP (Server-side logic)
* MySQL (Database)
* Sessions for authentication and role-based access

### External APIs

* **OSRM Routing API** – for route distance and travel time simulation

---

## 📂 Project Directory Structure

```
FinalRouting/
│── admin/                 # Admin-related files
│── pictures/              # Static images
│── uploads/               # User profile images
│── about.php
│── api.php                # Backend API for routing & simulation
│── contact.php
│── db_connect.php         # Database connection
│── login.php
│── logout.php
│── registration.php
│── user_home.php
│── profile.php
│── update_profile.php
│
│── admin_home.php         # Admin dashboard
│── manage_users.php       # User management (Admin)
│── edit_user.php
│── delete_user.php
│── admin_profile.php
│── update_admin_profile.php
│
│── add_routes.html        # Route editor UI
│── add_routes.css
│── add_routes1.js         # Route creation logic
│── admin_addroutes.php
│
│── simulate_routes.php    # Route simulation
│── simulate_routes.js
│
│── reports.php
│── style.css
│── iligan_busroutes(db).sql
│── README.md
```

---

## User Roles and Features

### Regular User

* Register and login to the system
* View and update personal profile
* View available bus routes
* Simulate routes and view paths on the map

### Admin

* Secure login with role-based access
* Manage users (add, edit, delete)
* Add and edit bus stops and routes
* Run route simulations
* View reports and system data

---

## Database Structure

**Database Name:** `iligan_busroute`

### Tables

* `user_login` – stores user and admin credentials
* `bus_nodes` – bus stops and school locations
* `routes` – route names
* `route_stops` – ordered stops per route with distance and travel time

Relationships are enforced using **foreign keys** to maintain data integrity.

---

## System Flow (Overall Process)

### 1. User Authentication

* User opens the website
* Logs in or registers an account
* Credentials are verified securely using hashed passwords
* A session is created

### 2. Role-Based Access

* System checks user role
* **Admin** → Redirected to Admin Dashboard
* **User** → Redirected to User Home Page

### 3. Route Management (Admin)

* Admin adds bus stops using an interactive map
* Routes are created by selecting ordered stops
* Data is saved into the MySQL database

### 4. Route Simulation

* User or Admin selects a route
* System sends coordinates to **OSRM API**
* OSRM calculates distance and travel time
* Route is displayed on the map using Leaflet

### 5. Data Visualization

* Routes and stops are rendered using Leaflet + OpenStreetMap
* Travel paths are clearly visualized

### 6. Logout

* User logs out
* Session is destroyed
* User is redirected to login page

---

## Conceptual Basis

* Graph Theory (nodes = bus stops, edges = routes)
* Shortest path computation via OSRM
* Real-world road network integration

---

## How to Run the Project

1. Install **XAMPP** or similar local server
2. Place the project folder inside `htdocs`
3. Import the database file into phpMyAdmin
4. Update database credentials in `db_connect.php`
5. Open browser and navigate to:

   ```
   http://localhost/FinalRouting/login.php
   ```

---

## Notes

* Admin accounts are identified by email ending with `@admin.com`
* Passwords are securely hashed
* The system is designed for academic and prototype use

---

## Authors
<p align="center">
  <strong>Project Leader</strong><br>
  Alieza Amor Atienda<br><br>
  <strong>Members</strong><br>
  April Grace Sagadrata<br>
  Cristine Obinsa<br><br>
  Bachelor of Science in Information Technology<br>
  Mindanao State University – Iligan Institute of Technology
</p>


---

## License

This project is for **academic and research purposes only**.
